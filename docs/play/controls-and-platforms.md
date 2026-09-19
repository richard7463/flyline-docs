# Controls and platforms

**Status: Implemented**

## Desktop browser

WASD, arrow keys, or a held mouse pointer control direction. Space triggers GF escape when it is READY. Pause opens the menu without deleting the lineage.

## Touch devices

Press and drag in the dish to use the floating joystick. The joystick appears at the touch position. **GF ESCAPE** stays in the lower-right area so it does not compete with the full-screen joystick.

## Browser and saves

The project uses Phaser 3 and native ES modules. Lineage state is stored in the current browser's `localStorage`; clearing site data or choosing **Clear lineage save** starts over.

A modern desktop or mobile browser is recommended. Automated mobile checks can verify controls and events, but they cannot replace real-device checks of touch feel, sound, orientation, or long-session pacing.
