# DrSim rendering changes

Based on Viser v1.1.1. This branch adds degree 0–3 spherical harmonics,
SuperSplat-style splat filtering, and valid three-component quad vertices.
Upstream sorting, cleanup, and on-demand rendering are preserved.

From the DrSim repository, with its Python environment active and Node.js 24+:

```bash
git submodule update --init third_party/viser
cd third_party/viser/src/viser/client
npm ci
npm run build
cd ../../../../..
python -m pip install -e third_party/viser
```

Restart the Python server and hard-refresh the browser. Use
`http://localhost:8080/?fixedDpr=1` to disable adaptive resolution on a
standard-DPI display.

To inspect our changes: `git -C third_party/viser diff v1.1.1 HEAD`.
