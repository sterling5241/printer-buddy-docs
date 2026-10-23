# Camera streamer

Printer Buddy's camera streamer is a replacement for crowsnest and camera-streamer. It streams your USB, Pi and network cameras and is set up, updated and controlled from Printer Buddy like every other part.

## Tiers

| Tier | What it does |
|---|---|
| **off** | Streamer not installed |
| **light** | One camera, MJPEG (ustreamer) |
| **basic** | Every USB / Pi camera, MJPEG (ustreamer) |
| **full** | Adds network cameras and WebRTC (go2rtc); needs more CPU |

Pick it with **Camera streamer** in the installer, or switch tiers in the **Updates** list (home page ☰). It runs as its own service, `printer-buddy-streamer`, which you can restart or stop from the home page ☰ drawer.

## Cameras

Each printer's cameras come from Moonraker. On a printer page, the camera's settings let you add or edit Moonraker cameras, flip or rotate them and pick the **main camera** &mdash; the one the AI and timelapses use.
