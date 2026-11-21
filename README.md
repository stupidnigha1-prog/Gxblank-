# GXPAIN Controller Studio

GXPAIN is a portable, single-page controller tester and macro recorder. Open
`index.html` in a current desktop browser; no build step or installation is
required. If the browser does not expose a connected gamepad when opened as a
local file, serve the page from `localhost` or HTTPS and try again.

## Use

- Connect a gamepad and press a button to see live input through the browser's
  Gamepad API. Keyboard and clickable diagram input can also be captured while
  this page is focused.
- Select a controller layout and save a local profile. Saved data stays in the
  current browser on the current device.
- Choose **Start Recording**, use the keyboard or gamepad, then choose **Stop**.
  **Preview Playback** replays the recorded sequence in the GXPAIN page.
- Choose **Export File** to save a portable JSON macro. On another device, open
  GXPAIN and use **Import File** to load and preview it.

## Limitations

Web browsers do not provide a standard way for a page to inject keyboard events
into other applications, send output to a physical gamepad, or write macro
firmware to a controller. GXPAIN therefore records and previews inputs inside
its own page; exported macro files can be moved between devices, but they do
not install themselves into a controller. Browser timers and connected
hardware determine actual input latency; 1 ms timing cannot be guaranteed.
Stick speed and deadzone are saved as profile settings and do not alter the
physical controller.
