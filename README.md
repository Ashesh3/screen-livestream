![image](https://i.imgur.com/vNY4o3W.png)

This project allows you to stream any window, tab or your whole desktop to a streaming service like Twitch or Youtube Live right from within the browser without any additional software!

# HTML5 to RTMP streaming gateway proxy

This project intends to allow an endpoint user to submit RTMP live video streaming directly using web browser and `getUserMedia`, without installing additional software. Currently, only Firefox with `MediaRecorder` API is supported.

## Usage

Start the server by `npm install` and `node server.js`, then open the browse to http://127.0.0.1:1437

Please make sure there's an rtmp server up and running; try `nginx-rtmp-module` if you don't have one.

In production, the server should limit what the client can choose to push stream to.

## How does it work

From `getUserMedia`, `MediaRecorder`, via `socket.io` to `nodejs`, then to `ffmpeg` transcoding and publishing to `rtmp`. You can guess what happened in between.
