CST LAN Challenge - Fist Fight A WebAR (Android & iOS)

Overview:
- Loads the animated FBX directly from AWS S3:
  https://cst-lan.s3.eu-north-1.amazonaws.com/Fist+Fight+A.fbx
  Local fallback: Fist_Fight_A.fbx
- Automatically normalizes height to 25 cm tabletop size and aligns fighter flush on y = 0.
- Cyber-HUD Glassmorphic loading screen with real-time streaming telemetry, 3-stage breadcrumbs (STREAM -> RIGGING -> READY), clenched cyber fist combat emblem, and smooth 3D reveal.

Cross-Platform 6-DoF AR (Walk 360° Around Fighter):
- Android (Chrome + ARCore WebXR): Plays the full Mixamo combat animation directly from FBX, scans for a real horizontal table surface, snaps fighter upright onto table facing you, locks with a persistent ARCore World Anchor, and enables 360° walk-around.
- iPhone (Safari + Apple AR Quick Look): Uses native Quick Look table plane anchoring.

Hosting:
- Host on HTTPS (Netlify, Vercel, GitHub Pages) — required for mobile camera & WebXR.
- Generate QR code: python make_qr.py https://your-hosted-domain/
