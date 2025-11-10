# DaVinci Resolve DNxHR Converter

A simple bash script that converts any video source into **DNxHR HQ** format (wrapped in `.mov`), which is compatible with the **Linux build of DaVinci Resolve**.

This project aims to overcome the codec incompatibility issue on DaVinci Resolve for Linux, which cannot natively decode H.264/H.265 codecs that are used widely.

## Requirements

[FFmpeg](https://ffmpeg.org) must be installed and included in `$PATH`.

## Installation & Usage

Clone this repository and use the bash script right away:

```bash
git clone https://github.com/OngYean/davinci-resolve-media-converter.git
cd davinci-resolve-media-converter
chmod +x ./convert-dnxhr

# This creates your_video_converted.mov within the same directory as the original file
./convert-dnxhr your_video.mov

# You can include multiple files as well
./convert-dnxhr your_video_1.mov your_video_2.mov

```

Additionally, you may move the script file to the user-space bin directory:

```bash
mkdir -p ~/.local/bin
cp convert-dnxhr ~/.local/bin/

# Now you can use this command globally within the user space
convert-dnxhr your_video.mov
convert-dnxhr your_video_1.mov your_video_2.mov
```