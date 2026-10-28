# 72 Hours to Act — XCeed conference simulation

A complete static, browser-based team game for the XCeed **Beyond Medicine** conference. No npm, framework, backend, accounts, or external API is required. Open `index.html` locally or host the folder with GitHub Pages. The site uses Google Fonts when connected to the internet, with system-font fallbacks offline.

> **Fictional scenario.** Navara and the events described are invented for educational use. The game depicts a fictional Amnesty International takeover as part of its narrative; this does not imply real-world involvement, endorsement, or approval by Amnesty International.

## Overview

- **Audience:** ~100 conference attendees, in workshop rotations of ~30; teams of ~5–6 share a laptop/tablet.
- **Total workshop:** 60 minutes, including briefing, 30-minute game, SBAR preparation, spoken handovers, and debrief.
- **Mission:** Respond to the disappearance of six students following the arrest of 40 university demonstrators in the fictional country Navara.
- **Budget:** £10,000 initially. Teams can buy, sell, and replace resources; resource prices decrease at each checkpoint.
- **Resources:** 9 options, grouped into Medical, Legal and Advocacy; one active resource per group.
- **Decisions:** 3 shared binary crisis decisions, with hidden deterministic outcomes. Resources give information, progress, fundraising, and a single agreed premium medical fee waiver; they do not change the underlying outcome.
- **Scoring:** 9 objectives (3 per category) plus final cash and quality of SBAR handover. The website tracks objectives and cash separately.
- **Persistence:** automatic localStorage on the team's browser, plus downloadable JSON record and printable SBAR handover.

## Suggested 60-minute session

| Elapsed | Activity | Website action |
|---|---|---|
| 00:00–05:00 | Facilitator introduces fictional scenario, rules, roles | Enter team name, read mission |
| 05:00–10:00 | Team chooses resources, allocates budget | Purchase up to one per category |
| **10:00** | Crisis 1: medical ethics | Click **Begin Crisis 1** |
| 10:00–17:00 | Review updates, choose A/B, log result, rebalance resources | Make decision, finish checkpoint, use market |
| **17:00** | Crisis 2: unverified photographic evidence | Click **Reveal Crisis 2** |
| 17:00–22:00 | Review updates, choose A/B, log result, rebalance resources | Make decision, finish checkpoint, use market |
| **22:00** | Crisis 3: secret tribunal, £2k funding withdrawal | Click **Reveal Crisis 3** |
| 22:00–30:00 | Decide on emergency campaign; finish simulation | Make decision, finish checkpoint |
| 30:00–40:00 | Prepare handover | Complete four SBAR fields |
| 40:00–55:00 | All teams read SBAR aloud; compare trade-offs | Print/export if needed |
| 55:00–60:00 | Facilitator closes; discuss transfer to clinical practice | Debrief |

**Facilitator note:** The website is deliberately **facilitator-paced**, not auto-timed. Announce the three crises at the agreed times and ask teams to click when ready. This accommodates different group speeds and avoids a participant being interrupted mid-discussion.

## Team roles (optional, recommended)

1. **Team lead:** chairs the decision and delegates tasks.
2. **Finance lead:** checks cash and resource purchases.
3. **Medical lead:** considers patient safety and confidentiality.
4. **Legal lead:** considers evidence, representation, and legal risk.
5. **Advocacy lead:** considers families, media, fundraising, and public trust.
6. **Scribe / SBAR lead:** prepares the final spoken handover.

Roles are discussion aids, not separate accounts or game permissions. Each team uses a single shared device.

## The nine objectives

### Medical
- **M1** Identify urgent medical needs.
- **M2** Secure medical assessment and treatment.
- **M3** Establish ongoing medical monitoring.

### Legal
- **L1** Confirm the whereabouts of all six missing students.
- **L2** Secure independent legal representation.
- **L3** Initiate a formal legal challenge.

### Advocacy
- **A1** Establish safe communication with the families.
- **A2** Raise verified public and international awareness.
- **A3** Secure funding and external organisational support.

An objective is achieved only when the active resource explicitly awards it at a checkpoint. Objectives newly awarded at the current checkpoint are provisional until that checkpoint is completed. Selling the resource during that checkpoint revokes its newly awarded objectives and donations; achievements and funds confirmed at earlier checkpoints are retained.

## Resource mechanics

| Tier | Initial | After Crisis 1 | After Crisis 2 | After Crisis 3 |
|---|---:|---:|---:|---:|
| Budget | £1,500 | £1,200 | £900 | £600 |
| Mid-range | £3,000 | £2,400 | £1,800 | £1,200 |
| Premium | £5,000 | £4,000 | £3,000 | £2,000 |

- One active resource per category. To switch, sell the current one and buy a replacement during the market phase.
- **Refund:** 70% of the actual amount paid at checkpoint 1; 40% at checkpoint 2; 10% at checkpoint 3; rounded to the nearest £50.
- Buying is available during preparation and **between** crises. Selling is also available while reviewing a crisis; newly awarded checkpoint progress is forfeited if sold.
- A newly purchased resource starts earning progress at the **next** crisis checkpoint, never retroactively. No new purchases are available after Crisis 3 because there is no subsequent earning checkpoint.
- Teams cannot buy a resource or select a fee-requiring option unless they have sufficient available cash. The Crisis 3 donor withdrawal may create a negative balance, which the team can address by selling resources.
- The premium medical resource pays the £1,000 fee for Crisis 1 option B if active at the moment of decision. It does not change the clinical outcome.
- Advocacy fundraising is awarded automatically at the relevant checkpoints while the resource is active. No duplicate payouts for repeated renders or visits.

### Resource progress matrix

The following assumes a resource was purchased at the start and retained. Later purchases miss prior checkpoints.

| Resource | Crisis 1 | Crisis 2 | Crisis 3 | Total advocacy donations |
|---|---|---|---|---:|
| Volunteer Medical Network | M1 | — | M2 | — |
| Local Emergency Medical Team | M1, M2 | — | M3 | — |
| International Medical Response Team | M1, M2, M3 | — | — | — |
| Student Legal Clinic | — | L1 | — | — |
| Local Human Rights Lawyer | — | L1, L2 | L3 | — |
| International Legal Team | L1, L2 | L3 | — | — |
| Student Advocacy Network | A1, +£100 | +£150 | +£250 | £500 |
| Human Rights Campaign Team | A1, +£400 | A2, +£600 | A3, +£1,000 | £2,000 |
| International Advocacy Coalition | A1, A2, +£1,000 | A3, +£1,500 | +£1,500 | £4,000 |

## The three crises

### Crisis 1 — A Life on the Line (minute 10)

A doctor reports that Mariam Hassan, 21, with Type 1 diabetes may have gone more than 24 hours without insulin. The doctor offers to circulate identifiable medical records and location without consent, potentially accelerating care but exposing her to risk. A secure, independent pathway costs £1,000. A relief fund offers £2,000 if care is safely arranged.

- **A — Circulate records:** the records leak, exposing Mariam; safeguarding costs £1,000, relief funding withdrawn. **Net −£1,000.**
- **B — Pay for confidential assessment:** care arranged, £2,000 relief grant. **Net +£1,000**, or **+£2,000** if the premium medical resource pays the fee.

**Discussion:** Is faster action always better? How do consent, proportionality, safeguarding and clinical urgency interact? Note that emergency sharing of information can be lawful and ethical in some circumstances; this exercise tests *unnecessarily broad circulation* versus a secure, proportionate route, not a universal rule that consent is always required before lifesaving disclosure.

### Crisis 2 — The Evidence That Could Change Everything (minute 17)

Anonymous photographs allegedly show the six missing students. Publication offers an immediate conditional £3,000 donation, but the donor will reclaim it if the images are proved false. Detainees may be transferred within six hours.

- **A — Publish:** £3,000 initially arrives, then must be repaid after the photographs are proven fake. A fictional correction/settlement costs £2,000. **Net −£2,000.**
- **B — Withhold:** the photographs are later shown to be fake; a supporter donates £500. **Net +£500.**

**Legal resource intelligence:** Student Legal Clinic estimates 15% chance fake; Local Human Rights Lawyer 40%; International Legal Team 60%. These are fictional, deliberately different assessments based on unequal investigation capability, not empirically calibrated probabilities. The true outcome is the same for every team.

**Discussion:** When is evidence strong enough to publish? How do urgency, reputational risk, financial temptation and misinformation interact?

### Crisis 3 — The Final Countdown (minute 22)

All six students face a secret military tribunal in 12 hours; sentencing may follow immediately. A donor withdraws £2,000 from each team's **cash balance**. An international emergency campaign costs £3,000.

- **A — Fund campaign:** costs £3,000; campaign secures a temporary postponement and attracts £5,000 donations. **Net +£2,000**, excluding the separate −£2,000 donor withdrawal. Requires £3,000 available cash.
- **B — Preserve funds:** tribunal proceeds without postponement; a supporter donates £500. **Net +£500**, excluding the donor withdrawal.

**Discussion:** When is it worth risking scarce funds on a time-sensitive opportunity? How does prior resource allocation affect what options remain open?

## Handover and debrief

At 30 minutes, the simulation ends. Teams prepare an **SBAR** handover:

- **Situation:** Immediate threat to the six students.
- **Background:** Arrests, previous crises, major decisions.
- **Assessment:** Verified facts, objectives achieved, remaining risks, available cash.
- **Recommendation:** What the incoming fictional Amnesty team should prioritise next.

Every team reads its handover aloud. Compare both the **objective score /9** and **remaining cash**; do not use cash alone as a measure of ethical or operational success. Ask teams what they delegated, how they managed uncertainty, and what changed under time pressure. Connect this to clinical A2E leadership, escalation, resource allocation, closed-loop communication and SBAR.

## GitHub Pages publishing

1. Create a new GitHub repository (for example `72-hours-to-act`).
2. Upload **`index.html`**, **`styles.css`** and **`app.js`** to the repository root. Uploading this README is optional but recommended.
3. In GitHub, open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**, select **main**, select **/(root)**, and save.
5. GitHub will provide a public `https://<username>.github.io/<repository>/` URL when the site is deployed.
6. Open the URL on a laptop or tablet and test one full game before the conference.

The website is static, so a GitHub Pages deployment does not require npm, a build step, or a server. Any team with the URL can start a separate local session on its own device.

## Editing the game

All game content and prices are in `app.js` in the `DATA` object:

- `DATA.objectives` — nine objectives.
- `DATA.resources` — names, descriptions, perks and four progress updates for each resource.
- `DATA.crises` — crisis narratives, choices and hidden outcomes.
- `price()` — discount schedule.
- `refund()` — cancellation schedule.
- `beginCrisis()` — checkpoint progress and funding.
- `decide()` — choice validation, premium medical fee coverage and fixed outcomes.

**If changing objective timing or amounts, play-test from a fresh session.** The Reset button clears local progress. Saved games created with earlier content may not reflect new rules.

## Technical notes and limits

- No real-time multiplayer, shared facilitator dashboard, accounts, or central score collection. Each team's data is stored locally in its browser via `localStorage`.
- A facilitator cannot see other teams' results automatically. Teams can download a JSON record or print their handover and share it manually.
- Local storage can be cleared by browser settings or private browsing. Export the record before closing or switching devices.
- No anti-cheat controls. Participants who inspect the JavaScript can read hidden outcomes; this is intended as a collaborative educational workshop, not a competitive secure assessment.
- The website is usable offline after its files are available locally; external web fonts may not load.
- Designed for current Chrome, Edge, Firefox and Safari. Use a modern browser and test your intended devices.
- The medical and legal details are fictional teaching scenarios, not clinical or legal advice.

## Conference facilitator checklist

- Test the full game on the venue Wi-Fi and one phone/tablet.
- Share the URL/QR code, and confirm each team has one device.
- Announce crises at minutes 10, 17, and 22; do not show the hidden outcomes beforehand.
- Tell teams that the same decision outcome applies to everyone, but resources may offer advice and agreed perks.
- At 30 minutes, ensure teams have clicked through to the SBAR screen.
- Ask each team to present its SBAR; discuss trade-offs, not just the final scores.
