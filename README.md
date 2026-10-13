# PhoneCam (Vercel static website)

A small, original browser-based phone camera → OBS prototype. It uses WebRTC via PeerJS and the PeerJS cloud signaling service. It does not include a watermark or upload video to your Vercel site.

## Deploy to Vercel
1. Create a GitHub repository and upload `index.html` and `vercel.json`.
2. Import that repository in Vercel.
3. Deploy with the default settings (no build command, no output directory needed).
4. Open the deployed HTTPS URL on your iPhone 6 Plus in Safari.
5. Tap **Use this device as camera** → **Start camera** → allow camera/microphone.
6. Copy the viewer link and add it in OBS as **Sources → + → Browser**.

## How it works
- Vercel hosts only the static page.
- PeerJS Cloud is used for signaling; WebRTC attempts to send video directly between the phone and PC.
- If a network requires a TURN relay, this minimal prototype does not provide one, so the connection may fail on some networks. Same-Wi-Fi connections are a good first test.
- Keep Safari open and prevent the phone from sleeping while using the camera.
- Use a private viewer URL. Anyone who obtains the link may be able to view the camera feed.

## Limitations
- Prototype, not a full VDO.Ninja replacement.
- PeerJS CDN and PeerJS Cloud are third-party dependencies.
- Audio playback/autoplay behavior can vary in OBS Browser Source.
- Resolution depends on the phone, browser, heat and network.
- No analytics, accounts or persistent storage.

## License note
This is an original minimal implementation, not a copy of VDO.Ninja's source code or branding. If you instead fork/modify VDO.Ninja itself, review its AGPL-3.0 license and comply with the applicable source-code and attribution obligations.
