# XCeed — 72 Hours to Act (v3)

Static browser game for GitHub Pages. Upload `index.html`, `styles.css` and `app.js` to the root of your repository. Enable Settings > Pages > Deploy from branch > main > /(root).

## Flow
1. Welcome and situation: 40 arrested students in fictional Navara; six missing.
2. Rules: start with £10,000 and complete at least **6 of 9 objectives** to qualify for Amnesty International to consider taking over the fictional case. Six is not an acceptance guarantee.
3. Allocate roles: Team Leader, Banker, Medical Lead, Legal Lead, Advocacy Lead, Handover Lead. **Only the Team Leader touches the computer.**
4. Preparation and resource purchases before the first crisis at minute 7.
5. Crisis 1: A/B choice, then three objective questions.
6. Crisis 2: A/B choice, then three objective questions.
7. Crisis 3: A/B choice, then three objective questions.
8. Free-form spoken handover to the fictional incoming Amnesty team. No SBAR template.

## Questions and resources
Each checkpoint offers science (Medical), Islamic history (Legal), and Islamic deen (Advocacy) general-knowledge questions. Correct answers award M1–M3, L1–L3 and A1–A3 respectively. Resource tier affects only the number of answer choices: budget 4 (hard), mid-range 3 (medium), premium 2 (easy). With no resource, the question is hard. There is no automatic objective completion from purchases.

**Upgrade rule:** Teams may see a question, then refund their active resource and buy a higher-tier resource to make that *same* question easier, if they have enough funds. The question remains answerable until they submit a choice. Once submitted, the answer is final and cannot be upgraded or retried.

One active resource per category. Refunds after crisis 1/2/3 are 70%/40%/10% of paid price, rounded to nearest £50. Resource prices reduce with each checkpoint. The premium medical resource retains the special perk of covering Crisis 1's £1,000 secure-care fee for option B.

The three A/B crisis outcomes and their financial consequences are fixed. The £2,000 donor withdrawal at Crisis 3 affects all teams. The game stores progress in browser localStorage and supports JSON export.

## Important
Amnesty International is used as a **fictional receiving organisation for educational purposes**. This project does not imply any real partnership or endorsement. For public release, confirm permission to use its name or change the in-game recipient to a generic international human rights organisation.

## Updating GitHub
Extract the ZIP, then upload and overwrite `index.html`, `styles.css`, `app.js` and optionally `README.md` in the repository root. Commit changes. Refresh the GitHub Pages website with Ctrl+Shift+R after deployment.
