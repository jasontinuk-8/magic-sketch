# Magic Sketch Web 1.0 (PWA)

Retro pixel drawing with six ink colours, FREE/AXIS, REVERSE, DRAW, CLEAR, tap-to-start/calibrate, Save/Share, and device tilt.

## Publish (required for iPhone motion)

Upload the **contents** of this folder to an HTTPS static host (GitHub Pages, Netlify, Cloudflare Pages). Open the resulting HTTPS URL in iPhone Safari. Tap **Enable motion controls**, choose **Allow**, then tap the canvas to choose the starting point and calibrate. Use the tilt controls; tap DRAW to toggle drawing.

To install on iPhone: Safari Share → Add to Home Screen → Add. The service worker caches resources after the first online load. If iOS Home Screen mode doesn't present the motion permission prompt, first grant permission in Safari and test; browser/platform behavior varies.

Desktop fallback: tap canvas to start; arrow keys move; space toggles drawing. Browser permissions, device sensor axes and refresh rates differ. Recalibrate after rotating phone.

## Notes

- HTTPS or localhost required for sensor access. Opening index.html as a local file is not a reliable way to use motion/PWA.
- AXIS chooses the dominant axis per frame. Default direction follows Magic Sketch iOS 1.6 (legacy reversed direction).
- This is a web implementation, not a byte-for-byte SwiftUI port. Real iPhone Safari testing is required.
- No account, tracking, or remote backend. Images generated locally.
