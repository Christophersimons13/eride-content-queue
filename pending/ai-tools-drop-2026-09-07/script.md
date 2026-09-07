# AI Tools Drop - Video Script, Week of 7 September 2026

**Episode 5. Long form, 16:9, 1920x1080, 30fps.**
Target runtime 14 to 15 minutes at 160 words per minute.

## Production notes

- Voice: ElevenLabs, voice ID `P1LmKcX63Ihgqy11sVRt` (Andrew, South African male), model `eleven_multilingual_v2`.
- Settings: stability 0.60, similarity_boost 0.75, style 0.15, use_speaker_boost true, output `mp3_44100_128`.
- Render narration one segment per API call. Do not batch the whole script into one request - a single mispronunciation then costs one segment, not the episode.
- ON-SCREEN TEXT blocks are ASCII-only. No em dashes, no en dashes, no curly quotes, no ellipsis characters, no arrows. Run `ascii_fix.py` before handing to Shotstack.
- Numbers are written longhand in NARRATION so the voice model reads them correctly, and as digits in ON-SCREEN TEXT. This mismatch is deliberate. Do not reconcile them.
- SEGMENT 16 is the AI disclosure. It must hold on screen for a minimum of five seconds and must not be cut for runtime.

## Pronunciation guide

| Written | Say it as |
| --- | --- |
| Gemini | JEM-in-eye |
| ThunderPhone | THUN-der-fone |
| Syspro | SIS-pro |
| Torque | TORK |
| Tajima | tah-JEE-mah |
| DST | dee-ess-tee |
| MagiCrew | MAJ-ee-crew |
| Tadata | tah-DAH-tah |
| Fotor | FOH-tor |
| Lyria | LEER-ee-ah |
| Mythos | MY-thoss |
| Fable | FAY-bul |
| Astra | ASS-trah |
| POPIA | poh-PEE-uh |
| n8n | en-EIGHT-en |
| MCP | em-see-pee |
| CVE | see-vee-ee |
| DigitalOcean | DIJ-it-al OH-shun |
| Frankfurt | FRANK-furt |
| Apache | uh-PATCH-ee |
| ZDR | zed-dee-arr |
| SIP | sip |
| Vulavula | voo-lah-VOO-lah |
| Lelapa | leh-LAH-pah |
| isiZulu | iss-ee-ZOO-loo |

## Timing table

| Segment | Title | Start | End |
| --- | --- | --- | --- |
| 1 | Cold open | 0:00 | 0:31 |
| 2 | What kind of week this was | 0:31 | 1:26 |
| 3 | Gemini 3.8 Flash | 1:26 | 2:26 |
| 4 | ThunderPhone | 2:26 | 3:24 |
| 5 | Syspro Torque | 3:24 | 4:24 |
| 6 | Stitch AI | 4:24 | 5:26 |
| 7 | Claude Fable 5.1 | 5:26 | 6:23 |
| 8 | GPT-6 Astra | 6:23 | 7:24 |
| 9 | Tadata | 7:24 | 8:21 |
| 10 | AI Toolbox 3.0 | 8:21 | 9:22 |
| 11 | MagiCrew | 9:22 | 10:20 |
| 12 | Video Agent by Fotor | 10:20 | 11:17 |
| 13 | The short list | 11:17 | 12:16 |
| 14 | Did not launch this week | 12:16 | 13:11 |
| 15 | What I would actually try | 13:11 | 14:20 |
| 16 | AI disclosure | 14:20 | 14:34 |
| 17 | Close | 14:34 | 15:10 |

---

## SEGMENT 1 - Cold open (0:00 to 0:31)

**NARRATION**

OpenAI released a model this week and rated it Critical for cyber capability. Their own safety document says it finds security flaws nobody knew about and builds working attacks, without a person guiding it. That is not a product feature. That is a change to your threat model. Also this week: a model at twelve rand per million tokens, a voice agent at thirty-two cents a minute that switches to isiZulu mid-call, and exactly one launch built in South Africa. Let us go.

**ON-SCREEN TEXT**

```
AI TOOLS DROP
Week of 7 September 2026

Rated CRITICAL for cyber
```

**B-ROLL / VISUAL**

Kling clip: slow push into a dark server aisle, single amber indicator pulsing. Cut to warning-red full-frame title card at 0:12. Palette bg #111111, accent #F5C542, warning #E5533D for the word CRITICAL.

---

## SEGMENT 2 - What kind of week this was (0:31 to 1:26)

**NARRATION**

Right, framing, and two admissions before I sell you anything. This was a frontier-model week. Google, OpenAI and Anthropic all shipped, and the small-tool launches were thinner than usual. Ten items made the shortlist. Admission one: the rand rate. I priced everything at fifteen rand ninety-seven, the live rate on Saturday. But the public sources disagreed by eleven percent this week, one of them showing seventeen seventy-one off a stale August stamp. If you are quoting a client, pull your own rate. I round to sixteen rand for mental maths. Admission two, and this one is structural. Across all ten tools on this list, not one vendor mentions POPIA anywhere in their documentation. Not one. So every data-handling answer I give you today is inferred from privacy language written for Europe. That is the honest state of it, and it is worth knowing before you sign anything.

**ON-SCREEN TEXT**

```
THIS WEEK
10 tools shortlisted
FX used: R15.97 / USD

Source spread: 11 percent
Pull your own rate

POPIA mentions across
all 10 vendors: ZERO
```

**B-ROLL / VISUAL**

Shotstack motion graphic: three rate quotes stacking, the outlier 17.7101 struck through in warning red. Then a ten-row vendor list with a POPIA column, every cell filling with a red dash. Hold the zero count three seconds.

---

## SEGMENT 3 - Gemini 3.8 Flash (1:26 to 2:26)

**NARRATION**

Top pick, and it is a boring one on purpose. Gemini three point eight Flash, out on the second of September. Seventy-five US cents per million input tokens, three dollars seventy-five out. Call it twelve rand in, sixty rand out. There is a free tier that is actually free, not a trial. But the reason it is my pick is one row on the pricing page. The row is headed, used to improve our products. Free tier: yes. Paid tier: no. That is the clearest statement of the free-versus-paid data bargain any major vendor publishes, and it is the line that lets you tell a client whether their file trains somebody's model. Two catches. Search grounding is not on the free tier. And that price is promotional through December, then it doubles on the first of January. Build your model on one dollar fifty. No African residency, and their terms say data may be cached in any country.

**ON-SCREEN TEXT**

```
GEMINI 3.8 FLASH
Google - 2 September

R12 in / R60 out per 1M tokens

Used to improve our products
Free tier: YES
Paid tier: NO

Price doubles 1 Jan 2027
Model on $1.50, not $0.75
```

**B-ROLL / VISUAL**

Soul still B1 with Ken Burns push. At 2:20 cut to a clean recreation of the pricing table row, the words Paid Tier: No highlighted in accent yellow, held four seconds. Then a two-bar cost graph, 2026 versus 2027, second bar double height.

---

## SEGMENT 4 - ThunderPhone (2:26 to 3:24)

**NARRATION**

ThunderPhone, first of September, fourteenth on Product Hunt that day. Voice AI agents at two US cents a minute on the entry tier. Thirty-two South African cents. Roughly nineteen rand for an hour of talk time. And here is why it lands harder here than almost anywhere: forty-plus languages, including switching language mid-call. We have twelve official languages and a phone that nobody answers after five. An agent that starts in English and moves to isiZulu when the caller does is not a demo trick in this market. Two honest problems. No free tier, you pay from minute one. And that two cents is a floor, not a price. Verbal acknowledgement adds two cents, supervision adds eight, premium voices three, text-to-speech another three. A fully-loaded agent costs more than double the headline. Hosting location is not stated anywhere on their security or privacy pages. For recorded customer calls, ask them directly before you go live.

**ON-SCREEN TEXT**

```
THUNDERPHONE
1 September - PH #14

R0.32 per minute
R19 per hour of talk time

40+ languages
Switches mid-call

No free tier
Add-ons can double it
Hosting location: NOT STATED
```

**B-ROLL / VISUAL**

Kling clip: an empty reception desk, phone ringing, nobody there. Then Shotstack stacked-bar graphic showing base price 0.02 growing to 0.18 as each add-on stacks in, each one labelled.

---

## SEGMENT 5 - Syspro Torque (3:24 to 4:24)

**NARRATION**

The only South African launch this week. Syspro, headquartered in Johannesburg, launched Torque on the second. No-code AI agents that act inside a manufacturing ERP, not beside it giving advice. They call the logging the Glass House: every action recorded with the rule that fired, the data it used, and why. Plus an upfront cost estimate per workflow. In a factory that has to explain a decision to an auditor, that logging is the entire product. Now the honest part. No published price at all, they say usage-based and stop there. Not generally available, it is controlled release, and you need Syspro eight, twenty-twenty-six R one. And this is the bit worth hearing: despite the Johannesburg head office, there is no African data residency. Their privacy policy says data may go outside your country, such as the United States. A South African company selling to South African manufacturers, routing the data offshore. Do not assume a local vendor means local data.

**ON-SCREEN TEXT**

```
SYSPRO TORQUE
Johannesburg - 2 September
The only SA launch this week

Glass House logging
Every action: rule, data, why

No published price
Not generally available
Needs Syspro 8 2026 R1

SA head office
NO African data residency
```

**B-ROLL / VISUAL**

Soul still A16, the Johannesburg skyline, Ken Burns pull back. Cut to a factory-floor Kling clip. At 5:00 a map graphic: a pin on Johannesburg, an arrow leaving for a US pin, the arrow in warning red.

---

## SEGMENT 6 - Stitch AI (4:24 to 5:26)

**NARRATION**

Narrow, but if it is your trade it is the best value on the page. Stitch AI by Dynamic Mockups, second of September, twelfth on Product Hunt. Embroidery digitising. You feed it artwork and fifteen seconds later you have a photoreal mockup, a Tajima DST stitch file, a production sheet and a stitch count. Manual digitising costs ten to fifty dollars per design. The desktop software costs one hundred to three thousand. This is free right now, no card. If you supply school or corporate uniforms, that is the difference between quoting on the call and quoting in two days. It also has the best data disclosure on this list: processing in the EU, or other regions where AWS operates. A real answer. Caveats: free with no expiry stated is a launch price, and the parent product's Pro tier is fifteen dollars, so about two hundred and forty rand is probably where it lands. And nothing states whether your client's logo trains their model.

**ON-SCREEN TEXT**

```
STITCH AI
Dynamic Mockups - 2 September

Artwork to DST file: 15 seconds
Mockup + stitch count + sheet

Replaces:
$10-50 per design manual
$100-3,000 software

FREE right now, no card
Processing: EU or AWS regions
```

**B-ROLL / VISUAL**

Kling clip: embroidery machine head moving fast across fabric. Then a split-screen wipe, flat logo on the left, stitched mockup on the right. A cost-comparison graphic, two tall bars beside a zero bar in accent yellow.

---

## SEGMENT 7 - Claude Fable 5.1 (5:26 to 6:23)

**NARRATION**

Anthropic, first of September. Claude Fable five point one, with Mythos alongside it. One million tokens of context by default, one hundred and twenty-eight thousand out. A full contract set in one pass without chunking. But the number that matters commercially is the cache read: twenty-five US cents per million tokens, seventy-five percent below the old rate. Four rand per million. If your product re-reads the same big document across many queries, which is what a compliance or document-review tool does, your cost profile just changed. Input ten dollars, output fifty. Two things to know. Mythos five point one is restricted to United States organisations, so half the launch is not available to you. And there is a breaking change: tool choice set to any or tool now returns a four hundred error. Check your integrations before upgrading. If Anthropic will not take your card, Fable is on Bedrock, Google Cloud and Foundry.

**ON-SCREEN TEXT**

```
CLAUDE FABLE 5.1
Anthropic - 1 September

1M context as standard
128k output

Cache read: R4 per 1M
Down 75 percent

Mythos 5.1: US orgs only
BREAKING: tool_choice any/tool
now returns 400
```

**B-ROLL / VISUAL**

Shotstack graphic: a document stack growing tall, a bracket labelled 1,000,000 tokens closing around all of it. Then the cache price dropping, old figure crossed out in red, new figure landing in accent yellow.

---

## SEGMENT 8 - GPT-6 Astra (6:23 to 7:24)

**NARRATION**

The warning item, and the warning is not about the price. GPT-six Astra, third of September. It builds documents, spreadsheets and decks from your templates, which is the headline. It is also OpenAI's first model rated Critical for cyber capability under their own framework. Their safety overview says it finds previously unknown security flaws and develops new ways to exploit them across many well-protected systems, without a person guiding each step. Read that as a defender, not a buyer. The capability OpenAI is gating is the same capability that turns up in less careful hands. If your security thinking assumes that finding a novel flaw in your stack needs a skilled human spending weeks, that assumption has a shorter shelf life than it did last month. The response for a small business is unglamorous. Patch faster. Multi-factor everywhere. Know what you have exposed to the internet. On the product: ten dollars in, fifty out, promotional with no expiry. Limited rollout. No African region.

**ON-SCREEN TEXT**

```
GPT-6 ASTRA
OpenAI - 3 September

FIRST model rated
CRITICAL for cyber

Finds unknown flaws
Builds exploits
No human guiding each step

Do this week:
Patch. MFA. Audit exposure.
```

**B-ROLL / VISUAL**

Hold the words CRITICAL FOR CYBER full frame in warning red for four seconds, no motion. Then Kling clip: a padlock icon assembling then dissolving. Close on a three-item checklist card ticking in one line at a time.

---

## SEGMENT 9 - Tadata (7:24 to 8:21)

**NARRATION**

Tadata, sixth of September, second on Product Hunt. An AI employee that lives in Slack. Morning brief, drafts your follow-ups. The thing I actually like is the default: their own copy says nothing is sent until you approve it. For a tool holding your inbox, that is the correct default and it is not the default everywhere. Where it gets thin: the free offer is fifty dollars or one thousand credits, one time only. That is a trial, not a free tier. After it, thirty-nine dollars a month for Lite, one hundred and forty-nine for Pro. Six hundred and twenty-three rand, or two thousand three hundred and eighty. And what a credit buys is not defined anywhere, so you cannot forecast your spend before you commit. Hosting not stated. Worth it only if you already live in Slack and your pipeline is worth more than six hundred rand a month of tooling.

**ON-SCREEN TEXT**

```
TADATA
6 September - PH #2

Slack AI employee
Morning brief + draft replies
Nothing sent until you approve

Free: $50 one time only
Then R623 to R4,775 / month
Credit value: UNDEFINED
```

**B-ROLL / VISUAL**

Shotstack mock Slack panel, a morning brief typing in, then an approval dialog with Approve and Discard buttons. Then a pricing ladder, four rungs in rand, with a question mark over the credit unit.

---

## SEGMENT 10 - AI Toolbox 3.0 (8:21 to 9:22)

**NARRATION**

Best data disclosure of the week, and it wins on one sentence. AI Toolbox three point oh, sixth of September, number one on Product Hunt. It is a browser extension that adds folders, search and export across ChatGPT, Gemini, Claude and Grok. If you use AI for client work, your chat history is a working record with no filing system. This gives you one, across four platforms. And their privacy policy says plainly: servers hosted with DigitalOcean in Frankfurt, Germany. Naming the provider and the city is more than almost anyone on this list manages. Read the fine print though. That Frankfurt line covers the ChatGPT module only, and it is weaker for the other three. It is priced per module: ten dollars a month each, fifty-nine a year, ninety-nine lifetime, or one hundred and ninety-nine for all access lifetime. Three thousand one hundred and seventy-eight rand for everything, forever, as a single exchange-rate hit rather than a monthly one. Chromium browsers only.

**ON-SCREEN TEXT**

```
AI TOOLBOX 3.0
6 September - PH #1

Folders, search, export across
ChatGPT, Gemini, Claude, Grok

Servers: DigitalOcean, Frankfurt
Best disclosure this week

Per MODULE pricing
All Access Lifetime: R3,178
Chromium only
```

**B-ROLL / VISUAL**

Screen-capture style graphic: a chaotic chat sidebar reorganising into labelled folders. Then a map pin on Frankfurt in accent yellow, held three seconds. Then a per-module grid so the pricing structure reads at a glance.

---

## SEGMENT 11 - MagiCrew (9:22 to 10:20)

**NARRATION**

MagiCrew, third of September, third on Product Hunt. An open-source multi-agent platform, Apache licensed. It does one thing nothing else on this list can do: you can run it on infrastructure you control. If a client contract or a POPIA assessment says the data does not leave a machine you own, this is the only tool today that gives you a path. Everything else on this page routes offshore. The caveats are real. Paid tiers are ten, twenty-five, fifty and one hundred dollars, and the entry tier is sixty-six percent off a twenty-nine dollar price with no expiry, which makes that list price fictional. No free tier on the pricing page. Points are the billing unit and are undefined. The demo interface shows yuan, so the primary market is probably Chinese. And it is a Product Hunt launch of an existing project, with repository activity going back through last year. Not new. Arguably reassuring.

**ON-SCREEN TEXT**

```
MAGICREW
3 September - PH #3

Apache licensed, self-hostable
The only real residency answer

Run it on hardware you own

No free tier on pricing page
Points: UNDEFINED
Demo UI shows yuan
Existing project, not new code
```

**B-ROLL / VISUAL**

Shotstack graphic: nine tool logos with arrows leaving South Africa offshore, then one arrow that loops back and stays inside the border. Hold that contrast four seconds. Then a terminal window with a git clone line.

---

## SEGMENT 12 - Video Agent by Fotor (10:20 to 11:17)

**NARRATION**

Biggest community response of the week and I cannot tell you what it costs. Video Agent by Fotor, thirty-first of August, number one on Product Hunt with three hundred and seventy-seven upvotes. AI video generation, beta, web only. The free plan gives you fifty agent chats and one task, enough to judge whether the output clears your quality bar. Now the strange part. Fotor's own pricing page renders no readable price. Dashes where numbers should be, and a literal unrendered credits placeholder in the markup. The only figures I have are second-hand from a review site, nine dollars and twenty dollars, and I am labelling those unconfirmed because they are. Worse, their privacy policy returned a four-oh-three error on two attempts. I am not saying it is bad. I am saying I could not read it, and you should not upload client footage to a service whose privacy terms will not open.

**ON-SCREEN TEXT**

```
VIDEO AGENT BY FOTOR
31 August - PH #1, 377 upvotes

Free: 50 agent chats, 1 task
Watermarked output

Pricing page renders no price
Only second-hand figures exist

Privacy policy: 403 error
Data posture UNVERIFIED
```

**B-ROLL / VISUAL**

Screen recording style: a pricing page with empty skeleton rows and visible dashes. Then a browser error card reading 403 in warning red, held three seconds.

---

## SEGMENT 13 - The short list (11:17 to 12:16)

**NARRATION**

Six quick ones. Dial, a rival phone product at three dollars a month per number plus thirteen to twenty-two cents a minute. Seven times ThunderPhone's floor, no free tier, and its headline iMessage integration is close to useless in an Android-majority market. Skip it. Lyria three point five, Google's music model, updated on the third. Royalty-free background audio for social video. Agentic video understanding shipped on the first, cutting token use on long video by about eighty-eight percent. The unglamorous local application is reviewing hours of retail or warehouse camera footage without the cost being absurd. Then the housekeeping, and this is the most actionable thing on the page. n8n shipped bug-fix releases between the first and the fourth, including a fix for two CVEs. If you self-host n8n, patch it this week. ChatGPT added Zendesk and OneNote plugins in beta. And CleanShot five is a good screenshot tool that is Mac only, so limited use here.

**ON-SCREEN TEXT**

```
ALSO THIS WEEK

Dial - 7x the price, skip it
Lyria 3.5 - music generation
Video understanding - 88% fewer
  tokens on long footage

n8n 2.37 / 2.38
Two CVEs fixed
PATCH IT THIS WEEK

ChatGPT - Zendesk, OneNote
CleanShot 5 - Mac only
```

**B-ROLL / VISUAL**

Fast six-card sequence, roughly eight seconds each. Hold the n8n card longest, in warning red, with PATCH IT THIS WEEK at full width.

---

## SEGMENT 14 - Did not launch this week (12:16 to 13:11)

**NARRATION**

Three things people are calling new that are not, because saying so is the point of doing this weekly. Refiant Protea, a South African-founded model line with a ten-million-token context window, is circulating as fresh. Their own announcement is dated the eighth of July. A recycled index page made it look current. Framer AI Agents, actually the sixteenth of June. And Stratos Lab, ECOBLOX and Digital Parks Africa announced what they call Africa's most powerful AI cloud on the twenty-sixth of August. Five days outside my window, so it does not qualify today. But given that nine of the ten tools I just covered route your data offshore, African compute deserves a proper segment, and I will do that one. Last: Lelapa AI and Vulavula, the South African multilingual speech work, kept surfacing and I could not date-verify a release inside this window. So it stays off.

**ON-SCREEN TEXT**

```
NOT NEW THIS WEEK

Refiant Protea - 8 July
Framer AI Agents - 16 June
Africa AI Cloud - 26 August
  (5 days outside window)

Could not date-verify:
Lelapa AI / Vulavula
```

**B-ROLL / VISUAL**

Calendar graphic with the 31 August to 7 September window highlighted in accent yellow, three date pins falling clearly outside it in grey. Understated, no drama.

---

## SEGMENT 15 - What I would actually try (13:11 to 14:20)

**NARRATION**

Two things, and one thing to do rather than buy. One: Gemini three point eight Flash, on the paid tier. Not the most exciting thing that shipped, but the one where the numbers work and the data answer is written down. Twelve rand per million input tokens, and a pricing table stating that paid-tier data is not used to improve their products. Move one real workload across. Document classification, message triage, catalogue text. And price it at the January rate of one dollar fifty, not the promotional seventy-five cents. Two: AI Toolbox, free tier first, because it fixes a problem you have not named. Your AI chat history is a client record with no filing system. Test it a week on real work. If it holds, all access lifetime at one hundred and ninety-nine dollars is a single exchange-rate hit, not a subscription. And the thing to do rather than buy: if you self-host n8n, patch it. Two CVEs fixed the same week OpenAI shipped a model rated Critical for finding novel exploits on its own. Those two facts belong in the same sentence.

**ON-SCREEN TEXT**

```
WHAT I WOULD TRY

1. Gemini 3.8 Flash, paid tier
   Model it at $1.50, not $0.75

2. AI Toolbox, free tier first
   Then R3,178 lifetime if it holds

DO, DO NOT BUY:
Patch your self-hosted n8n
```

**B-ROLL / VISUAL**

Three numbered cards, clean, accent yellow numerals, one at a time with a short hold on each. No stock footage. Let the recommendations sit.

---

## SEGMENT 16 - AI disclosure (14:20 to 14:34)

**NARRATION**

Quick disclosure. The voice you are hearing is AI generated, and the visuals in this video were made with AI tools. The research, the pricing checks and the opinions are mine.

**ON-SCREEN TEXT**

```
AI DISCLOSURE

Voice: AI generated
Visuals: AI generated
Research and opinions: human
```

**B-ROLL / VISUAL**

Static full-frame card, bg #111111, white text, no motion. **Minimum five seconds on screen. Do not cut this segment for runtime.**

---

## SEGMENT 17 - Close (14:34 to 15:10)

**NARRATION**

That is the week. A cheap model with a written-down data answer, a voice agent that speaks your caller's language, one Johannesburg launch that still sends the data to America, and a frontier model that changed your security homework. Written version with every price, every link and every source is on the WhatsApp channel, along with the two things I would try. If this was useful, join the channel and you get it every Monday morning. Next week I want to cover African compute properly, and Lelapa AI if I can date-verify it. See you Monday.

**ON-SCREEN TEXT**

```
JOIN THE WHATSAPP CHANNEL
Every Monday morning

Full write-up
Every price, every source link

NEXT WEEK
African compute, properly
```

**B-ROLL / VISUAL**

Soul still B6 with a slow Ken Burns. WhatsApp channel card holds from 15:40 to end, full width, accent yellow border. Final frame holds three seconds in silence.
