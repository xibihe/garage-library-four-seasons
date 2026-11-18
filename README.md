# Garage Library · Four Seasons

An interactive Gaussian splat artwork by [xibihe](https://github.com/xibihe). A camera path passes through the same garage library in four seasons. Click the scene to start a small ripple from that point. Ripples from repeated clicks can travel together.

## Run locally

Keep `index.html` and the four `season-*.spz` files in one directory. Start a static server from that directory:

```sh
python3 -m http.server 8000 --bind 127.0.0.1
```

Open [localhost:8000](http://127.0.0.1:8000/) in a WebGL 2 browser. The viewer loads Three.js and Spark from their CDNs. Each season contains two million splats at the original resolution.

## Controls

- The original five-view camera path plays once when the scenes finish loading. Use **Camera path** to replay it or save your own views in the current browser.
- Select **Small ripple**, **Double crest**, or **Crosscurrent** under **Wave**, then click the scene. Each click launches the selected effect independently. The season buttons jump directly to a scene.
- Drag to look, right-drag or Shift-drag to pan, and scroll to move forward or back. Use WASD to walk, Q to lower the camera, and E to raise it. Manual camera movement takes over during path playback.
- Press H to toggle the interface. Use **Record** to capture an MP4 on browsers that support H.264 through WebCodecs.

## Credits and license

Copyright © 2026 [xibihe](https://github.com/xibihe). The viewer source and project documentation are available under the [MIT License](LICENSE). The bundled SPZ scene assets are outside the source license.

The walking motion was inspired by Will Eastcott's [Splat Walk](https://github.com/willeastcott/splat-walk).
