# Changelog

Milestones for Vox, grouped by month. Entries describe outcomes only; implementation details are not published.

## 2026-11

- **Narration that flows.** Film narration is now voiced as connected passages, each in one take, not sentence by sentence. Takes generated one sentence at a time had reset their pitch and fallen at every full stop.
- **Less dead air.** A narrated film was measured for silence: pauses inside takes reached 0.88 s and each sound effect delayed the next line by 1.4 s. In the film tools, narration and character voices were tightened, and effects play under the voices instead of pushing them back.

## 2026-10

- **Drum hits and beat returns (10-29).** The breakdown marks kick, snare and hi-hat hits (87–99% F1 on known-answer songs) and the moments a beat comes back, shown as lanes beside the waveforms. The companion editor's beat grid moved from 26–46 ms late to 3–5 ms. The mix view now shows the waveform of every layer.
- **Film-level audit (10-29).** Two finished films were separated back into voice and background and measured line by line. This confirmed flat line-to-line loudness, found a score that hardly dipped under the storyteller, and identified fixes for the film tools' mix.
- **Measured, not built (10-29).** A more elaborate mix-loudness pass was dropped because mixes already landed 0.37 dB from target on average.
- **Scenes voiced as scenes (10-20).** After a blind listening comparison, dialogue for films is generated a scene at a time. On test scenes, line-to-line loudness variation rose (0.8 → 1.9 dB and 2.0 → 2.8 dB) and flat falling endings fell (100% → 67%). Scenes can be continued from a kept start without changing approved lines, and a scene that cannot be voiced falls back to lines voiced one by one.
- **Why long films sounded flat (10-20).** Our voices were compared with professionally acted film dialogue and an audiobook. Within a line they matched acted speech; between lines they did not. This diagnosis set the direction for the rest of the month.
- **Model storage (10-20).** A model-cache loss took some sound features offline and showed the need for verified, restorable model storage.
- **Emotional performance (10-17).** A shared vocabulary for how a line is performed is now used by Vox and the film tools. An engine study found that re-designing a voice "in" an emotion changes who is speaking, so identity and performance are now handled separately.
- **Per-line dynamics and scene space (10-17).** In Comicat films, voices gained per-line loudness, pace and pause variation from their delivery notes, and a sense of the room they are in. By ear, heavy reverb and elaborate music direction were turned down in favour of subtler settings.
- **Runaway safeguard (10-13).** A take that never ends now fails in about two and a half minutes with a readable reason, where one used to hold the shared card for over 20 minutes.
- **Studio redesign and library (10-10).** Simpler three-column layout, grouped menu, per-page advanced controls, and an English/Bangla switch that shows only the voices and engines that fit. The new library archives untouched takes automatically but never deletes them; 840 items were archived in the first sweep, all files kept.
- **Clone from a scene (10-09).** Voices can be cloned from a scene of up to ten minutes; each speaker becomes a voice family with checked variations. Clones from real performed moments matched the original intonation at 0.58 on average (up to 0.91); written emotion instructions scored 0.23.
- **Hand-off with Comicat (10-09).** A sound can be sent from Comicat to Vox, edited or remastered, and returned.
- **Engine audit (10-09).** A full review reproduced a list of defects in loudness edge cases, text splitting and responsiveness, recorded for hardening.
- **Music fixed (10-03).** Generated music had come out fizzy and without a detectable beat. Regenerated from the same prompts and seeds, all three test cues now have a steady beat; confirmed by ear.

## 2026-09

- **One-to-one connection with ZipCat (09-26).** ZipCat's voice, music, atmosphere and foley tools now mirror Vox exactly and read its live catalogue.
- **Tonal buzz removed (09-26).** A faint tonal buzz in generated music and effects was traced and largely removed at the source; 17 earlier files were repaired.
- **Bangla foundations (09-23).** Bangla voices from native references, with every take checked by reading it back. A clean native reference reached 3.5% character error, against 8.4% for a synthetic reference and 18.2% for a two-speaker clip. Writing English words in Bangla script took a mixed line from 14.5% to 0.0%.
- **Finishing (09).** Finishing presets for common deliveries, top-end restoration for band-limited voices (upper-band spectral flatness 0.39 → 0.63, against 0.62 for a human recording), and loudness that lands within a few tenths of a dB of target, where renders previously fell 0.8–1.8 dB short.
- **Studio foundations (09).** Local voice studio with voice design, cloning and a voice library; long-form narration; multi-speaker dialogue; music beds, atmospheres, sound effects and foley; audio breakdown of songs and scenes; subtitles with every take.
