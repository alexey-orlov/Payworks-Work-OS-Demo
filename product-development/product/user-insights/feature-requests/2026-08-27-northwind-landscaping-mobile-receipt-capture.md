---
account: northwind-landscaping
requested: 2026-08-27
area: expense-management
type: feature
priority_signal: must-have
tracker_ref: "-"
source: ../../customers/accounts/northwind-landscaping/calls/summaries/2026-08-27.md
features: []
initiatives: [expense-management-vp2]
updated: 2026-08-31
---

# [Expense Management] Mobile receipt capture with site/job attribution and offline queuing

**Who asked:** Their Controller at Northwind Landscaping — the person who owns finance, payroll reporting, and the entire expense process end to end.

**The underlying need — photo is table stakes; site attribution is the actual unlock.** The current process loses $3,000–$4,000 a year in unreadable thermal receipts and costs the A/P clerk 2.5 days per month-end sorting a physical shoebox. Photo capture solves the paper problem. But without site attribution at the moment of capture, the coding problem remains — the A/P clerk still has to translate "north arena" to "contract 2019-14" three weeks later, off a faded receipt, for expenses that are billable to municipal clients. A miscoding is silent: no error, just a smaller municipal invoice.

*"It solves the paper. It absolutely solves the paper, and it solves the fading, and honestly it probably solves half the 'never showed up' ones, because the moment of, I have it in my hand, is the only moment it's guaranteed to exist." — Their Controller*

*"What it doesn't solve is the coding. If I get six hundred and fifty photos a month with no job number on them, I've moved the shoebox, I haven't emptied it. It's now a digital shoebox and my clerk still has two and a half days." — Their Controller*

*"So for me the picture is table stakes and the thing that actually matters is, at the moment he takes the picture, can he tell me what site it was for. Even just the site. I'll do the rest." — Their Controller*

**Site attribution — location-aware, privacy-respecting.** The crew member knows the site name (e.g., "north arena") but not the contract number. A dropdown of the day's sites is sufficient — he is typically at 3–4 in a day. Location-awareness at capture time is preferred ("the phone knows where he is better than I do"), but consent and union-side sensitivities require it to be opt-in at the moment of capture, not ambient tracking.

*"Three or four, and honestly it should just know. He's standing at the site. Or he was twenty minutes ago. The phone knows where he is better than I do." — Their Controller*

*"I don't want to be creepy about tracking guys. I want to be really clear about that, that's a whole other conversation with our union side. But at the moment he chooses to take the picture, yeah." — Their Controller*

**Offline queuing is non-negotiable.** Some contracts are beyond cellular coverage (past the escarpment in Ontario; dead spots in BC). If the app says "no connection, try again" the user closes it and the receipt is gone. The app must queue the photo locally and display a visible count of pending uploads ("3 waiting to send"). Without this signal, users will keep the paper backup indefinitely — destroying the value of the digital capture.

*"Then it has to keep it. It cannot say 'no connection, try again.' Because he's going to close it and get in the truck and the receipt is now gone, and we're back to the shoebox but with extra steps." — Their Controller*

*"And it has to be obvious that it kept it. Like, some little thing that says 'three waiting to send.' Because otherwise he doesn't trust it and he keeps the paper too, and then what have we gained." — Their Controller*

**Context note — mileage is a different shape.** Their HR Manager noted that her expense reports are four lines, one of which is a CRA mileage claim (72¢/km for the first 5,000 km, then a lower rate). Mileage has no receipt — it is kilometres × rate. Photo capture and mileage entry are two different input shapes and must not be conflated in the flow.

**What they do today instead:** Receipts go in a glove-box envelope; the supervisor brings the envelope in at month end "or doesn't." The A/P clerk sorts the Reebok shoebox (the same physical box for four years) by yard and keys 400+ lines. Thermal paper fades on dashboards in July; $3,000–$4,000/year in unreadable or missing receipts are reimbursed anyway but cannot be billed to municipal clients.

**Signal strength — strong, direct, first-hand.** This is the first record in the corpus providing detailed field evidence for expense receipt capture from the client (Controller) side. Prior records came from the channel side (Birchbark Books, bookkeeper persona). The Controller's "table stakes" framing is deliberate: he is not asking for it as a differentiator — he considers it a baseline. The differentiator is the job/site coding at capture time.

## Draft ticket

**Objective:** Let a route supervisor or crew member capture a receipt photo on a mobile phone at the point of purchase, tag it with the job site at that moment, and have it queue locally when offline — so the A/P clerk receives a coded digital receipt rather than a physical envelope at month end.

**Acceptance criteria seed:**
- A user can photograph a receipt on a mobile phone and submit it as an expense entry without accessing a desktop.
- At capture, the user selects the job site from a short list (≤5 entries) scoped to their known sites for the period; location-awareness may pre-fill this if the user has granted consent.
- When the device has no cellular signal, the photo and site tag are stored locally and queued for upload; the app shows a count of pending uploads ("3 waiting to send") that persists until synced.
- The queued capture cannot be lost by closing the app or rebooting the device.
- Once synced, the site tag maps to the job/contract number for coding; the A/P clerk sees both the site name (what the submitter selected) and the coded job number (what the system resolved).
- Mileage claims (distance × CRA rate, no receipt) are a distinct entry type, not a photo-upload variant.
- The capture flow works for crew members who are not currently in Payworks as named users (see submitter-access record).
