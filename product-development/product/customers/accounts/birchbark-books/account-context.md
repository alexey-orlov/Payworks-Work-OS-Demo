---
updated: 2026-08-31
areas: [payroll, employee-self-service]
features: [payroll-hub]
initiatives: []
---

# Birchbark Books & Accounting (birchbark-books) — Account Context

> **Synthetic account, now with one real record.** Birchbark is a composite bookkeeping
> practice, created so the **Accountant** and **Bookkeeper** personas — half the FY27
> strategy, and the channel that "brings a book of clients" — have a customer voice in
> this repo instead of appearing only in strategy documents. **The firmographics below
> are still illustrative** — treat them as the shape of the practice, not as findings.
> The 2026-08-18 channel research call in History IS a filed research record, and
> anything sourced to it is evidence like any other.

## Who they are

- A **bookkeeping and small-practice accounting firm** carrying roughly **40 SMB payroll clients**, most of them under 20 employees. The firm itself runs about 14 staff — a practice owner, a small team of bookkeepers, and administrative support.
- **Two hats at once, which is the whole point of this account:** Birchbark is a Payworks *customer* (it runs its own payroll and self-service on the platform) and a Payworks *channel* (it chooses, recommends and administers payroll for the clients it serves). Persona 6, "The Accountant", is the practice owner; Persona 7, "The Bookkeeper", is the hands-on processor doing the runs.
- The practice sits in the segment the FY27 strategy is aiming at: 2,983 active accounts carry the Accountant channel tag today, concentrated in BC and Ontario, with Québec at 86 against a 3% provincial-share target.

## Current truth

- **Modules in use for its own staff:** Payroll and Employee Self Service. Its client-facing work runs through **Payroll Hub** — one dashboard across every client's upcoming payroll obligations, which is what a practice with 40 client databases actually needs to stay ahead of deadlines. **Firm Management** (firm admin portal, team access across client accounts) is `planned` in the catalog and is the obvious next conversation with this kind of account.
- **What this account is for, in this repo:** the channel personas' pains are documented in `business-info.md` — audit-trail gaps that make change tracing hard, sharing that requires CSV export then manual formatting, no native scheduled report delivery, GL export formats that do not match every client chart of accounts. Those are stated needs from Payworks' own JTBD material, not findings from this firm. When channel-side work needs a customer to point at, point here; when it needs evidence, it still needs a filed research record.
- **ARR convention matters here.** The figure in [portfolio.yaml](../portfolio.yaml) is the **firm's own subscription only**. The ~40 client accounts it administers are separate `CustID`s with their own billing and are not rolled into this row — counting them here would double-count the base and inflate any channel ARR view. See the conventions block at the top of that file.

## History

- 2026-08-18 — Channel research call with the Firm Principal and Senior Bookkeeper — framed explicitly as research, not sales. Cross-client expense visibility, firm templates, receipt retention and advance change notice → [summary](calls/summaries/2026-08-18.md) · [transcript](../../../user-insights/transcripts/2026-08-18-birchbark-books-call.md)
