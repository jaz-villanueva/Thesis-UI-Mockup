# Thesis UI Mockup

Tablet interface mockup for gesture and touch control of a 3-drone swarm.

Live: https://jaz-villanueva.github.io/Thesis-UI-Mockup/

## Install as an app (PWA)

- **Android / Chrome / Edge:** open the live link, then use the browser menu > *Install app* (or *Add to Home screen*).
- **iPad / iPhone (Safari):** open the live link, tap Share > *Add to Home Screen*.

The installed app opens fullscreen in landscape and works offline after the first load (hand tracking too, once it has loaded once).

When you change `index.html` or the icons, bump `VERSION` in `sw.js` so installed copies pick up the update.

## Proposed changes for the project repository

The `shujimaki/` folder holds changes staged for
[Shujimaki/touch-vision-drone-control](https://github.com/Shujimaki/touch-vision-drone-control). Each file sits at the path it will have there. None of them are in that repository yet.

- `shujimaki/CONTEXT.md`: revises DEC-06 and DEC-08, and adds DEC-13 to DEC-18. These cover obstacles, the panel layout, gesture lift-off and landing, OptiTrack Motive and layout sync, the interim 1.44 m ceiling, and the mockup's status as a design prototype. It also notes these in OPEN-01, OPEN-02, OPEN-05, OPEN-08 and OPEN-10.
- `shujimaki/README.md`: records OptiTrack Motive and links this mockup.
- `shujimaki/protocol/README.md`: adds the `course` message, the `layout_read` and `layout_apply` commands, and `drones[].link_quality`.
- `shujimaki/protocol/examples/`: the complete examples folder. The course follows proposal Figure 5, the altitude limits are 0.5 to 1.44 m, and there are two new examples for layout sync.

The project's `scripts/check.py` passes on these changes: ignored files, secrets, links, JSON and Mermaid.

## Third-party files

`vendor/mediapipe/` holds MediaPipe Tasks Vision 1.0.1 and the `gesture_recognizer.task` float16 v1 model (SHA-256 `97952348cf6a6a4915c2ea1496b4b37ebabc50cbbf80571435643c455f2b0482`). Both are copied unchanged from the pinned versions in the project README. MediaPipe is licensed under the Apache License 2.0; see `vendor/mediapipe/tasks-vision-1.0.1/LICENSE`.
