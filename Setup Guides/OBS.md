# Setting Up OBS

OBS is a fantastic tool for recording videos, adding overlays, and controlling inputs for screencasts.

## Install

### Linux

Tested on `Pop!_OS 19.04`, following these instructions: [Linux Install Directions](https://obsproject.com/wiki/install-instructions#ubuntu-installation).

**Note:** I added the `-y` flag because I've run these commands enough to know what they're doing.  If you're unsure, don't use it!

1. Check if `ffmpeg` exists using `whereis ffmpeg`.
2. If `ffmpeg` isn't installed, use `sudo apt-get install ffmpeg -y`
3. `sudo add-apt-repository ppa:obsproject/obs-studio -y`
4. `sudo apt-get update`
5. `sudo apt-get install obs-studio -y`

### Windows

1. Download the latest Windows Version of OBS
2. Run the installer
   - **Tip:** If running multiple drives, make sure to install it on an appropriate drive.  I put it on my SSD C:/ drive to maximize performance of the application.
   - Default settings should be fine, but make sure to read each step thoroughly!
3. Move onto configuring OBS

## Settings

### General

1. Theme: Dark

### Output

1. Recording
   - Path: `W:/obs/src` (External drive, don't waste SSD life)
   - Check "Generate File Name without Space"

## Resources

- [OBS](https://obsproject.com/download)
- [Linux Install Directions](https://obsproject.com/wiki/install-instructions#ubuntu-installation)
