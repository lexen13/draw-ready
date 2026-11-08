# Draw Ready (GitHub Pages version)

Camille's AUMT CPT1 study app as an installable web app.

## Publish
1. Create a repo (e.g. `draw-ready`) and upload every file in this folder to the root.
2. Repo **Settings → Pages**: Source = *Deploy from a branch*, Branch = `main` / root. Save.
3. Open `https://<your-username>.github.io/draw-ready/` on her iPhone in **Safari** → Share → **Add to Home Screen**.
4. She always opens it from the home-screen icon. Progress saves on the phone automatically.

## Optional: save online (Firebase, free tier)
1. console.firebase.google.com → Add project.
2. **Build → Authentication → Get started → Email/Password → Enable.**
3. **Build → Firestore Database → Create database** (production mode), then **Rules** tab: paste `firestore.rules`, Publish.
4. **Authentication → Settings → Authorized domains → Add** `<your-username>.github.io`.
5. **Project settings → Your apps → Web app (</>)** → register → copy the `firebaseConfig` values into `firebase-config.js` (replace `window.DR_FIREBASE = null;`).
6. Commit. In the app: Today tab → Backup → sign in or create an account. The chip reads "✓ Saving online to …" when it works.

## Updating
Replace `index.html` (and `sw.js`) with the new build and commit. Leave `firebase-config.js` alone once it's filled in. The app picks up the new version the next time it opens with a connection.
