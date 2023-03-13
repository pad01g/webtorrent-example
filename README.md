# example file server and image viewer

## what is this

serve image via webtorrent and show it on browser. if central server has image, fetch it from there. if image is not found, switch to webtorrent.

## install

```
npm install
```

## run browerable http server

```
npx http-server
```

## run tracker server

```
npx bittorrent-tracker
```

## how to experiment

seed the same picture by webtorrent cli command

```
# installing together didn't work for some reason
npm install -g node-pre-gyp
npm install -g node-gyp
npm install -g webtorrent-hybrid

webtorrent-hybrid seed  'magnet:?xt=urn:btih:3f9c83eb47b1f029b4d7c7b45408dabe395cca47&dn=l.jpg&tr=wss%3A%2F%2Ftracker.btorrent.xyz&tr=wss%3A%2F%2Ftracker.openwebtorrent.com&tr=udp%3A%2F%2Ftracker.leechers-paradise.org%3A6969&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337&tr=udp%3A%2F%2Fexplodie.org%3A6969&tr=udp%3A%2F%2Ftracker.empire-js.us%3A1337&tr=http%3A%2F%2F10.24.95.8:8000%2Fannounce&tr=udp%3A%2F%2F10.24.95.8:8000&tr=ws%3A%2F%2F10.24.95.8:8000' --verbose --keep-seeding

```

then open `http://127.0.0.1:8080` to see if image is downloaded