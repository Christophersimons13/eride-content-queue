= AI Tools Drop - Video Script
= Episode 3, week of 10 to 17 August 2026
= Target runtime 14:00 to 14:30. Narration is 2,295 words, which lands at about 14:20 at a 160 words per minute delivery. That sits at the top of the 10 to 15 minute band for this series. If the ElevenLabs render comes back longer than 15:00, cut the n8n Domains.co.za aside and the second half of the Lettertrace limitations, in that order.
= Voice: ElevenLabs, South African male, measured and dry. No hype. No exclamation points.
= All ON-SCREEN TEXT is ASCII-only. No em dashes, no smart quotes, no ellipsis characters.

---

## Production notes before recording

**Tone for this episode.** This is a thin week and the script says so in the first thirty seconds. Do not let the voice oversell. The credibility of the series comes from admitting a quiet week and going deeper on the four things that matter. The through-line is: broken pricing pages, and what a South African operator should do about them.

**Pace.** Slightly slower than episode 2. There are fewer tools and more explanation per tool.

**Pronunciation guide** (feed as a note to the voice, or spell phonetically in the input text if the voice mangles a name):

| Name | Say it as |
|---|---|
| Dograh | DOH-gruh |
| BetterClaw | BETTER-claw |
| Lettertrace | LETTER-trace |
| Vizard | VIZ-ard, rhymes with wizard |
| n8n | say it as "n-eight-n", letter, number, letter |
| GLM-5.3 | G-L-M five point three |
| Z.ai | Zed dot A-I |
| Zhipu | JEE-poo |
| xAI | X-A-I |
| POPIA | poh-PEE-uh |
| Xneelo | ex-NEE-loh |
| SAHPRA | SAH-pra |
| Vapi | VAH-pee |
| Supabase | SOO-puh-base |
| C2PA | C-two-P-A |
| oqoqo | oh-KOH-koh |
| Talvo | TAL-voh |

**ElevenLabs settings:** voice ID `P1LmKcX63Ihgqy11sVRt`, model `eleven_multilingual_v2`, stability 0.60, similarity_boost 0.75, style 0.15, use_speaker_boost true, output `mp3_44100_128`.

---

## 0:00 - 0:40 | Cold open

**NARRATION**

Three vendors this week could not tell me what their own product costs. One renders zero where the paid price should be. One shows two different prices for every tier. One puts a get-started-for-free button next to a three hundred dollar a month plan. That is the real story of this week in AI, and it is more useful to you than any benchmark score. Thin week for products, heavy week for models. So instead of padding the list, I am going deeper on the four things a South African business could actually use, and being straight with you about the rest.

**ON-SCREEN TEXT**

```
THREE VENDORS.
THREE BROKEN PRICING PAGES.
ONE THIN WEEK.
```

**B-ROLL / VISUAL**

Cold open on a dark frame. Three price tags fade in one at a time, each one glitching to a zero or to two conflicting numbers. On the last line, cut to the series title card. Palette: bg #111111, accent #F5C542 on the numbers, warning #E5533D on the glitch frames.

---

## 0:40 - 1:45 | Why this week matters

**NARRATION**

From the tenth to the sixteenth of August, the Product Hunt leaderboards were almost entirely developer infrastructure. Evaluation harnesses. Agent sandboxes. Command line tools. Useful if you write code for a living, irrelevant if you run a salon or a logistics business. Nine items are verified inside the seven day window. About four are things you could adopt without a developer sitting next to you.

Here is the part I actually want you to hear. On the twelfth of August, TechCentral published a survey of roughly a hundred South African tech decision makers. Only about twenty five percent are running AI in production. Forty three percent are still piloting. One in four. That is the real number.

Hold that against what I am about to show you, because two of this week's items cost nothing at all to run. Free forever, no credit card. The gap between piloting and production is usually not a tooling gap. So: fewer tools, more depth, and one thing I want you to go and do.

**ON-SCREEN TEXT**

```
SA FIRMS RUNNING AI IN PRODUCTION
25 PERCENT
STILL PILOTING
43 PERCENT
SOURCE: TECHCENTRAL, 12 AUG 2026
```

**B-ROLL / VISUAL**

Motion graphic: a simple horizontal bar filling to 25 percent in accent yellow, then a second bar to 43 percent in muted grey. Hold on the two numbers. Then a slow push on an abstract Johannesburg skyline still (reuse Group B divider image from episode 1 cache if suitable).

---

## 1:45 - 3:20 | Tool one: Gemini 3.7 Flash

**NARRATION**

Start with the biggest one, because it is the cheapest serious model you can put into production this week. Google made Gemini three point seven Flash generally available on the thirteenth. One million token context window, sixty four thousand tokens out, selectable thinking levels. It replaced the previous Flash release three weeks after that one shipped, which tells you something about the pace.

The benchmarks moved properly. Coding, from forty nine percent to sixty five point three on DeepSWE. Business process automation, seventeen to thirty point four. That second one is the difference between a model that drafts a document and a model that runs a workflow.

Now the two things the launch coverage did not lead with.

First, the price. Seventy five cents per million tokens in, three seventy five out. About twelve rand and sixty one rand. But that applies only through the thirty first of December. On the first of January it doubles. If you are building a 2027 budget on this week's number, your budget is wrong.

Second, and bigger. The free tier trains on your data. Google's own pricing page says free tier usage is used to improve Google products. If you are putting a client's immigration file, or anything with an identity number in it, through the free tier, that is not a preference problem, that is a POPIA problem. Pay for the tier. It is cheap.

Where it fits: immigration document review, invoice batches at about six rand per million tokens, contract summarising, agency drafting at volume.

**ON-SCREEN TEXT**

```
GEMINI 3.7 FLASH
GA 13 AUGUST 2026

NOW      0.75 IN / 3.75 OUT PER 1M
1 JAN    1.50 IN / 7.50 OUT PER 1M
         PRICE DOUBLES

FREE TIER TRAINS ON YOUR DATA
```

**B-ROLL / VISUAL**

Kling clip: a document stack being read page by page, cool blue light, no faces. Then a Shotstack table animation for the price change, with the 1 Jan row highlighted in warning red #E5533D. Close the segment on the POPIA line in full-frame text, style "future".

---

## 3:20 - 5:20 | Tool two: Dograh

**NARRATION**

This is my pick of the week, and it is open source.

Dograh won Product Hunt on the twelfth. A platform for building voice AI phone agents, positioned against Vapi, licensed BSD two clause. Visual flow builder, telephony, human transfer, monitoring, thirty plus model integrations including local models. Free forever if you host it yourself, no usage limits. Or one cent a minute hosted, about sixteen South African cents, with credits from five dollars.

But the reason it is my pick is one feature. Seventy plus languages, with switching mid call.

Think about what that means here. A caller opens in English, switches to isiZulu halfway through a sentence, because that is how people actually speak. Every overseas voice platform I have looked at treats language as a setting you choose at the start of the call. This one treats it as something that changes during the call. That is the difference between a voice agent that works in South Africa and one that frustrates every second caller.

Where I would use it: immigration intake, capturing the pathway and passport details and handing to a consultant on request. Beauty and wellness, confirming tomorrow's bookings and rebooking cancellations. Collections reminders in fintech, with the recording staying on infrastructure you own.

Three honest limitations. One, the pricing contradicts itself: the HTML page says enterprise is custom, their own pricing file says on premise starts at two thousand five hundred dollars a month, about forty thousand rand. Raise it before you sign. Two, one cent a minute is the platform fee, not your bill. You still pay the model and telephony providers on top.

Three, and this matters most. Nowhere on that page does it say anything about regions or South African phone numbers. For a telephony product, local number availability is the whole question. Make it your first question to them, not your first surprise.

**ON-SCREEN TEXT**

```
DOGRAH
PRODUCT HUNT NO. 1, 12 AUGUST

OPEN SOURCE, BSD-2
FREE FOREVER SELF-HOSTED
70+ LANGUAGES, SWITCHES MID-CALL
HOSTED: 1 CENT PER MINUTE
        ABOUT 16 SA CENTS

UNANSWERED: SA PHONE NUMBERS
```

**B-ROLL / VISUAL**

Kling clip: a phone handset on a desk, warm light, ringing. Then a Shotstack animation of a waveform where the language label above it changes from EN to ZU to AF mid-waveform, in accent yellow. Close on the "unanswered" line in warning red.

---

## 5:20 - 6:55 | Tool three: BetterClaw

**NARRATION**

BetterClaw came second on Product Hunt on the eleventh. A hosted agent platform, pitched as deploy an agent in sixty seconds for zero dollars forever.

I am recommending it, but not for the reason they would like. The product is fine. What is genuinely valuable is the free tier: zero dollars a month, forever, explicitly no credit card. One agent, five hundred credits, three connectors, seven day memory, a kill switch and a sandbox.

Why that matters here specifically. For a South African founder, the usual blocker on an American tool is not the price, it is the card. Three steps into a signup and it wants a US billing address. No card means you can find out this afternoon whether your agent idea holds up, at zero rand. And one credit is one minute of agent uptime, so five hundred credits is roughly five hundred minutes a month. A legible unit.

Two things to plan around. The seven day memory on free is a hard ceiling and it decides what you can test. An agent that forgets a client after a week cannot track an immigration case. It can run a weekly competitor price check, or triage your support inbox every morning. And bring your own key means free covers the orchestration, not the thinking.

One warning. Three different versions of the free tier are in circulation. The vendor page says five hundred credits. The Product Hunt post and Capterra both say a hundred tasks. Trust the vendor page.

**ON-SCREEN TEXT**

```
BETTERCLAW
PRODUCT HUNT NO. 2, 11 AUGUST

FREE FOREVER, NO CREDIT CARD
1 AGENT, 500 CREDITS PER MONTH
1 CREDIT = 1 MINUTE OF UPTIME
7-DAY MEMORY CAP

PRO 49 USD, ABOUT R794 PER MONTH
```

**B-ROLL / VISUAL**

Shotstack motion graphic carrying this whole segment. A card icon with a strikethrough in accent yellow on the "no credit card" line. A countdown from 7 to 0 on the memory cap, in warning red. Keep it graphic-led, no Kling clip needed here.

---

## 6:55 - 8:35 | Tool four: n8n 2.35.0

**NARRATION**

Quick one for anyone already running n8n, and there are more of you in Johannesburg than you would think.

Version two point three five point zero landed on the eleventh. The headline for self hosters: the AI Assistant, which used to be a paid Cloud feature, now works on Community and self hosted installs. If you kept your automation on local infrastructure for data residency reasons, you no longer pay a capability penalty for that choice. It also adds Agent Builder test runs with a human in the loop, better approval steps over Slack and Telegram, and token counting for local models.

Three cautions. The official n8n documentation changelog does not list two point three five point zero at all. It showed two point three four as latest stable while listing two point three five point three in beta. GitHub and the docs disagree, so check which build you are installing before you touch production. Second, n8n Agents is still beta for self hosted and explicitly not available for self hosted Enterprise. Third, pricing is euros only. Starter twenty euros, about three hundred and seventy five rand. Pro fifty euros, about nine hundred and forty. You eat the FX on every invoice.

And one I had to leave out. Domains dot co dot za launched self hosted n8n VPS hosting inside South Africa. Most relevant thing on my whole shortlist to a local operator, and dated the twenty ninth of July. Twelve days outside my window, so it does not count as a launch. If you run n8n locally, look at it anyway.

**ON-SCREEN TEXT**

```
n8n 2.35.0
11 AUGUST 2026

AI ASSISTANT NOW ON SELF-HOSTED
AGENT BUILDER TEST RUNS, HITL
LOCAL MODEL TOKEN COUNTING

CAUTION: DOCS CHANGELOG DISAGREES
PRICING IN EUROS ONLY
```

**B-ROLL / VISUAL**

Shotstack node-graph animation: nodes connecting in sequence, one node lighting up in accent yellow labelled AI ASSISTANT. Then a split-screen graphic showing "GITHUB: 2.35.0" against "DOCS: 2.34" with a warning-red divider.

---

## 8:35 - 9:40 | Tool five: Lettertrace

**NARRATION**

Fifth, and the last one I would recommend. Lettertrace came third on Product Hunt on the twelfth. Free, MIT licensed, and it answers one question: when someone asks Claude or ChatGPT or Gemini about your category, does your business get mentioned?

It tracks visibility, share of voice, prominence, sentiment and competitor comparison across those three plus Google AI Overviews. Keys encrypted at rest, results into your own Supabase instance, which is a real POPIA advantage over a hosted tracker holding your data.

Concretely: someone asks an assistant how to get a South African work visa. Does your consultancy come up, or a competitor? That is now measurable rather than a guess.

Two limitations. Bring your own key means three separate API accounts with three separate cards before you see one report, so free understates the setup. And you must run your own Supabase. Fine if you are technical. A hard blocker if you are a salon owner, and I am not going to pretend otherwise.

**ON-SCREEN TEXT**

```
LETTERTRACE
PRODUCT HUNT NO. 3, 12 AUGUST

FREE, MIT LICENCE
TRACKS CLAUDE, CHATGPT, GEMINI
PLUS GOOGLE AI OVERVIEWS
DATA STAYS IN YOUR SUPABASE

NEEDS: 3 API KEYS, OWN SUPABASE
```

**B-ROLL / VISUAL**

Shotstack graphic: three model logos as abstract shapes, a search query typing in, then a brand marker appearing or failing to appear in the answer. Keep it abstract, no real logos.

---

## 9:40 - 11:35 | The broken pricing pages

**NARRATION**

Now the segment I opened with, because it is the most practically useful thing here.

Three products launched this week that I could not price from the vendor's own website.

Vizard shipped a conversational video agent. The free tier is documented properly. The paid tiers render as zero dollars, fifty percent off, zero dollars billed yearly. The page is broken. A review site says twenty nine and thirty nine dollars a month, but those are the reviewer's numbers, not Vizard's, and I am not handing you a price the vendor does not publish. The free tier watermarks output anyway, so it is no good for client work.

Z dot A-I released GLM five point three on the fourteenth. Their subscription page shows two prices for every single tier. Lite at twelve sixty and at eighteen dollars. Pro at fifty six and at eighty. Max at a hundred and seventeen sixty and at a hundred and sixty eight. And it gets worse: the page never says GLM five point three is included. The copy references five point two and five turbo. You cannot confirm from the vendor that a subscription buys you the model that launched this week.

And xAI shipped Grok Bot on the eleventh. Two hundred dollars a month for Ultra, three hundred for SuperGrok Heavy, a hundred and twenty per seat for Teams. Roughly three thousand two hundred to four thousand eight hundred rand. Beta software, enterprise waitlist only. And on the same page as those numbers, a get started for free button with no trial terms stated anywhere.

Here is the rule. If a vendor cannot state its own price clearly, that tells you something about how it will handle your invoice, your renewal and your support ticket. A broken pricing page is the first evidence you have about how a company operates. Treat it accordingly.

**ON-SCREEN TEXT**

```
COULD NOT PRICE FROM VENDOR SITE

VIZARD      PAID TIERS RENDER AS 0
Z.AI        TWO PRICES PER TIER
XAI         FREE BUTTON NEXT TO 300 USD

RULE: IF THEY CANNOT PRICE IT,
BE CAREFUL WHAT ELSE THEY CANNOT DO
```

**B-ROLL / VISUAL**

The strongest graphic moment in the episode. Three price cards side by side, each one failing in a different way: one collapsing to zero, one flickering between two numbers, one with a contradictory button. Then the rule appears full-frame, style "future", accent yellow on "RULE".

---

## 11:35 - 12:55 | The Claude watermark, and what to do about it

**NARRATION**

One policy change you need to know about, because it applies whether you agreed to it or not.

On the fourteenth, Anthropic published how Claude's text watermarking works. Any Claude model launched on or after the second of August now embeds a statistical watermark in the text it generates. Global. No opt out. Signed provenance metadata on generated image files too, and a detection API. So if you draft a client proposal with Claude, that text carries a detectable marker.

Two things. First, it cannot do what people will assume it does. Anthropic says so themselves: the watermark cannot distinguish Claude wrote this from Claude heavily edited this. South African experts told ITWeb the same thing on the fourteenth. It is not evidence of misconduct.

Second, the bigger point. This is EU compliance delivered worldwide. The European AI Act drove it, and it reached your desk in Johannesburg through vendor policy, not South African law. You will keep inheriting European regulation through the tools you use, whether or not our own policy keeps up.

The thing to do, and it costs nothing. Decide this week what you tell clients about AI assistance in written work, and put it in your engagement letter. Do not wait for a client to run a detector and phone you about it.

**ON-SCREEN TEXT**

```
CLAUDE TEXT WATERMARKING
14 AUGUST 2026

MODELS FROM 2 AUG ONWARDS
GLOBAL, NO OPT-OUT
CANNOT TELL WROTE FROM EDITED

DO THIS: PUT AI DISCLOSURE
IN YOUR ENGAGEMENT LETTER
```

**B-ROLL / VISUAL**

Kling clip: a printed document under a light, a faint pattern becoming visible across the text. Then full-frame on the "DO THIS" instruction, style "future".

---

## 12:55 - 14:30 | What I would actually try, and close

**NARRATION**

Thin week. Here is what I would do with it.

First pick, Dograh. The only thing here that is free forever with no usage cap, and its standout feature, switching language mid call across seventy plus languages, maps onto a South African reality overseas vendors do not plan for. Self host it, point it at a test line, see whether it handles a caller moving from English to isiZulu mid sentence. First question to the vendor: South African phone numbers.

Second pick, BetterClaw's free tier. Not because the product is remarkable, but because zero rand and no credit card is the cheapest honest way to find out whether an agent idea works. Test short tasks.

One to avoid. Grok Bot. Three thousand two hundred to four thousand eight hundred rand a month, in beta, no published trial terms. There is no version of that maths that works for a small South African business.

And the free thing again, because it will catch someone out: write your AI disclosure into your client terms.

That is the week. Four tools worth your time, three vendors who could not price their own products, and a survey telling us only one in four South African firms are running any of this in production. Two of this week's items cost nothing. The gap is not the tooling.

The full written version, with every price, every rand conversion and every source link, is on the WhatsApp channel. Join it there, and I will see you next Monday.

**ON-SCREEN TEXT**

```
THIS WEEK

TRY      DOGRAH, SELF-HOSTED
TRY      BETTERCLAW FREE TIER
AVOID    GROK BOT
DO       AI DISCLOSURE IN YOUR TERMS

FULL WRITTEN VERSION
ON THE WHATSAPP CHANNEL
```

**B-ROLL / VISUAL**

Summary card animation, each line landing in sequence. TRY lines in accent yellow, AVOID in warning red, DO in white. Hold four seconds. Then the end card with the WhatsApp channel call to action and the AI disclosure strip along the bottom edge.

---

## Mandatory on-video disclosure

A persistent strip must appear in the lower third of the final frame, and again as a three second full-frame card before the end card:

```
THIS VIDEO USES AI-GENERATED VISUALS
AND AN AI-GENERATED VOICE.
RESEARCH AND SCRIPT VERIFIED
AGAINST SOURCE PAGES.
```

The same disclosure goes in the platform-level AI content declaration at upload on YouTube, TikTok, Instagram and Facebook.

---

## Segment timing summary

Durations below are derived from the actual narration word counts at 160 words per minute. The segment headings in the body of this script carry the same timestamps, and both must be updated together if the copy changes.

| Segment | In | Out | Words | Duration |
|---|---|---|---|---|
| Cold open | 0:00 | 0:40 | 102 | 0:40 |
| Why this week matters | 0:40 | 1:45 | 171 | 1:05 |
| Gemini 3.7 Flash | 1:45 | 3:20 | 254 | 1:35 |
| Dograh | 3:20 | 5:20 | 313 | 2:00 |
| BetterClaw | 5:20 | 6:55 | 250 | 1:35 |
| n8n 2.35.0 | 6:55 | 8:35 | 263 | 1:40 |
| Lettertrace | 8:35 | 9:40 | 165 | 1:05 |
| Broken pricing pages | 9:40 | 11:35 | 309 | 1:55 |
| Claude watermarking | 11:35 | 12:55 | 217 | 1:20 |
| Picks and close | 12:55 | 14:30 | 251 | 1:35 |

Narration total 2,295 words, about 14:20 at 160 words per minute. Allow up to 14:30 finished with the title sting and end card.
