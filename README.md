# Sono

Your track. Finished.

Sono is a self-contained browser-based audio mastering application for WAV and MP3 files. Audio is decoded, analysed, edited, mastered, previewed and exported locally in the browser. No account, upload server, API key or external mastering service is required.

## Live Application

[Open Sono](https://averydimbulb79.github.io/sono_mastering/)

## Project Status

Sono is currently a functional browser-based beta. The core workflow is operational, including audio import, analysis, waveform editing, mastering, A/B comparison and local export.

| Area | Status | Current Capability |
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

## Development Progress

| Version | Milestone | Progress |
| --- | --- | --- |
| 1 | Initial mastering workspace with upload, analysis, profiles, controls and export | Completed |
| 2 | Removed external processing requirements and moved the full workflow into the browser | Completed |
| 3 | Renamed the application from Sino to Sono and updated the public address | Completed |
| 4 | Added real section removal and adjustable fade-in and fade-out processing | Completed |
| 5 | Redesigned editing for easier use with waveform drag selection, larger controls, sliders and presets | Current |

## How to Use Sono

1. Open the [live application](https://averydimbulb79.github.io/sono_mastering/).
2. Choose or drag in a WAV or MP3 mix.
3. Review the waveform and audio analysis.
4. If necessary, drag across the waveform to highlight an unwanted section.
5. Select Remove Highlighted Section.
6. Adjust the fade-in and fade-out lengths with the sliders or use a preset.
7. Choose a mastering profile and refine the mastering controls.
8. Optionally add a reference track.
9. Choose a loudness target and select Master Track.
10. Compare the edited source and mastered version using the A/B controls.
11. Export the finished master as WAV or MP3.

## Editing Workflow

### Removing a Section

Drag horizontally across the waveform to highlight the audio you want to remove. Sono displays the start time, end time and selected duration.

The time fields can also be edited manually or marked from the current playhead position.

Selecting Remove Highlighted Section joins the audio before and after the selection. Reset Edits restores the original uploaded file.

### Applying Fades

Use the Fade In and Fade Out sliders to set each duration in seconds. The fade is applied when the slider is released.

The available quick presets are:

| Preset | Fade Length |
| --- | --- |
| None | 0 seconds |
| Short | 0.5 seconds |
| Medium | 2 seconds |
| Long | 5 seconds |

The presets adjust both fade-in and fade-out together. The sliders can be used when different durations are required.

All edits are included in playback, analysis, mastering and the exported file.

## Mastering Profiles

| Profile | Intended Character |
| --- | --- |
| Auto | Analyses the source and selects balanced starting values |
| Clean | Controlled, clear and restrained |
| Warm | Fuller low-mid tone with gentle saturation |
| Acoustic | Natural, open and less compressed |
| Punch | Stronger impact, density and presence |
| Atmospheric | Wider and more spacious |

## Fine Mastering Controls

| Control | Purpose |
| --- | --- |
| Warmth | Adjusts body, saturation and low-mid character |
| Brightness | Adjusts high-frequency clarity and air |
| Bass | Adjusts low-frequency weight |
| Punch | Adjusts compression and impact |
| Presence | Adjusts vocal and midrange focus |
| Width | Adjusts the stereo image |
| Loudness | Adjusts the intended density and output level |

## Local Processing and Privacy

Sono processes audio on the user’s device. Uploaded tracks are not sent to a remote mastering server.

| Process | Location |
| --- | --- |
| File decoding | Browser |
| Audio analysis | Browser |
| Section removal | Browser |
| Fade processing | Browser |
| Mastering render | Browser |
| WAV encoding | Browser |
| MP3 encoding | Browser |

## Technical Overview

| Component | Purpose |
| --- | --- |
| Web Audio API | Audio decoding and playback |
| OfflineAudioContext | Offline mastering render |
| Canvas | Waveform display |
| Browser DSP nodes | Tone shaping, dynamics, stereo processing and gain |
| Embedded LAME encoder | MP3 export |
| Blob and object URLs | Local file generation and download |
| HTML, CSS and JavaScript | Self-contained interface and application logic |

## Audio Workflow

| Stage | Action |
| --- | --- |
| Upload | Import a WAV or MP3 file |
| Decode | Convert the file into browser-accessible audio data |
| Analyse | Measure levels, dynamics, stereo image and tonal balance |
| Edit | Remove sections and apply fades |
| Master | Process tone, dynamics, width and loudness |
| Compare | Switch between the edited source and mastered result |
| Adjust | Refine the profile and mastering controls |
| Render | Create the processed audio locally |
| Export | Download the master as WAV or MP3 |

## Browser Support

Chrome and Microsoft Edge are recommended on desktop.

Other modern browsers may work, but audio decoding, available memory and download behaviour can vary.

## Current Limitations

| Limitation | Detail |
| --- | --- |
| Loudness measurement | The displayed LUFS value is a practical browser-based estimate, not a certified broadcast meter reading |
| True-peak measurement | Sono currently applies a sample-peak ceiling rather than full oversampled true-peak metering |
| Large files | Long, high-resolution files can consume substantial browser memory during analysis and rendering |
| Editing history | Reset Edits restores the original file, but individual edit undo and redo are not yet available |
| Project saving | Sessions are not saved after the page is closed or refreshed |
| Mobile performance | Large audio files may exceed the memory available on mobile devices |

## Planned Improvements

| Priority | Improvement |
| --- | --- |
| High | Undo and redo for individual edits |
| High | Zoomable waveform for more precise selection |
| High | Improved loudness and true-peak measurement |
| Medium | Before-and-after analysis comparison |
| Medium | Keyboard shortcuts for playback and editing |
| Medium | Optional export naming controls |
| Medium | Improved mobile editing |
| Future | Project save and restore without uploading audio to a server |

## Repository Structure

For the single-file release, the complete application is stored in `index.html`. Styling, application logic and the MP3 encoder are embedded so GitHub Pages can serve the app without a build process.

| File | Purpose |
| --- | --- |
| `index.html` | Complete Sono application |
| `README.md` | Project information and development progress |
| `LICENSE` | Project licence, if included |

## Running Locally

1. Download `index.html`.
2. Open it in Chrome or Microsoft Edge.
3. Import a WAV or MP3 file.
4. Edit, master and export the track.

An internet connection is not required for audio processing or export.

## Licence

See the repository’s `LICENSE` file for usage and distribution terms.
