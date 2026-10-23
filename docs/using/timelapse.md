# Timelapse

## Turning it on

Pick **Video = timelapse** in the installer. It installs `ffmpeg`, which makes the videos.

## How it records

| Setting | Choices | Default |
|---|---|---|
| Mode | every layer, or every few seconds | every layer |
| Interval (interval mode) | seconds between frames | 10 s |
| Frame rate | frames per second in the video | 25 |
| Keep | how many timelapses to keep per printer | 20 |

A timelapse starts with the print and the video is made when it ends. Prints with fewer than two frames don't make a video.

## Finding your videos

Open the printer's **Timelapses** tab to watch, download or delete them. They're stored in Printer Buddy's `data/` folder.
