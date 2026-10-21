# SONO

**Your track. Finished.** Browser-based audio editing and mastering with local processing.

**[Open SONO](https://averydimbulb79.github.io/sono_mastering/)** · [Source](https://github.com/Averydimbulb79/sono_mastering)

## Current status

Web-first development on `main`. The previous application is preserved in [legacy/](legacy/) and the complete [pre-transition backup](../../tree/backup/pre-web-first-main). Windows packaging will follow web acceptance.

## Features

- Import WAV/MP3 audio and preview the waveform.
- Original/enhanced A/B listening controls.
- Auto mastering and configurable advanced parameters.
- Clip removal, fades, local processing, and audio export.
- Responsive desktop/mobile workspace.

## Important limitation

Advanced checkboxes currently bypass existing mastering parameter adjustments; they are **not** separate spectral-restoration algorithms. More sophisticated non-AI restoration and artifact reduction are planned and must be validated before being described as implemented.

## Development policy

Implement and test changes on `main`; preserve backup checkpoints and document each release. No server upload is required for the current local audio-processing workflow.
