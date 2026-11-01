# XCeed Navara Response — GitHub Pages

A slideshow-based team workshop for five devices, using the approved Crisis 1 and 2 puzzle screens and Crisis 3 version 2. **No hint controls.**

## Publish

1. Create a new GitHub repository, for example `xceed-navara`.
2. Upload **all files and the `puzzles` directory** from this ZIP to the repository root. Do not upload the ZIP itself.
3. Go to **Settings → Pages → Build and deployment → Deploy from a branch**, select `main` and `/ (root)`, then Save.
4. Open `https://YOUR-USERNAME.github.io/xceed-navara/`.

## IMPORTANT: cross-device sync needs Firebase

GitHub Pages only serves static files. It cannot, by itself, keep five phones in sync. The website includes Firebase Realtime Database integration, which requires **one-time configuration**.

1. Create a Firebase project at https://console.firebase.google.com/.
2. Add a **Web app** and copy its `firebaseConfig` object.
3. Enable **Authentication → Sign-in method → Anonymous**.
4. Create **Realtime Database** (not Firestore), choose a region and note its `databaseURL`.
5. Edit `config.js` to set `window.XCEED_FIREBASE_CONFIG = { ... }`, including `databaseURL`.
6. Set Realtime Database rules for a short, controlled workshop (example below). Publish the updated `config.js` to GitHub.

Example temporary rules for a supervised pilot:

```json
{
  "rules": {
    "teams": {
      "$team": {
        ".read": "auth != null",
        ".write": "auth != null"
      }
    }
  }
}
```

**Security warning:** These simple pilot rules let any anonymously signed-in user with your Firebase config read or modify team data. Use unpredictable team codes, do not store personal information, and tighten rules before a public conference. For production, add server-enforced role permissions and team-code authentication, preferably with Cloud Functions or a custom backend. The client-side role restriction is a usability feature, **not a security boundary**.

## Using the slideshow

- Each person opens the same website and enters the same team code, but selects a distinct role.
- The leader sees briefing, decisions, and team progress. Each specialist sees **only their assigned puzzle** in each crisis. Finance sees budget and handover.
- **ORANGE Next** is a leader-only preview. It does not change other devices.
- The leader clicks **RED Release** to make the next arrow red on every device.
- Everyone clicks the **RED Next** arrow. When all five roles have acknowledged, the next slide appears on all devices.
- The leader can use **Force advance** for rehearsals if a participant is absent.
- Only the leader can select interventions. The team budget begins at £12,000.

## Limitations

- The app has not undergone real-device or live Firebase end-to-end testing. Test with five devices before the event.
- The original puzzle HTML files are embedded as iframes with role-specific display filters; this preserves their approved mechanics and appearance.
- Client-side state is not suitable for high-stakes privacy or secure competition. It is a workshop game.
- Without Firebase, local demo mode can synchronise tabs on one browser origin but **not separate devices**. Do not assume manual mode is networked.
