# AI Tools Drop - Video Script, 5 October 2026

Episode 9. Long form, 16:9. Window: 28 September to 5 October 2026.

## Production notes

- Measured runtime 15:08 across 17 segments, 2,413 narration words at 160 words per minute. If the delivered read lands long, trim segment 15 first, then 14, then 13.
- Read by ElevenLabs. Voice ID `P1LmKcX63Ihgqy11sVRt` (Andrew, South African male), model `eleven_multilingual_v2`, stability 0.60, similarity_boost 0.75, style 0.15, use_speaker_boost true, output `mp3_44100_128`.
- One API call per segment. Never batch. Output files `seg01.mp3` through `seg17.mp3` into `audio/`.
- Numbers are written longhand in narration so the voice reads them naturally. Overlays use digits. The mismatch is deliberate.
- All on-screen text is ASCII only. No em dashes, no curly quotes, no ellipsis characters, no arrows.
- Segment 16 is the AI disclosure. It must hold on screen for at least five seconds and must not be cut for time. If the edit runs long, trim segments 15, 14 or 13 instead.
- Segment 3 covers Eleven v4, a newer model from the same vendor as this pipeline's voice. That is editorial. Keep `eleven_multilingual_v2` for this episode unless Michael decides otherwise.

## Timing

| Segment | Title | Start | End |
| --- | --- | --- | --- |
| 1 | COLD OPEN | 0:00 | 0:34 |
| 2 | THE WEEK IN ONE PARAGRAPH | 0:34 | 1:24 |
| 3 | ELEVEN V4 | 1:24 | 2:21 |
| 4 | WHATSAPP BUSINESS PRICING | 2:21 | 3:20 |
| 5 | SHOPIFY CANVAS | 3:20 | 4:16 |
| 6 | GPT-6.1 SOL AND THE DECISIONS API | 4:16 | 5:14 |
| 7 | DOTS, SPACE AND PAGES | 5:14 | 6:10 |
| 8 | CLOUDFLARE CLEF AND STRANDS DECIDER | 6:10 | 7:10 |
| 9 | MICROSOFT MAI VOICE AND TRANSCRIBE | 7:10 | 8:04 |
| 10 | CHATGPT VIRTUAL TRY-ON | 8:04 | 9:02 |
| 11 | SUNO SPEECH | 9:02 | 10:00 |
| 12 | NOT FOR US YET | 10:00 | 10:55 |
| 13 | THE SOUTH AFRICAN CORNER | 10:55 | 11:52 |
| 14 | WHAT THE DECISION MODELS MEAN FOR YOUR BILL | 11:52 | 12:47 |
| 15 | WHAT I LEFT OUT | 12:47 | 13:43 |
| 16 | DISCLOSURE | 13:43 | 14:08 |
| 17 | WHAT I WOULD ACTUALLY TRY, AND CLOSE | 14:08 | 15:08 |

---

## Pronunciation guide

| Written | Say |
| --- | --- |
| ElevenLabs | eh-LEV-en labs |
| Eleven v4 | eleven vee-FOUR |
| isiZulu | ee-see-ZOO-loo |
| isiXhosa | ee-see-KOH-sah |
| Sesotho | seh-SOO-too |
| Setswana | seh-TSWAH-nah |
| Swahili | swah-HEE-lee |
| Wati | WAH-tee |
| Shopify | SHOP-ih-fy |
| Sidekick | SIDE-kick |
| GPT-6.1 | gee-pee-tee six point one |
| Sol | sol |
| Luna | LOO-nah |
| Astra | ASS-trah |
| Codex | KOH-dex |
| Dots | dots |
| Cloudflare | CLOWD-flair |
| Clef | klef |
| Strands | strands |
| Decider | dee-SIDE-er |
| MAI | em-ay-EYE |
| Foundry | FOWN-dree |
| Suno | SOO-noh |
| Argon | AR-gon |
| Gemini | JEM-in-eye |
| Muse | myooz |
| Exten | EX-ten |
| Fort Hare | fort HAIR |
| POPIA | poh-PEE-uh |

---

## SEGMENT 1 - COLD OPEN (0:00 to 0:34)

**NARRATION**

On the first of October, a lot of South African businesses started paying for something that used to be free. Replying to customers on WhatsApp. Not everyone, and not on the free app, but if you run a WhatsApp bot through a provider, your September bill and your October bill will look different. That is one of nine things this week, and it is the only one that costs you money whether you act or not. This is the AI Tools Drop for the week of the fifth of October.

**ON-SCREEN TEXT**

```
AI TOOLS DROP
Week of 5 October 2026
9 items. 28 Sep to 5 Oct.
```

**B-ROLL / VISUAL**

Black open. A WhatsApp-style chat bubble (generic, no Meta logo) types "Thanks, we will get back to you" and a small price tag drops onto it in the accent colour. Cut to cached Soul still B1 with a slow push in. Title card on the final line.

---

## SEGMENT 2 - THE WEEK IN ONE PARAGRAPH (0:34 to 1:24)

**NARRATION**

Here is the week in one breath. ElevenLabs shipped a new voice model at a steep discount that ends on the twelfth. Meta changed WhatsApp Business pricing. Shopify let merchants design a store by chatting. OpenAI held its developer day and shipped a cheaper top-tier model, always-on agents and the start of an office suite. Cloudflare and Amazon released small models that only choose answers, which is more useful than it sounds. Microsoft and Suno shipped speech tools, and ChatGPT can now try clothes on you. Two big launches are not available to us yet, and I have kept them separate rather than pretend otherwise. One of the nine is a pricing change, not a tool. Rand figures today use sixteen sixty-seven to the dollar. The rand is a little weaker than last week.

**ON-SCREEN TEXT**

```
THIS WEEK
9 items
1 is a pricing change, not a tool
2 big launches: not available in SA yet
1 discount ends 12 Oct
FX: R16.67 / USD
```

**B-ROLL / VISUAL**

Shotstack motion graphic. Rows animate in about 0.6 seconds apart. "not available in SA yet" and "ends 12 Oct" in the warning colour.

---

## SEGMENT 3 - ELEVEN V4 (1:24 to 2:21)

**NARRATION**

Number one, and my pick of the week. Eleven v4 from ElevenLabs, announced on the twenty-eighth of September, with a faster sibling called v4 Turbo for live voice agents. More emotion, better cloning, and more than ninety languages, up from about seventy. Now the part that matters here. Afrikaans is on the list. Swahili is on the list. isiZulu, isiXhosa, Sesotho and Setswana are not. So this is an English and Afrikaans tool for us, not a local languages tool. The price is the reason to look this week. On the API, v4 is two point two US cents per thousand characters until the twelfth of October, about thirty-seven cents in rand, against a normal price of eight cents. Creator plans and up also get triple credits until the twelfth. Two catches. There are no style or speed sliders on v4, and professional voice clones were still rolling out when I checked.

**ON-SCREEN TEXT**

```
1. ELEVEN V4 + V4 TURBO
Announced 28 Sep 2026

ON THE LIST: Afrikaans, Swahili, English
NOT LISTED: isiZulu, isiXhosa,
Sesotho, Setswana

API: USD 0.022 / 1K chars until 12 OCT
(approx R0.37) - list USD 0.08 (approx R1.33)
Creator+: 3x credits until 12 OCT
```

**B-ROLL / VISUAL**

Kling clip 1 (animated waveform rising over an abstract studio desk). Then split card: "ON THE LIST" in accent colour, "NOT LISTED" in warning colour. "until 12 OCT" pulses once.

---

## SEGMENT 4 - WHATSAPP BUSINESS PRICING (2:21 to 3:20)

**NARRATION**

Number two is not a tool. It is a bill. From the first of October, Meta charges for replies sent through the WhatsApp Business Platform, which is the API that chatbot providers like Wati use. Free-form replies inside the twenty-four hour window are now charged per message once you pass a free allowance of a thousand a month. Here is the honest part. I could not load Meta's own pricing page with the new rules, so this comes from providers and press. And they disagree. Wati says the thousand free messages are per business account. An Indian business paper says per phone number. I also did not find the South African rate. The good news. Wati says the free WhatsApp Business app, the one on your phone, is not affected. And conversations that start from a click-to-WhatsApp ad now get up to seven days free. If you use a bot, ask your provider what you sent in September.

**ON-SCREEN TEXT**

```
2. WHATSAPP BUSINESS PLATFORM (API)
PRICING CHANGE - NOT A TOOL
From 1 OCT 2026: replies billed per message
after 1,000 free a month

Per account or per number? Sources disagree.
SA rate: not confirmed
WhatsApp Business APP: not affected
Click-to-WhatsApp ads: up to 7 days free
```

**B-ROLL / VISUAL**

Cached Soul still B2 (abstract phone and message streams). Counter graphic ticks from 998 to 1,001, the last digit turning warning colour. "Sources disagree" in warning colour.

---

## SEGMENT 5 - SHOPIFY CANVAS (3:20 to 4:16)

**NARRATION**

Number three. Shopify Canvas, launched on the first of October. You set up your store by chatting with Sidekick, Shopify's AI agent, and it edits the real files behind your theme while you watch. You can zoom around the whole store, test it on different screen sizes, and still click anything to change it by hand. For a small brand without a developer, that is a real shortcut. The limits at launch are long, though. No third-party themes, no app blocks, no translations, no multiple markets, and theme updates are not supported. It is desktop only. So if your store runs in two languages or two currencies, wait. No separate price was announced, and Sidekick is described as included with Shopify plans, but I have not seen that confirmed for Canvas itself. My advice is simple. Duplicate your theme and try it on the copy, never on the live store.

**ON-SCREEN TEXT**

```
3. SHOPIFY CANVAS
Launched 1 Oct 2026. Desktop only.
Build your store by chatting with Sidekick

NOT AT LAUNCH: third-party themes, app blocks,
translations, markets, theme updates

Price: not announced
TRY IT ON A DUPLICATE THEME
```

**B-ROLL / VISUAL**

Kling clip 2 (a generic storefront layout assembling itself tile by tile). Then the limits card with the "NOT AT LAUNCH" header in warning colour.

---

## SEGMENT 6 - GPT-6.1 SOL AND THE DECISIONS API (4:16 to 5:14)

**NARRATION**

Number four, for builders. At OpenAI's developer day on the twenty-ninth, GPT-6 Sol was replaced after one week by GPT-6.1 Sol. OpenAI says it gets close to its top model, Astra, at a fifth of the price. Two dollars per million input tokens, about thirty-three rand, and ten dollars out, about a hundred and sixty-seven rand. Cached input is ten US cents. Reported context is over a million tokens. It is in Codex and ChatGPT Work on paid plans, but not yet in normal chat. The more interesting one for small businesses is the Decisions API. You give it a question and a fixed list of answers, and it picks one. Classify a message, route a ticket, choose the next step. The catch is that it is in limited preview, and as of the second of October no price had been published. So it is one to watch rather than build on today.

**ON-SCREEN TEXT**

```
4. GPT-6.1 SOL + DECISIONS API
OpenAI DevDay, 29 Sep 2026

GPT-6.1 SOL: USD 2 in / USD 10 out per 1M tokens
(approx R33 / R167). Cached: USD 0.10
Codex + ChatGPT Work. Not yet in Chat.

DECISIONS API: limited preview
Price: not published (2 Oct)
```

**B-ROLL / VISUAL**

Cached Soul still B3 (abstract code on glass). Price card animates in. "limited preview" and "not published" in warning colour.

---

## SEGMENT 7 - DOTS, SPACE AND PAGES (5:14 to 6:10)

**NARRATION**

Number five, same event, different audience. OpenAI launched Dots, which it calls always-on agents. They work in the background towards goals you set, and you can message them through Slack or Teams. It also launched Space, a shared workspace for a team and ChatGPT, and Pages, a document editor built for people and agents to write together. Slides, its answer to PowerPoint, comes in the next few weeks. For a small agency or consultancy already paying for ChatGPT, that is shared projects and documents in one place. Now the limits. Dots is only for Pro and Business Premium users in what OpenAI calls eligible markets, and it did not say which markets. And an agent that runs on its own, with your logins, is a security decision, not a convenience. In the same week, TechCentral reported that OpenAI agents had leaked fifty-three users' images. Give agents the least access they need.

**ON-SCREEN TEXT**

```
5. DOTS + SPACE + PAGES
OpenAI DevDay, 29 Sep 2026

DOTS: always-on agents
Pro + Business Premium, "eligible markets"
(list not published)
SPACE: shared team workspace
PAGES: documents for people + agents
SLIDES: coming weeks

Agents with logins = security decision
```

**B-ROLL / VISUAL**

Kling clip 3 (small glowing dots moving between abstract document panels). Last line in warning colour.

---

## SEGMENT 8 - CLOUDFLARE CLEF AND STRANDS DECIDER (6:10 to 7:10)

**NARRATION**

Number six, and the quiet one I like most. On the first of October, Cloudflare released Clef and a smaller Clef-flash, and Amazon released Strands Decider 2B. These are decision models. They do not write anything. You give them a message and a set of questions, yes or no, pick one, or score it, and they return probabilities. Cloudflare says the flash model answers in under forty milliseconds at the median. Why should you care. Put one in front of your WhatsApp bot. It decides whether a message is a booking, a complaint or needs a human, and only then do you pay a big model to reply. The weights are open, and Amazon's two-billion model runs on ordinary hardware, so client data can stay on your machine. Workers AI has a free plan. A developer write-up reports about four rand per million tokens for Clef, but Cloudflare's own page did not confirm that in what I read.

**ON-SCREEN TEXT**

```
6. CLOUDFLARE CLEF + AMAZON STRANDS DECIDER 2B
Released 1 Oct 2026. Open weights.

They choose. They do not write.
yes/no - pick one - score
Clef-flash median: 38.8 ms

Workers AI: free plan available
Clef approx R4 / 1M input tokens (UNCONFIRMED)
Decider 2B: runs locally, free
```

**B-ROLL / VISUAL**

Shotstack motion graphic: three incoming messages sorted into three labelled bins, BOOKING, COMPLAINT, HUMAN. "UNCONFIRMED" in warning colour.

---

## SEGMENT 9 - MICROSOFT MAI VOICE AND TRANSCRIBE (7:10 to 8:04)

**NARRATION**

Number seven. Microsoft released three speech models on the first of October, through its Foundry platform on Azure. MAI-Transcribe-2-Streaming turns live audio into text across sixty languages and detects the language as it goes. MAI-Voice-2.1 speaks twenty-three languages and keeps the same voice across all of them, and there is a cheaper Flash version for high volume. Prices are clear. Transcription is fifty-four US cents an hour of audio until the end of the year, about nine rand. Voice is twenty-two dollars per million characters, about three hundred and sixty-seven rand, and Flash is fifteen dollars, about two hundred and fifty rand. What I could not confirm is the language list. Microsoft's post gives counts but not names, so I cannot tell you whether any South African language is in there. If you already run on Azure, it is worth a test on English calls.

**ON-SCREEN TEXT**

```
7. MICROSOFT MAI MODELS
Released 1 Oct 2026. Microsoft Foundry.

TRANSCRIBE-2-STREAMING: 60 languages
USD 0.54 / hour (approx R9) to year end
VOICE-2.1: 23 languages - USD 22 / 1M chars (approx R367)
VOICE-2.1-FLASH: USD 15 / 1M chars (approx R250)

SA languages: NOT CONFIRMED
```

**B-ROLL / VISUAL**

Kling clip 4 (live caption text flowing beneath an abstract call-centre headset). Last line in warning colour.

---

## SEGMENT 10 - CHATGPT VIRTUAL TRY-ON (8:04 to 9:02)

**NARRATION**

Number eight. On the first of October, OpenAI launched virtual try-on in ChatGPT, globally. In shopping results there is now a Try On button. You upload a selfie or a full-body photo and it shows you wearing the item. You can also upload a screenshot of something from any website. It runs on the new Images two point five model, and there is a Favourites library to save what you like. Why does a business care. Because shoppers will start asking ChatGPT how your product looks on them, so your product photos and listings need to be clean and easy to find. One important caution. ET Now reports that uploaded photos are used for training by default. Check that setting before you upload a photo of yourself, and never upload a client's photo to test it. For boutiques, stylists and salons, look at how your items appear, and leave it there for now.

**ON-SCREEN TEXT**

```
8. CHATGPT VIRTUAL TRY-ON
Global launch, 1 Oct 2026. Images 2.5.

Upload a selfie - see the item on you
Favourites library for saved products

PRIVACY: photos used for training by default
(reported - check your settings)
Never upload client photos
```

**B-ROLL / VISUAL**

Cached Soul still B6 (abstract fashion rail). "PRIVACY" block in warning colour.

---

## SEGMENT 11 - SUNO SPEECH (9:02 to 10:00)

**NARRATION**

Number nine. Suno, the music generator, opened a beta called Speech on the first of October, for everyone, on web and on the phone apps. It makes a spoken voice and the music behind it in one take. So a radio-style ad, a podcast intro or a promo sting comes out as one piece, not a voice file and a music file you have to mix. For agencies, that is a fast way to show a client a rough version before paying a voice artist. The gaps are real, though. Suno has not published a separate Speech price or limit. There are no separate commercial terms for Speech either. And Suno's free plan says plainly, no commercial rights. So treat anything from the free plan as a draft only. If it goes into a client's ad, use a paid plan, and read the terms first. It is also a beta, so expect things to change.

**ON-SCREEN TEXT**

```
9. SUNO SPEECH (BETA)
Opened to all users, 1 Oct 2026
Voice + music in one take

Speech price: not published
Free plan: NO COMMERCIAL RIGHTS
Paid plan for client work
```

**B-ROLL / VISUAL**

Kling clip 5 (abstract sound bars morphing into a speaking silhouette). "NO COMMERCIAL RIGHTS" in warning colour.

---

## SEGMENT 12 - NOT FOR US YET (10:00 to 10:55)

**NARRATION**

Two of the biggest launches of the week are not available to us, and I want to be clear about that rather than hype them. Google's Gemini 4 Argon is its most powerful model yet. It went first to trusted cybersecurity defenders and the US government. Paid API customers and top-tier subscribers come later, with no date. So no South African business can use it today. Meta's Muse for Small Business connects to your Facebook and Instagram pages, Shopify and Stripe, and works across them for you. Meta's own page says it is available only in the US and Canada. And there is local hardware news. TechCentral reports that Ray-Ban and Oakley Meta smart glasses are getting an official South African launch, likely without Muse. TechCentral says this year. Another newsletter says twenty twenty-seven. I cannot confirm which is right, so I am not giving you a date.

**ON-SCREEN TEXT**

```
NOT FOR US YET

GEMINI 4 ARGON
Cyber defenders + US government first
Wider access: no date

MUSE FOR SMALL BUSINESS
US and Canada only

META GLASSES IN SA
Official launch coming - date UNCONFIRMED
Likely without Muse
```

**B-ROLL / VISUAL**

Three cards, each with a grey "NOT AVAILABLE IN SA" stamp in the warning colour. Static, no motion.

---

## SEGMENT 13 - THE SOUTH AFRICAN CORNER (10:55 to 11:52)

**NARRATION**

Every week I look for South African launches. This week I found a South African story, but not a new launch, and I want to keep those apart. Disrupt Africa profiled Exten AI, a local startup founded by Luncedo Simelane. You describe an app in plain language, and it builds the app and sets up the backend too. Database, file storage and user logins. That last part is where most of these tools stop, so it is a serious idea. But it launched earlier this year, it is in closed testing, it is running a pilot with the University of Fort Hare, and it is raising one and a half million rand. So follow it. Do not plan a client project on it yet. And one honest count. In the material I read this week, no vendor mentioned POPIA by name, and none of the nine documented an African hosting region.

**ON-SCREEN TEXT**

```
SA CORNER
EXTEN AI - South African app builder
Plain language in - app + backend out
Launched earlier in 2026. Closed testing.
Pilot: University of Fort Hare
Raising R1.5m

FOLLOW IT. DO NOT BUILD ON IT YET.

This week: POPIA mentions 0. African regions 0.
```

**B-ROLL / VISUAL**

Cached Soul still A16 (Joburg skyline) under the card. The final line in warning colour.

---

## SEGMENT 14 - WHAT THE DECISION MODELS MEAN FOR YOUR BILL (11:52 to 12:47)

**NARRATION**

Let me connect two items, because together they matter more than either alone. WhatsApp replies through the API now cost money after a free allowance. And this week, small models arrived whose only job is to decide. Put those together. Most messages a small business gets are simple. What time do you open. Can I book Thursday. Where is my order. If a tiny, cheap model sorts every message first, you can answer the simple ones with a saved reply, and only send the hard ones to an expensive model or a person. Fewer long replies, fewer big model calls, and a person sees the messages that need a person. I am not giving you a rand saving, because I do not have the South African WhatsApp rate. But the shape of the sum is right. Count first, sort second, and pay for the expensive step last.

**ON-SCREEN TEXT**

```
THE SUM
1. WhatsApp API replies now cost money
2. Decision models sort messages cheaply

Sort first - simple: saved reply
           - hard: big model or a person

SA WhatsApp rate: not confirmed
Count. Sort. Pay last.
```

**B-ROLL / VISUAL**

Simple flow diagram in Shotstack. Message enters, small grey box labelled SORT, two arrows drawn as plain lines to SAVED REPLY and PERSON. ASCII labels only.

---

## SEGMENT 15 - WHAT I LEFT OUT (12:47 to 13:43)

**NARRATION**

A word on what I left out, so you know it was a choice. n8n launched a new Agents builder on the twenty-fifth of September. That is three days before this window, so it misses the cut, even though it is useful. Tavus showed a video conversation model called Griffin, but only as a research preview for selected testers, so there is nothing for you to sign up for. The Product Hunt board was mostly tools for other AI agents, with little that fits a South African small business. And Microsoft's uplift on monthly-billed annual subscriptions, which I warned about last week, took effect on the first of October. If you did not ask your reseller about it, it is now on your bill. None of those earned a full slot. I would rather give you nine things that are real and current than fifteen that pad the list.

**ON-SCREEN TEXT**

```
LEFT OUT ON PURPOSE
n8n Agents - launched 25 Sep (outside window)
Tavus Griffin - research preview only
Product Hunt - mostly agent infrastructure

LAST WEEK'S WARNING
Microsoft 5% CSP uplift took effect 1 OCT
```

**B-ROLL / VISUAL**

Plain text list over cached Soul still B1, dimmed. "took effect 1 OCT" in warning colour.

---

## SEGMENT 16 - DISCLOSURE (13:43 to 14:08)

**NARRATION**

Quick disclosure, and it stays in every episode. The voice you are listening to is AI generated. The still images and the animated clips are AI generated. The research, the fact checking, the pricing and every opinion are mine. Every claim was checked against a published source, and where I could not confirm something, I said so out loud.

**ON-SCREEN TEXT**

```
AI DISCLOSURE
Voice: AI generated
Visuals: AI generated
Research and opinions: human
```

**B-ROLL / VISUAL**

Static card, no motion, no Ken Burns. Full-frame, centred, high contrast. Must hold a minimum of five seconds. Do not cut this segment for time under any circumstances.

---

## SEGMENT 17 - WHAT I WOULD ACTUALLY TRY, AND CLOSE (14:08 to 15:08)

**NARRATION**

So what would I actually do this week. First pick, Eleven v4, before the twelfth of October. Write one short script in English and one in Afrikaans, generate both at the discounted price, and compare them with the voice you use now. It will cost you a few rand. Just do not plan isiZulu or isiXhosa work on it, because they are not on the list. Second pick, if you sell on Shopify, Canvas. Duplicate your theme and rebuild one product page by chatting. Never on the live store. And one thing that is not a purchase. If you run a WhatsApp bot through a provider, message them today. Ask how many replies you sent in September, and what that volume costs from October. That one question could save you a surprise at month end. That is the drop. The full written version, with every source, is on the WhatsApp channel. Follow it, and I will see you next Monday.

**ON-SCREEN TEXT**

```
WHAT I WOULD ACTUALLY TRY

1. ELEVEN V4 - before 12 OCT
One English + one Afrikaans script.
Compare with your current voice.

2. SHOPIFY CANVAS
Duplicate your theme. One page by chat.

3. NOT A PURCHASE - DO THIS
WhatsApp bot? Ask your provider:
September replies + October cost

FX: R16.67 / USD (2 sources)

FULL WRITTEN VERSION ON THE WHATSAPP CHANNEL
Next drop: Monday
```

**B-ROLL / VISUAL**

Three numbered cards, building in sequence, accent colour. Card three in warning colour because it is time-sensitive. FX line in smaller type at the bottom. Close on the WhatsApp channel CTA over Soul still A16 (Joburg skyline), slow push out, fade to black on the "Next drop: Monday" line.

---
