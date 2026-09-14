# AI Tools Drop - Video Script, 14 September 2026

**Episode 6. Target runtime 13 to 15 minutes. 16:9 primary, 9:16 cut-down derived from SEGMENTS 1, 4, 5 and 16.**

---

## PRODUCTION NOTES

- **Voice:** ElevenLabs voice ID `P1LmKcX63Ihgqy11sVRt` (Andrew, South African male).
- **Model:** `eleven_multilingual_v2`. Stability 0.60, similarity_boost 0.75, style 0.15, use_speaker_boost true. Output `mp3_44100_128`.
- **One API call per segment. Never batch segments into a single call.** Batching produces drifting pace and breaks the timing table.
- **All ON-SCREEN TEXT is ASCII-only.** No smart quotes, no em dashes, no ellipsis characters, no arrows. Run `ascii_fix.py` before render.
- **Numbers are written longhand in NARRATION and as digits in ON-SCREEN TEXT.** This is deliberate. Do not reconcile the two.
- **SEGMENT 16 (AI disclosure) must hold on screen for a minimum of five seconds and must not be cut for runtime.** If the edit runs long, trim SEGMENT 12 or SEGMENT 13 instead.
- Uncertain or unverified figures render in the warning colour `#E5533D`, not the accent colour.

### Pronunciation guide

| Written | Say |
| --- | --- |
| Desert Ant Labs | DEZ-ert Ant Labs |
| Relaticle | rel-AT-i-kul |
| Widgo | WIJ-oh |
| Typewise Nova | TYPE-wise NOH-vah |
| n8n | en-EIGHT-en |
| GoodLads | GOOD-lads |
| Cognition | kog-NISH-un |
| Devin | DEV-in |
| Loqua | LOH-kwah |
| Subanana | soo-bah-NAH-nah |
| AGPL | ay-gee-pee-EL |
| MCP | em-see-PEE |
| POPIA | poh-PEE-uh |
| Lelapa | leh-LAH-pah |
| Vulavula | voo-lah-VOO-lah |
| Injini | in-JEE-nee |
| AfriSLM | AF-ree-slim |
| Zurich | ZOO-rik |
| Samrand | SAM-rand |
| Cassava | kuh-SAH-vah |
| Stratos Lab | STRAT-oss Lab |
| Nairametrics | NY-rah-metrics |

---

## TIMING

| Segment | Title | Start | End |
| --- | --- | --- | --- |
| 1 | COLD OPEN | 0:00 | 0:37 |
| 2 | WHY THIS WEEK MATTERS | 0:37 | 1:20 |
| 3 | DESERT ANT LABS | 1:20 | 2:21 |
| 4 | RELATICLE | 2:21 | 3:24 |
| 5 | WIDGO | 3:24 | 4:27 |
| 6 | TYPEWISE NOVA | 4:27 | 5:35 |
| 7 | N8N | 5:35 | 6:36 |
| 8 | GOODLADS | 6:36 | 7:35 |
| 9 | COGNITION SWE-2 AND DEVIN | 7:35 | 8:39 |
| 10 | LOQUA | 8:39 | 9:33 |
| 11 | LIVE CAPTIONS BY SUBANANA | 9:33 | 10:32 |
| 12 | THE AFRICAN COMPUTE STORY | 10:32 | 11:20 |
| 13 | WHAT DID NOT LAUNCH | 11:20 | 12:23 |
| 14 | SIX FOR SIX ON POPIA | 12:23 | 13:06 |
| 15 | WHAT I WOULD ACTUALLY TRY | 13:06 | 14:11 |
| 16 | AI DISCLOSURE | 14:11 | 14:36 |
| 17 | CLOSE AND CALL TO ACTION | 14:36 | 15:12 |

---

## SEGMENT 1 - COLD OPEN (0:00 to 0:37)

**NARRATION**

Nine AI tools launched this week. If your requirement is that customer data stays inside South Africa, exactly two of them can honestly say yes, and both get there the same way. You host it yourself, or the model runs on the phone and never phones home. Not one vendor on this list offers African data residency. Meanwhile the money that would fix that did move this week. Twice. To Lagos, and to Cairo. So this is a defensive week. Two tools I would actually put my hands on, and one I would keep away from client work.

**ON-SCREEN TEXT**

```
9 LAUNCHES THIS WEEK
2 KEEP YOUR DATA IN SA
0 OFFER AFRICAN RESIDENCY
```

**B-ROLL / VISUAL**

Kling clip 1. Slow push in on a dark server rack, single amber status light pulsing, Johannesburg skyline visible soft-focus through a window behind it. Cut hard on "Twice" to a stylised Africa map with two amber pins landing on Lagos and Cairo, and a grey unlit pin over Johannesburg.

---

## SEGMENT 2 - WHY THIS WEEK MATTERS (0:37 to 1:20)

**NARRATION**

Here is the pattern I keep hitting. The tools are getting genuinely good. The local plumbing underneath them is not arriving at the same speed. This week that gap got loud enough to become the whole episode. Nine launches, and the best data posture of the lot belongs to a small Amsterdam outfit whose entire pitch is that nothing ever leaves the device. Not a policy promise. An architecture. The rand is at sixteen and eleven cents, and I will round to sixteen when I talk. Four sources, spread of nought point three seven percent, the tightest since I started this series. Everything I name has a verified launch date inside the last seven days.

**ON-SCREEN TEXT**

```
R16.11 TO THE DOLLAR
4 SOURCES, 0.37 PERCENT SPREAD
GOOGLE FINANCE EXCLUDED AGAIN
```

**B-ROLL / VISUAL**

Shotstack motion graphic. Four source cards fanning in with their rate values, converging on a single R16.11 figure in accent yellow. Google Finance card greys out and slides off frame left.

---

## SEGMENT 3 - DESERT ANT LABS (1:20 to 2:21)

**NARRATION**

Number one, and my pick of the week. Desert Ant Labs, out of Amsterdam, landed on the Product Hunt board on the tenth of September. Seven audio models, seven text, four vision, one software development kit across phones, web and embedded. All of them run on the device. The one that matters is called Redact. Twenty three million parameters, small enough to sit inside a mobile app, and its job is to strip personal information out of text before anything gets transmitted. Their privacy policy says inference data is never sent to them, and that is a different category of claim from we promise not to train on it. One is architecture. The other is a policy that can change on a Tuesday. Free up to a hundred thousand monthly active devices per platform. Now the honest part. There is no published paid price at all, so if you cross that line you are negotiating blind. And twenty seven languages, none of them ours.

**ON-SCREEN TEXT**

```
DESERT ANT LABS
On-device models, Amsterdam
FREE to 100,000 devices per platform
Redact: 23M params, strips PII on-device
LIMIT: no SA languages, no paid price published
```

**B-ROLL / VISUAL**

Soul still B2 (phone in hand, dark interior). Ken Burns slow push. Overlay a simple animated diagram: text with red PII blocks entering a phone outline, clean text exiting upward to a cloud icon, red blocks staying inside the phone. "no paid price published" renders in warning red.

---

## SEGMENT 4 - RELATICLE (2:21 to 3:24)

**NARRATION**

Second. Relaticle. An open source AI customer relationship manager under the AGPL licence, built to be self-hosted, which means the database can sit on a machine in Johannesburg and nobody needs to give you permission. Number six on the board on the eighth of September, version three point five point eight tagged on the twelfth. Be clear on what that launch was, though. An existing project with a year of history that ran a Product Hunt launch this week. Not a debut. Their privacy policy states they do not train on customer relationship data. And here is the catch most write-ups skipped. Self-hosting does not turn off the credit metering. Their own pricing page says so. Three hundred AI credits a month whether you host it or they do. So you control where the data lives, but not how much AI you get. Cloud Pro is nineteen dollars a month, about three hundred rand. Then enterprise starts at twenty thousand dollars a year. Nothing in between.

**ON-SCREEN TEXT**

```
RELATICLE
Self-hostable AI CRM, AGPL
Self-host FREE forever
BUT: 300 AI credits/mo even self-hosted
Cloud Pro $19/mo = approx R306
Enterprise from $20,000/yr = approx R322,200
```

**B-ROLL / VISUAL**

Shotstack. Split frame: left side a rack labelled "YOUR VPS, JOHANNESBURG" in accent yellow, right side a generic cloud labelled "LOCATION NOT NAMED" in warning red. Credit counter graphic ticking down 300 to 0 across both halves identically.

---

## SEGMENT 5 - WIDGO (3:24 to 4:27)

**NARRATION**

Third. Widgo. An AI sales representative that sits on your website, qualifies the visitor and hands off. Number two on the eighth of September, US company. I am putting it this high for a reason that has nothing to do with the product. Of all nine tools this week, Widgo's privacy policy is the clearest. It names the processing regions, US and EU. It names the subprocessors. It states outright that conversation content is not used to train foundation models. That is the standard I want to hold this list to, and most of them fail it. The free tier is real too. Five hundred sessions a month, no card. For a salon or a clinic taking booking enquiries after hours, which is when most enquiries actually arrive, that goes a long way. The limits. European residency on request only, no African option at all, and a brutal pricing cliff. Free, then two hundred and forty nine dollars, about four thousand rand. Nothing for the business doing six hundred sessions.

**ON-SCREEN TEXT**

```
WIDGO
AI sales rep for your website
FREE forever: 500 sessions/mo, no card
Growth $249/mo = approx R4,011
BEST disclosure of the week
LIMIT: EU residency on request, no Africa
```

**B-ROLL / VISUAL**

Soul still B6 (laptop on desk, warm interior). Overlay a checklist animating in with green ticks: "Regions named", "Subprocessors named", "No foundation model training". Then a fourth line in warning red: "No African region".

---

## SEGMENT 6 - TYPEWISE NOVA (4:27 to 5:35)

**NARRATION**

Fourth, and this one has a clock on it. Typewise, out of Zurich, launched Nova on the tenth of September, dated in their own press release, and took number one on Product Hunt. An AI customer experience operator, and the interesting part is not the model, it is the billing. You pay per resolution. A full resolution counts one, a partial counts a half, an unresolved ticket is free. The vendor carries the risk of their own product failing, which is rare enough to deserve rewarding. The data commitments are the strongest written ones of the week too. European or US hosting, customer data never used to train anyone's model, zero retention on the language model layer, Amazon Frankfurt named. Now the clock. The launch gift is a thousand resolutions plus three months with no base fee, no card, and it expires on the twentieth of September. Six days from today. The catch is that gift is a trial, not a free tier, and there is no African hosting option. Ask in writing which region a South African account lands on.

**ON-SCREEN TEXT**

```
TYPEWISE NOVA
Outcome billing: unresolved = FREE
LAUNCH GIFT EXPIRES 20 SEPT
1,000 resolutions + 3 months no base fee
No card required
Starter $99/mo = approx R1,595
```

**B-ROLL / VISUAL**

Kling clip 2. Countdown timer motif, amber digits over a dark support-desk scene. "EXPIRES 20 SEPT" pulses once in warning red. Then a Shotstack graphic: three ticket cards, two marked resolved with a price tag, one marked unresolved with "R0" stamped across it.

---

## SEGMENT 7 - N8N (5:35 to 6:36)

**NARRATION**

Fifth. n8n moved to a new minor line. Four releases inside the window, the tenth and eleventh of September plus a beta on the fourteenth. And there is a trap here. Stable is still two point three eight point seven. The two point three nine line is out but not tagged stable, and n8n's own changelog has no entry for it at all. Which means every feature description you read about this release from a third party is unverified. Do not put it on anything that matters yet. What n8n is for is the point, though. Self-hosted automation with a real node ecosystem. Run it locally and your automation data does not leave the country. In a week where no vendor offers African residency, that is the answer, and it is a boring answer. One detail to end on. Somebody in the community built a POPIA compliance grader as an n8n workflow template. A volunteer. Only POPIA artefact I found anywhere this week.

**ON-SCREEN TEXT**

```
n8n 2.39.x
4 releases 10 to 14 Sept
STABLE IS STILL 2.38.7
No vendor changelog entry for 2.39
Self-host free, priced in euros
Community POPIA grader template exists
```

**B-ROLL / VISUAL**

Shotstack. Version-number graphic: "2.39.5 BETA" in warning red above "2.38.7 STABLE" in accent yellow, with a dotted line between them. Then a node-graph animation of a workflow assembling itself, ending on a card reading "POPIA GRADER - COMMUNITY BUILT".

---

## SEGMENT 8 - GOODLADS (6:36 to 7:35)

**NARRATION**

Sixth. GoodLads. An AI growth manager for Google Ads, number seven on the eighth of September. It is here for the pricing structure, not the intelligence. Flat monthly fees instead of a percentage of ad spend. If you are a retailer putting thirty to eighty thousand rand a month into Google Ads, a fifteen percent agency cut is a great deal more than sixteen hundred rand, and a flat fee does not scale against you. There is a Product Hunt code for fifty percent off with no published expiry, which cuts both ways. The problems are on the paperwork side. The trial requires a card. No country is named anywhere in their privacy policy, so you do not know where your campaign data or customer lists are processed. And the training clause is worded narrowly, talking about generalised or non-personalised use, which is not a commitment not to train. Read it before you connect an ads account.

**ON-SCREEN TEXT**

```
GOODLADS
AI Google Ads manager
FLAT FEE, not percent of spend
Pro $100/mo = approx R1,611
Code MAKEITEASY = 50 percent off
LIMIT: card for trial, no country named
```

**B-ROLL / VISUAL**

Shotstack comparison bars. Left bar grows with ad spend labelled "15 PERCENT OF SPEND" in warning red. Right bar stays flat labelled "R1,611 FLAT" in accent yellow. Then a privacy-policy document graphic with a magnifier over an empty field labelled "COUNTRY: NOT NAMED".

---

## SEGMENT 9 - COGNITION SWE-2 AND DEVIN (7:35 to 8:39)

**NARRATION**

Seventh, and this is the warning item, so stay with me. Cognition released a software engineering model called SWE-2 on the tenth of September. Fifty percent on the FrontierCode benchmark, a real number and a strong position. And it is free in the Devin desktop app and command line tool through the tenth of October. Sounds excellent. Read the security documentation before you point it at a client repository. Devin's own documentation says that by default, they may use your data for model training purposes. The opt-out is available on paid plans. So on the free tier, the exact tier being promoted until October, your code is training data and you cannot switch that off without paying. Worst default of the nine. Their infrastructure is Amazon with no region named. And the line going around that it is sixty four percent cheaper than the competition is a Product Hunt tagline I could not verify anywhere. Throwaway projects, or pay the twenty dollars and turn the opt-out on. Not client work.

**ON-SCREEN TEXT**

```
COGNITION SWE-2 in DEVIN
50.0 percent FrontierCode 1.1
Free in Devin Desktop and CLI to 10 Oct
WARNING: free tier may train on your code
Opt-out is PAID PLANS ONLY
Pro $20/mo = approx R322
```

**B-ROLL / VISUAL**

Kling clip 3. Code scrolling on a dark monitor, then the frame washes with a warning-red vignette. Shotstack overlay: a toggle switch labelled "TRAINING OPT-OUT" shown greyed and locked with a padlock, captioned "PAID PLANS ONLY" in warning red. Hold on this longer than the other tool cards.

---

## SEGMENT 10 - LOQUA (8:39 to 9:33)

**NARRATION**

Eighth. Loqua. Voice dictation that reads what is on your screen to improve accuracy, which is a genuine step up on blind speech to text. Number two on the eleventh of September. Two things to know. First, this was a relaunch. The original announcement was a press release in July. Second, and this is the real issue, the marketing contradicts the policy. The pricing page claims never trained on your data and zero cloud data retention. The privacy policy says audio is sent to third parties including in the United States, and says nothing about training. When the sales page and the legal page disagree, the legal page binds you. Also there are no prices on the pricing page. Page is live, tiers listed, amounts absent. Free tier is five thousand words a week. Fine for drafting. Not for client or patient notes.

**ON-SCREEN TEXT**

```
LOQUA
Dictation with screen context
Free tier: 5,000 words/week
NO PRICES PUBLISHED on live pricing page
Pricing page: "never trained on your data"
Privacy policy: audio to US third parties, silent on training
```

**B-ROLL / VISUAL**

Shotstack split-screen document comparison. Left panel headed "PRICING PAGE" with the privacy claims in accent yellow. Right panel headed "PRIVACY POLICY" with the contradicting text in warning red. Animate a red line connecting the two contradicting statements.

---

## SEGMENT 11 - LIVE CAPTIONS BY SUBANANA (9:33 to 10:32)

**NARRATION**

Ninth, and last for a specific reason. Live Captions by Subanana, a Hong Kong company, real-time captioning, number five on the tenth of September. The published accuracy table covers fifty two languages. Swahili, at sixty one point eight percent, is the only African language on it. No Zulu. No Xhosa. No Afrikaans. No Sesotho. A multilingual captioning product with fifty two languages and none of ours deserves to be named plainly rather than politely. What they get right is infrastructure disclosure. Their security page names Amazon Singapore. You actually know where the data goes, which is rarer here than it should be. Singapore also means a long round trip for real-time work. Two more things. Live Captions is only on the top tier, fifty dollars a month, about eight hundred rand. And new individual accounts are opted in to training by default, while team accounts are opted out. If you sign up as an individual, change that setting first.

**ON-SCREEN TEXT**

```
LIVE CAPTIONS by SUBANANA
52 languages
1 AFRICAN LANGUAGE: Swahili 61.8 percent
No Zulu, Xhosa, Afrikaans, Sesotho
Live Captions is MAX TIER ONLY: $50/mo approx R806
Individual accounts opted IN to training
```

**B-ROLL / VISUAL**

Shotstack. Grid of 52 language chips filling the frame, all dim grey. One chip lights amber labelled "SWAHILI". Then four chips outlined in warning red with strikethroughs labelled "ZULU", "XHOSA", "AFRIKAANS", "SESOTHO". Hold.

---

## SEGMENT 12 - THE AFRICAN COMPUTE STORY (10:32 to 11:20)

**NARRATION**

Now the structural part, because it answers everything I have just said. African compute moved this week. Twice. Neither time here. Digital Parks Africa announced a data centre in Lagos on the eighth of September. They are a South African operator based at Samrand, and this is their first facility outside South Africa. What pushed it there was not opportunity, it was regulation. The Central Bank of Nigeria issued a payment data localisation mandate in June, full compliance by the first of January. A hard deadline created a market, and a South African company went and built for it. South Africa has no equivalent mandate. That is the entire difference. Cassava and Vodafone also announced Egypt's first national AI factory on the eighth, roughly a billion dollars.

**ON-SCREEN TEXT**

```
DIGITAL PARKS AFRICA: Lagos, 8 Sept
SA operator, first facility outside SA
Driver: CBN data localisation, deadline 1 Jan 2027
SA HAS NO EQUIVALENT MANDATE
CASSAVA + VODAFONE: Egypt AI factory, approx $1bn
```

**B-ROLL / VISUAL**

Soul still A16 (Johannesburg skyline). Overlay the stylised Africa map from SEGMENT 1, now animating: amber pin drops on Lagos with the date, second amber pin on Cairo, then the Johannesburg pin stays grey while a caption reads "NO MANDATE" in warning red.

---

## SEGMENT 13 - WHAT DID NOT LAUNCH (11:20 to 12:23)

**NARRATION**

Three things I had to leave out, and the omissions tell you as much as the list did. Lelapa AI added voice generation on the fifth of September. Two days outside my window, so out on the date rule, and out on a second rule too, because the coverage describes stated intent and the Vulavula release notes still stop at the twelfth of August. Sixth week running that has come up unresolved. Then the painful one. Tether TranslatePsy released AfriSLM, offline open source models covering nineteen African languages including Zulu, Xhosa, Afrikaans, Tswana and Sotho. Second of September, five days outside the window. Precisely the thing missing from every tool on this list, and my own date rule put it out. Go and look at it anyway. And Injini launched an AI for Education venture builder here on the ninth of September, applications open until the twenty seventh. Locally built, but an incubator, not a tool. If you are in education technology, put that date in your diary.

**ON-SCREEN TEXT**

```
OUT ON THE DATE RULE
Lelapa AI voice: 5 Sept, 2 days early
Also: no shipped artefact, release notes stop 12 Aug
Tether AfriSLM: 2 Sept, 19 African languages
Includes Zulu, Xhosa, Afrikaans, Tswana, Sotho
Injini AI for Education: 9 Sept, applications to 27 Sept
```

**B-ROLL / VISUAL**

Shotstack calendar graphic. Seven-day window highlighted in accent yellow, with three cards sitting just outside its left edge in warning red, each labelled with its date. The AfriSLM card enlarges and the five South African language names animate in underneath it.

---

## SEGMENT 14 - SIX FOR SIX ON POPIA (12:23 to 13:06)

**NARRATION**

Sixth week of this series. Sixth week that not one vendor I have covered has published anything referencing POPIA. Every privacy policy, every data processing agreement, every security page for all nine tools, plus searches across fourteen domains. Nothing. A volunteer got there before any vendor did. Two more honest notes. Five of these vendors' privacy paths returned errors, and two have no pricing page at all. And the two biggest South African technology publications render their AI sections completely without dates, which makes it impossible to filter them against a seven day rule. That is the largest gap in this week's coverage and I would rather flag it than pretend it is not there.

**ON-SCREEN TEXT**

```
POPIA MENTIONS BY VENDORS: 0
Six weeks. Six zeros.
9 vendors checked, 14 domains searched
Only POPIA tool: a community n8n template
5 vendor privacy pages returned errors
SA tech press AI sections render undated
```

**B-ROLL / VISUAL**

Shotstack. Six large zeros animating in sequence, each labelled with a week date, all in warning red. Then a single accent-yellow card reading "1 COMMUNITY TEMPLATE" appearing beneath them.

---

## SEGMENT 15 - WHAT I WOULD ACTUALLY TRY (13:06 to 14:11)

**NARRATION**

Two things, and one warning. First, Desert Ant Labs Redact. Free to a hundred thousand devices, runs on the phone, and the data genuinely does not leave. For an immigration or fintech intake flow, stripping personal information on the client's device before upload changes the shape of your compliance problem instead of just documenting it. Missing South African languages is a real limitation, but detecting personal information on an identity document or a payslip is mostly structural, not idiomatic. Start with one form. Second, Typewise Nova, before the twentieth of September. A thousand resolutions plus three months with no base fee, no card. Six days. Unresolved tickets are free under their model, so a real test costs you nothing and still tells you something. Get their answer in writing on whether a South African account lands on European or US hosting. And the warning. The Devin free tier. Strong model, free until October, and on that plan your code may become training data with the opt-out locked behind payment. Throwaway repositories, or pay.

**ON-SCREEN TEXT**

```
WHAT I WOULD ACTUALLY TRY
1. DESERT ANT REDACT - free, on-device, start with 1 form
2. TYPEWISE NOVA - before 20 Sept, no card
CAREFUL WITH: Devin free tier
Free plan may train on your code
```

**B-ROLL / VISUAL**

Shotstack. Two clean numbered cards in accent yellow sliding in, then a third card in warning red with a caution outline. Kling clip 4: a hand putting a phone face down on a desk, slow, deliberate, as the Redact point lands.

---

## SEGMENT 16 - AI DISCLOSURE (14:11 to 14:36)

**NARRATION**

Before I close. The visuals in this video are AI generated and the voice you are hearing is an AI voice. The research, the pricing, the dates and the opinions are mine, and every figure I quoted is linked to its source in the written version.

**ON-SCREEN TEXT**

```
AI DISCLOSURE
Visuals: AI generated
Voice: AI generated
Research, pricing and opinions: human
Sources linked in the written article
```

**B-ROLL / VISUAL**

Static Shotstack card, minimal, high contrast. **Must hold a minimum of five seconds. Do not trim this segment for runtime.** No motion, no music swell.

---

## SEGMENT 17 - CLOSE AND CALL TO ACTION (14:36 to 15:12)

**NARRATION**

That is the week. Nine launches, two that keep your data where you can see it, one to keep away from client work, and a compute story that moved everywhere except here. The full written version has every price in rand, every source link and the honest gaps spelled out. Link below. The WhatsApp channel is where this lands first every Monday morning, and where I put the things too small for a video. Come and join it. Next week I will still be counting POPIA mentions, and I would genuinely like to stop at six.

**ON-SCREEN TEXT**

```
JOIN THE WHATSAPP CHANNEL
Every Monday, 11am SAST
Full written version: link below
```

**B-ROLL / VISUAL**

Kling clip 5. Slow pull back from the Johannesburg skyline at dusk, lights coming on. Shotstack end card with the WhatsApp channel call to action in accent yellow, held to the end of the audio.

---
