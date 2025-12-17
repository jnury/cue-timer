# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

CueTimer is a single-page web application for running timed cue sequences. It's designed for presentations, broadcasts, or any scenario requiring countdown timers with associated messages.

## Architecture

The entire application lives in `index.html` - a self-contained file with inline CSS and JavaScript (no build tools or dependencies).

**Key components:**
- **Edit mode**: Script input with live preview and parsing
- **Play mode**: Countdown display, message queue, and playback controls

**Script format**: `M'SS'' : message` (e.g., `0'10'' : first event` means trigger at 10 seconds)

**State management**: Global variables track events array, current index, timing, and playback state. Script content persists to localStorage under `cue-timer-script`.

**Audio/Visual feedback**: Web Audio API beeps at T-2s and T-1s, with screen flash. Wake Lock API prevents screen sleep during playback.

## Development

Open `index.html` directly in a browser. No build step or server required.
