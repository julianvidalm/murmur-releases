# Murmur releases

Binary releases of **Murmur**, a Windows desktop app for local meeting recording, transcription and read-aloud. Everything runs on your machine; no audio or text is sent to a cloud service.

This repository only hosts installers and update packages. It contains no source code.

## Install

1. Open the [latest release](../../releases/latest).
2. Download `Murmur.App-win-Setup.exe` and run it.

Murmur installs for the current user only (no administrator rights needed) and starts automatically after setup.

## Updates

Murmur checks this repository in the background at startup and every few hours. When a new version is available it is downloaded silently and applied the next time Murmur exits.

## Models

Models are not included in the installer. Place them in `%USERPROFILE%\Murmur\models` (or set custom paths in Settings):

| Purpose | File |
|---|---|
| Transcription (Whisper) | `ggml-large-v3.bin` |
| Voice activity detection | `ggml-silero-v6.2.0.bin` |
| Read-aloud voice (Kokoro) | `kokoro.onnx` |

Whisper and Silero models: [huggingface.co/ggerganov/whisper.cpp](https://huggingface.co/ggerganov/whisper.cpp/tree/main).

Installing, updating or uninstalling Murmur never touches your models, recordings (`%USERPROFILE%\Murmur\recordings`) or settings (`%LOCALAPPDATA%\Murmur`).

## Requirements

- Windows 10/11 x64
- Optional: NVIDIA GPU with the CUDA Toolkit for faster transcription (falls back to CPU)
- Optional: [Ollama](https://ollama.com) for the adapted read-aloud mode

## Uninstall

Settings → Apps → Installed apps → Murmur → Uninstall.
