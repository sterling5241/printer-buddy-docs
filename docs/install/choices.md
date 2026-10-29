# Install choices

The installer asks these when you install, and you can change them later with **2) Change setup**. They're saved in `printer-buddy.env` in the Printer Buddy folder.

| Choice | Options (first = default) |
|---|---|
| Interface | basic, advanced |
| AI detection | off, basic, heavy |
| Video | snapshots, live, timelapse |
| Notifications | basic, advanced |
| Remote access | off, on |
| Camera streamer | off, light, basic, full |
| Release channel | stable, nightly |

## Interface

- **basic** &mdash; dashboard, Quick View and each printer's status page.
- **advanced** &mdash; everything in basic, plus Control, Console, Files, History, list view and printer groups.

## AI detection

- **off** &mdash; no failure detection.
- **basic** &mdash; light model that runs on a Pi.
- **heavy** &mdash; bigger, more accurate model; needs a strong PC or a GPU.

See [AI failure detection](../using/ai.md).

## Video

- **snapshots** &mdash; camera pictures, refreshed every few seconds.
- **live** &mdash; smooth live stream.
- **timelapse** &mdash; live stream plus a timelapse of every print (installs `ffmpeg`).

## Notifications

- **basic** &mdash; ntfy or Discord when prints start, pause, finish or fail.
- **advanced** &mdash; basic plus Telegram, Pushover and email, and progress updates.

## Remote access

- **off** &mdash; only reachable on your home network.
- **on** &mdash; share links that work from anywhere. See [Remote access](../using/remote.md).

## Camera streamer

- **off** &mdash; streamer not installed.
- **light** &mdash; one camera, MJPEG (ustreamer).
- **basic** &mdash; every USB / Pi camera, MJPEG (ustreamer).
- **full** &mdash; adds network cameras and WebRTC (go2rtc); needs more CPU.

See [Camera streamer](../using/camera-streamer.md).

## Release channel

- **stable** &mdash; tested releases.
- **nightly** &mdash; the newest builds, may have bugs.

You can also put single parts on nightly &mdash; see [Dev/beta builds](../updates/dev-builds.md).

## Setting them without the menu

Every choice has a command-line flag:

```bash
./install.sh --ui advanced --ai basic --video timelapse --stream basic
```
