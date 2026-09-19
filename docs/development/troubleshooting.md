# Troubleshooting

**Status: Implemented guidance**

## Blank page

Serve the project through an HTTP server rather than `file://`. Then check the browser console for module paths and Phaser loading errors.

## Game starts without sound

Browsers usually require a user gesture before WebAudio can resume. Starting the game through the start button should unlock audio; this is normal browser behavior.

## Touch movement does not work

Confirm that the floating joystick appears when the dish is touched, and that the GF and pause buttons are not covered by the joystick layer. Automated touch checks cannot fully replace a real phone check.

## Experimental figures changed

First confirm that GF rules, the predator's committed lunge, and metric definitions were not changed. Rerun the fixed seed `1337` assay and check whether a new random-number consumption point changed the existing order. Report the changed setup and result rather than silently restoring a number.

## Save looks wrong

Use **Clear lineage save** and reload. This removes only the local lineage stored by the current browser site.
