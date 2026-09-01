---
account: birchbark-books
requested: 2026-08-18
area: expense-management
type: feature
priority_signal: must-have
tracker_ref: "-"
source: ../../customers/accounts/birchbark-books/calls/summaries/2026-08-18.md
features: []
initiatives: [expense-management-vp2]
updated: 2026-08-31
---

# [Expense Management] Receipt capture the firm can audit — visible guesses, source image, seven-year retention

**Who asked:** Their Senior Bookkeeper at Birchbark Books & Accounting, the processor for ~40 client books (Persona 7, "The Bookkeeper").

**The underlying need — remove the 80% that is obvious so the firm's time goes to the 20% that is judgment.** Expense coding costs the firm roughly three hours per client per month averaged — about 120 hours a month across the book, which she called "most of a person." The spread is extreme: the best client's technicians photograph everything and it arrives coded (about an hour a month), the worst hands over a freezer bag of a year's receipts and costs two days every February. Capture at the moment of purchase is wanted, but only if what arrives is something the firm can interrogate — because the firm, not the client and not the software, is the one who explains the entry to CRA seven years later.

*"It helps enormously, with a condition." — Their Senior Bookkeeper*

*"It has to reach me in a form I can question. So if the app reads the receipt and guesses the category, fine, great, but I need to see that it guessed and I need to be able to see the picture." — Their Senior Bookkeeper*

*"at year end I'm the one explaining it. And if the answer is 'the software decided,' that's not an answer I can give anyone. I need the receipt attached to the entry forever, not for ninety days." — Their Senior Bookkeeper*

*"Seven years. CRA. And I would want to be able to get all seven years out if a client leaves us, which — clients do leave." — Their Senior Bookkeeper*

*"I want the eighty percent that's obviously business to arrive without me touching it, so I've got time for the twenty percent that's a judgment call. That's the whole ask." — Their Senior Bookkeeper*

**What they do today instead:** receipts arrive in whatever form each of forty clients produces them — coded photographs from one client, a physical bag of paper from another — and the firm keys them manually. She notes she cannot hire for this work: two job postings open since March, and *"Nobody wants to key receipts, and the ones who do want it want sixty-five thousand and they leave in a year."*

**A boundary the customer drew for us, unprompted.** The hardest part of small-business expense in her account is card commingling — at an eleven-person client the owner has one Visa that buys truck parts and groceries — so the real question is ownership, not capture. She named it as the hardest problem and then explicitly took it off our plate: *"that's a judgment call and it's mine and it always will be. I'm not asking you to solve it." — Their Senior Bookkeeper*. Do not scope automated business-vs-personal classification off this record.

**Signal strength — strong, prompted, and conditional.** The question was ours ("does it help you or does it just move your work?"); the answer was immediate and emphatic, and the two conditions were volunteered without being asked for. This is the **first record in the corpus that states receipt capture as a customer requirement.** The [expense-management-vp2](../../initiatives/expense-management-vp2.md) page has held receipt capture as an unbacked hypothesis on the grounds that "no design-partner record states them" — this record states it, from the channel side. It is not the client-side A/P view; that gap remains open.

## Draft ticket

**Objective:** Let a client's staff capture a receipt at the point of purchase on a phone and have it arrive coded, while the administering firm retains the ability to see how it was coded, inspect the source image, and rely on the receipt as evidence for the full statutory retention period.

**Acceptance criteria seed:**
- A receipt captured by photo attaches to its expense entry and the source image is viewable from the entry at any time.
- Where a category, vendor or amount was derived automatically, the entry shows that it was derived — a reviewer can tell a machine value from a human-entered one at a glance.
- A derived value can be overridden by the firm, and the override is distinguishable from both the original derivation and an untouched value.
- Receipt images and their entries are retained for at least seven years, not a rolling window.
- A firm can export a client's full receipt history — images plus entries — for the whole retention period, including when the client leaves the firm.
- No automatic business-versus-personal determination is made on the firm's behalf; ambiguous items surface for human judgment rather than being silently classified.
