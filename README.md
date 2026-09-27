# Thesis UI Mockup

Tablet interface mockup for gesture and touch control of a 3-drone swarm.

Live: https://jaz-villanueva.github.io/Thesis-UI-Mockup/

## Install as an app (PWA)

- **Android / Chrome / Edge:** open the live link, then use the browser menu > *Install app* (or *Add to Home screen*).
- **iPad / iPhone (Safari):** open the live link, tap Share > *Add to Home Screen*.

The installed app opens fullscreen in landscape and works offline after the first load (hand tracking too, once it has loaded once).

When you change `index.html` or the icons, bump `VERSION` in `sw.js` so installed copies pick up the update.

## Proposed changes for the project repository

`CONTEXT.md` and `protocol/examples/` are changes staged here first for
[Shujimaki/touch-vision-drone-control](https://github.com/Shujimaki/touch-vision-drone-control), at the same paths. They are not in that repository yet.

- `CONTEXT.md`: adds DEC-13. Only the restricted zone rejects drags, and only in course trials. O1 and O2 are left to the onboard Multi-ranger stop, and there is no route planning.
- `protocol/examples/welcome.json`: course positions now match proposal Figure 5 (O1 and O2 are 53 x 51 cm, H1 at 1.31, 2.70; H2 and H3 at x 3.99, both yaw 90; pads at y 0.45).
- `protocol/examples/input-three-drones-climbing.json`, `telemetry-cf3-defensive-hover.json`: drone positions and range readings moved so they stay consistent with the corrected course.

The project's `scripts/check.py` passes on these changes.
