---
date: 2026-08-27
type: call
customers: [northwind-landscaping]
areas: [expense-management, payroll, employee-self-service]
features: []
initiatives: [expense-management-vp2]
themes: [receipt-capture, approval-chain, payroll-integration, mobile, offline, job-coding, status-visibility, seasonal-workforce]
---

# Transcript — Northwind Landscaping Expense Call 2026-08-27

**Summary:** [../../../customers/accounts/northwind-landscaping/calls/summaries/2026-08-27.md](../../../customers/accounts/northwind-landscaping/calls/summaries/2026-08-27.md)

> Raw transcript — immutable from filing. Corrections belong in the summary.
> Customer-side speakers appear as role titles only (controller, hr.manager).
> Payworks team: Michelle Tremblay, Dean Murphy, Vanessa Lee.

---

WEBVTT

NOTE Synthetic material - generated for the Payworks Work OS; not a record of a real meeting. Customer-side speakers are role titles only; Payworks staff are fictional.

1
00:00:00.000 --> 00:00:06.320
Dean Murphy: …should be, yeah. Let me just check she's got the right link, because I sent two.

2
00:00:06.900 --> 00:00:11.240
Michelle Tremblay (she/her): There's someone in the waiting room. Is that… that's the Controller?

3
00:00:11.240 --> 00:00:13.010
Dean Murphy: That'll be him, yeah, let him in.

4
00:00:16.480 --> 00:00:17.660
Michelle Tremblay (she/her): Good morning.

5
00:00:19.220 --> 00:00:21.559
controller: Morning. Can you hear me okay?

6
00:00:21.560 --> 00:00:23.120
Michelle Tremblay (she/her): Loud and clear, yeah.

7
00:00:23.120 --> 00:00:32.870
controller: Good, good. Sorry, I'm in the truck— no, I'm not in the truck, I'm at the Ontario office, but I'm in a meeting room that has a terrible microphone, so.

8
00:00:33.100 --> 00:00:34.940
Michelle Tremblay (she/her): You sound great, honestly.

9
00:00:35.410 --> 00:00:39.980
controller: Okay. The HR Manager said she was going to join too, is she… okay, there she is.

10
00:00:41.220 --> 00:00:42.610
hr.manager: Hi! Sorry, sorry.

11
00:00:42.610 --> 00:00:43.760
Michelle Tremblay (she/her): No, you're right on time.

12
00:00:43.760 --> 00:00:53.550
hr.manager: I was on the analytics 2.0 training, and it ran over, so… I'm going to have to hop off at ten to, but I wanted to at least be here for the start so I could introduce everybody.

13
00:00:53.550 --> 00:00:54.320
Michelle Tremblay (she/her): Perfect.

14
00:00:54.680 --> 00:01:07.150
hr.manager: So, um, the Controller — this is Michelle, she's the product manager who does the expense side. Margaret is the one I've been meeting with all summer about performance management, and she said, you know what, you should really talk to the Controller.

15
00:01:07.480 --> 00:01:08.640
controller: Right, yeah.

16
00:01:08.640 --> 00:01:20.440
hr.manager: Because I told her, I put my expense report in, it goes to the Head of HR, she approves it, and then it disappears into accounts payable and I get my money. That's the whole of what I know about it.

17
00:01:20.900 --> 00:01:22.679
controller: That's the whole of what you need to know about it.

18
00:01:22.680 --> 00:01:24.400
hr.manager: [laughs] Exactly.

19
00:01:24.400 --> 00:01:31.760
Michelle Tremblay (she/her): Well, that's actually a useful data point on its own, that it's invisible if it's working. Um…

20
00:01:31.760 --> 00:01:44.120
Michelle Tremblay (she/her): So, quick intros — I'm Michelle, I'm the product lead on the payroll and expense side. Dean you know. And Vanessa is on our product design team, she's going to mostly listen today and maybe show you something at the end if we have time.

21
00:01:44.680 --> 00:01:45.900
Vanessa Lee: Hi, nice to meet you.

22
00:01:46.240 --> 00:01:47.560
controller: Hi, Vanessa.

23
00:01:48.020 --> 00:02:00.699
Michelle Tremblay (she/her): Um, before we get going — do you mind if I record? It just means I'm not typing the whole time. It stays internal to our product team, we don't share it out.

24
00:02:01.220 --> 00:02:02.400
controller: No, that's fine with me.

25
00:02:02.400 --> 00:02:03.240
hr.manager: Fine with me.

26
00:02:03.240 --> 00:02:04.320
Michelle Tremblay (she/her): Thank you.

27
00:02:05.100 --> 00:02:17.320
Michelle Tremblay (she/her): So the way I'd like to do this — there's no demo, there's no, like, here's what we built. We're at the stage where I mostly want to understand what actually happens today. And there's three things I'm curious about.

28
00:02:17.320 --> 00:02:29.879
Michelle Tremblay (she/her): One is how a receipt gets from wherever it's created back to you. Two is who says yes to it. And three is how the money actually reaches the person. And then if there's time, the mobile piece, because the HR Manager has mentioned that to Margaret about four times.

29
00:02:29.880 --> 00:02:31.980
hr.manager: I have. I will again.

30
00:02:32.400 --> 00:02:34.100
controller: [laughs] She's not wrong, though.

31
00:02:34.720 --> 00:02:37.019
Michelle Tremblay (she/her): Good. So — receipts. Walk me through it.

32
00:02:38.400 --> 00:02:47.559
controller: Okay. So. It's… I want to be careful not to make it sound worse than it is, because it works, it's just, it's not good, if that makes sense.

33
00:02:47.560 --> 00:02:48.560
Michelle Tremblay (she/her): It does, yeah.

34
00:02:48.940 --> 00:03:04.120
controller: So we've got, call it sixty-some trucks between Ontario and BC. Every truck has a fuel card, so fuel is not really the problem, fuel goes on the card, the card statement comes to me, that's, what, twenty-eight grand a month, but it's clean, it's one file.

35
00:03:04.480 --> 00:03:05.300
Michelle Tremblay (she/her): Mm-hmm.

36
00:03:05.400 --> 00:03:19.879
controller: The problem is everything that isn't fuel. So a crew's out at a site, they run out of, you know, mulch, or a fitting for the irrigation, or the mower throws a belt. They're not driving back to the yard. They go to the supply place down the road and they buy it.

37
00:03:20.120 --> 00:03:21.000
Michelle Tremblay (she/her): On what?

38
00:03:21.400 --> 00:03:33.180
controller: Depends who. Some of the route supervisors have a company card. A lot of them don't, so it's their own Visa, or there's a petty cash float at each yard, two hundred bucks, which is gone by the tenth of the month, always.

39
00:03:33.560 --> 00:03:34.800
Michelle Tremblay (she/her): [laughs] Always.

40
00:03:34.800 --> 00:03:42.099
controller: Always. Every single yard, every single month. It's like a law of physics. Six yards, six floats, all empty by the tenth.

41
00:03:42.440 --> 00:03:43.640
Michelle Tremblay (she/her): And then the receipt?

42
00:03:44.100 --> 00:03:56.680
controller: The receipt goes in the truck. Genuinely. There's an envelope in the glove box, it's supposed to go in the envelope, and at the end of the month the supervisor brings the envelope in, or doesn't, and…

43
00:03:57.100 --> 00:03:57.900
Michelle Tremblay (she/her): Or doesn't.

44
00:03:57.900 --> 00:04:11.640
controller: Or doesn't, yeah. And then it's my A/P clerk sitting there with an actual shoebox — I'm not being cute, it is a Reebok box, it's been the same box for four years — sorting receipts by yard and keying them in.

45
00:04:12.180 --> 00:04:13.760
hr.manager: I've seen the box. It's real.

46
00:04:14.240 --> 00:04:15.560
Michelle Tremblay (she/her): How many, roughly?

47
00:04:16.100 --> 00:04:29.320
controller: In season? Six hundred, six-fifty a month. That's May through October. February it's maybe two-fifty, because it's just snow removal and the yards. And most of them are small, like, sixty bucks is your median receipt.

48
00:04:29.680 --> 00:04:31.400
Michelle Tremblay (she/her): And in dollars, total?

49
00:04:31.900 --> 00:04:41.720
controller: About forty thousand a month in season. February, fifteen. So call it three-fifty a year in reimbursements and small purchases, not counting the fuel cards.

50
00:04:42.240 --> 00:04:47.339
Michelle Tremblay (she/her): Okay. And the keying — how long does that take her? Is that a day, is that…

51
00:04:47.340 --> 00:04:59.560
controller: Two and a half days at month end. Every month. It's about four hundred lines by the time she's split out the taxes and coded them. And that's two and a half days she is not doing anything else, which at month end is…

52
00:04:59.560 --> 00:05:00.900
Michelle Tremblay (she/her): Is the worst two and a half days.

53
00:05:00.900 --> 00:05:07.560
controller: It's the worst two and a half days to lose, yeah. She's supposed to be closing the month, and she's sorting a shoebox.

54
00:05:08.240 --> 00:05:14.679
Michelle Tremblay (she/her): Can I ask — when you say coded, what is she actually deciding? Like what does she have to know to code it?

55
00:05:15.100 --> 00:05:16.100
controller: Two things.

56
00:05:16.560 --> 00:05:31.320
controller: GL account, which is usually obvious, mulch is materials, a belt is repairs and maintenance. And the job. That one's the important one. Because we've got eleven municipal contracts, and on most of those, materials are billable back to the municipality.

57
00:05:31.680 --> 00:05:32.900
Michelle Tremblay (she/her): Oh, interesting.

58
00:05:32.900 --> 00:05:47.400
controller: Yeah, so it's not a cost thing, it's a revenue thing. If that bag of grass seed doesn't get coded to the right job number, we don't bill for it. And nobody's going to catch that. There's no report that says "here's the seed you forgot to bill."

59
00:05:47.900 --> 00:05:52.220
Michelle Tremblay (she/her): And the guy at the counter buying the seed, does he know the job number?

60
00:05:52.680 --> 00:06:04.240
controller: He knows the site. He'd say, that's the north arena. He doesn't know it's contract 2019-14. My clerk knows that. Or she has a sheet. So she's doing the translation, three weeks after the fact, off a faded receipt.

61
00:06:04.680 --> 00:06:06.600
Michelle Tremblay (she/her): Right, and if she gets it wrong—

62
00:06:06.600 --> 00:06:15.180
controller: If she gets it wrong nobody knows. That's the thing. There's no error, there's just a slightly smaller invoice to the municipality and everyone goes home happy.

63
00:06:15.680 --> 00:06:16.900
Michelle Tremblay (she/her): Hm. Okay.

64
00:06:17.400 --> 00:06:18.900
Michelle Tremblay (she/her): Um, you said faded.

65
00:06:19.400 --> 00:06:32.680
controller: Oh, that's — yeah. Thermal paper. Sits on a dashboard in July. By the time it gets to us it's a blank piece of paper. We probably eat three, four thousand a year in receipts that we cannot read or that just never show up.

66
00:06:33.100 --> 00:06:34.400
Michelle Tremblay (she/her): And what happens to those?

67
00:06:34.400 --> 00:06:44.339
controller: I reimburse the guy anyway. Because he did buy it, and I'm not going to have a fight about forty dollars of irrigation fittings with a supervisor who's been out since five in the morning.

68
00:06:44.340 --> 00:06:45.320
Michelle Tremblay (she/her): Sure.

69
00:06:45.320 --> 00:06:52.760
controller: But I can't bill it out, and I can't defend it if we get looked at. So it just goes to a miscellaneous bucket and I feel bad about it.

70
00:06:53.320 --> 00:07:04.160
Michelle Tremblay (she/her): Okay. So if I said to you, the crew takes a picture of the receipt at the counter, on their phone, before they get back in the truck — does that solve it, or does that create a new problem?

71
00:07:05.100 --> 00:07:06.400
controller: Both, probably.

72
00:07:06.900 --> 00:07:07.680
Michelle Tremblay (she/her): Go on.

73
00:07:07.680 --> 00:07:22.120
controller: It solves the paper. It absolutely solves the paper, and it solves the fading, and honestly it probably solves half the "never showed up" ones, because the moment of, I have it in my hand, is the only moment it's guaranteed to exist.

74
00:07:22.560 --> 00:07:23.320
Michelle Tremblay (she/her): Right.

75
00:07:23.320 --> 00:07:35.780
controller: What it doesn't solve is the coding. If I get six hundred and fifty photos a month with no job number on them, I've moved the shoebox, I haven't emptied it. It's now a digital shoebox and my clerk still has two and a half days.

76
00:07:36.240 --> 00:07:37.400
Michelle Tremblay (she/her): That's fair.

77
00:07:37.400 --> 00:07:49.640
controller: So for me the picture is table stakes and the thing that actually matters is, at the moment he takes the picture, can he tell me what site it was for. Even just the site. I'll do the rest.

78
00:07:50.100 --> 00:07:56.799
Michelle Tremblay (she/her): So a dropdown that says which site, and it's short, because he's only ever at, what, three or four sites in a day?

79
00:07:56.800 --> 00:08:07.360
controller: Three or four, and honestly it should just know. He's standing at the site. Or he was twenty minutes ago. The phone knows where he is better than I do.

80
00:08:07.900 --> 00:08:09.240
Michelle Tremblay (she/her): Mm. Yeah.

81
00:08:09.240 --> 00:08:19.780
controller: I don't want to be creepy about tracking guys. I want to be really clear about that, that's a whole other conversation with our union side. But at the moment he chooses to take the picture, yeah.

82
00:08:20.240 --> 00:08:21.560
Michelle Tremblay (she/her): Understood. That's helpful.

83
00:08:22.100 --> 00:08:23.100
hr.manager: Can I add one thing?

84
00:08:23.100 --> 00:08:23.900
Michelle Tremblay (she/her): Please.

85
00:08:23.900 --> 00:08:36.480
hr.manager: The office side is completely different, and I don't want us to only talk about trucks, because there's, um, there's a whole other pile of this that looks nothing like that. My expense report is a mileage claim and a hotel.

86
00:08:36.480 --> 00:08:37.400
Michelle Tremblay (she/her): Right.

87
00:08:37.400 --> 00:08:50.320
hr.manager: When I go out to BC, or when I do the site visits in the fall for the review cycle. So mine is four lines and one of them is mileage, and mileage doesn't have a receipt at all, it's kilometres times a rate.

88
00:08:50.680 --> 00:08:51.900
Michelle Tremblay (she/her): What's the rate?

89
00:08:51.900 --> 00:09:00.240
hr.manager: Um, we use the CRA one, so it's… seventy-two cents? Seventy? The Controller would know. I just type the kilometres in and the spreadsheet does it.

90
00:09:00.240 --> 00:09:04.560
controller: Seventy-two for the first five thousand. And she does about eleven thousand a year, so.

91
00:09:04.560 --> 00:09:05.900
hr.manager: See, this is why he's here.

92
00:09:06.400 --> 00:09:07.640
Michelle Tremblay (she/her): [laughs] Right.

93
00:09:08.100 --> 00:09:19.679
Michelle Tremblay (she/her): Okay, that's genuinely useful, because a mileage line and a photo of a receipt are two different shapes of thing and we should not pretend they're the same. Um, let me move to approvals, because I want to get there before you have to go.

94
00:09:19.680 --> 00:09:20.900
hr.manager: Yeah, I've got, um, fifteen minutes.

95
00:09:21.400 --> 00:09:24.320
Michelle Tremblay (she/her): Great. So who says yes today?

96
00:09:24.900 --> 00:09:26.500
controller: Depends on the number.

97
00:09:26.900 --> 00:09:27.800
Michelle Tremblay (she/her): Tell me the numbers.

98
00:09:28.240 --> 00:09:41.320
controller: So, right now — and this is a policy that I wrote, so, you know, blame me — anything under five hundred, the supervisor's manager signs it. That's the regional manager. Five hundred to twenty-five hundred, it comes to me.

99
00:09:41.680 --> 00:09:42.400
Michelle Tremblay (she/her): Mm-hmm.

100
00:09:42.400 --> 00:09:52.780
controller: Over twenty-five hundred, it's me and the Ops Director, so two signatures. And over five thousand, it goes to the Owner. And the Owner is not fast.

101
00:09:53.240 --> 00:09:54.900
Michelle Tremblay (she/her): [laughs] How not fast?

102
00:09:54.900 --> 00:10:05.680
controller: He's, uh… he's on a site somewhere. He's a very hands-on owner. Which is great for the business and it means a five thousand dollar approval can sit for eleven days.

103
00:10:06.100 --> 00:10:07.480
Michelle Tremblay (she/her): How often does that happen?

104
00:10:07.900 --> 00:10:16.240
controller: Over five? Not often. Six, eight times a year. It's a piece of equipment, or it's a big material order for a job that we didn't plan for.

105
00:10:16.680 --> 00:10:21.240
Michelle Tremblay (she/her): Okay. And that five thousand number — where did that come from?

106
00:10:21.680 --> 00:10:33.320
controller: Honestly? It came from our insurer, sort of, and partly it's just, it's the number where I stop being comfortable being the last set of eyes. There's no science in it. It's been five thousand since before I got here.

107
00:10:33.780 --> 00:10:34.900
Michelle Tremblay (she/her): That's a very honest answer.

108
00:10:34.900 --> 00:10:44.100
controller: [laughs] Well, you asked. I'd say the same about the five hundred. It's round. Round numbers are easy to remember and people actually follow rules they can remember.

109
00:10:44.560 --> 00:10:45.900
Michelle Tremblay (she/her): Mm. That's a real point.

110
00:10:46.400 --> 00:10:56.240
controller: What I would want from a system — and I've thought about this — is I want the tiers to be mine. Not, here's three levels, pick one. I want to say, this yard, this dollar figure, this person.

111
00:10:56.680 --> 00:10:57.400
Michelle Tremblay (she/her): Why per yard?

112
00:10:57.900 --> 00:11:10.320
controller: Because BC is different. BC has two yards and no regional manager, they report straight into the Ops Director. If I have to use the Ontario chain out there, everything routes to a person who doesn't exist.

113
00:11:10.680 --> 00:11:11.900
Michelle Tremblay (she/her): Got it.

114
00:11:12.240 --> 00:11:13.480
hr.manager: Can I push back a bit?

115
00:11:13.480 --> 00:11:14.400
Michelle Tremblay (she/her): Please do.

116
00:11:14.400 --> 00:11:28.780
hr.manager: Um. So I hear all of that and it makes sense from a finance chair. But I've lived through what happens when you build a beautiful approval chain with a lot of steps in it, and I would just… I'd wave a small flag.

117
00:11:29.240 --> 00:11:30.100
Michelle Tremblay (she/her): Say more.

118
00:11:30.100 --> 00:11:44.560
hr.manager: The merit spreadsheet. Right? Margaret's seen it. That thing has, what, four approvals in it — the manager, the one-up, the Head of HR, the exec team. And every single year it stalls. Not because anyone disagrees. Because somebody's on vacation.

119
00:11:44.900 --> 00:11:45.900
controller: That's true.

120
00:11:45.900 --> 00:12:00.240
hr.manager: And then I'm the one chasing. I send fourteen emails. So if you're going to give the Controller his four tiers, and I'm not saying don't, then the thing I would beg for is: what happens when the person in tier three is in Portugal for two weeks.

121
00:12:00.680 --> 00:12:02.240
Michelle Tremblay (she/her): Delegation. Yeah.

122
00:12:02.240 --> 00:12:14.320
hr.manager: Delegation, or escalation, or just — it goes to their one-up automatically after some number of days. Anything. Because right now the answer is "the HR Manager notices and phones someone," and that doesn't scale and it makes me the system.

123
00:12:14.680 --> 00:12:16.100
Michelle Tremblay (she/her): [laughs] It makes you the system.

124
00:12:16.100 --> 00:12:19.320
hr.manager: I am the escalation path. Write that down.

125
00:12:19.320 --> 00:12:20.560
Michelle Tremblay (she/her): I have written that down.

126
00:12:21.100 --> 00:12:29.680
controller: No, she's — that's fair. I'd take an auto-escalate after, I don't know, five business days. As long as it tells me it did it. I don't want things approving themselves quietly.

127
00:12:30.100 --> 00:12:31.400
Michelle Tremblay (she/her): So notify, not silent.

128
00:12:31.400 --> 00:12:37.680
controller: Notify. And it should still say who it went to and why. If I get audited I need to point at the trail.

129
00:12:38.240 --> 00:12:47.320
Michelle Tremblay (she/her): Okay. Um, one more on thresholds, then I'll move on — does the threshold apply to the receipt, or to the whole report? Because those give you very different behaviour.

130
00:12:47.780 --> 00:12:48.900
controller: Say that again?

131
00:12:48.900 --> 00:13:01.240
Michelle Tremblay (she/her): So if a supervisor submits eight receipts and they add up to twenty-eight hundred, is that over your twenty-five hundred line, or is it eight things that are all under five hundred?

132
00:13:01.680 --> 00:13:04.400
controller: Hmm. Today it's the report. So it's over.

133
00:13:04.900 --> 00:13:05.900
Michelle Tremblay (she/her): And is that right?

134
00:13:06.400 --> 00:13:18.240
controller: …Probably not, actually. Because that's how you get someone submitting twice in a month to stay under. Which — I know that happens. I'm not going to pretend I don't know that happens.

135
00:13:18.680 --> 00:13:19.900
Michelle Tremblay (she/her): Does it, really?

136
00:13:19.900 --> 00:13:29.320
controller: It's not fraud, it's not — nobody's stealing. It's a guy who doesn't want to wait for the Ops Director, so he splits it. And from his side that's just being practical.

137
00:13:29.780 --> 00:13:35.100
Michelle Tremblay (she/her): Right. Okay, that's a really good thing for me to know, thank you.

138
00:13:35.560 --> 00:13:40.680
hr.manager: I have to hop in about four minutes, is there anything you need from me specifically?

139
00:13:40.680 --> 00:13:47.320
Michelle Tremblay (she/her): Yes actually — the payroll piece, because that's the bit I think you'll both have a view on. Where does the money come out of?

140
00:13:47.780 --> 00:13:49.100
controller: Accounts payable. Not payroll.

141
00:13:49.100 --> 00:13:50.240
Michelle Tremblay (she/her): Not payroll at all?

142
00:13:50.240 --> 00:14:02.680
controller: Not at all. It's an EFT run out of A/P, and A/P runs every second Thursday. Payroll's biweekly too but on the opposite Thursday, so… yeah. You can see where this is going.

143
00:14:03.100 --> 00:14:04.400
Michelle Tremblay (she/her): They're a week apart.

144
00:14:04.400 --> 00:14:19.560
controller: They're a week apart, and the receipt has to be in before A/P cutoff, which is the Monday. So if you buy something on a Tuesday and your envelope gets to the office three weeks later, you're waiting a month for a hundred and eighty dollars you put on your own Visa.

145
00:14:20.100 --> 00:14:21.240
Michelle Tremblay (she/her): And people notice that.

146
00:14:21.240 --> 00:14:32.320
controller: People notice that a lot. That's the single thing I get phoned about. Not "where's my paycheque," they never phone about that, payroll's fine. It's "where's my ninety bucks from the Home Hardware."

147
00:14:32.780 --> 00:14:36.400
Michelle Tremblay (she/her): So would you want it on the pay run instead?

148
00:14:36.900 --> 00:14:38.240
controller: For the hourly guys, yes.

149
00:14:38.680 --> 00:14:39.560
Michelle Tremblay (she/her): Only hourly?

150
00:14:39.560 --> 00:14:53.240
controller: Well — no, I'd take it for everyone, but the hourly guys are where it hurts. They're the ones fronting money on a personal card. The salaried people have a company card mostly, so it's not their cash, they don't care as much.

151
00:14:53.680 --> 00:14:54.900
hr.manager: I care a little.

152
00:14:54.900 --> 00:14:56.400
controller: You care a normal amount.

153
00:14:56.400 --> 00:14:57.680
hr.manager: [laughs] I care a normal amount.

154
00:14:58.240 --> 00:15:04.320
Michelle Tremblay (she/her): Okay so if it went on the pay run, what has to be true? What would make you not do it?

155
00:15:04.780 --> 00:15:06.100
controller: Two things, and they're both hard.

156
00:15:06.560 --> 00:15:07.320
Michelle Tremblay (she/her): Go.

157
00:15:07.320 --> 00:15:20.680
controller: One. It's a reimbursement, it's not income. It cannot be taxable, it cannot show up on a T4, it should not touch anybody's, um, pensionable earnings, EI, none of it. If it does that once we'd have a very bad year.

158
00:15:21.100 --> 00:15:22.240
Michelle Tremblay (she/her): Understood, yeah.

159
00:15:22.240 --> 00:15:36.320
controller: And two — and this is the one I actually lose sleep over — I approve the payroll register. I look at it, I sign it, we transmit. If expenses can push things into a pay run after I've approved that register, then I haven't approved anything.

160
00:15:36.780 --> 00:15:38.100
Michelle Tremblay (she/her): So it has to be locked.

161
00:15:38.100 --> 00:15:52.560
controller: It has to be locked and it has to be visible before I lock it. Those are different asks. I need to see, on the register, here's your regular pay, here's your overtime, and here's four hundred and twelve dollars of expenses with a link so I can see what they were.

162
00:15:53.100 --> 00:15:54.240
Michelle Tremblay (she/her): Line-level, or a total?

163
00:15:54.240 --> 00:16:05.680
controller: Total on the register, but clickable. I'm not reading six hundred receipts on a register. But when the guy phones and says my expenses are wrong, I need to get to the receipt in one click, not go to another system.

164
00:16:06.240 --> 00:16:07.400
Michelle Tremblay (she/her): That's clear. Thank you.

165
00:16:07.900 --> 00:16:15.320
controller: And there's a cutoff problem. Payroll cutoff for us is Monday at noon for a Thursday pay date. Expenses don't respect Monday noon.

166
00:16:15.780 --> 00:16:16.900
Michelle Tremblay (she/her): So what should happen?

167
00:16:16.900 --> 00:16:28.560
controller: It should roll to the next one. Quietly, automatically, and the guy should be able to see, in whatever app he's got, "approved, paying on the eleventh." That's it. That's ninety percent of my phone calls gone.

168
00:16:29.100 --> 00:16:30.400
Michelle Tremblay (she/her): Status visibility.

169
00:16:30.400 --> 00:16:39.240
controller: Status visibility. He doesn't need it faster, necessarily. He needs to know. Half the frustration is not the wait, it's not knowing if the envelope even arrived.

170
00:16:39.680 --> 00:16:41.900
hr.manager: That's true of literally everything here, by the way.

171
00:16:42.400 --> 00:16:43.240
Michelle Tremblay (she/her): Say more?

172
00:16:43.240 --> 00:16:54.680
hr.manager: Just — reviews, time off, expenses. The number one question I get is "did it go through." Not "can you approve it," just, did the thing I did land somewhere. It's the same question every time.

173
00:16:55.100 --> 00:16:56.400
Michelle Tremblay (she/her): That's a good line, I'm stealing that.

174
00:16:56.900 --> 00:17:01.240
hr.manager: Take it. Um, I do have to go, I'm so sorry.

175
00:17:01.240 --> 00:17:04.680
Michelle Tremblay (she/her): No, thank you so much, this was really valuable. One quick—

176
00:17:04.680 --> 00:17:13.320
hr.manager: Mobile! Can I do thirty seconds on mobile before I go, because I know the Controller's going to be reasonable about it and I want to be unreasonable first.

177
00:17:13.780 --> 00:17:15.100
Michelle Tremblay (she/her): [laughs] Please.

178
00:17:15.100 --> 00:17:28.560
hr.manager: Our supervisors do not have desks. I want to say that as plainly as I can. A route supervisor's office is a truck. He has a phone. He does not have a laptop, he's never going to have a laptop, and if he did it would live in the yard office and he'd see it Fridays.

179
00:17:28.900 --> 00:17:29.900
Michelle Tremblay (she/her): Mm-hmm.

180
00:17:29.900 --> 00:17:44.320
hr.manager: So anything you build for that layer of the company that assumes a browser on a desk is already dead. Not "less good." Dead. That's the same thing I've been telling Margaret about reviews, it's the same thing here.

181
00:17:44.780 --> 00:17:47.100
Michelle Tremblay (she/her): And is the current Payworks app not—

182
00:17:47.100 --> 00:17:58.560
hr.manager: The app is time. It's punch in, punch out, request time off. Which is fine, it works. But a supervisor can't do anything as a supervisor in it. He can only be an employee in it.

183
00:17:59.100 --> 00:18:00.240
Michelle Tremblay (she/her): That's a really clean way to put it.

184
00:18:00.240 --> 00:18:09.680
hr.manager: That's the whole thing. He's a manager for nine hours a day and the app only knows him as an employee. Okay, I really have to go. Thank you! Send me anything you need.

185
00:18:09.680 --> 00:18:11.400
Michelle Tremblay (she/her): Thank you so much. Take care.

186
00:18:11.400 --> 00:18:12.240
controller: Bye.

187
00:18:12.240 --> 00:18:13.100
Vanessa Lee: Bye, thank you!

188
00:18:16.780 --> 00:18:19.100
Michelle Tremblay (she/her): She's very good at this.

189
00:18:19.100 --> 00:18:24.560
controller: She's been here nineteen years. She knows where everything is buried, including some of it she buried.

190
00:18:24.560 --> 00:18:26.100
Michelle Tremblay (she/her): [laughs]

191
00:18:26.680 --> 00:18:31.320
Michelle Tremblay (she/her): So, mobile. She was unreasonable. Be reasonable at me.

192
00:18:31.780 --> 00:18:33.100
controller: [laughs] Okay.

193
00:18:33.560 --> 00:18:44.240
controller: I agree with every word of it for capture. Hundred percent. The picture has to happen on a phone at the counter, there is no other place it can happen, if you make that a web form on a desktop nothing will ever be captured.

194
00:18:44.680 --> 00:18:45.560
Michelle Tremblay (she/her): But.

195
00:18:45.560 --> 00:18:58.320
controller: But. Approving on a phone. I get twitchy above a certain number. And I'll tell you exactly why, and it's not a security thing, it's a — it's an attention thing.

196
00:18:58.780 --> 00:18:59.900
Michelle Tremblay (she/her): Attention how?

197
00:18:59.900 --> 00:19:12.560
controller: If I'm approving twenty-eight hundred dollars, I want to be looking at the job it's coded to, and the budget on that job, and whether we've already bought this. That's three things on a screen. On a phone that's three swipes and I'm not going to do it.

198
00:19:13.100 --> 00:19:14.240
Michelle Tremblay (she/her): You'd just tap yes.

199
00:19:14.240 --> 00:19:24.680
controller: I'd tap yes. In a parking lot. I know myself. And then it's not really an approval, it's a formality, and I've built a control that doesn't control anything, which is worse than not having it.

200
00:19:25.100 --> 00:19:26.400
Michelle Tremblay (she/her): That's a genuinely interesting objection.

201
00:19:26.400 --> 00:19:38.320
controller: So my line would be — small stuff, phone, absolutely, get it moving, that's the whole point. My tier, the twenty-five hundred and up, I'd honestly rather it made me go to a real screen.

202
00:19:38.780 --> 00:19:41.100
Michelle Tremblay (she/her): Would you want us to enforce that, or just… let you?

203
00:19:41.100 --> 00:19:52.560
controller: Enforce it. If it's optional I'll do it in the parking lot. [laughs] No — genuinely, make it a setting I turn on, and then make it stick. "Approvals over X require desktop." I'd turn that on day one.

204
00:19:53.100 --> 00:19:55.240
Michelle Tremblay (she/her): Huh. You're the second person to ask me for that this month, and I'd have bet money nobody would ask once.

205
00:19:55.240 --> 00:20:03.680
controller: Everybody asks you for more mobile. I'm asking you for a fence. It's the same reason my five thousand goes to the Owner. Some decisions should be slightly annoying.

206
00:20:04.240 --> 00:20:05.400
Michelle Tremblay (she/her): "Some decisions should be slightly annoying."

207
00:20:05.900 --> 00:20:07.240
controller: Put that on the box.

208
00:20:07.680 --> 00:20:09.400
Vanessa Lee: Can I ask about the capture side?

209
00:20:09.400 --> 00:20:10.240
controller: Yeah, go ahead.

210
00:20:10.680 --> 00:20:20.320
Vanessa Lee: Um, when you say the phone at the counter — do your crews have signal? Because a lot of what you're describing sounds like it might be, you know, out past where there's coverage.

211
00:20:20.780 --> 00:20:22.100
controller: That's a very good question.

212
00:20:22.560 --> 00:20:33.240
controller: Um. Mostly yes. The municipal sites are in town, that's fine. But we've got two contracts that are, uh, they're out past the escarpment and there's nothing out there. And BC has dead spots.

213
00:20:33.680 --> 00:20:34.900
Vanessa Lee: So if the photo fails to upload…

214
00:20:34.900 --> 00:20:46.320
controller: Then it has to keep it. It cannot say "no connection, try again." Because he's going to close it and get in the truck and the receipt is now gone, and we're back to the shoebox but with extra steps.

215
00:20:46.780 --> 00:20:48.100
Vanessa Lee: Right. That's what I wanted to check.

216
00:20:48.100 --> 00:20:57.560
controller: And it has to be obvious that it kept it. Like, some little thing that says "three waiting to send." Because otherwise he doesn't trust it and he keeps the paper too, and then what have we gained.

217
00:20:58.100 --> 00:20:59.400
Michelle Tremblay (she/her): He keeps the paper too. [laughs]

218
00:20:59.400 --> 00:21:07.680
controller: They will absolutely keep the paper for the first six months regardless. That's fine. I just don't want them keeping it forever because the app lied to them once.

219
00:21:08.240 --> 00:21:14.320
Michelle Tremblay (she/her): Okay. Um, can I ask a slightly commercial question, and you can tell me to get lost.

220
00:21:14.780 --> 00:21:15.900
controller: Go for it.

221
00:21:15.900 --> 00:21:24.560
Michelle Tremblay (she/her): Have you looked at buying something standalone for this? Like a dedicated expense tool. Because there's a bunch of them and they're decent.

222
00:21:25.100 --> 00:21:26.400
controller: We did. Last year.

223
00:21:26.900 --> 00:21:27.680
Michelle Tremblay (she/her): And?

224
00:21:27.680 --> 00:21:41.320
controller: The one we looked at hardest was nine dollars a user a month, and they wanted a two hundred seat minimum, so that's twenty-one, twenty-two thousand a year. Which, fine, I could defend twenty-two thousand against two and a half days of clerk time.

225
00:21:41.780 --> 00:21:42.900
Michelle Tremblay (she/her): So what stopped it?

226
00:21:42.900 --> 00:21:54.560
controller: It didn't talk to payroll. And it didn't know what a job number was, which meant I'd be exporting a CSV into the job costing anyway, and I've got enough CSVs. So I'd be paying twenty-two grand to move the problem.

227
00:21:55.100 --> 00:21:56.400
Michelle Tremblay (she/her): That's very useful to hear.

228
00:21:56.400 --> 00:22:08.680
controller: And look — I'll be straight with you, part of why I took this call is our renewal is coming up, and when it does I'd rather be having a conversation about adding something than about the number going up for the same thing.

229
00:22:09.240 --> 00:22:10.400
Michelle Tremblay (she/her): That's fair.

230
00:22:10.400 --> 00:22:20.320
controller: I don't know the exact date off the top of my head, Amanda would, but it's, uh, it's on the horizon. So if there's a pilot or an early version, I'd want to be in it. Genuinely.

231
00:22:20.780 --> 00:22:23.100
Michelle Tremblay (she/her): Noted, and I'll flag that to Amanda rather than guess at it.

232
00:22:23.560 --> 00:22:24.900
controller: Yeah, she keeps all that.

233
00:22:25.400 --> 00:22:32.240
Michelle Tremblay (she/her): Um, I've got about eight minutes left. Is there anything I haven't asked that I should have?

234
00:22:32.680 --> 00:22:34.400
controller: Yeah, actually. Two things.

235
00:22:34.900 --> 00:22:35.680
Michelle Tremblay (she/her): Please.

236
00:22:35.680 --> 00:22:48.320
controller: One is who's allowed to submit. Right now it's supervisors and up, because the crew guys aren't in a system at all, they're a name on a time sheet. But half the actual purchases are made by a crew member because the supervisor's at another site.

237
00:22:48.780 --> 00:22:50.100
Michelle Tremblay (she/her): So it's submitted under the supervisor's name.

238
00:22:50.100 --> 00:23:01.560
controller: It's submitted under the supervisor and it's the crew guy's Visa. Which is — that's not great, right? I'm reimbursing a person who didn't spend the money and trusting him to pass it on. Which he does. But still.

239
00:23:02.100 --> 00:23:03.400
Michelle Tremblay (she/her): No, that's a real problem.

240
00:23:03.400 --> 00:23:15.680
controller: It's a real problem and it's invisible because it works. So if we're doing this, I'd want everybody who might buy something to be able to submit, which is, what, another two hundred and something people who currently have no login.

241
00:23:16.240 --> 00:23:17.400
Michelle Tremblay (she/her): And that's a cost question for you.

242
00:23:17.400 --> 00:23:27.320
controller: It's a cost question and it's a — I mean, half those guys are seasonal. They're here April to November. So am I paying for two hundred logins in February? That's the thing I'd want to understand.

243
00:23:27.780 --> 00:23:29.100
Michelle Tremblay (she/her): Understood. And the second thing?

244
00:23:29.560 --> 00:23:41.240
controller: Second thing is the seasonal piece again but for approvals. Our regional managers turn over. Not constantly, but we've had three in that Ontario west chair in four years. And every time, somebody has to go rebuild the routing.

245
00:23:41.680 --> 00:23:42.900
Michelle Tremblay (she/her): Who does that today?

246
00:23:42.900 --> 00:23:53.560
controller: Me. Badly. In a Word document. There is a document called Approval Authority dot doc and I was last updated — I would rather not tell you when it was last updated.

247
00:23:54.100 --> 00:23:55.400
Michelle Tremblay (she/her): [laughs] Ballpark?

248
00:23:55.400 --> 00:23:58.680
controller: Twenty twenty-three. Maybe twenty twenty-two.

249
00:23:58.680 --> 00:24:00.240
Michelle Tremblay (she/her): Okay, so it should follow the position, not the person.

250
00:24:00.240 --> 00:24:11.320
controller: The position, yes. That's exactly it. Approvals should hang off "regional manager, Ontario west," and if you put a new person in that chair in the HR side, the approvals should just follow. Nobody should have to remember.

251
00:24:11.780 --> 00:24:14.100
Michelle Tremblay (she/her): That's a really important requirement, thank you.

252
00:24:14.560 --> 00:24:24.240
controller: I mean that's true of a lot of it, isn't it. The system already knows who reports to who. Payroll knows. It's just, expense doesn't ask payroll.

253
00:24:24.680 --> 00:24:26.900
Michelle Tremblay (she/her): [laughs] That's, uh. Yeah. That's the whole project, kind of.

254
00:24:27.400 --> 00:24:28.240
controller: Well, there you go.

255
00:24:28.680 --> 00:24:35.320
Vanessa Lee: Can I ask one design-ish question? Um, when the supervisor gets an approval — where does he get it? Like what wakes him up?

256
00:24:35.780 --> 00:24:37.100
controller: Today? Nothing wakes him up.

257
00:24:37.100 --> 00:24:37.900
Vanessa Lee: [laughs] Right.

258
00:24:37.900 --> 00:24:49.560
controller: Today it's paper in a tray. If it were me building it — email is fine for the regional managers, they're at a computer sometimes. For the yard-level guys it has to be the phone, and it has to be a badge, not an email.

259
00:24:50.100 --> 00:24:51.400
Vanessa Lee: Because email is…

260
00:24:51.400 --> 00:25:00.680
controller: Half of them don't have a company email. That's the other thing. The HR Manager could tell you more about that than me, but a lot of the field guys have no email address at all in the system.

261
00:25:01.240 --> 00:25:02.400
Michelle Tremblay (she/her): Oh, that's significant.

262
00:25:02.400 --> 00:25:13.320
controller: It's significant for you. It's a headache for her — she's got some issue where the review system won't pull an employee unless there's a company email on the Payworks file, and half of them don't have one.

263
00:25:13.780 --> 00:25:16.100
Michelle Tremblay (she/her): Yeah, she's mentioned that to Margaret. Same root.

264
00:25:16.560 --> 00:25:22.240
controller: Probably. Anyway. If your notification story is email, it doesn't reach the people who most need it.

265
00:25:22.680 --> 00:25:29.320
Michelle Tremblay (she/her): That's a great note to end on, honestly. Um, let me tell you what happens next.

266
00:25:29.780 --> 00:25:30.900
controller: Sure.

267
00:25:30.900 --> 00:25:43.560
Michelle Tremblay (she/her): I'm going to write this up, and there's a decent chance a bunch of what you said changes what we're building, particularly the register-lock piece and the position-based approvals. Um, I'd love to come back in three or four weeks with something to look at.

268
00:25:44.100 --> 00:25:45.400
controller: Yeah, happy to.

269
00:25:45.400 --> 00:25:53.680
Michelle Tremblay (she/her): And it'll be ugly. Vanessa will show you something that looks nothing like Payworks and that's on purpose, it's a discussion starter, you can't hurt our feelings.

270
00:25:53.680 --> 00:25:54.900
Vanessa Lee: Please hurt our feelings.

271
00:25:55.400 --> 00:25:56.680
controller: [laughs] I'll do my best.

272
00:25:57.100 --> 00:26:07.320
controller: Um, one ask from me — if you do come back, can I bring my A/P clerk? Because I've described her job to you for half an hour and I have almost certainly got some of it wrong.

273
00:26:07.780 --> 00:26:10.100
Michelle Tremblay (she/her): Yes. Please. That's the person I most want to talk to.

274
00:26:10.560 --> 00:26:14.240
controller: Good. She'll be delighted. She'll bring the shoebox.

275
00:26:14.680 --> 00:26:16.400
Michelle Tremblay (she/her): I would genuinely like to see the shoebox.

276
00:26:16.400 --> 00:26:18.680
controller: [laughs] Okay. Thanks, everyone.

277
00:26:18.680 --> 00:26:20.240
Michelle Tremblay (she/her): Thank you so much for the time.

278
00:26:20.240 --> 00:26:21.400
Vanessa Lee: Thanks!

279
00:26:21.400 --> 00:26:22.560
controller: Take care. Bye.
