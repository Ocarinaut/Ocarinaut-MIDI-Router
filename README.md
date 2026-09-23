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
2. HTTPSで配備したURLをWeb MIDI対応ブラウザで開き、MIDIアクセスを許可します。
3. 各入力を割り当て、SEQTRAK出力を確認してStart Routingを押します。
4. 演奏中はアプリを前景に維持します。Wake Lockは対応ブラウザでのみ要求されます。

## Release to GitHub Pages

Push to the `main` branch triggers GitHub Actions to build and deploy this static site to GitHub Pages. In the repository settings, set **Pages → Source** to **GitHub Actions** once. Open the resulting HTTPS URL in a Web MIDI-capable iPad browser.

## Limitations

iPad SafariのWeb MIDI対応は保証されません。ブラウザのバックグラウンド動作中のMIDI処理も保証されません。
