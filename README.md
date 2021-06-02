# Twitch Recorder Go by OP
Record Twitch Live streams & Upload to Google Drive if needed

This program can monitor and record multiple Twitch streams live and convert it to .mkv files.

## Requirements
[Streamlink](https://streamlink.github.io/)  If using streamlink download method (default)

[Ffmpeg](https://ffmpeg.org/) If using ffmpeg download method (specify -ffmpeg (./twitch-recorder-go -ffmpeg))

[Twitch](https://dev.twitch.tv/console) Register a Twitch app

## Drive
Ignore this, if you are not planning to upload to drive.

Specify -drive (./twitch-recorder-go -drive) to upload to drive.

[Drive](https://developers.google.com/drive/api/v3/enable-drive-api) Register a Google API APP with OAuth2 & Use Google Playground OAuth2 to get Access & Refresh tokens

[Playground](https://developers.google.com/oauthplayground/)

## Config

Create `config.json` file (use -config to specify the path to the config file)

```properties
{
 "twitch": {
  "client_id": "XXXXXXXXXX",
  "client_secret": "XXXXXXXXXX",
 },
 "vod_directory": "C:\\Users\\Overpowered",
 "channels": [
  "pokelawls",
  "sodapoppin"
 ],
 "twitch_app": {},
 "drive": {
    "refresh_token": "XXXXXXXXXX",
    "access_token": "XXXXXXXXXX"
 }
}
```

## Running the program

Run in a shell like cmd or bash terminal.

```shell script
./path-to-twitch-recorder-go/twitch-recorder-go -config ./config.json
```
## Build

1. Install [go](https://golang.org/dl/)
2. Git clone the project

Run in a shell like cmd or bash terminal.
```shell script
go build
```