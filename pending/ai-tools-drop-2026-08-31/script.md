# AI Tools Drop  -  Video Script
## Episode 04  -  Week of 24 to 31 August 2026
**Measured runtime: 14:57 at 160 words per minute. Format: 16:9, 1920x1080, 30fps.**

---

## PRODUCTION NOTES

- Narration is written to be read aloud by ElevenLabs. Numbers appear longhand in NARRATION on purpose  -  the voice model mangles digits. ON-SCREEN TEXT uses digits. **Do not reconcile the two.**
- All ON-SCREEN TEXT is ASCII-only. No em dashes, no en dashes, no curly quotes, no ellipsis characters, no arrows. This prevents encoding corruption on Windows and PowerShell.
- No emoji anywhere, on screen or in narration.
- The AI-disclosure card is mandatory and non-negotiable. See the DISCLOSURE segment.
- Two honesty disclosures are structural to this episode and must not be cut for time: the incomplete Product Hunt coverage, and the four-way disagreement on the rand.

### ElevenLabs settings

| Setting | Value |
|---|---|
| Voice ID | `P1LmKcX63Ihgqy11sVRt` (Andrew, SA male) |
| Model | `eleven_multilingual_v2` |
| Stability | 0.60 |
| Similarity boost | 0.75 |
| Style | 0.15 |
| Speaker boost | true |
| Output format | `mp3_44100_128` |

**Voice decision still outstanding:** this reuses the E-Migration Assist voice. See BRIEF.md section 2 for the A/B decision.

### Pronunciation guide

| Written | Say it as |
|---|---|
| Telviva | tel-VEE-vah |
| Viva | VEE-vah |
| POPIA | poh-PEE-uh |
| Jotform | JOT-form |
| x1 | eks-ONE |
| Screenify | SCREEN-ih-fye |
| ify | IF-ee |
| MCP-Builder | em-see-pee BILL-der |
| Skydive | SKY-dive |
| Speko | SPEK-oh |
| Helply | HELP-lee |
| Lightfield | LIGHT-feeld |
| Qoder | KOH-der |
| n8n | en-EIGHT-en |
| diarization | dye-uh-rye-ZAY-shun |
| Ling | ling |
| Hy4 | hy-FOUR |
| Expo Go | EKS-poh go |
| TestFlight | TEST-flight |
| MEDDPICC | MED-pick |

---

## SEGMENT 1  -  COLD OPEN (0:00 to 0:28)

**NARRATION**

Neither OpenAI nor Anthropic launched a product this week. And yet the most useful thing that happened in artificial intelligence, for a South African business, happened in Johannesburg. A local company shipped a voice and WhatsApp agent hosted in South African data centres. That is the headline. But before I get to it, I owe you two admissions about this week's research, because one of them changes every rand figure I am about to give you.

**ON-SCREEN TEXT**

```
AI TOOLS DROP
Week of 24 - 31 August 2026

No OpenAI launch.
No Anthropic launch.
The best tool this week is South African.
```

**B-ROLL / VISUAL**

Cold open on the Joburg golden-hour skyline still (reuse A16 from episode 02 if cached). Slow Ken Burns push in. Title card cuts in hard at 0:12 on the beat of "That is the headline." Palette: bg #111111, accent #F5C542.

---

## SEGMENT 2  -  TWO ADMISSIONS (0:28 to 1:25)

**NARRATION**

First admission. Product Hunt's leaderboards would not load for four of the seven days in this window. So anything that launched in the last three days of August is very likely missing from this episode. That is a gap in my coverage, not a quiet week. I would rather tell you that than pad the list with old releases.

Second admission, and it matters more. There is no agreed price for the rand this week. Four sources gave me four answers, spanning nine point seven percent. Google Finance says seventeen point seven one. Wise says seventeen point one one. XE says sixteen point one seven, and Investing dot com agrees with XE within a hundredth. Every rand figure in this episode uses sixteen point one seven, because that is the only number with two independently dated sources agreeing. Use the dollar figure and your own bank's rate on the day.

**ON-SCREEN TEXT**

```
ADMISSION 1
Product Hunt boards failed on 26, 28, 29, 30 Aug.
Coverage is honest, not exhaustive.

ADMISSION 2
USD/ZAR quoted four ways this week.

XE            16.17  (30 Aug)
Investing     16.17  (28 Aug)
Wise          17.11  (undated)
Google        17.71  (25 Aug)

This episode uses 16.17
```

**B-ROLL / VISUAL**

Shotstack motion graphic. Admission 1 as a plain text block on #111111. Then wipe to the FX table, building row by row, 0.4s apart. XE and Investing rows highlight in accent #F5C542 as they land. Google Finance row flashes #E5533D once. Final line "This episode uses 16.17" scales up 8 percent and holds.

---

## SEGMENT 3  -  TELVIVA VIVA (1:25 to 2:47)

**NARRATION**

Number one, and the top pick of the week. Telviva Viva. Telviva is a South African cloud telephony provider, so it already owned the hard part. Viva is a digital agent in four tiers. Starter is a voice-only receptionist doing round-the-clock answering and routing. Business adds WhatsApp and web chat, answering from an uploaded FAQ. Professional connects to your CRM knowledge base. Enterprise does live lookups into your CRM or ERP, so a customer can ask what their balance is and get a real answer.

What makes it the pick is not the feature list. It is that the whole thing runs on locally hosted, POPIA-compliant infrastructure inside South African data centres, with private cloud options for financial services, healthcare and legal. No foreign card. No KYC wall. No US phone number. And it hands over to a human with the full conversation context carried across, which is what most agents get wrong.

Now the honest part. There is no published price. Anywhere. The only description of cost is a fixed monthly fee for unlimited simultaneous interactions. I fetched the vendor page and the press release; neither gives a figure. Telviva also claims more than forty percent of inbound volume resolved without a human, and that figure is vendor-reported and unaudited. Ask for a reference customer in your own sector.

**ON-SCREEN TEXT**

```
1. TELVIVA VIVA
Voice + WhatsApp agent. Built in SA.

STARTER        Voice receptionist, 24/7
BUSINESS       + WhatsApp and web chat
PROFESSIONAL   + your CRM knowledge base
ENTERPRISE     + live CRM / ERP lookups

WIN    Hosted in SA data centres. POPIA-ready.
WATCH  No published price. Anywhere.
CLAIM  40%+ resolution. Vendor-reported.

telviva.co.za
```

**B-ROLL / VISUAL**

Kling clip 1, 5 seconds: a Joburg office at dusk, a phone on a desk lighting up. Then Soul still B1 as a divider. Tier list builds as four stacked rows with accent-coloured labels. WATCH line in #E5533D. Close on the URL lower-third.

---

## SEGMENT 4  -  GEMINI 3.5 TRANSCRIBE (2:47 to 3:50)

**NARRATION**

Number two. Gemini three point five Transcribe went generally available on the twenty-sixth. Speech to text with automatic language detection, speaker diarization, word-level timestamps, and custom vocabulary biasing. That last one matters here more than most places, because generic speech recognition mangles South African names, and this lets you bias against that.

The price is the story. On the paid tier, Google's own blended figure is about half a US cent per minute. Roughly eight South African cents. An hour of recorded client audio, transcribed, with the speakers separated, costs you about five rand.

Here is the catch. On the free tier, Google's pricing page marks your content as used to improve our products. On the paid tier it marks that as no. For client audio that is a direct POPIA problem. Do not put an intake interview through the free tier to save eight cents a minute. Pay for it.

It is an API, not an app, so you need a developer to wire it up.

**ON-SCREEN TEXT**

```
2. GEMINI 3.5 TRANSCRIBE  (GA 26 Aug)
Speech to text with speakers separated.

PAID TIER   ~$0.005 / min blended
            ~R0.08 / min
            1 hour of audio = about R5

FREE TIER   Content "used to improve our products"
            Paid tier: No

VERDICT  Pay for it. Client audio is not worth 8 cents.
```

**B-ROLL / VISUAL**

Shotstack graphic only, no Kling needed. Waveform animation across the lower third while the price block builds. The FREE TIER warning block in #E5533D with a 0.3s shake on entry. VERDICT line holds 2 seconds.

---

## SEGMENT 5  -  JOTFORM AI DATA ASSISTANT (3:50 to 5:00)

**NARRATION**

Number three. Jotform's AI Data Assistant, out on the twenty-fifth. It sits inside Jotform Tables and lets you talk to your own form submissions. Turn them into tables, insights and charts, and speak the request instead of typing it. If your team already runs intake or quotes through Jotform, this is an upgrade with no migration.

The free tier is unusually well documented. Five active forms, one hundred submissions a month, a hundred megabytes of upload space. Published to the digit, which I respect. Bronze is thirty-nine dollars a month, about six hundred and thirty rand, billed in dollars.

But here is the thing. The AI Data Assistant does not appear on Jotform's pricing page at all. Not once. The product page publishes no price and no data-training statement. So no vendor page anywhere tells you what this costs or which plan includes it. And Jotform serves two different pricing pages depending on whether the URL has a trailing slash. One shows the amounts, one does not, and they disagree on how many users the company has.

Good product, probably. Read the data processing agreement first.

**ON-SCREEN TEXT**

```
3. JOTFORM AI DATA ASSISTANT  (25 Aug)
Talk to your form submissions.

FREE     5 forms, 100 submissions/mo, 100 MB
BRONZE   $39/mo  (about R631)
SILVER   $49/mo  (about R792)
GOLD     $129/mo (about R2,086)

WATCH  New product is absent from the pricing page.
WATCH  Two pricing pages. One has no amounts.
WATCH  No data-training statement published.
```

**B-ROLL / VISUAL**

Soul still B2 as a divider. Price ladder builds bottom to top. Then a split-screen motion graphic: left panel labelled "jotform.com/pricing" showing amounts, right panel labelled "jotform.com/pricing/" with the amounts struck through in #E5533D. Hold 2 seconds on the contradiction.

---

## SEGMENT 6  -  X1 (5:00 to 6:08)

**NARRATION**

Number four. x1, which the internet is calling Lovable for iPhone apps. It plans your screens and flows, designs the brand and layout, builds step by step, then prepares your App Store assets and handles release prep. The output is real React Native. You preview on your phone through Expo Go, run a beta through TestFlight, then submit.

The part that makes this worth your time is that paid plans export the full source code as a zip. That turns it from a walled garden into a head start. Build the first version yourself, then hand the code to a local developer.

Free tier is one hundred credits, no credit card, and the credits never expire. Paid plans are twenty, fifty and a hundred dollars a month, so entry is about three hundred and twenty rand.

Limitations. iPhone only, no Android path stated. You need an Apple Developer account to publish, which is a separate annual cost x1 does not cover. It is credit-based, so heavy iteration burns budget. And nothing on the page says whether it trains on your project data.

**ON-SCREEN TEXT**

```
4. X1 - AI APP STUDIO  (26 Aug)
Idea to App Store. Real React Native out.

FREE     100 credits. No card. Never expire.
PAID     $20 / $50 / $100 per month
         $20/mo = about R323

WIN    Paid plans export full source as a ZIP.
WATCH  iPhone only. No Android path.
WATCH  Apple Developer account required. Not included.

x1.new
```

**B-ROLL / VISUAL**

Kling clip 2, 5 seconds: hands holding a phone, an app interface assembling itself. Then Shotstack: the pricing block, then the WIN line sliding in from the left in accent #F5C542. WATCH lines in #E5533D, stacked.

---

## SEGMENT 7  -  SCREENIFY STUDIO 2.0 (6:08 to 7:15)

**NARRATION**

Number five, and this one has the cleanest data posture of the whole week. Screenify Studio two point oh, a native Mac cinematic screen recorder. Auto-zoom on clicks, cursor smoothing, three-dimensional device mockups, callouts, transitions, captions, voiceover.

The pitch is one sentence: nothing leaves your Mac unless you choose to share it. Captions run Whisper locally. Translation, background removal and smart clipping all run on the Apple Neural Engine. For an agency recording unreleased client screens, that is a genuine POPIA and non-disclosure win, not a marketing line.

It is also a one-time purchase, which beats a subscription when the rand is where it is. Free forever tier with a watermark and a five-minute export limit. Pro is a hundred and forty-nine dollars once, about two thousand four hundred rand.

Two things to know. It is Mac only. And the pricing page shows two prices for the same tier at once. Pro appears as a hundred and forty-nine and as an early-access price of a hundred and seventy-nine, simultaneously. Which one you pay is not resolvable from the page.

**ON-SCREEN TEXT**

```
5. SCREENIFY STUDIO 2.0  (26 Aug)
Cinematic Mac demos. Processed on-device.

FREE     $0 forever. 1080p, 5 min, watermarked.
PRO      $149 once  (about R2,409)
PRO+     $249 once  (about R4,026)

WIN    Nothing leaves your Mac. Whisper runs local.
WATCH  macOS only.
WATCH  Page shows TWO prices per tier at once.
       Pro: $149 and $179. Pro+: $249 and $299.
```

**B-ROLL / VISUAL**

Soul still B3 as divider. Then a Shotstack graphic showing a laptop outline with a padlock icon and the words "on-device" pulsing gently. For the double-pricing beat: show $149 and $179 side by side, both in #E5533D, with a question mark between them. Hold 2 seconds.

---

## SEGMENT 8  -  IFY (7:15 to 8:18)

**NARRATION**

Number six. A tool called ify, spelled i-f-y. It is a resolution layer that sits on top of the helpdesk you already have, whether that is Freshdesk, Zendesk, Salesforce or HubSpot, and works across email, chat, WhatsApp and Slack. It builds its own knowledge base by reading your sites and documentation.

That is the right design. The single biggest reason small businesses never adopt support AI is that it demands a helpdesk migration, and this one does not. WhatsApp as a first-class channel is the correct call for this market.

Then you get to the pricing page, and the pricing page has no price. Agents are zero dollars, seats are zero dollars. And for the only thing actually billed, resolved tickets, it says talk to us for a rate. So you cannot budget before a sales call. Worse, a resolution counts whether the AI closed it or one of your own people did. You pay either way.

No statement on data privacy or training anywhere on that page.

**ON-SCREEN TEXT**

```
6. IFY  (26 Aug)
Resolution AI on the helpdesk you already have.

WORKS WITH   Freshdesk, Zendesk, Salesforce, HubSpot
CHANNELS     Email, chat, WhatsApp, Slack

PER AGENT    $0
PER SEAT     $0
RESOLVED TICKET  "Talk to us for a rate"

WATCH  A pricing page with no price on the billed unit.
WATCH  You pay even when a human resolves it.
```

**B-ROLL / VISUAL**

Shotstack only. The three-line price block builds; the third line lands and the "Talk to us for a rate" text flashes #E5533D twice. No Kling clip here, keep the cost down.

---

## SEGMENT 9  -  MCP-BUILDER (8:18 to 9:22)

**NARRATION**

Number seven. MCP-Builder dot AI. You describe your use case, and it builds, secures and hosts a production MCP server that your AI tools reach at a single URL. It connects modern APIs, legacy databases, ERP systems and storage to Claude, ChatGPT, Copilot, Cursor, Gemini, Perplexity, n8n and Zapier.

This solves the hardest step in small-business AI adoption, which is getting an assistant to safely read the ugly system your business actually runs on. And its data posture is unusually strong for a launch-week tool. No data stored on the server. Data read at request time and forwarded, not persisted. Full audit logs on every tool call. European hosting and residency available, and an on-premise option.

Now the catch. No free tier. Entry is twenty-nine dollars a month, about four hundred and seventy rand, and that tier allows one hundred requests a month. One hundred. That is a demo allowance, not a working one, and requests count per account, not per server. Also, the residency is European, not South African.

**ON-SCREEN TEXT**

```
7. MCP-BUILDER.AI  (26 Aug)
Your legacy system, reachable by your AI tools.

LAUNCH   $29/mo   1 server, 100 requests/mo
PRO      $75/mo   3 servers, 1,000 requests/mo
SCALE    $290/mo  20 servers, 100,000 requests/mo

WIN    No data stored. EU residency. On-prem option.
WATCH  No free tier.
WATCH  100 requests/mo is a demo, not a workload.
```

**B-ROLL / VISUAL**

Kling clip 3, 5 seconds: a server rack with cables, slow dolly past. Then Shotstack: the tier table, with the "100 requests/mo" cell highlighted in #E5533D and a small annotation reading "per account, not per server".

---

## SEGMENT 10  -  SKYDIVE (9:22 to 10:26)

**NARRATION**

Number eight. Skydive, the top launch of the twenty-seventh. Cloud agents that work across your tools. The pricing model is the interesting part: your subscription fee converts one for one into a dollar credit balance, and the agents spend that balance on model usage and sandbox time.

Model usage is passed through at cost. You can set a monthly cap at any time. And pay-as-you-go workspaces have no overdraft cushion, which means the agent stops rather than running up a bill. For a business earning rands and spending dollars, a hard stop is worth more than a discount. Free workspace is zero dollars, no card, two seats. Starter is twenty dollars a month, about three hundred and twenty rand.

Which is also the limitation. Twenty dollars of agent work is not much if you are running anything serious. No privacy or training statement in the pricing docs. And Skydive appears to have launched twice in eight days under two different taglines, so treat this as a feature release, not something brand new.

**ON-SCREEN TEXT**

```
8. SKYDIVE  (27 Aug)
Cloud agents with a hard spend cap.

FREE      $0/mo. No card. 2 seats.
STARTER   $20/mo = $20 of credit (about R323)
TEAM      $200/mo = $200 of credit (about R3,234)

WIN    Model cost passed through AT COST.
WIN    No overdraft. Agents stop, not spend.
WATCH  The fee IS the credit.
WATCH  Second launch in 8 days.
```

**B-ROLL / VISUAL**

Shotstack only. Animate a budget bar filling to full and then stopping hard at the cap line, with a small "STOP" label. That single animation carries the segment.

---

## SEGMENT 11  -  SPEKO (10:26 to 11:30)

**NARRATION**

Number nine. Speko, which calls itself OpenRouter for voice. A hosted, provider-neutral router in front of speech-to-text, language models and text-to-speech, plus an open client-side runtime for LiveKit and Pipecat with your own keys held locally.

The reason it is on this list is per-language benchmarking. It publishes word error rate next to price per minute across sixteen speech models, thirteen language models and twenty-two voice models. In a multilingual country, that is the axis that matters. And on its own table the spread on the same transcription task runs seventeen times from cheapest to most expensive.

Pricing is a flat nine cents a minute all in, about one rand forty-six, or you route to providers and pay their rate plus five percent. No free tier, but every account gets a hundred dollars of signup credit.

Two warnings. Both tiers are in public preview with no service level agreement. And I found no page confirming the benchmarks cover isiZulu, Afrikaans or South African English. Test it on your own audio first.

**ON-SCREEN TEXT**

```
9. SPEKO  (27 Aug)
One API in front of every speech model.

SPEKO INFRA   $0.09 / min all-in (about R1.46)
ROUTER        Provider rate + 5%
SIGNUP        $100 credit. No free tier.

WIN    Word error rate published per model.
WIN    Same task: $0.0010/min to $0.0170/min. 17x.
WATCH  Public preview. No SLA.
WATCH  No proof the benchmarks cover SA languages.
```

**B-ROLL / VISUAL**

Soul still B6 as divider. Then a Shotstack bar chart animating the 17x price spread between the cheapest and most expensive model. Two bars only, labelled with the rates. Keep it simple.

---

## SEGMENT 12  -  HELPLY (11:30 to 12:35)

**NARRATION**

Number ten, and this is the one I would be careful with. Helply. An AI-native helpdesk charging one dollar per ticket with unlimited free seats. Every ticket includes an AI teammate that resolves, escalates, detects churn and generates documentation.

The arithmetic is clean and I like clean arithmetic. Pricing that scales with your customers instead of your headcount is genuinely useful when your staff cost is in rands and your software cost is in dollars.

Then you read the floor. Minimum two hundred and fifty tickets a month, so two hundred and fifty dollars a month whether you have the volume or not. About four thousand rand. And the minimum annual contract is three thousand dollars, roughly forty-eight and a half thousand rand committed before you know whether the AI resolves anything at all. Any customer conversation processed counts as a ticket, so the meter is broad.

If your monthly volume is not comfortably above two hundred and fifty, this is a seat-based helpdesk with extra steps. Run your own numbers first.

**ON-SCREEN TEXT**

```
10. HELPLY  (24 Aug)
$1 per ticket. Unlimited free seats.

PER TICKET     $1
MINIMUM        250 tickets/mo = $250/mo
               about R4,042 / month
ANNUAL FLOOR   $3,000  (about R48,510)

WIN    Scales with customers, not headcount.
WATCH  You pay the floor whether you use it or not.
WATCH  Any conversation counts as a ticket.
```

**B-ROLL / VISUAL**

Shotstack only. Show a ticket counter climbing from 0 to 250 and stopping, with the cost line staying pinned at $250 the whole way up. That visual makes the floor obvious without narration explaining it twice.

---

## SEGMENT 13  -  ALSO THIS WEEK (12:35 to 13:39)

**NARRATION**

Four quick ones. Gemini Omni Flash went generally available on the twenty-seventh. Video generation, paid tier only, at roughly six dollars a minute of seven-twenty video. A thirty-second clip is three dollars before you iterate. Agency tool, not a small-business tool.

Lightfield launched an AI-native CRM on the twenty-sixth. Pro is a thousand dollars a month, but its own FAQ says to budget about fourteen hundred and fifty dollars per month per active seller. Roughly twenty-three thousand rand per seller. Priced out of this market.

ChatGPT shipped better control over temporary chats on the twenty-seventh. A non-personalised temporary chat uses no memory, no custom instructions and no plugins, and creates no memories. The closest thing to a clean-room mode for client data.

And the best free thing this week is in Vercel's changelog. Ling three point oh Flash Fin is free on their AI Gateway until the twenty-fifth of September, through a model ID that stops serving rather than billing you when the allowance runs out. A hard budget guarantee. Take it.

**ON-SCREEN TEXT**

```
ALSO THIS WEEK

GEMINI OMNI FLASH   GA 27 Aug. ~$6/min of video.
                    No free tier. Agency budget only.

LIGHTFIELD CRM      $1,000/mo Pro.
                    Own FAQ: ~$1,450/mo PER SELLER.
                    About R23,447 per seller.

CHATGPT             Temporary chat controls, 27 Aug.
                    No memory, no plugins, no traces.

VERCEL AI GATEWAY   Ling 3.0 Flash Fin FREE to 25 Sept.
                    Stops serving, does not bill.
```

**B-ROLL / VISUAL**

Rapid-fire Shotstack cards, one per item, 12 seconds each, hard cuts. No Kling. The Vercel card gets the accent colour and a slightly longer hold, since it is the actionable one.

---

## SEGMENT 14  -  WHAT I WOULD ACTUALLY TRY (13:39 to 14:32)

**NARRATION**

So. What would I actually do this week.

First, get a quote from Telviva for Viva. It is the only tool on this list built for the channels South African customers actually use, hosted inside the country, by a vendor that already owns local telephony. Go in knowing there is no published price, and ask for the fixed monthly fee across all four tiers in writing.

Second, put Gemini three point five Transcribe on the paid tier to work. At eight cents a minute there is no excuse for a professional practice not to have a proper record of every client call. Pay for it. The free tier trains on your content.

And one to be careful with: Helply. Run your ticket volume through the arithmetic before you commit forty-eight thousand rand a year to a floor you might not fill.

**ON-SCREEN TEXT**

```
WHAT I WOULD ACTUALLY TRY

1. TELVIVA VIVA
   Get the quote. Ask for all four tiers in writing.

2. GEMINI 3.5 TRANSCRIBE  (paid tier)
   R0.08/min. No excuse not to record client calls.

CAREFUL WITH
   HELPLY. R48,510/year floor before proof.
```

**B-ROLL / VISUAL**

Clean Shotstack summary card on #111111. Items 1 and 2 in accent #F5C542. The CAREFUL WITH block in #E5533D, separated by a thin rule. Hold the full card for 4 seconds at the end of the segment.

---

## SEGMENT 15  -  DISCLOSURE (14:32 to 14:42)

**NARRATION**

This video was produced with AI-generated visuals and an AI voice. The research, the prices and the warnings are mine, checked against the vendors' own pages.

**ON-SCREEN TEXT**

```
AI DISCLOSURE

Visuals: AI-generated.
Voice: AI-generated.
Research, pricing and analysis: human-verified
against vendor pages on 31 August 2026.
```

**B-ROLL / VISUAL**

Full-frame card, `style: "future"`. Static, no motion. Must be on screen for a minimum of five seconds and must not be cut for runtime. This card is also required at upload time via each platform's own AI-content disclosure setting.

---

## SEGMENT 16  -  CLOSE AND CTA (14:42 to 14:57)

**NARRATION**

That is the week. Ten tools, one local winner, and a rand nobody can agree on. The full written breakdown with every price and every source link is on the WhatsApp channel. Join it, and I will see you next Monday.

**ON-SCREEN TEXT**

```
AI TOOLS DROP
Every Monday.

Full written breakdown, all prices, all sources:
WhatsApp channel link in the description.

Next episode: Monday 7 September 2026.
```

**B-ROLL / VISUAL**

Return to the Joburg skyline still, now at night. Slow pull back. End card holds 6 seconds with the channel link lower-third. Fade to #111111.

---

## SEGMENT TIMING SUMMARY

*Measured from actual narration word counts at 160 words per minute on 31 August 2026. Headings above are in sync with this table. Re-measure with the script in BRIEF.md section 9 if you edit any narration.*

| Segment | Timecode | Narration words |
|---|---|---:|
| 1. COLD OPEN | 0:00 - 0:28 | 76 |
| 2. TWO ADMISSIONS | 0:28 - 1:25 | 150 |
| 3. TELVIVA VIVA | 1:25 - 2:47 | 220 |
| 4. GEMINI 3.5 TRANSCRIBE | 2:47 - 3:50 | 167 |
| 5. JOTFORM AI DATA ASSISTANT | 3:50 - 5:00 | 186 |
| 6. X1 | 5:00 - 6:08 | 182 |
| 7. SCREENIFY STUDIO 2.0 | 6:08 - 7:15 | 179 |
| 8. IFY | 7:15 - 8:18 | 168 |
| 9. MCP-BUILDER | 8:18 - 9:22 | 170 |
| 10. SKYDIVE | 9:22 - 10:26 | 172 |
| 11. SPEKO | 10:26 - 11:30 | 171 |
| 12. HELPLY | 11:30 - 12:35 | 172 |
| 13. ALSO THIS WEEK | 12:35 - 13:39 | 172 |
| 14. WHAT I WOULD ACTUALLY TRY | 13:39 - 14:32 | 141 |
| 15. DISCLOSURE | 14:32 - 14:42 | 26 |
| 16. CLOSE AND CTA | 14:42 - 14:57 | 41 |
| **TOTAL** | **14:57** | **2,393** |
