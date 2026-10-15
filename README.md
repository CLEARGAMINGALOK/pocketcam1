# PocketCam for GitHub Pages (static hosting)

This version is designed to be hosted on GitHub Pages. It does **not** need you to run Node.js or host your own server.

## Publish it
1. Sign in to GitHub and create a new repository, e.g. `pocketcam`.
2. Upload `index.html` from this folder to the repository root.
3. Open **Settings → Pages**.
4. Under Build and deployment, choose **Deploy from a branch**.
5. Select the `main` branch and `/ (root)`, then save.
6. Wait for GitHub Pages to publish your site. Open the HTTPS URL it gives you on both phone and PC.

## Pairing
1. On the phone, open the site, choose **Phone**, enter a unique room code, and tap **Start phone camera**. Grant camera/microphone access.
2. On the PC, open the same URL, choose **PC viewer**, enter the exact same room code, and tap **Connect to phone**.
3. Keep both browser tabs open.

## Important limitations
- This static version uses the public PeerJS Cloud signaling service by default. It is convenient for a demo, but its availability, rate limits, privacy, and long-term support are not guaranteed. For production, use your own signaling server or a managed signaling service.
- Both devices need internet access. Some firewalls/NATs require TURN infrastructure, which this starter does not configure.
- The room code is not authentication. Do not use predictable codes on a public deployment.
- Audio is available in the PC browser stream. It does not automatically become a system-wide microphone for Discord, Zoom, or other apps. OBS can capture the viewer page as a Browser Source; other apps may require a virtual audio routing device.
- This is not Bluetooth audio. USB tethering can provide a network connection, but it does not turn a website into a native webcam driver.
- The phone browser must remain open while streaming.
