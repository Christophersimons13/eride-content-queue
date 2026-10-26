# AI Tools Drop - Video Script, 26 October 2026

Episode 12. Long form, 16:9. Window: 19 to 26 October 2026.

## Production notes

- Measured runtime 13:25 across 16 segments, 2,137 narration words at 160 words per minute. If the delivered read lands long, trim segment 14 first, then 13, then 12.
- This episode has **16 segments, not 17**. Seven tools made the main list this week rather than eight. That is deliberate, not a missing segment.
- Read by ElevenLabs. Voice ID `P1LmKcX63Ihgqy11sVRt` (Andrew, South African male), model `eleven_multilingual_v2`, stability 0.60, similarity_boost 0.75, style 0.15, use_speaker_boost true, output `mp3_44100_128`.
- One API call per segment. Never batch. Output files `seg01.mp3` through `seg16.mp3` into `audio/`.
- Numbers are written longhand in narration so the voice reads them naturally. Overlays use digits. The mismatch is deliberate.
- All on-screen text is ASCII only. No em dashes, no curly quotes, no ellipsis characters, no arrows.
- Segment 15 is the AI disclosure. It must hold on screen for at least five seconds and must not be cut for time. If the edit runs long, trim segments 14, 13 or 12 instead.
- Segment 5 covers Perplexity Computer, the tool this series is researched with. The narration discloses that. Do not remove the disclosure line.
- Segments 6 and 7 cover ElevenLabs and Mistral voice products, and the follow-ups mention Kling 4.0. That is editorial. Do not switch voice vendors, video models or settings for this episode.

## Timing

| Segment | Title | Start | End |
| --- | --- | --- | --- |
| 1 | COLD OPEN | 0:00 | 0:30 |
| 2 | THE WEEK IN ONE PARAGRAPH | 0:30 | 1:23 |
| 3 | CANVA CRAFT | 1:23 | 2:25 |
| 4 | GOOGLE MEET SPEECH TRANSLATION | 2:25 | 3:25 |
| 5 | PERPLEXITY COMPUTER ON MAC | 3:25 | 4:26 |
| 6 | ELEVENLABS REALTIME | 4:26 | 5:22 |
| 7 | MISTRAL VOXTRAL 3 | 5:22 | 6:15 |
| 8 | RECURSIVE FLINT | 6:15 | 7:13 |
| 9 | OCTANE AI PHOENIX | 7:13 | 8:08 |
| 10 | NOT FOR US YET | 8:08 | 8:56 |
| 11 | THE SOUTH AFRICAN CORNER | 8:56 | 9:50 |
| 12 | WHAT A ONE RAND PHONE AGENT MEANS | 9:50 | 10:44 |
| 13 | LAST WEEK'S FOLLOW-UPS | 10:44 | 11:18 |
| 14 | WHAT I LEFT OUT | 11:18 | 12:01 |
| 15 | DISCLOSURE | 12:01 | 12:26 |
| 16 | WHAT I WOULD ACTUALLY TRY, AND CLOSE | 12:26 | 13:25 |

---

## Pronunciation guide

| Written | Say |
| --- | --- |
| Canva | KAN-vah |
| Craft | krahft |
| Dream Lab | dreem lab |
| Google Meet | GOO-gl meet |
| Afrikaans | af-ri-KAHNS |
| Perplexity | per-PLEK-si-tee |
| Qwen | chwen |
| ElevenLabs | eh-LEV-en labs |
| Mistral | MIS-trahl |
| Voxtral | VOKS-trahl |
| Recursive Flint | ree-KER-siv flint |
| Octane | OK-tayn |
| Shopify | SHOP-ih-fy |
| Klaviyo | KLAY-vee-oh |
| Claude Duet | klohd dyoo-ET |
| 1Password | one PASS-wurd |
| Muse | myooz |
| DCDT | spelled out, dee-see-dee-TEE |
| CAPES | kayps |
| Kling | kling |
| isiZulu | ee-see-ZOO-loo |
| isiXhosa | ee-see-KOH-sah |
| POPIA | poh-PEE-uh |
| Sandton | SAND-tn |

---

## SEGMENT 1 - COLD OPEN (0:00 to 0:30)

**NARRATION**

A poster where the AI actually spells your prices correctly. A meeting where your client hears you in Afrikaans while you speak English. And an AI phone agent for well under a rand and a half a minute. That was this week. Seven tools made the list, three are not available to us yet, and there is free AI training on offer in South Africa. This is the AI Tools Drop for the week of the twenty-sixth of October.

**ON-SCREEN TEXT**

```
AI TOOLS DROP
Week of 26 October 2026
7 tools. 19 Oct to 26 Oct.
```

**B-ROLL / VISUAL**

Built in Shotstack, not Kling. A generic poster layout assembles on a dark background: a headline block, a price block reading "R250", a footer. No Canva marks, no real brand names. Title card fades in over it.

---

## SEGMENT 2 - THE WEEK IN ONE PARAGRAPH (0:30 to 1:23)

**NARRATION**

Here is the week in one paragraph. Canva released its own image model, called Craft, designed for posters and social posts where the words need to be readable, and it is open to free accounts. Google Meet's live speech translation now covers sixty-three languages. Afrikaans is in. isiZulu and isiXhosa are not. Perplexity's Computer agent can now run entirely on a Mac with no internet. ElevenLabs and Mistral both launched cheaper models for AI phone agents. For builders, there is a free coding model that runs on a laptop, and a rebuilt quiz tool for Shopify stores. The biggest launch of the week, Anthropic's Claude Duet, is US only for now. It was not a thin week, but several big names either launched before the window or are not usable from here. So seven tools, covered properly, rather than eight with padding.

**ON-SCREEN TEXT**

```
THIS WEEK

Canva Craft: readable text in images
Google Meet: 63 languages, incl. Afrikaans
Perplexity: offline agent on Mac
Voice agents: ElevenLabs + Mistral
Builders: Flint, Octane Phoenix

Claude Duet: US only
```

**B-ROLL / VISUAL**

Cached Soul still B2 (desk workspace), slow Ken Burns push in. Lines build one at a time. "US only" in warning colour.

---

## SEGMENT 3 - CANVA CRAFT (1:23 to 2:25)

**NARRATION**

First, Canva Craft. On the twenty-second of October Canva released its first image model that it built itself. Most image generators struggle with words. You ask for a poster that says "Specials this week" and you get something close but misspelled. Canva says Craft plans the layout first, where the headline sits, how big the price is, and only then draws. It outputs up to two K resolution in more than thirty shapes, so one prompt can give you an Instagram post, a WhatsApp Status and an A4 poster. Canva reports it debuted fourth on a public image leaderboard. That is the company's own claim, and the readable text has not been independently tested yet. Pricing is simple. There is no separate charge. It lives inside Dream Lab, and Canva's own help page says free accounts get twenty Dream Lab uses in total, while Pro accounts get up to five hundred a month. So test it, but check every word before it goes to print.

**ON-SCREEN TEXT**

```
CANVA CRAFT (22 Oct)
Image model built for designs with text
Up to 2K, 30+ aspect ratios
Free: 20 Dream Lab uses (lifetime)
Pro: up to 500 per month
Text claims not independently verified
```

**B-ROLL / VISUAL**

Kling clip K1: blank poster sheets on a studio table, abstract shapes and blocks of colour arranging themselves into a layout. No readable text, no Canva logo. Last line in warning colour.

---

## SEGMENT 4 - GOOGLE MEET SPEECH TRANSLATION (2:25 to 3:25)

**NARRATION**

Second, Google Meet. On the twenty-second Google expanded live speech translation in Meet to sixty-three languages. Each person in the meeting hears the others in their own language, in a voice like the speaker's, and Meet detects the language automatically, even if someone switches halfway through a sentence. For South Africa, the language list matters. Afrikaans and English are on it, and so is Swahili. isiZulu, isiXhosa, Sesotho and Setswana are not. So this is useful for a client in Mozambique, Congo or China, less so for most local calls. You need the meeting host on an eligible plan: Workspace Business Standard or above, or Google AI Pro. Business Starter is not on the list. Translation is capped at ninety minutes per meeting on those plans, and it does not work on dial-in calls or recordings. Google also says some regions are excluded without naming them, so run a test call before you rely on it with a client.

**ON-SCREEN TEXT**

```
GOOGLE MEET SPEECH TRANSLATION (22 Oct)
63 languages, auto-detected
Includes: Afrikaans, English, Swahili
Not included: isiZulu, isiXhosa, Sesotho, Setswana
Needs Business Standard+ or Google AI Pro
90 min per meeting
```

**B-ROLL / VISUAL**

Shotstack motion graphic: two generic video-call tiles with abstract speech bubbles in two colours swapping sides. No Google UI, no faces. "Not included" line in warning colour.

---

## SEGMENT 5 - PERPLEXITY COMPUTER ON MAC (3:25 to 4:26)

**NARRATION**

Third, and a disclosure before I start. This series is researched and produced using Perplexity Computer, so weigh my view on this one accordingly. On the twentieth of October Perplexity added a mode to its Mac app that runs both the AI model and the agent entirely on the Mac, with no internet connection. With your permission it can read local files and work in Notes, Mail, Messages and Numbers. For example, go through this week's emails, find the deadlines and write a to-do list into Notes. Nothing goes to the cloud unless you approve it. Now the catch. It needs an Apple silicon Mac, and Perplexity recommends at least thirty-six gigabytes of memory, which most small-business laptops do not have. The local model is also weaker than the cloud models. It is included in the Pro plan, reported at twenty dollars a month, about three hundred and thirty rand. Useful during load-shedding or on a flight, if you have the hardware.

**ON-SCREEN TEXT**

```
PERPLEXITY COMPUTER, LOCAL ON MAC (20 Oct)
Disclosure: this series uses Perplexity
Runs offline on Apple silicon
Recommended: 36 GB memory
Pro: approx USD 20 / R331 per month
```

**B-ROLL / VISUAL**

Cached Soul still B2, cool grade, slow drift. Disclosure line in accent colour and held for the full segment. "36 GB memory" in warning colour.

---

## SEGMENT 6 - ELEVENLABS REALTIME (4:26 to 5:22)

**NARRATION**

Fourth, ElevenLabs. On the twentieth they launched Eleven Realtime version one, in two sizes, Mini and Max. These are speech-to-speech models, which means one model listens and answers, instead of three separate systems passing text between them. In practice that makes AI phone agents sound less robotic. They handle pauses, interruptions, and people talking over each other. Mini is the fast, cheaper one for simple calls. Max thinks before it answers and is meant for calls where the agent must look things up or book something. ElevenLabs lists both at eight US cents a minute plus usage, which is about one rand thirty-three a minute before the model costs. They say up to ninety languages, but they do not name them, so test isiZulu or Sesotho yourself before you promise it to a client. You also still need a developer to connect it to your phone line and your booking system.

**ON-SCREEN TEXT**

```
ELEVENLABS REALTIME V1 (20 Oct)
Mini: fast, low cost
Max: thinks first, uses tools
USD 0.08/min + usage (approx R1.33)
"Up to 90 languages" - not named
Needs a developer
```

**B-ROLL / VISUAL**

Kling clip K2: an abstract waveform pulsing in a dark room, a desk phone silhouette at the edge of frame, amber edge light. No brand marks. "not named" in warning colour.

---

## SEGMENT 7 - MISTRAL VOXTRAL 3 (5:22 to 6:15)

**NARRATION**

Fifth, the cheaper option. Mistral, the French AI company, released Voxtral 3 on the twentieth. It is a full kit for voice: transcription, speech, and a voice agent that can answer and place calls and connect to existing call-centre software. The headline is price. Mistral lists voice agents at four US cents a minute with its smaller model, about sixty-six cents in rand, and eight cents with a larger one. Transcription starts at about three rand fifty an hour of audio, with speaker labels, which is very useful for recorded consultations. Two honest limitations. The voice output covers thirty-five languages, fewer than ElevenLabs, and no South African language list is given. And its professional voice cloning has no published consent policy yet. Mistral offers servers hosted in Europe, which makes a POPIA cross-border assessment simpler than a US-only service. Simpler, not unnecessary.

**ON-SCREEN TEXT**

```
MISTRAL VOXTRAL 3 (20 Oct)
Voice agent: USD 0.04/min (approx R0.66)
Transcription: approx R3.48 per hour
Speech: 35+ languages
No SA language list
Voice clone consent policy: not published
EU hosting available
```

**B-ROLL / VISUAL**

Cached Soul still B3 (network mesh), cool grade, slow drift. Price line in accent colour. "not published" in warning colour.

---

## SEGMENT 8 - RECURSIVE FLINT (6:15 to 7:13)

**NARRATION**

Sixth, one for the builders. A company called Recursive released Flint, a coding model you download and run on your own machine. It is free, with the weights published under an open licence. It is designed to be fast on ordinary developer hardware. Recursive reports more than a hundred and twenty-five tokens a second on an M4 Pro MacBook, which is faster than you can read, and it works with tools developers already use, like Ollama and LM Studio. Why this matters here: every coding assistant you pay for bills you in dollars per use. A local model costs you only electricity, and your client's code never leaves the machine, which is useful when a contract says it may not. The honest part comes from Recursive itself. Flint needs more guidance than the big paid models. Break the work into small tasks and give clear instructions. And the speed figures are the company's own.

**ON-SCREEN TEXT**

```
RECURSIVE FLINT
Local coding model, free (Apache 2.0)
Works with Ollama, LM Studio, llama.cpp
No per-use dollar billing
Needs more guidance than paid models
Speed figures: vendor claim
```

**B-ROLL / VISUAL**

Shotstack motion graphic: generic code-shaped blocks of colour scrolling on a laptop outline. No readable code, no logos. Last two lines in warning colour.

---

## SEGMENT 9 - OCTANE AI PHOENIX (7:13 to 8:08)

**NARRATION**

Seventh, for Shopify stores. On the twenty-first Octane AI announced Phoenix, a quiz builder rebuilt around AI. You describe the quiz you want, say "help customers find the right shampoo", and it builds the questions, the logic and the results page from your product catalogue. It checks every path a shopper could take for dead ends and out-of-stock products. Shoppers can even answer with a photo, of their hair for example, and it picks products. It also reports what each answer earns in sales. Now the reality check. It is Shopify only. The entry plan is fifty dollars a month, about eight hundred and thirty rand, limited to two quizzes, with a fourteen-day free trial. That only pays off if your store has real traffic. And a customer's photo is personal information under POPIA, so your privacy notice needs to say what you do with it.

**ON-SCREEN TEXT**

```
OCTANE AI PHOENIX (21 Oct)
AI-built product quiz for Shopify
Checks for dead ends + out-of-stock
Basic: USD 50 / approx R829 per month
14-day free trial. 2 quizzes on Basic.
Photos = personal info under POPIA
```

**B-ROLL / VISUAL**

Kling clip K3: hair and skincare bottles, unbranded, on a bright bathroom shelf, soft morning light, a slow camera slide. No labels, no faces. POPIA line in warning colour.

---

## SEGMENT 10 - NOT FOR US YET (8:08 to 8:56)

**NARRATION**

Three launches that are not for us yet. First, Claude Duet from Anthropic, released on the twenty-first. It is an assistant that sends you a morning brief, watches your connected apps, and asks before it sends, pays or deletes anything. Anthropic pitches it at small business owners, but it is a waitlist for Pro and Max users in the US only. Second, 1Password for Agents, which lets an AI agent log in to sites without ever seeing your password. Right now it only works with Meta's Muse assistant, and other agents are on a waitlist. Business accounts are not supported. Third, ElevenLabs' live call translation, which is an alpha for enterprise customers only. If any of these opens up here, it goes straight into the main list.

**ON-SCREEN TEXT**

```
NOT FOR US YET

CLAUDE DUET (21 Oct)
Waitlist. US Pro + Max only.

1PASSWORD FOR AGENTS (22 Oct)
Muse only. No business accounts.

ELEVEN REALTIME TRANSLATION (21 Oct)
Enterprise alpha
```

**B-ROLL / VISUAL**

Plain text cards over cached Soul still B1, dimmed. "US Pro + Max only", "No business accounts" and "Enterprise alpha" in warning colour.

---

## SEGMENT 11 - THE SOUTH AFRICAN CORNER (8:56 to 9:50)

**NARRATION**

The South African corner. On the twentieth, Meta and the Department of Communications and Digital Technologies launched the AI Academy South Africa. It has two free tracks. The pitch competition has closed. Ten startups pitch in Johannesburg on Friday, and two winners get just over eighty-two thousand rand each in funding that takes no shares. The part you can still join is the eight-week online masterclass, which runs from the basics to building apps on Meta's models, and enrolment stays open until January. Second, for recruitment and staffing firms, the CAPES AI Action Plan was announced on the fourteenth, so just outside our window, but its launch webinar is tomorrow, Tuesday, at twelve. It includes a free short course. And AI Expo Africa is on Wednesday and Thursday at the Sandton Convention Centre. If anything usable launches there, it will be in next week's drop.

**ON-SCREEN TEXT**

```
SA CORNER

META + DCDT AI ACADEMY SA (20 Oct)
Free 8-week masterclass
Enrol until January 2027
Pitch finals: Joburg, 30 Oct

CAPES AI ACTION PLAN (staffing firms)
Webinar: Tue 27 Oct, 12h00

AI EXPO AFRICA: Sandton, 28-29 Oct
```

**B-ROLL / VISUAL**

Cached Soul still A16 (Joburg skyline), slow push in. "Enrol until January 2027" in accent colour.

---

## SEGMENT 12 - WHAT A ONE RAND PHONE AGENT MEANS (9:50 to 10:44)

**NARRATION**

Two of this week's tools put AI phone agents at roughly one rand a minute, so here is what that means in practice. Say a salon gets forty booking calls a day, each about two minutes. That is around eighty minutes a day, so somewhere between about fifty and a hundred and five rand a day in voice costs, before the model and the developer. That is my rough maths, not a vendor quote. Cheaper than a receptionist, yes, but that is the wrong comparison. The right question is which calls you are comfortable letting a machine handle. Bookings and opening hours, probably yes. A complaint, a refund, or anything medical, no. And under POPIA, callers should be told they are speaking to an AI and that the call is recorded. Start with after-hours calls only, listen to the recordings for two weeks, then decide.

**ON-SCREEN TEXT**

```
ROUGH EXAMPLE (MY MATHS)
40 calls x 2 min = 80 min/day
At R0.66 - R1.33/min: approx R53 - R106/day
Plus model + developer costs

AI: bookings, opening hours
HUMAN: complaints, refunds, medical
Tell callers it is an AI
```

**B-ROLL / VISUAL**

A plain bar chart with ASCII labels only, labelled "ROUGH EXAMPLE (MY MATHS)". Two bins drawn below it, labelled AI and HUMAN. "Tell callers it is an AI" in warning colour.

---

## SEGMENT 13 - LAST WEEK'S FOLLOW-UPS (10:44 to 11:18)

**NARRATION**

Three follow-ups. First, Kling four point oh, the video model, became available on the fifteenth of October. That is outside this week's window, so it is not on the main list, but it now makes clips of up to thirty seconds in 4K with sound. Second, OpenAI's Decisions API, which I covered as a preview two weeks ago, became generally available on the twenty-second. Third, nothing has changed on Gemini 4 Argon for South African Pro users, and the introductory developer price still ends on the thirtieth of November.

**ON-SCREEN TEXT**

```
FOLLOW-UPS

KLING 4.0: released 15 Oct (outside window)
Up to 30 sec, 4K, with audio

OPENAI DECISIONS API: GA on 22 Oct

GEMINI 4 ARGON: intro API price ends 30 Nov
```

**B-ROLL / VISUAL**

Plain text list over cached Soul still B1, dimmed. "outside window" and "ends 30 Nov" in warning colour.

---

## SEGMENT 14 - WHAT I LEFT OUT (11:18 to 12:01)

**NARRATION**

Now what I left out on purpose. Shopify released tools that turn an AI agent into a personal shopper across its catalogue, but there was no word on regions, prices or plans, and checkout runs on Shop Pay, so I could not confirm it works from here. DeepSeek's latest fast model launched just before the window. A handful of new developer models, Mercury 3, MiniMax and FLUX 3 Max, have no clear small-business use yet. And Grok Bot had another weekly update, but the product launched in August. The rule stays the same. If I cannot confirm it launched in the last seven days and works for us, it does not go on the list.

**ON-SCREEN TEXT**

```
LEFT OUT

Shopify shop.md: region + price not stated
DeepSeek V4.1 Flash: 17 Oct
Mercury 3, MiniMax M3.1, FLUX 3 Max: dev only
Grok Bot: launched August

Rule: last 7 days, and usable here
```

**B-ROLL / VISUAL**

Each line appears, then gets a small grey "OLD", "UNCLEAR" or "NICHE" stamp. Plain text over cached Soul still B6, dimmed.

---

## SEGMENT 15 - DISCLOSURE (12:01 to 12:26)

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

## SEGMENT 16 - WHAT I WOULD ACTUALLY TRY, AND CLOSE (12:26 to 13:25)

**NARRATION**

So what would I actually do this week. First pick, Canva Craft. You probably already have Canva. Open Dream Lab, and spend a few of your uses on next month's specials poster and a price list. Compare the result with what you would have made by hand, and check every single word and every price before anything goes to print. Second pick, if you are on Google Workspace Business Standard or Google AI Pro, try Meet's speech translation. Set up a test call with a colleague, one of you speaking Afrikaans, and judge it honestly before you use it with a client. Do not use it for isiZulu or isiXhosa speakers yet; those languages are not supported. And if you were thinking about an AI phone line, start with after-hours calls only. That is the drop. The full written version, with every source, is on the WhatsApp channel. Follow it, and I will see you next Monday.

**ON-SCREEN TEXT**

```
WHAT I WOULD ACTUALLY TRY

1. CANVA CRAFT
Next month's specials poster.
Check every word and price.

2. GOOGLE MEET TRANSLATION
Test call in Afrikaans first.
Not for isiZulu or isiXhosa yet.

FX: R16.57 / USD (3 sources)

FULL WRITTEN VERSION ON THE WHATSAPP CHANNEL
Next drop: Monday
```

**B-ROLL / VISUAL**

Two numbered cards, building in sequence, accent colour. "Not for isiZulu or isiXhosa yet" in warning colour. FX line in smaller type at the bottom. Close on the WhatsApp channel CTA over Soul still A16 (Joburg skyline), slow push out, fade to black on the "Next drop: Monday" line.

---
