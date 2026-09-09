# Audio Annotation Workbench

A local, browser-based tool that speeds up manual audio transcription and annotation work — built after doing real audio-annotation tasks and noticing how much time gets lost on repetitive actions rather than the actual listening.

**Live use case:** platforms like Perit AI, Appen, Lionbridge, and TELUS International assign human annotators short audio clips to transcribe *verbatim*, using a fixed tag system (speaker turns, overlapping speech, background noise, filled pauses, etc.). The bottleneck isn't understanding the audio — it's the repeated manual actions: reaching for the mouse to replay 3 seconds, remembering exact tag syntax, switching context between a tag reference sheet and the editor.

This tool removes that friction. It does **not** transcribe anything automatically — the annotator still listens and types every word. It just makes the mechanical parts faster.

## Why I built this

While completing an audio-annotation assessment, I found myself repeatedly:
- Re-clicking play/pause and dragging the seek bar for the same few seconds
- Looking up tag syntax (`<ga>`, `[hn]`, `<ol></ol>`, etc.) in a separate reference doc
- Losing my place in the transcript while switching windows

None of that is the actual skill being tested (listening accuracy). So I built a single-page tool to eliminate it.

## Features

- **Playback control**: variable speed (0.5x–1.25x), 3-second skip back/forward
- **A/B loop**: mark a start and end point in the audio and loop it on repeat — no more manually re-dragging the seek bar for a tricky phrase
- **One-click tag insertion**: buttons for speaker tags, overlap/quality markers, non-speech sounds, and backchannel words — each labeled with a plain-language description so you don't need to memorize the syntax
- **Synced text editor**: tags insert directly at your cursor position
- **Keyboard shortcuts**: `Ctrl+Space` play/pause, `Ctrl+←/→` skip, `Ctrl+L` toggle loop
- **Local export**: download the finished transcript as `.txt`
- **Fully offline**: single HTML file, no server, no data leaves your machine, no login

## Explicit non-goal

This is **not** a speech-to-text or auto-transcription tool. Annotation platforms pay specifically for human-verified transcripts, and most fingerprint for AI-generated submissions. Feeding AI output into these platforms as your own work is both against the terms of the job and defeats the actual purpose (producing clean human-labeled training data). This tool speeds up the human, it doesn't replace them.

## Tech

Single-file HTML/CSS/vanilla JS. No build step, no dependencies, no backend. Open `index.html` in any browser.

## What I'd extend next

- Auto-save to browser storage so a session survives a refresh
- Configurable tag sets (different platforms use different tag vocabularies)
- Waveform visualization for faster navigation to specific sounds

---

Built by [Vinod Kumar B N](https://vinod-ai-verse.lovable.app) — AI/ML student, Bangalore.
