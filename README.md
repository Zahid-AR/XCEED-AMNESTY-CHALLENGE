# 72 Hours to Act — XCeed (complete rebuild)

This is a new, self-contained slideshow-style website. **Only `index.html` is needed**. No CSS/JS assets, build process, or external libraries.

## GitHub Pages deployment
1. In `Zahid-AR/XCEED-AMNESTY-CHALLENGE`, open the root `index.html` file.
2. Click the pencil (Edit) icon. Select all old contents, replace with the contents of the new `index.html`, and commit. Alternatively, upload the new `index.html` to the repository root, replacing the old one.
3. Wait for GitHub Pages deployment, then hard-refresh with Ctrl+Shift+R.
4. Old `styles.css` and `app.js` files can remain in the repository but are not used by this new page.

## Play
- 13 full-screen slide-like stages, including situation, rules, roles, marketplace, three crises, three question checkpoints, and handover.
- Back and Undo controls; Undo rolls back purchases, choices, submitted answers, and navigation.
- Nine objectives, each with hard/medium/easy questions (27 question variants).
- After seeing a question, a team can switch resources if they can afford it; questions update accordingly.
- Crisis outcomes and resource spending use a shared budget; no persistent money tracker or action log.
- Progress is saved in the browser's localStorage. Restart resets the game after confirmation.

## Note
The three crisis decisions are deterministic. Trivia is an initial question set to be reviewed by workshop facilitators before use. The 7-minute first crisis is facilitator-paced rather than automatically timed.
