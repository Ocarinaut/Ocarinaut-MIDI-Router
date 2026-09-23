# Ocarinaut MIDI Router

iPad前景運用のための静的Web MIDI Routerです。iPadではWeb MIDI対応ブラウザ（例: MIDIWeb Browser）でHTTPS URLを開き、演奏中は常に前景に維持してください。

## Development

Node.js 24+で `npm install`、`npm run dev`、`npm run build` を実行します。

このMacではプロジェクトローカルのNodeランタイムを使えます。最初に以下を実行してください。

```bash
source ./.env-node
npm run dev
```

## iPad execution

1. PD Powered USB HubへiPad、SEQTRAK、4コントローラを接続します。
2. HTTPSで配備したURLをWeb MIDI対応ブラウザで開き、MIDIアクセスを許可します。MIDIWeb Browserの場合は、先に同ブラウザの **Request MIDI Site** でこのURLを有効化してからページを再読み込みし、**Connect MIDI** をタップします。
3. 各入力を割り当て、SEQTRAK出力を確認してStart Routingを押します。
4. 演奏中はアプリを前景に維持します。Wake Lockは対応ブラウザでのみ要求されます。

## Release to GitHub Pages

Push to the `main` branch triggers GitHub Actions to build and deploy this static site to GitHub Pages. In the repository settings, set **Pages → Source** to **GitHub Actions** once. Open the resulting HTTPS URL in a Web MIDI-capable iPad browser.

## Limitations

iPad SafariのWeb MIDI対応は保証されません。ブラウザのバックグラウンド動作中のMIDI処理も保証されません。

## Verification status

2026-09-23 に iPad + MIDIWeb Browser + PD Powered USB Hub 環境で、Launchkey 49 MK4、MPK mini、nanoKEY Fold、Keith McMillen 12 Step の入力、SEQTRAKへの送信、複数入力による同一チャンネル・同一ノートの保持、およびCC送信を実機確認しました。詳細は [STEP 3 verification](docs/step3-verification.md) を参照してください。
