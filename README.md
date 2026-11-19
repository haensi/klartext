# Klartext

Reads the secret messages hidden in striped puzzle boxes. Point the camera at a box and
the message appears in place, or take or choose a photo.

Everything runs in the browser. The page loads nothing from other sites and pictures
never leave the device.

## Put it on GitHub Pages

1. Create a new **public** repository on GitHub, for example `klartext`.
2. Upload every file in this folder to the top level of the repository
   (**Add file**, **Upload files**, drag them in, **Commit changes**).
3. Open **Settings**, then **Pages**. Under **Build and deployment** choose
   **Deploy from a branch**, branch `main`, folder `/ (root)`, and **Save**.
4. After a minute or so the site is live at `https://<your-username>.github.io/klartext/`.

With git instead of the upload page:

```sh
cd klartext
git init -b main
git add -A
git commit -m "Klartext"
git remote add origin https://github.com/<your-username>/klartext.git
git push -u origin main
```

Then do step 3 once.

To serve it at `https://<your-username>.github.io/` itself, name the repository
`<your-username>.github.io`. Nothing in the files needs to change either way; all
paths are relative.

## Use it like an app on the iPhone

Open the site in Safari, tap **Share**, then **Add to Home Screen**. It gets its own
icon, opens full screen, and keeps working without a connection after the first visit.

Safari asks for camera access each time. To allow it for good:
Settings, Apps, Safari, Camera, **Allow**.

## Files

| File | What it is |
| --- | --- |
| `index.html` | The whole app: camera loop, stripe detection, decoding, interface. |
| `manifest.webmanifest` | Name, colours and icons for the home-screen app. |
| `sw.js` | Lets the app open offline. It always tries the network first, so an update you push shows up on the next visit. |
| `icon-192.png`, `icon-512.png`, `apple-touch-icon.png`, `favicon-32.png` | Icons. |
| `.nojekyll` | Tells GitHub Pages to serve the files as they are. Optional; your file manager may hide it. |

## Tips for a clean read

- Hold the phone about 15 to 25 cm from the page and keep the box inside the corner marks.
- If the text looks mushy, try **2×** and a little more distance, or use **Freeze**.
- Good, even light helps more than anything else.
