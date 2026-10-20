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

Downloads: Whisper from [ggerganov/whisper.cpp](https://huggingface.co/ggerganov/whisper.cpp/tree/main), Silero VAD from [ggml-org/whisper-vad](https://huggingface.co/ggml-org/whisper-vad/tree/main).

Installing, updating or uninstalling Murmur never touches your models, recordings (`%USERPROFILE%\Murmur\recordings`) or settings (`%LOCALAPPDATA%\Murmur`).

## Requirements

- Windows 10/11 x64
- Optional: a GPU for faster transcription: an NVIDIA RTX 30 or newer with the CUDA Toolkit, or any GPU with its driver through Vulkan (falls back to CPU)
- Optional: [Ollama](https://ollama.com) for the adapted read-aloud mode

## License

Murmur is free to use, at home or at work, on any number of computers. You may pass on the installer or portable package unmodified and free of charge, together with its `licenses` folder. It is provided as is, without warranty. See [LICENSE](LICENSE); the installed app carries it as `LICENSE.txt`, and the open-source components it includes are listed with their licenses in its `licenses` folder.

## Uninstall

Settings → Apps → Installed apps → Murmur → Uninstall.
