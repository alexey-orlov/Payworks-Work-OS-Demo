# Transcript: Internal Product Sync — Onboarding Profile Foundation & Pilot Scope

**Date:** 2026-08-26  
**Source:** product-development/inbox/2026-08-26-internal-product-sync.txt (moved from inbox)  
**Summary:** [product/meetings/other/summaries/2026-08-26-internal-product-sync.md](../summaries/2026-08-26-internal-product-sync.md)

---

WEBVTT

NOTE Synthetic material - generated for the Payworks Work OS; not a record of a real meeting. Internal Payworks product sync; all participants are fictional.

00:00:04.000 --> 00:00:07.000
Michelle Tremblay (she/her): …can you hear me? I think my headset switched.

00:00:07.000 --> 00:00:09.000
Claire Sutton: Yeah, you're good.

00:00:09.000 --> 00:00:12.000
Michelle Tremblay (she/her): Okay. It does that when the laptop wakes up.

00:00:13.000 --> 00:00:16.000
Margaret Foster: Is Vanessa coming? I have her on the invite.

00:00:16.000 --> 00:00:22.000
Claire Sutton: She's coming, she's on the tail end of a thing with Curtis. She said start without her, she'll catch up.

00:00:22.000 --> 00:00:23.000
Margaret Foster: Okay.

00:00:24.000 --> 00:00:31.000
Michelle Tremblay (she/her): Um, so — I want to actually land two things today. I don't want to have another one of these where we talk for forty minutes and nothing's decided.

00:00:31.000 --> 00:00:33.000
Claire Sutton: [laughs] Agreed.

00:00:33.000 --> 00:00:45.000
Michelle Tremblay (she/her): The two things are: does onboarding sit on the employee profile foundation we're building in expense VP2, or does it build its own. And second, what's actually in the onboarding pilot.

00:00:45.000 --> 00:00:47.000
Claire Sutton: Yep. Those are the two.

00:00:47.000 --> 00:00:53.000
Michelle Tremblay (she/her): And I'd rather we argue properly and decide, than be polite and not.

00:00:53.000 --> 00:00:56.000
Margaret Foster: I can help with the first part of that. [laughs]

00:00:56.000 --> 00:00:58.000
Michelle Tremblay (she/her): I'm counting on it.

00:00:59.000 --> 00:01:05.000
Margaret Foster: How was Acme last week? Dean said it was good.

00:01:05.000 --> 00:01:15.000
Michelle Tremblay (she/her): It was — yeah, it was useful. Seventy-five people, one payroll admin who does everything. Completely different problem from Northwind. I'll write it up.

00:01:15.000 --> 00:01:16.000
Claire Sutton: Different how?

00:01:16.000 --> 00:01:27.000
Michelle Tremblay (she/her): Their receipts are already digital. They're PDFs in email. Nobody's photographing a piece of paper. So the whole capture story we've been building lands kind of flat with them.

00:01:27.000 --> 00:01:28.000
Claire Sutton: Huh.

00:01:28.000 --> 00:01:35.000
Michelle Tremblay (she/her): And their HR manager really did not want mobile approvals. Like, actively against. She wanted it blocked, not discouraged.

00:01:35.000 --> 00:01:37.000
Claire Sutton: Is that the first time you've heard that?

00:01:37.000 --> 00:01:41.000
Michelle Tremblay (she/her): Second, sort of. Amanda says the Northwind controller has said something in the same direction.

00:01:41.000 --> 00:01:44.000
Margaret Foster: You're talking to him tomorrow, right?

00:01:44.000 --> 00:01:48.000
Michelle Tremblay (she/her): Tomorrow morning, yeah. Thank you for that, by the way, that was a good intro.

00:01:48.000 --> 00:01:50.000
Margaret Foster: That was the HR Manager, not me. She's a gem.

00:01:51.000 --> 00:01:57.000
Michelle Tremblay (she/her): Okay, we're going to run out of time. Let me do the profile thing first because it's the one that blocks people.

00:01:58.000 --> 00:02:11.000
Michelle Tremblay (she/her): So — MJ-01 in expense VP2 is the employee profile foundation. It's drafted. It's not dev-ready, we've got a translation checkpoint on it next week. And Claire's onboarding brief needs an employee record.

00:02:11.000 --> 00:02:12.000
Claire Sutton: It does.

00:02:12.000 --> 00:02:20.000
Michelle Tremblay (she/her): And my read is she should use ours. And I think Claire is about to tell me why she shouldn't, so.

00:02:20.000 --> 00:02:22.000
Claire Sutton: [laughs] I mean, yes.

00:02:22.000 --> 00:02:23.000
Michelle Tremblay (she/her): Go ahead. Genuinely.

00:02:24.000 --> 00:02:32.000
Claire Sutton: Okay. So I want to be clear I'm not being territorial about it, I actually came into this week assuming I'd reuse it, and then I read MJ-01 properly.

00:02:32.000 --> 00:02:33.000
Michelle Tremblay (she/her): Okay.

00:02:33.000 --> 00:02:40.000
Claire Sutton: And there are three things. The first one's boring and it's schedule. The second one's the real one. The third one's about how we work.

00:02:40.000 --> 00:02:41.000
Michelle Tremblay (she/her): Do the real one second, then.

00:02:42.000 --> 00:02:53.000
Claire Sutton: Schedule first. MJ-01 isn't dev-ready. VP2 has already moved once — it moved from the June milestone to the September one. If onboarding sits on top of MJ-01, my date is your date.

00:02:53.000 --> 00:02:54.000
Michelle Tremblay (she/her): That's true.

00:02:54.000 --> 00:03:03.000
Claire Sutton: And I've got a pilot I want in the field in November, and November isn't arbitrary, I'll come back to why November when we do the second decision.

00:03:03.000 --> 00:03:04.000
Michelle Tremblay (she/her): Okay.

00:03:05.000 --> 00:03:16.000
Claire Sutton: Second thing. The real one. MJ-01's profile is modelled for a claimant. Right? Look at what's on it — cost centre, default GL, reimbursement method, approver chain, employee number.

00:03:16.000 --> 00:03:17.000
Michelle Tremblay (she/her): Yeah.

00:03:17.000 --> 00:03:26.000
Claire Sutton: Every one of those assumes the person already exists in payroll. The employee number is the spine of that record. It's the join key for everything.

00:03:26.000 --> 00:03:27.000
Michelle Tremblay (she/her): It is.

00:03:27.000 --> 00:03:38.000
Claire Sutton: My central object is a person who does not have an employee number. That's the whole job. Onboarding is the period between "we said yes to you" and "you are a row in payroll."

00:03:38.000 --> 00:03:40.000
Margaret Foster: Mm. That's a good way to put it.

00:03:40.000 --> 00:03:51.000
Claire Sutton: So I'd be extending a data model whose first assumption is precisely the thing I don't have. And in my experience that's how you get a really ugly nullable field that eight modules then have to check for.

00:03:51.000 --> 00:03:52.000
Michelle Tremblay (she/her): Right.

00:03:52.000 --> 00:04:03.000
Claire Sutton: And the third thing, which I'll say quickly because it's a bit whiny — every field I need goes through your release train. If I want to add a "background check status," I'm filing into someone else's Value Package and waiting for your milestone.

00:04:04.000 --> 00:04:05.000
Michelle Tremblay (she/her): That's not whiny, that's real.

00:04:05.000 --> 00:04:11.000
Claire Sutton: So my proposal is onboarding builds its own record in the HR module. Candidate, pre-hire, whatever we call it.

00:04:11.000 --> 00:04:16.000
Claire Sutton: And it hands off to the payroll employee record at the moment of hire. One clean handoff, one seam.

00:04:16.000 --> 00:04:18.000
Michelle Tremblay (she/her): Okay. Can I take those in reverse?

00:04:18.000 --> 00:04:19.000
Claire Sutton: Sure.

00:04:20.000 --> 00:04:31.000
Michelle Tremblay (she/her): The release train thing — I'll fix that, and I'll come back to it, because I think that's a real objection and I think it's separable from the data question. Park it.

00:04:31.000 --> 00:04:32.000
Claire Sutton: Parked.

00:04:32.000 --> 00:04:43.000
Michelle Tremblay (she/her): The second one, the real one. So — you're right about what's on the record. You're wrong that we assume the employee number exists.

00:04:43.000 --> 00:04:45.000
Claire Sutton: …Okay, say more.

00:04:45.000 --> 00:04:58.000
Michelle Tremblay (she/her): We had exactly this. VP1 shipped, and within about three weeks we had a support case: a new salaried hire flies out in week one, expenses a hotel, submits it, and there's no payroll record yet because they haven't hit their first pay run.

00:04:58.000 --> 00:05:00.000
Margaret Foster: Oh, I remember that one.

00:05:00.000 --> 00:05:08.000
Michelle Tremblay (she/her): So MJ-01 already has a state for "person exists in HR, payroll record pending." We call it unposted. It's in the draft.

00:05:08.000 --> 00:05:12.000
Claire Sutton: Hm. I read that as an error state. I genuinely read that as an error state.

00:05:12.000 --> 00:05:19.000
Michelle Tremblay (she/her): It reads like one, that's fair, it's badly named. But it's not. It's a real lifecycle state with its own rules.

00:05:19.000 --> 00:05:23.000
Claire Sutton: Okay, but unposted is still after hire. Mine is before hire.

00:05:23.000 --> 00:05:24.000
Michelle Tremblay (she/her): Yes.

00:05:24.000 --> 00:05:33.000
Claire Sutton: So it's not the same state, it's one step further back on the same line. Which — okay, I'll grant that's a smaller ask than a whole new model.

00:05:33.000 --> 00:05:41.000
Michelle Tremblay (she/her): It's the same axis. That's my whole point. You're not adding a dimension, you're adding a value to one that's already there.

00:05:41.000 --> 00:05:43.000
Claire Sutton: Mm. Alright, keep going.

00:05:43.000 --> 00:05:44.000
Michelle Tremblay (she/her): The approver chain.

00:05:45.000 --> 00:05:53.000
Michelle Tremblay (she/her): Onboarding needs to route tasks to a manager. "Sign this," "order a laptop," "confirm the start date." Yes?

00:05:53.000 --> 00:05:54.000
Claire Sutton: Yes.

00:05:54.000 --> 00:06:02.000
Michelle Tremblay (she/her): Expense needs to route claims to a manager. Same chain. Same question: who does this person report to, and who covers when they're away.

00:06:02.000 --> 00:06:03.000
Claire Sutton: Sure.

00:06:03.000 --> 00:06:12.000
Michelle Tremblay (she/her): If we build two of those, then the day somebody changes a reporting line, two systems have to learn about it. And one of them will be wrong.

00:06:12.000 --> 00:06:14.000
Claire Sutton: Not if there's a single source of the org chart.

00:06:14.000 --> 00:06:23.000
Michelle Tremblay (she/her): There isn't one, though. That's the actual state of the world. The org relationship lives on the payroll record and everything else copies it.

00:06:23.000 --> 00:06:24.000
Claire Sutton: Ugh. Right.

00:06:24.000 --> 00:06:34.000
Michelle Tremblay (she/her): And this is the thing I'd want in the record if we go your way — we sell "six integrated modules, one shared database." That's on the first slide of every deck.

00:06:34.000 --> 00:06:35.000
Claire Sutton: I know.

00:06:35.000 --> 00:06:44.000
Michelle Tremblay (she/her): If onboarding has its own person and expense has its own person, that's not one database. That's two, with a sync. And a sync is a thing that breaks at two in the morning.

00:06:44.000 --> 00:06:47.000
Margaret Foster: Can I come in on this with the research side?

00:06:47.000 --> 00:06:48.000
Michelle Tremblay (she/her): Please.

00:06:48.000 --> 00:07:00.000
Margaret Foster: Um. So, two of the partners have described this exact wall to me without either of them knowing they were describing the same thing, which is usually when I start paying attention.

00:07:00.000 --> 00:07:01.000
Claire Sutton: Which two?

00:07:01.000 --> 00:07:14.000
Margaret Foster: Maplewood and Northwind. Northwind's HR Manager has a thing where their review system won't pull an employee unless there's a company email address on the Payworks file. And half their field people don't have one.

00:07:14.000 --> 00:07:15.000
Claire Sutton: Right, I've seen that in the transcript.

00:07:15.000 --> 00:07:26.000
Margaret Foster: So what actually happens is — a manager tries to start a review, the employee doesn't come up, they phone HR, HR goes into the Payworks profile, types in an email, waits twenty-four hours, and it works.

00:07:26.000 --> 00:07:27.000
Michelle Tremblay (she/her): Which is an onboarding failure.

00:07:27.000 --> 00:07:37.000
Margaret Foster: That's what I'm saying. It shows up in performance management, it's caused at onboarding, and the reason it's possible at all is that the person became an employee in payroll before anybody finished setting them up.

00:07:37.000 --> 00:07:38.000
Claire Sutton: Mm.

00:07:38.000 --> 00:07:50.000
Margaret Foster: And Maplewood said the same thing in different words. Their payroll manager sent me a spreadsheet — an enormous one — and the line I wrote down was, the employee record isn't real until payroll says it is.

00:07:50.000 --> 00:07:52.000
Claire Sutton: That's a good quote.

00:07:52.000 --> 00:08:02.000
Margaret Foster: And I think if you build a second record, you don't fix that, you double it. Now there's a moment where they're real in onboarding and not real in payroll and a manager is standing there.

00:08:02.000 --> 00:08:07.000
Claire Sutton: Okay, but that moment exists no matter where the record lives. That's a real moment in the world.

00:08:07.000 --> 00:08:08.000
Margaret Foster: Sure.

00:08:08.000 --> 00:08:15.000
Claire Sutton: Somebody accepts an offer on Tuesday and starts on the fifteenth. There's two weeks where they exist and they aren't an employee. That's just true.

00:08:15.000 --> 00:08:19.000
Michelle Tremblay (she/her): Yes. And the question is whether that's one record in two states or two records.

00:08:19.000 --> 00:08:20.000
Claire Sutton: …Right.

00:08:22.000 --> 00:08:24.000
Vanessa Lee: Sorry! Sorry. Hi. I'm here.

00:08:24.000 --> 00:08:25.000
Michelle Tremblay (she/her): Hi.

00:08:25.000 --> 00:08:29.000
Vanessa Lee: Curtis went long. What did I miss, are we on the profile thing?

00:08:29.000 --> 00:08:36.000
Claire Sutton: We're on the profile thing. I said onboarding should build its own record, Michelle is patiently dismantling me.

00:08:36.000 --> 00:08:38.000
Michelle Tremblay (she/her): I would say vigorously.

00:08:38.000 --> 00:08:39.000
Claire Sutton: [laughs] Vigorously.

00:08:39.000 --> 00:08:41.000
Vanessa Lee: Can I say a design thing, or is it too early?

00:08:41.000 --> 00:08:42.000
Michelle Tremblay (she/her): No, go.

00:08:42.000 --> 00:08:55.000
Vanessa Lee: Um. If they're two records they're two screens. Not on purpose — nobody decides that — but they get built by different people six months apart and they drift. And I've watched that happen here before.

00:08:55.000 --> 00:08:56.000
Claire Sutton: With what?

00:08:56.000 --> 00:09:07.000
Vanessa Lee: Time and Absence. There are two places to see a person's schedule and they don't look the same and they don't have the same fields, and every time we do a usability session somebody says "wait, is this the same person?"

00:09:07.000 --> 00:09:08.000
Michelle Tremblay (she/her): That's fair.

00:09:08.000 --> 00:09:18.000
Vanessa Lee: And in onboarding the person looking at that screen is a brand new hire in their first week. That's the worst possible week to show somebody two products and tell them it's one.

00:09:18.000 --> 00:09:20.000
Claire Sutton: Yeah, that's a good point, actually.

00:09:21.000 --> 00:09:24.000
Michelle Tremblay (she/her): Can I do the cost, and then Claire you tell me if you still want to build it.

00:09:24.000 --> 00:09:25.000
Claire Sutton: Do the cost.

00:09:25.000 --> 00:09:34.000
Michelle Tremblay (she/her): MJ-01 is eleven weeks of two engineers. That's the estimate that came back from the translation session, and Sonia thinks it's honest.

00:09:34.000 --> 00:09:35.000
Claire Sutton: Twenty-two engineer-weeks.

00:09:35.000 --> 00:09:47.000
Michelle Tremblay (she/her): Twenty-two. And a second foundation isn't twenty-two, it's worse, because you'd be building it while we're actively changing the same tables. So call it eleven, twelve weeks and that's the optimistic version.

00:09:47.000 --> 00:09:48.000
Claire Sutton: Mm.

00:09:48.000 --> 00:09:56.000
Michelle Tremblay (she/her): Which is basically a quarter of your team's year, spent on a thing that already exists, to avoid a dependency.

00:09:56.000 --> 00:09:59.000
Claire Sutton: To avoid a dependency and to own my own schedule, which isn't nothing.

00:09:59.000 --> 00:10:00.000
Michelle Tremblay (she/her): No, it isn't.

00:10:00.000 --> 00:10:10.000
Michelle Tremblay (she/her): And the other cost, which nobody's mentioned — Time and Absence are next in the queue for the same foundation. That was the whole point of doing MJ-01 as a foundation and not as part of receipt capture.

00:10:10.000 --> 00:10:11.000
Claire Sutton: Right.

00:10:11.000 --> 00:10:20.000
Michelle Tremblay (she/her): So if onboarding forks it, the fork isn't the second thing, it's the thing Time then has to choose between. And they'll choose wrong, because they'll choose whichever one is finished.

00:10:20.000 --> 00:10:22.000
Margaret Foster: [laughs] That's true and it's depressing.

00:10:23.000 --> 00:10:26.000
Michelle Tremblay (she/her): So. Claire.

00:10:27.000 --> 00:10:35.000
Claire Sutton: …Okay. I think you've got me on the data question. I don't think you've got me on the schedule question, and I want to be honest that those are different.

00:10:35.000 --> 00:10:36.000
Michelle Tremblay (she/her): Agreed, they are.

00:10:36.000 --> 00:10:44.000
Claire Sutton: I'll reuse the foundation. But I want two things and I want them written down, not agreed in a meeting and forgotten.

00:10:44.000 --> 00:10:45.000
Michelle Tremblay (she/her): Name them.

00:10:45.000 --> 00:10:56.000
Claire Sutton: One. MJ-01 grows a pre-hire state before it goes dev-ready. Not after. Because if it goes dev-ready without it, it will never get added, we both know that, it'll be a VP3 item forever.

00:10:56.000 --> 00:10:59.000
Michelle Tremblay (she/her): That's, uh. Hm. That has a cost.

00:10:59.000 --> 00:11:00.000
Claire Sutton: I know it does.

00:11:00.000 --> 00:11:09.000
Michelle Tremblay (she/her): Three weeks, maybe four, and it's three weeks in front of MJ-02, so receipt capture moves right by that much. That's the actual price.

00:11:09.000 --> 00:11:11.000
Claire Sutton: And is that a price you can pay?

00:11:11.000 --> 00:11:22.000
Michelle Tremblay (she/her): …Yeah. I can pay it. I'd rather pay three weeks now than have onboarding build a parallel person. It's the cheaper of the two by a factor of three or four.

00:11:22.000 --> 00:11:23.000
Claire Sutton: Okay.

00:11:23.000 --> 00:11:33.000
Michelle Tremblay (she/her): But I want it scoped tightly. Pre-hire state, plus whatever the minimum is to hold a person before they have an employee number. Not the whole candidate world.

00:11:33.000 --> 00:11:37.000
Claire Sutton: Fine. I'm not trying to put an applicant tracking system in your Micro Job.

00:11:37.000 --> 00:11:38.000
Michelle Tremblay (she/her): [laughs] Good.

00:11:38.000 --> 00:11:39.000
Claire Sutton: Second thing.

00:11:39.000 --> 00:11:50.000
Claire Sutton: The release train problem you parked. I need a named extension point — onboarding-owned fields that live on the profile but that I can add to without shipping an expense release.

00:11:50.000 --> 00:11:51.000
Michelle Tremblay (she/her): Yes. That's reasonable.

00:11:51.000 --> 00:12:00.000
Claire Sutton: Because otherwise in four months I'm going to need a "work permit expiry" field and I'll be sat waiting for your milestone and I'll be very unpleasant about it.

00:12:00.000 --> 00:12:03.000
Michelle Tremblay (she/her): [laughs] Noted. Yes. Named seam, in the Micro Job.

00:12:03.000 --> 00:12:07.000
Vanessa Lee: Does the seam have a design implication? Like, are those fields on the same screen?

00:12:07.000 --> 00:12:08.000
Michelle Tremblay (she/her): Say more?

00:12:08.000 --> 00:12:19.000
Vanessa Lee: Just — if onboarding can add fields, then the profile screen has to have somewhere for them to go, and that's a layout question, and if we don't decide it now we'll decide it badly under pressure in MJ-02.

00:12:19.000 --> 00:12:21.000
Michelle Tremblay (she/her): That's a good catch. Can you own that?

00:12:21.000 --> 00:12:26.000
Vanessa Lee: I can take a pass at it. I'd want it settled before the MJ-02 dev-ready bundle, not during.

00:12:26.000 --> 00:12:27.000
Michelle Tremblay (she/her): Before. Agreed.

00:12:28.000 --> 00:12:34.000
Michelle Tremblay (she/her): Okay so let me say it back and somebody stop me if it's wrong.

00:12:34.000 --> 00:12:45.000
Michelle Tremblay (she/her): Employee onboarding reuses the expense VP2 employee profile foundation. It does not build its own record. In exchange, MJ-01 gains a pre-hire state before it goes dev-ready.

00:12:45.000 --> 00:12:46.000
Claire Sutton: Yes.

00:12:46.000 --> 00:12:53.000
Michelle Tremblay (she/her): That pushes MJ-02, receipt capture, right by three to four weeks, and I'm accepting that as the cost.

00:12:53.000 --> 00:12:54.000
Claire Sutton: Yes.

00:12:54.000 --> 00:13:00.000
Michelle Tremblay (she/her): And there's a named extension point so onboarding can add its own fields without an expense release.

00:13:00.000 --> 00:13:01.000
Claire Sutton: Yes. Good.

00:13:01.000 --> 00:13:07.000
Michelle Tremblay (she/her): And the rejected option was onboarding builds its own record in HR, which we costed at eleven to twelve weeks of two engineers.

00:13:07.000 --> 00:13:14.000
Claire Sutton: And rejected for — can we say the reason properly? Because I don't want the record to say "it was cheaper." That's the smallest reason.

00:13:14.000 --> 00:13:15.000
Michelle Tremblay (she/her): Say it, then.

00:13:15.000 --> 00:13:25.000
Claire Sutton: It's rejected because two records means two org charts, and the thing we sell is one database. The cost is the second reason. And Vanessa's drift point is the third.

00:13:25.000 --> 00:13:27.000
Margaret Foster: I'd put my thing in there too, if that's alright.

00:13:27.000 --> 00:13:28.000
Claire Sutton: Please.

00:13:28.000 --> 00:13:36.000
Margaret Foster: The partner evidence. Two accounts independently described the same wall, and a second record widens it rather than closing it.

00:13:36.000 --> 00:13:38.000
Michelle Tremblay (she/her): Good. That's the decision. Claire, will you write it up?

00:13:38.000 --> 00:13:44.000
Claire Sutton: I'll write it. It touches both initiatives so it needs to hang off both pages, I'll make sure it does.

00:13:44.000 --> 00:13:45.000
Michelle Tremblay (she/her): Thank you.

00:13:46.000 --> 00:13:49.000
Michelle Tremblay (she/her): Okay. Twenty minutes. Second decision. The pilot.

00:13:50.000 --> 00:13:52.000
Claire Sutton: Do you want me to frame it or do you want Margaret to?

00:13:52.000 --> 00:13:56.000
Michelle Tremblay (she/her): You frame it, and then Margaret, I know you have views, so.

00:13:56.000 --> 00:13:58.000
Margaret Foster: I have views. [laughs]

00:13:58.000 --> 00:14:11.000
Claire Sutton: So. The onboarding Product Brief as it stands covers the whole thing. Admin sets up the new hire, tasks get assigned across HR and IT and payroll, documents get collected and signed, the new hire does their self-serve stuff, and it all lands in payroll on day one.

00:14:11.000 --> 00:14:12.000
Michelle Tremblay (she/her): That's the full picture.

00:14:12.000 --> 00:14:23.000
Claire Sutton: That's the full picture and it's about two years of work. So the pilot has to be a slice. And my proposal is the slice is Employee Self Service. The new hire's own experience, and nothing else.

00:14:23.000 --> 00:14:24.000
Michelle Tremblay (she/her): Say what's in it.

00:14:24.000 --> 00:14:36.000
Claire Sutton: New hire gets a link before day one. They fill in their own personal details, their banking, their tax forms, they upload their SIN and their void cheque, they see what's happening on their first day. That's it.

00:14:36.000 --> 00:14:38.000
Claire Sutton: The admin side stays exactly as it is today.

00:14:38.000 --> 00:14:40.000
Margaret Foster: And that's my problem with it.

00:14:40.000 --> 00:14:41.000
Claire Sutton: I know it is.

00:14:41.000 --> 00:14:43.000
Michelle Tremblay (she/her): Go ahead, Margaret.

00:14:43.000 --> 00:14:55.000
Margaret Foster: Okay. So. I've done thirteen interviews this summer, and onboarding came up unprompted in — I'd have to check, but four or five of them. And I want to say something uncomfortable about it.

00:14:55.000 --> 00:14:56.000
Claire Sutton: Go on.

00:14:56.000 --> 00:15:08.000
Margaret Foster: Every single time, the pain they described was administrative. Not one person described a new hire having a bad experience. Not one. It was always the HR side drowning.

00:15:08.000 --> 00:15:09.000
Michelle Tremblay (she/her): Give me an example.

00:15:09.000 --> 00:15:21.000
Margaret Foster: Maplewood. Their payroll manager, at the very end of the call, out of nowhere — they'd just done three hundred plus seasonal terminations, ROEs for all of them, and she said she'd send me her onboarding spreadsheet.

00:15:21.000 --> 00:15:22.000
Claire Sutton: And she did.

00:15:22.000 --> 00:15:32.000
Margaret Foster: She did. It's enormous. It's got a tab per department. And she offered to build me the offboarding one as well, which tells you how much of her life is in that file.

00:15:32.000 --> 00:15:33.000
Michelle Tremblay (she/her): Mm.

00:15:33.000 --> 00:15:44.000
Margaret Foster: Cascadia's the same shape — they've got credential tracking for their installers, tickets and certifications, expiry dates, and it's all in someone's head and a calendar reminder.

00:15:44.000 --> 00:15:45.000
Claire Sutton: Yeah.

00:15:45.000 --> 00:15:56.000
Margaret Foster: And Northwind's email thing, which we just talked about, that's an admin setup step that gets missed. All three of those are on the admin side. So an ESS-only pilot tests the half nobody complained about.

00:15:56.000 --> 00:15:57.000
Michelle Tremblay (she/her): That's a strong argument.

00:15:57.000 --> 00:16:07.000
Margaret Foster: And I'll be blunt about the second half of it, which is that I'm the one who has to go back to Maplewood. She sent me a spreadsheet. She built me a thing. And if the first thing we ship doesn't touch it—

00:16:07.000 --> 00:16:08.000
Claire Sutton: That's fair.

00:16:08.000 --> 00:16:15.000
Margaret Foster: —then I look like I asked for her homework and filed it. And that's a real cost with a design partner, it's not a soft cost.

00:16:15.000 --> 00:16:17.000
Michelle Tremblay (she/her): No, it isn't. Okay. Claire.

00:16:18.000 --> 00:16:20.000
Claire Sutton: Can I ask you one thing before I answer?

00:16:20.000 --> 00:16:21.000
Margaret Foster: Yeah.

00:16:21.000 --> 00:16:26.000
Claire Sutton: In those thirteen interviews, how many of the people in the room were new hires?

00:16:27.000 --> 00:16:28.000
Margaret Foster: …None.

00:16:28.000 --> 00:16:29.000
Claire Sutton: Right.

00:16:29.000 --> 00:16:34.000
Margaret Foster: That's a cheap shot but it's a fair one. [laughs]

00:16:34.000 --> 00:16:44.000
Claire Sutton: It's a bit cheap. But it's the thing I keep coming back to. Every design partner we have is an HR manager or a payroll manager. Of course the pain they report is theirs. Nobody's interviewing the person on day one.

00:16:44.000 --> 00:16:45.000
Margaret Foster: Sure.

00:16:45.000 --> 00:16:53.000
Claire Sutton: But that's not actually my main reason, so let me do the main reason, because otherwise this sounds like I'm just being clever.

00:16:53.000 --> 00:16:54.000
Michelle Tremblay (she/her): Please.

00:16:54.000 --> 00:17:03.000
Claire Sutton: The admin side needs two things that do not exist. A document store, and a task orchestration engine. Neither of those is scheduled. Michelle, correct me.

00:17:03.000 --> 00:17:14.000
Michelle Tremblay (she/her): Correct. Document management is a Value Package that isn't in the plan, it's been "next year" for two years. And there's no task engine anywhere in the product. Absence has a hand-rolled workflow and that's it.

00:17:14.000 --> 00:17:15.000
Margaret Foster: So build them.

00:17:15.000 --> 00:17:25.000
Michelle Tremblay (she/her): That's two quarters, and the capacity for the first of them went to Time. Which was a retention-floor call, we made it in June, and I don't want to reopen it in a Wednesday sync.

00:17:25.000 --> 00:17:26.000
Margaret Foster: Mm.

00:17:26.000 --> 00:17:38.000
Claire Sutton: And here's the bit that actually decides it for me. If we pilot the admin side without those two things, we're not piloting anything. We're showing them a prototype and asking do you like it.

00:17:38.000 --> 00:17:39.000
Vanessa Lee: Which we've already done.

00:17:39.000 --> 00:17:40.000
Claire Sutton: Which we've already done, four times.

00:17:40.000 --> 00:17:50.000
Claire Sutton: And you cannot learn adoption from a mock. You can learn "is this the right shape." You cannot learn "did anyone use it in week three." And the pilot's whole job is the second question.

00:17:50.000 --> 00:17:53.000
Margaret Foster: …Okay, that one lands. I don't like it, but it lands.

00:17:53.000 --> 00:18:04.000
Claire Sutton: And the ESS slice is the only part that can actually run for real against MJ-01. It needs a person, a form, and a place to put a document, and two of those three exist today.

00:18:04.000 --> 00:18:05.000
Michelle Tremblay (she/her): Which one doesn't?

00:18:05.000 --> 00:18:14.000
Claire Sutton: The document. But for the ESS slice it's a SIN and a void cheque, that's it, and Employee Self Service already stores those today for existing employees.

00:18:14.000 --> 00:18:15.000
Michelle Tremblay (she/her): Right, it does.

00:18:15.000 --> 00:18:20.000
Claire Sutton: So it's not a document store. It's two documents we already know how to hold.

00:18:21.000 --> 00:18:22.000
Vanessa Lee: Can I add the design one?

00:18:22.000 --> 00:18:23.000
Michelle Tremblay (she/her): Yeah.

00:18:23.000 --> 00:18:35.000
Vanessa Lee: We have never once tested a flow where the new hire is the user. Every prototype we've made this year has an HR person driving it. Every single one. Even the ones about the employee.

00:18:35.000 --> 00:18:36.000
Margaret Foster: That's true.

00:18:36.000 --> 00:18:47.000
Vanessa Lee: And that's a real gap, because the assumptions are completely different. That person has no training, no context, they've never seen Payworks, they might be doing it on a phone in a parking lot before their first shift.

00:18:47.000 --> 00:18:48.000
Claire Sutton: That's exactly the case.

00:18:48.000 --> 00:18:58.000
Vanessa Lee: And, um — sorry, one more — the adoption argument. Margaret, you said this to Northwind's HR Manager and I wrote it down because I liked it so much.

00:18:58.000 --> 00:18:59.000
Margaret Foster: What did I say?

00:18:59.000 --> 00:19:07.000
Vanessa Lee: "They're at the beginning of this process, and if they don't adopt it, then nothing is flowing." You were talking about managers, but it's the same for a new hire.

00:19:07.000 --> 00:19:11.000
Margaret Foster: [laughs] Being quoted back at yourself is a very specific feeling.

00:19:11.000 --> 00:19:12.000
Michelle Tremblay (she/her): It really is.

00:19:13.000 --> 00:19:17.000
Michelle Tremblay (she/her): Margaret, what's the cost of the thing you're proposing? Just so it's on the record properly.

00:19:17.000 --> 00:19:19.000
Margaret Foster: The full HR-module pilot?

00:19:19.000 --> 00:19:20.000
Michelle Tremblay (she/her): Yeah.

00:19:20.000 --> 00:19:30.000
Margaret Foster: …Two quarters before we could start, if Michelle's right about the document store and the task engine. Which means the pilot is in January or February instead of November.

00:19:30.000 --> 00:19:32.000
Claire Sutton: And that's the November thing I flagged earlier.

00:19:32.000 --> 00:19:33.000
Michelle Tremblay (she/her): Go on.

00:19:33.000 --> 00:19:44.000
Claire Sutton: Northwind and Maplewood both hire seasonally. Their intake is spring. If we're in the field in November we get their winter admin hiring, which is small, but we're set up and instrumented for the spring wave.

00:19:44.000 --> 00:19:45.000
Michelle Tremblay (she/her): And if we're in January?

00:19:45.000 --> 00:19:56.000
Claire Sutton: If we're in January we're still shaking out bugs when the spring wave hits and we'll be told to get out of the way. And then the next real observation window is a year later.

00:19:56.000 --> 00:19:58.000
Margaret Foster: Hm. That I did not have.

00:19:58.000 --> 00:20:04.000
Claire Sutton: That's the thing I'd genuinely put at the top. It's not two quarters of delay, it's a year of learning.

00:20:04.000 --> 00:20:08.000
Margaret Foster: And there's a partner recruiting cost too, if we go full HR.

00:20:08.000 --> 00:20:09.000
Michelle Tremblay (she/her): Why?

00:20:09.000 --> 00:20:19.000
Margaret Foster: Because our current partners were recruited for performance management. For an admin onboarding pilot I'd want at least two with high-volume hiring, and that took six weeks last time. Realistically eight.

00:20:19.000 --> 00:20:22.000
Michelle Tremblay (she/her): Okay. So where are you?

00:20:23.000 --> 00:20:29.000
Margaret Foster: …I'll go along with it. But I want three things and I want them to be real, not politeness.

00:20:29.000 --> 00:20:30.000
Claire Sutton: Name them.

00:20:30.000 --> 00:20:42.000
Margaret Foster: One. The pilot instruments the admin handoffs even though they're manual. I want to know how many times someone had to do something by hand for each new hire in that pilot. Count it. Even if a human is counting it on paper.

00:20:42.000 --> 00:20:43.000
Claire Sutton: Yes. That's a good ask.

00:20:43.000 --> 00:20:52.000
Margaret Foster: Because otherwise in March somebody says "the onboarding pilot went great" and we've measured only the half we built, and that number goes in a deck.

00:20:52.000 --> 00:20:53.000
Michelle Tremblay (she/her): That's very fair.

00:20:53.000 --> 00:21:03.000
Margaret Foster: Two. The decision record has to say this is a sequencing call, not a judgment that the admin problem is smaller. In those words. Because I'm going to send it to Maplewood.

00:21:03.000 --> 00:21:05.000
Claire Sutton: You want to send the decision record to a customer?

00:21:05.000 --> 00:21:14.000
Margaret Foster: A version of it, yes. I want to be able to say, here's what we decided and here's exactly why, and your spreadsheet is not in a drawer.

00:21:14.000 --> 00:21:15.000
Michelle Tremblay (she/her): I like that a lot, actually.

00:21:15.000 --> 00:21:23.000
Margaret Foster: And three — somebody reads that spreadsheet properly and answers her. Not as pilot scope. As a human being who was sent a thing.

00:21:23.000 --> 00:21:26.000
Claire Sutton: I'll do that this week. That's overdue and that's on me.

00:21:26.000 --> 00:21:27.000
Margaret Foster: Thank you.

00:21:27.000 --> 00:21:32.000
Margaret Foster: And for the record I still think the admin side is the bigger problem. I'm not conceding that bit.

00:21:32.000 --> 00:21:35.000
Claire Sutton: You might be right. I'm not sure you're wrong.

00:21:35.000 --> 00:21:41.000
Michelle Tremblay (she/her): Then let's put that in the record as well. "Reviewers disagreed on whether the admin burden is the larger problem" or whatever the phrasing is.

00:21:41.000 --> 00:21:42.000
Margaret Foster: Yeah. Good.

00:21:43.000 --> 00:21:45.000
Michelle Tremblay (she/her): Okay, say-back. Second one.

00:21:45.000 --> 00:21:55.000
Michelle Tremblay (she/her): The onboarding pilot is scoped to Employee Self Service only. New hire self-serve: personal details, banking, tax forms, SIN and void cheque, first-day view. Admin side unchanged.

00:21:55.000 --> 00:21:56.000
Claire Sutton: Correct.

00:21:56.000 --> 00:22:07.000
Michelle Tremblay (she/her): Rejected alternative: pilot the full HR-module onboarding flow with admin task orchestration and document management. Rejected because it needs a document store and a task engine that aren't built or scheduled—

00:22:07.000 --> 00:22:08.000
Claire Sutton: Two quarters.

00:22:08.000 --> 00:22:19.000
Michelle Tremblay (she/her): Two quarters, which pushes the pilot past the seasonal hiring window and costs us a year of observation, plus six to eight weeks of new partner recruiting. And because a pilot without those pieces is a mock, and you can't learn adoption from a mock.

00:22:19.000 --> 00:22:20.000
Margaret Foster: And the counter-argument is on the record.

00:22:20.000 --> 00:22:29.000
Michelle Tremblay (she/her): Counter-argument on the record: the researched pain is administrative, four or five partners raised it unprompted, and it's a sequencing call rather than a ranking of the problems.

00:22:29.000 --> 00:22:30.000
Margaret Foster: Yes. Thank you.

00:22:30.000 --> 00:22:34.000
Michelle Tremblay (she/her): Plus the three conditions. Claire, same thing, you'll write it?

00:22:34.000 --> 00:22:38.000
Claire Sutton: I'll write both. And they both need to show up on the onboarding page.

00:22:38.000 --> 00:22:43.000
Michelle Tremblay (she/her): And the first one on the expense VP2 page as well, because it changes MJ-01 and MJ-02.

00:22:43.000 --> 00:22:44.000
Claire Sutton: Yep.

00:22:45.000 --> 00:22:48.000
Michelle Tremblay (she/her): Um. Four minutes. Anything else that can't wait?

00:22:48.000 --> 00:22:52.000
Vanessa Lee: Just — do I have a date for the profile layout thing? Or is it "before MJ-02"?

00:22:52.000 --> 00:22:56.000
Michelle Tremblay (she/her): Before MJ-02, and MJ-02 now starts three weeks later, so… mid-September?

00:22:56.000 --> 00:22:58.000
Vanessa Lee: Mid-September works. I'll book time with Curtis.

00:22:58.000 --> 00:23:04.000
Michelle Tremblay (she/her): Great. And I'll take the pre-hire state back into MJ-01 and re-run the translation checkpoint with the team.

00:23:04.000 --> 00:23:06.000
Claire Sutton: Do you want me in that?

00:23:06.000 --> 00:23:12.000
Michelle Tremblay (she/her): Yes, actually, because you'll spot the thing I don't. Sonia will send an invite.

00:23:12.000 --> 00:23:14.000
Claire Sutton: Okay.

00:23:14.000 --> 00:23:20.000
Margaret Foster: One open thing from me and then I'll drop it — we still don't know who owns the org chart.

00:23:20.000 --> 00:23:21.000
Michelle Tremblay (she/her): No, we don't.

00:23:21.000 --> 00:23:29.000
Margaret Foster: And both of these decisions kind of assume it's payroll, and payroll didn't say that, we said that. So somebody should actually ask.

00:23:29.000 --> 00:23:32.000
Michelle Tremblay (she/her): That's a fair flag. Can that be an open question on the brief rather than something we solve now?

00:23:32.000 --> 00:23:35.000
Margaret Foster: Open question is fine. I just don't want it to quietly become true.

00:23:35.000 --> 00:23:37.000
Claire Sutton: I'll put it in Open Questions and Risks on the brief.

00:23:37.000 --> 00:23:39.000
Michelle Tremblay (she/her): Good. Okay, I have to jump.

00:23:39.000 --> 00:23:42.000
Michelle Tremblay (she/her): Northwind controller tomorrow at nine, if anyone wants to lurk.

00:23:42.000 --> 00:23:44.000
Margaret Foster: I'd love to but I've got Birchbark follow-up.

00:23:44.000 --> 00:23:46.000
Vanessa Lee: I'm on it, I'm in the invite.

00:23:46.000 --> 00:23:48.000
Michelle Tremblay (she/her): Great. Thanks everyone. Good meeting, actually.

00:23:48.000 --> 00:23:50.000
Claire Sutton: It was. Thanks for the fight.

00:23:50.000 --> 00:23:52.000
Michelle Tremblay (she/her): [laughs] Any time. Bye.

00:23:52.000 --> 00:23:53.000
Margaret Foster: Bye.
