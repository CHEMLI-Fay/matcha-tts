# Matcha-TTS experiments

This repository is a [fork of B-Lounes/matcha-tts](https://github.com/B-Lounes/matcha-tts) used for standalone text-to-speech training and evaluation experiments. The Matcha-TTS architecture is upstream work.

## Repository contents

- `model.py` contains the model implementation used by this branch.
- `train_standalone.py` is an experimental training entry point.
- `main.py` runs an inference example with a local model checkpoint and vocoder.
- The notebooks explore evaluation and audio quality.
- `hifigan/` contains vocoder-related code.

## Inference prerequisites

Install the Python dependencies in `requirements.txt` and provide a compatible trained checkpoint. The checkpoint is not included in this repository. `main.py` reads its path from `MATCHA_CHECKPOINT_PATH`; without that variable it looks for `matcha_ljspeech.ckpt` in the current directory.

```powershell
$env:MATCHA_CHECKPOINT_PATH = "C:\path\to\your\checkpoint.ckpt"
python main.py
```

The script may also download vocoder weights. Depending on your environment, audio and phonemization tools such as eSpeak may be required. This is an experimental fork; the training and inference commands have not been verified as a reproducible release.

## Attribution

See the [upstream fork](https://github.com/B-Lounes/matcha-tts) for its history and the original Matcha-TTS project it builds on.
