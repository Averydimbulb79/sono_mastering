# Sono

Your track. Finished.

Sono is a self-contained browser-based audio mastering application for WAV and MP3 files. Audio is decoded, analysed, edited, mastered, previewed and exported locally in the browser. No account, upload server, API key or external mastering service is required.

## Live application

[Open Sono](https://averydimbulb79.github.io/sono_mastering/)

## Project status

Sono is currently a functional browser-based beta. The core workflow is operational, including audio import, analysis, waveform editing, mastering, A/B comparison and local export.

| Area | Status | Current capability |
| --- | --- | --- |
| Audio import | Complete | Opens WAV and MP3 files using browser-native decoding |
| Waveform and playback | Complete | Displays a seekable waveform with play, pause, position and volume controls |
| Audio analysis | Complete | Estimates loudness, peak level, RMS, crest factor, stereo width, correlation and tonal balance |
| Mastering profiles | Complete | Auto, Clean, Warm, Acoustic, Punch and Atmospheric profiles |
| Fine controls | Complete | Warmth, brightness, bass, punch, presence, stereo width and loudness |
| Reference track | Complete | Analyses an optional WAV or MP3 reference and informs the Auto profile |
| Audio editing | Complete | Drag-to-select section removal with precise start and end controls |
| Fades | Complete | Adjustable fade-in and fade-out sliders with quick presets |
| A/B monitoring | Complete | Switches between the edited source and mastered result with loudness matching |
| WAV export | Complete | Local 16-bit or 24-bit WAV rendering |
| MP3 export | Complete | Local 320 kbps MP3 encoding through the embedded encoder |
| Offline use | Complete | Runs from one HTML file without an internet connection after download |

## Development progress

| Version | Milestone | Progress |
| --- | --- | --- |
| 1 | Initial mastering workspace with upload, analysis, profiles, controls and export | Completed |
| 2 | Removed external processing requirements and moved the full workflow into the browser | Completed |
| 3 | Renamed the application from Sino to Sono and updated the public address | Completed |
| 4 | Added real section removal and adjustable fade-in and fade-out processing | Completed |
| 5 | Redesigned editing for easier use with waveform drag selection, larger controls, sliders and presets | Completed |
| 6 | Added edit history, keyboard shortcuts, click-safe cut joins and estimated inter-sample peak monitoring | Current |

## How to use Sono

1. Open the [live application](https://averydimbulb79.github.io/sono_mastering/).
2. Choose or drag in a WAV or MP3 mix.
3. Review the waveform and audio analysis.
4. If necessary, drag across the waveform to highlight an unwanted section, then select Remove Highlighted Section.
5. Adjust fade-in and fade-out lengths with the sliders or use a preset.
6. Choose a mastering profile and refine the mastering controls.
7. Optionally add a reference track.
8. Choose a loudness target and select Master Track.
9. Compare the edited source and mastered version using the A/B controls.
10. Export the finished master as WAV or MP3.

## Editing workflow

### Removing a section

Drag horizontally across the waveform to highlight the audio you want to remove. Sono displays the start time, end time and selected duration. The time fields can also be edited manually, or marked from the current playhead position.

Selecting Remove Highlighted Section joins the audio before and after the selection. Reset Edits restores the original uploaded file.

### Applying fades

Use the Fade In and Fade Out sliders to set each duration in seconds. The fade is applied when the slider is released. The None, Short, Medium and Long presets set both fades together.

Edits are included in playback, analysis, mastering and the exported file.

## Mastering profiles

| Profile | Intended character |
| --- | --- |
| Auto | Analyses the source and selects balanced starting values |
| Clean | Controlled, clear and restrained |
| Warm | Fuller low-mid tone with gentle saturation |
| Acoustic | Natural, open and less compressed |
| Punch | Stronger impact, density and presence |
| Atmospheric | Wider and more spacious |

## Local processing and privacy

Sono processes audio on the user’s device. Uploaded tracks are not sent to a remote mastering server.

| Process | Location |
| --- | --- |
| File decoding | Browser |
| Audio analysis | Browser |
| Section removal and fades | Browser |
| Mastering render | Browser |
| WAV encoding | Browser |
| MP3 encoding | Browser |

## Technical overview

| Component | Purpose |
| --- | --- |
| Web Audio API | Audio decoding and playback |
| OfflineAudioContext | Offline mastering render |
| Canvas | Waveform display |
| Browser DSP nodes | Tone shaping, dynamics, stereo processing and gain |
| Embedded LAME encoder | MP3 export |
| Blob and object URLs | Local file generation and download |
| HTML, CSS and JavaScript | Self-contained interface and application logic |

## Browser support

Chrome and Microsoft Edge are recommended on desktop. Other modern browsers may work, but audio decoding, memory limits and download behaviour can vary.

## Current limitations

| Limitation | Detail |
| --- | --- |
| Loudness measurement | The displayed LUFS value is a practical browser-based estimate, not a certified broadcast meter reading |
| True-peak measurement | Sono estimates inter-sample peaks with 4-point interpolation; this remains an approximation rather than a certified meter |
| Large files | Long, high-resolution files can consume substantial browser memory during analysis and rendering |
| Editing history | Up to 20 cut, fade and reset states can be undone or redone during the current session |
| Project saving | Sessions are not saved after the page is closed or refreshed |

## Planned improvements

| Priority | Improvement |
| --- | --- |
| High | Zoomable waveform for more precise selection |
| High | Standards-compliant BS.1770 loudness and oversampled true-peak measurement |
| High | Dedicated look-ahead brickwall limiter |
| Medium | Before-and-after analysis comparison |
| Medium | Additional keyboard shortcuts for playback and navigation |
| Medium | Optional export naming controls |
| Future | Project save and restore without uploading audio to a server |

## Repository structure

For the single-file release, the complete application is stored in `index.html`. Styling, application logic and the MP3 encoder are embedded so GitHub Pages can serve the app without a build process.

| File | Purpose |
| --- | --- |
| `index.html` | Complete Sono application |
| `README.md` | Project information and progress |
| `LICENSE` | Project licence, if included |

## Running locally

Download `index.html` and open it in Chrome or Edge. An internet connection is not required for audio processing or export.

## Licence

See the repository’s `LICENSE` file for usage and distribution terms.
