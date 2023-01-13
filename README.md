### Audio Recorder
Opus Audio Recorder is a web application using javascript, nodejs, express, Socket.io, Opus library, ffmpeg.

# Run on localhost.
---
# Audio Recorder
If support for MediaRecorder API is detected( in case of Firefox), my recorder is just a wrapper for it, for other case, I am using [Rillke](https://github.com/Rillke)'s [opus library](https://github.com/Rillke/opusenc.js) for compressing wav audio into ogg file on client side.

We can just host the files in `client` folder in any server, if you just want to record audio from microphone in one shot and save as `ogg` file, but if you do not want to run out of browser memory( while recording long podcasts and such,) you can keep sending the data as chunks to the server, at desired time intervals and server would join all of them into single file( `ffmpeg` needed for browsers other than firefox) and provide you the final link.


### Things needed:
* node (for server)
* ffmpeg (for media manipulation, OPTIONAL.)


### set-up:
 * npm install 
 * `ffmpeg` must be pre-installed and must be part of path

to start the application, just type `npm start` in the project root folder.

### Sources:
  * [Opus](https://github.com/Rillke/opusenc.js)
  * [Opus( older one)](https://github.com/kazuki/opus.js-sample)
  * [Wav Recorder](https://github.com/mattdiamond/Recorderjs)


### Overall Modules/Tools/Technologies which are used in this project:-
  * Nodejs
  * Express (to manage servers and routes.)
  * javascript
  * Socket.io (library used for the event-based communication between the client and the server.)
  * Opus library (Opus is used for high versatile audio codec.)
  * ffmpeg (to convert and play the audio. ffmpeg is a node module.)

