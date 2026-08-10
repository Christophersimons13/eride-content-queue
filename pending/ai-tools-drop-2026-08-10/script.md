# AI Tools Drop - Video Script
## Week of 4 to 10 August 2026

**Target runtime:** 13 minutes
**Narration word count:** approximately 1,950
**Voice:** ElevenLabs, South African male, conversational, unhurried
**Aspect:** 16:9, 1920x1080

All ON-SCREEN TEXT below is ASCII-safe. No smart quotes, no em dashes, no ellipsis characters. Do not let any editor auto-correct these strings.

---

### 0:00 - 0:30 | Cold open

**NARRATION**

The free version of ChatGPT no longer has a daily limit. That is not a promotion, it is not a trial, it is just gone. And separately, this week, ElevenLabs opened up their dubbing engine as an API, and Afrikaans is in the supported language list. So if you have made one video in English, you can now make it in Afrikaans without re-shooting anything. That is two things in one week that actually change what a small South African team can do. Ten launches this week. Let me take you through them.

**ON-SCREEN TEXT**
```
AI TOOLS DROP
Week of 4 to 10 August 2026
10 launches. Verified dates. SA pricing.
```

**B-ROLL / VISUAL**
Dark background, hex 111111. Yellow accent bar, hex F5C542, wipes in from the left. Title text in white. Hold three seconds, then cut to a fast montage of the ten product logos as a three-by-four grid, each tile lighting up in sequence over five seconds.

---

### 0:30 - 1:30 | Why this week matters

**NARRATION**

Quick context before we start. Every tool on this list launched or shipped a major update between the fourth and the tenth of August. Nothing older. I check the dates against the vendor's own page, and if I cannot verify it, it does not make the list. Two things got cut this week purely because their pricing pages would not resolve, and I will tell you which ones at the end.

One more thing worth mentioning. The rand firmed over the week, from about sixteen fifty to the dollar on Monday down to sixteen thirteen by Friday. Every dollar subscription I quote today is about two percent cheaper than it would have been last week. I am working off sixteen rand twenty for the conversions, but check the live rate before you commit to anything annual.

Now, the shape of this week. Two entries at the top that matter to almost everyone. Then a middle block of content and marketing tools. Then three developer tools, which are genuinely useful if you build software and completely irrelevant if you do not. And three of the ten are priced or gated in ways that make them a hard sell for a small business here. I will say so each time rather than pretending everything is a win.

**ON-SCREEN TEXT**
```
THE RULES
Launched 4 to 10 August 2026 only
Dates verified against vendor pages
Prices in USD and ZAR at R16.20
Limitations stated, not hidden
```

**B-ROLL / VISUAL**
Motion graphic. Four rules stack in one at a time, each with a yellow tick. Then a simple line chart showing USD to ZAR falling from 16.50 to 16.13 across the week, labelled with the two end values only. Keep the chart on screen for four seconds.

---

### 1:30 - 3:00 | Tool 1: ChatGPT August update

**NARRATION**

Start with the one that affects everybody. On the sixth of August OpenAI shipped the GPT five point six August update, and the headline for us is that free accounts now get unlimited text chats. No daily cap. The default model on the free tier is now Luna, and the reported accuracy improvement is significant, sixty two percent fewer factual errors than the previous free model.

Here is why that matters practically. If you have staff who hit the ChatGPT limit at eleven in the morning and then just stop using it for the rest of the day, that problem disappeared this week at no cost to you. And if you have people on a twenty dollar Plus seat, that is about three hundred and twenty four rand a month, who only ever type text prompts, you should probably go and look at whether they still need it.

The limitations are real though. Free users get Luna, not the flagship Sol model. There is a Think button that gives Luna more time to reason, but it does not upgrade you to the better model. Unlimited applies to text only, so file uploads, image generation and voice all keep their own separate limits. And the rollout is staggered, so what you see in your account this morning might not match what I am describing.

If your team works in Codex or ChatGPT Work, this release does nothing for you. OpenAI said explicitly that both are unchanged.

**ON-SCREEN TEXT**
```
1. CHATGPT AUGUST UPDATE
6 August 2026

GOOD: Free tier now unlimited text chats
GOOD: 62 pct fewer factual errors on Luna
WATCH: Free gets Luna, not flagship Sol
WATCH: Text only. Uploads and voice still capped

Free / Go USD 8 (R130) / Plus USD 20 (R324)
```

**B-ROLL / VISUAL**
Screen recording of the ChatGPT interface, cursor moving to the model selector. Then cut to a motion graphic comparing the old daily cap as a filling bar that stops, versus the new state as a bar with no ceiling. Then the pricing card.

---

### 3:00 - 4:30 | Tool 2: ElevenLabs Dubbing API

**NARRATION**

This is my pick of the week and I want to explain why properly.

On the sixth of August ElevenLabs opened their dubbing model as an API. It takes audio in one language and returns audio in another, and critically it works audio to audio rather than transcribing, translating and then re-synthesising. That is why the emotion survives. The speaker still sounds like themselves. Ninety plus languages, and Afrikaans is in the table.

Think about what that means for a country with eleven official languages. You record one client explainer video. You dub it into Afrikaans. Same voice, same warmth, no second shoot, no second voice artist, no second booking fee. For an immigration practice, or a wellness brand, or anyone whose clients are more comfortable in a language other than English, that is not a marginal improvement.

Now the honest part. The API is in alpha. Output is audio only, so you still need an editor to put it back over the video. Free tier dubs come out watermarked. And the model itself is not new, it shipped inside their creative product back in May. What is new is programmatic access, which matters if you want this inside a pipeline rather than clicking around in a browser.

On price, the free tier gives you ten thousand credits a month. Starter is six dollars, about ninety seven rand, and that is the tier that adds the commercial licence. Per minute dubbing rates I could only find second hand, reported at thirty three cents a source minute watermarked, so treat that as unconfirmed until ElevenLabs publish it themselves.

**ON-SCREEN TEXT**
```
2. ELEVENLABS DUBBING API
6 August 2026

GOOD: Afrikaans supported. 90 plus languages
GOOD: Audio to audio. Emotion survives
WATCH: Alpha. Audio only, not finished video
WATCH: Free tier output is watermarked

Free 10k credits / Starter USD 6 (R97)
```

**B-ROLL / VISUAL**
Waveform animation. One waveform on the left labelled ENGLISH, an arrow, a second waveform on the right labelled AFRIKAANS, both pulsing in sync to show the emotion is preserved. Then a scrolling list of supported languages with Afrikaans highlighted in yellow as it passes.

---

### 4:30 - 5:45 | Tool 3: Keystroke

**NARRATION**

Keystroke launched on the fifth of August out of Y Combinator, and the pitch is simple. It is what n8n would be if it were built for people who write code. Your AI agents and automation workflows live as TypeScript in your own repository, version controlled, reviewable in a pull request, and then deployed to a managed web app.

If your stack is already GitHub and Vercel, this slots in naturally. Over a thousand integrations, plus any REST API or MCP server. Memory, filesystem, code execution, web search, triggers, schedules, webhooks and approvals are all built in rather than bolted on. And the code is public on GitHub, so you are not locked into the hosted version.

Three caveats. It is an open alpha, so expect things to break. The licence is Elastic License two point zero, which is source available rather than genuinely open, and it carries commercial hosting restrictions, so read them if you were planning to build a product on top. And it assumes TypeScript, which means your non-technical ops person cannot pick this up the way they could with n8n's drag and drop canvas.

Free Hobby tier with about a hundred agent runs a month and a ten minute timeout. Pro is twenty dollars, about three hundred and twenty four rand.

**ON-SCREEN TEXT**
```
3. KEYSTROKE
5 August 2026

GOOD: Agents as TypeScript in your own repo
GOOD: 1000 plus integrations. Self hostable
WATCH: Open alpha. Elastic License 2.0
WATCH: Needs TypeScript. Not for non coders

Free Hobby / Pro USD 20 (R324)
```

**B-ROLL / VISUAL**
Split screen. Left side shows a typical drag and drop automation canvas with connected nodes. Right side shows the same logic as clean TypeScript in a code editor. Then a GitHub pull request diff view scrolling slowly.

---

### 5:45 - 6:45 | Tool 4: Aveiro

**NARRATION**

Aveiro launched on the sixth of August. It is a publishing workspace, so website, blog and newsletter in one subscription, with AI agents drafting and a human approving before anything goes live. ChatGPT, Claude or Cursor can write directly into it over MCP.

The appeal is consolidation. If you currently run WordPress plus Mailchimp plus something else, this is one bill and one place. Subscriber list, campaigns and analytics are bundled. Custom domain and branding removal are available even on the trial.

But read the pricing page carefully. What they call the Free plan is a fourteen day trial, and when it ends your live site pauses until you upgrade. That is a meaningful difference and the page does not lead with it. The trial caps are tight too, one site, ten pages, one editor, a thousand AI credits. Social publishing is mostly marked coming soon. And it is brand new with no track record.

Starter is twelve dollars, about a hundred and ninety four rand.

**ON-SCREEN TEXT**
```
4. AVEIRO
6 August 2026

GOOD: Site, blog, newsletter in one subscription
GOOD: Agents draft via MCP. Human approves
WATCH: Free is a 14 day trial, not a free tier
WATCH: Site pauses when trial ends

Starter USD 12 (R194) / Creator USD 29 (R470)
```

**B-ROLL / VISUAL**
Three tool logos, WordPress-style CMS, an email tool and an analytics tool, collapsing into a single Aveiro tile. Then a calendar graphic counting down fourteen days, with the final frame showing a greyed out website and the words TRIAL ENDED.

---

### 6:45 - 7:45 | Tool 5: AdAnt AI

**NARRATION**

AdAnt took the number one spot on Product Hunt for the fifth of August. It is creative agents for social video ads, TikTok, Instagram, YouTube. What separates it from generic video generators is that competitor and viral pattern research feeds directly into the ad creation, so it is not producing in a vacuum. You store your brand positioning and assets as a product profile and reference them inline, which keeps output consistent across campaigns. Over a hundred AI avatars, no watermark on paid output.

The catch is credits. Thirty nine dollars a month, about six hundred and thirty two rand, is reported to buy only a hundred and fifty credits, and video burns credits fast. The announced ChatGPT and Claude plugins have not actually shipped. And be aware there is a done for you Studio tier with a five thousand dollar monthly minimum, which is irrelevant to you but I would rather you know it exists before it comes up in a sales call.

Good fit if you are a salon, a wellness brand or a retailer who needs weekly social video and currently pays a freelancer per asset.

**ON-SCREEN TEXT**
```
5. ADANT AI
5 August 2026

GOOD: Competitor research feeds the creative
GOOD: 100 plus avatars, no watermark on paid
WATCH: Credit based. USD 39 buys about 150
WATCH: Announced plugins not shipped yet

USD 39 per month (about R632)
```

**B-ROLL / VISUAL**
Vertical phone frame in the centre playing three fast ad variants of the same product. Then a credit counter graphic draining from 150 as short clips render.

---

### 7:45 - 8:45 | Tool 6: Wispr Flow Notetaker

**NARRATION**

Released the fifth of August. It is a meeting notetaker that does not join your call as a participant. Instead it captures your Mac system audio directly. No awkward moment where a client asks who the extra person in the meeting is. Speaker identification pulls from your calendar, Gmail and Slack. Notes are readable from Claude, ChatGPT or Cursor over MCP. Works across Meet, Zoom, Teams, Slack huddles and in person.

Genuinely good product, and I still cannot fully recommend it here, for two reasons. It is macOS fourteen point four and up only, no Windows at launch. And the notetaker is English only. Their dictation feature does a hundred plus languages, but the notetaker does not, and if your meetings drift between English and Afrikaans or isiZulu, which most Johannesburg meetings do, that is a real limitation.

One more thing. Processing is cloud, not on device. If you handle POPIA sensitive client conversations, think that through before you switch it on. And the free plan has a weekly meeting cap that Wispr do not publish, which is an odd thing to leave off a pricing page.

Free tier exists. Pro is fifteen dollars a user, about two hundred and forty three rand.

**ON-SCREEN TEXT**
```
6. WISPR FLOW NOTETAKER
5 August 2026

GOOD: No bot joins the call
GOOD: Speaker ID from calendar and email
WATCH: macOS 14.4 plus only. No Windows
WATCH: English only. Cloud processing

Free tier / Pro USD 15 per user (R243)
```

**B-ROLL / VISUAL**
Video call grid with four participants. A fifth tile labelled NOTETAKER BOT appears, then is struck through and removed. Then a clean transcript scrolling with speaker names attributed in yellow.

---

### 8:45 - 9:45 | Tool 7: Cloudflare OS

**NARRATION**

Cloudflare announced this on the fourth of August. It is an open source, browser based agent workspace that runs inside your own Cloudflare account, Apache two point zero licensed, genuinely self hostable.

The part I want you to notice is not the workspace, it is the governance. Agents start with zero access and are granted capabilities explicitly, one at a time. Most agent platforms start permissive and hope. This one starts locked. And it is model agnostic through Cloudflare's AI Gateway with per person, per team and per app spend visibility, budgets and rate limits. If you have watched agent spend get away from you, that budgeting layer is arguably the actual product here.

Caveats. The README calls it early access with many rough edges. There is no hosted version yet. There are community reports, not confirmed by Cloudflare, that Dynamic Workers need a paid Workers plan, which would undercut the free and open framing, so verify that before you plan around it. And setting this up is a real engineering exercise, not an afternoon.

Software is free. Underlying Workers costs apply.

**ON-SCREEN TEXT**
```
7. CLOUDFLARE OS
4 to 5 August 2026

GOOD: Agents start with zero access by default
GOOD: Per team AI spend budgets and limits
WATCH: Early access. No hosted version yet
WATCH: Paid Workers plan requirement unconfirmed

Apache 2.0. Workers costs apply
```

**B-ROLL / VISUAL**
Animated permission model. A central agent node surrounded by greyed out capability tiles, each lighting up individually as a hand-drawn tick is applied. Then a spend dashboard with three team bars filling toward a budget line.

---

### 9:45 - 10:45 | Tool 8: Meta Muse Code

**NARRATION**

Meta launched Muse Code in beta on the fifth of August, a terminal coding agent for large codebases running on their new Muse Spark one point two model. Benchmarks are strong, eighty two point nine percent on Terminal Bench two point one, one million token context window. Background sub agents run in isolated git worktrees so parallel work does not collide.

Now listen carefully to this part, because it is the reason this tool is at number eight and not number three. There is a cheap contributor tier, and on that tier Meta trains on your prompts and your completions, and your rate limit drops from three thousand requests a minute to sixty. The price gap between contributor and standard is roughly twelve to one. That is exactly the kind of gap that makes someone click the wrong button on a Friday afternoon.

If you write client code under an NDA, the contributor tier is unusable. Not a nuance, a hard line. Contributor access is also restricted to selected countries and I could not confirm whether South Africa is one of them.

macOS and Linux only. No free tier, token priced. Standard is one dollar twenty five per million input tokens, about twenty rand, and four dollars twenty five per million output, about sixty nine rand.

**ON-SCREEN TEXT**
```
8. META MUSE CODE
5 August 2026 (beta)

GOOD: 82.9 pct Terminal Bench 2.1
GOOD: 1M context. Parallel git worktrees
WATCH: Contributor tier trains on your prompts
WATCH: macOS and Linux only. SA access unconfirmed

Standard USD 1.25 per M in (R20) / 4.25 out (R69)
```

**B-ROLL / VISUAL**
Terminal window with an agent working through a large repo, text scrolling. Then hard cut to a full-screen warning card, background hex E5533D, white text reading CONTRIBUTOR TIER TRAINS ON YOUR CODE. Hold two and a half seconds. This is the one moment in the video that should feel like a stop sign.

---

### 10:45 - 11:35 | Tool 9: Omniwork

**NARRATION**

Omniwork was Product Hunt's Launch of the Day on the ninth of August. It is a desktop app with specialist agents for research, scripts, images, video editing, music and social posting, so the whole content pipeline in one place instead of five tools stitched together. Over a hundred agents available even on the free tier.

Two problems. The free tier allows five deep tasks a month, which is enough to try and not enough to use. And the pricing page contradicts itself on the Pro tier, saying roughly ninety deep tasks a month in one place and thirty plus in a bullet on the same page. Get that clarified in writing before you subscribe, because at sixty nine dollars a month, about eleven hundred and eighteen rand, it is a hard sell against AdAnt at thirty nine or Aveiro at twelve unless you genuinely need the full pipeline.

**ON-SCREEN TEXT**
```
9. OMNIWORK
9 August 2026

GOOD: Whole content pipeline in one desktop app
GOOD: 100 plus agents on the free tier
WATCH: Free tier is 5 deep tasks per month
WATCH: Pricing page contradicts itself on Pro

Free Starter / Pro USD 69 (about R1118)
```

**B-ROLL / VISUAL**
Desktop app interface with an agent sidebar. Then a side by side of the two contradictory pricing statements, both highlighted in yellow with a question mark between them.

---

### 11:35 - 12:20 | Tool 10: Rindler

**NARRATION**

Last one. Rindler launched the seventh of August and it automates browser tasks on login gated sites, which is exactly where generic automation falls apart. It returns structured records rather than raw page content, and the billing is honest, one run equals one completed task equals one dollar, and failed runs are not charged.

The immigration use case writes itself. If your staff spend hours logged into Home Affairs and VFS portals doing repetitive lookups, this is aimed straight at that. But I have to be straight with you, whether it copes with South African government portals specifically is completely untested.

And the price floor is the highest on this list. A hundred dollars a month minimum, about sixteen hundred and twenty rand, with no cheaper tier. Starter covers one custom site, so a second portal pushes you to a thousand dollars a month. And billing is annual, billed monthly, which is a year long commitment presented as a monthly plan. Read it that way.

Only worth it if you can name the portal, count the hours it eats, and the maths clears sixteen hundred rand a month.

**ON-SCREEN TEXT**
```
10. RINDLER
7 August 2026

GOOD: Handles login gated portals
GOOD: Pay per successful run. Failures free
WATCH: USD 100 per month floor. No cheaper tier
WATCH: Annual commitment. SA portals untested

Starter USD 100 (about R1620) per month
```

**B-ROLL / VISUAL**
Browser window auto-filling a login form, then navigating a portal, then output resolving into a clean data table. Then a calculator graphic showing hours saved multiplied by an hourly rate against the R1620 line.

---

### 12:20 - 13:00 | Close and CTA

**NARRATION**

So. Two things I would actually do this week.

First, take the ElevenLabs dubbing API on the free tier, take one video you have already made, and dub it into Afrikaans. Listen to whether the tone survives. It costs nothing to find out, and if it works you have doubled the audience for every piece of content you already own.

Second, and this is the rare week where the advice is to spend less, go and audit who on your team is still paying for a ChatGPT seat they no longer need. The free tier is unlimited on text now. Keep Plus for the people who genuinely need uploads, images or voice.

Two I left out this week on pricing grounds, Soloop and Hey Noah, both interesting, neither with a pricing page I could verify. And one local note, Discovery published a genuinely useful piece on why they are going slow on AI coding agents, twenty to twenty five percent efficiency gains but no rush. Worth reading if you ever pitch AI tooling into a big South African corporate.

Full written version with every source link is in the description and on the WhatsApp channel. That is where this lands first every Monday morning. Link is below. See you next week.

**ON-SCREEN TEXT**
```
THIS WEEK, DO TWO THINGS

1. Dub one video into Afrikaans. Free tier.
2. Audit your paid ChatGPT seats.

FULL WRITTEN VERSION + ALL SOURCES
Join the WhatsApp channel
New drop every Monday, 11am SAST
```

**B-ROLL / VISUAL**
Return to the dark background. The two actions animate in as numbered cards. Then the end card with the WhatsApp channel QR code centre frame, held for eight seconds. Yellow accent bar closes across the bottom.

---

## AI disclosure

An on-video disclosure lower third must appear from 0:03 to 0:11 reading:

```
This video uses AI generated visuals and an AI voice.
```

Platform-level AI disclosure must also be set at upload on YouTube, Facebook, TikTok and Instagram.

---

## Pronunciation guide for ElevenLabs

Feed these as SSML phoneme hints or spell them phonetically in the input text where the voice mangles them on the first pass.

| Written | Say it as |
| --- | --- |
| Aveiro | ah-VAY-roh |
| AdAnt | AD-ant |
| Wispr | WISS-per |
| Rindler | RIND-ler, rhymes with kindler |
| Omniwork | OM-nee-work |
| Keystroke | KEY-stroke |
| Muse Spark | MYOOZ spark |
| ElevenLabs | eleven labs, two words, no pause |
| n8n | en-eight-en |
| MCP | em-see-pee, letters |
| POPIA | po-PEE-ah |
| VFS | vee-eff-ess, letters |
| Qwen | CHWEN |
| Soloop | SOH-loop |
| GPT-5.6 | gee-pee-tee five point six |
| Terminal-Bench 2.1 | terminal bench two point one |
| Apache 2.0 | apache two point oh |
| Afrikaans | af-ri-KAHNS |
| isiZulu | ee-see-ZOO-loo |
| Disrupt Africa | disrupt africa, no pause |

Voice settings: stability 0.60, similarity boost 0.75, style 0.15, speaker boost on. Model eleven_multilingual_v2. Output mp3_44100_128.
