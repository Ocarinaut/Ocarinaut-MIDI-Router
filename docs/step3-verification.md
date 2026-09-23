# STEP 3 — iPad verification

Date: 2026-09-23

## Confirmed working

- MIDIWeb Browserで、サイトごとのWeb MIDI有効化（Request MIDI Site）後にMIDI接続できること。
- Launchkey 49 MK4、MPK mini、nanoKEY Fold、Keith McMillen 12 StepからSEQTRAKへMIDI入力を送信できること。
- 複数の入力機器が同一チャンネル・同一ノートを重ねて押した場合、片方を離しても、もう一方が押されている間はノートが保持されること。
- Control Changeメッセージを送信できること。

## Operating notes

- 演奏中はiPadでRouterを前景表示のまま使用する。
- Web MIDIの利用可否と許可方式はブラウザに依存する。MIDIWeb Browserでは、Connect MIDIの前にRequest MIDI Siteを実行する。
