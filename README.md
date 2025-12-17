# CueTimer

A simple countdown timer for scripted events. Perfect for presentations, live broadcasts, or any scenario where you need timed cues with messages.

## Features

- **Script-based timing**: Define events with timestamps and messages
- **Visual countdown**: Large, readable countdown display
- **Audio alerts**: Beeps at T-2s and T-1s before each event
- **Screen flash**: Visual feedback when approaching events
- **Event queue**: See upcoming events while running
- **Jump to event**: Tap any queued event to skip ahead
- **Pause/Resume**: Full playback control
- **Auto-save**: Script persists in browser localStorage
- **Mobile-friendly**: Responsive design with wake lock to prevent screen sleep

## Script Format

Each line follows the format:
```
M'SS'' : message
```

Where:
- `M` = minutes
- `SS` = seconds
- `message` = text displayed during countdown

### Example

```
0'10'' : notification received
0'15'' : switch screen
0'20'' : click login
0'30'' : enter credentials
0'45'' : submit form
```

Events are sorted by timestamp automatically. The countdown shows the time remaining until each event triggers.

## Usage

1. Enter your script in the text area
2. Preview shows parsed events with durations
3. Click **START** to begin
4. Use **PAUSE** to pause/resume
5. Use **STOP** to return to edit mode
6. Tap any event in the queue to jump to it

## Deployment

Open `index.html` directly in a browser, or deploy as a static site.

## License

MIT
