# AI Tools Drop - Week of 5 October 2026

Episode 9. Window: 28 September to 5 October 2026. Written for South African founders and small businesses.

Rand figures use **R16.67 to the dollar**, the midpoint of [XE](https://www.xe.com/currencyconverter/convert/?Amount=1&From=USD&To=ZAR) (16.6702 at 09:07 UTC on 5 October) and [Trading Economics](https://tradingeconomics.com/south-africa/currency) (16.6692 at the same time). Only two sources returned a readable rate this week. The rand is about 1.5 percent weaker than last week's R16.43.

---

## This week in one paragraph

A busy week, and an unusually practical one. ElevenLabs shipped a new voice model that lists Afrikaans and Swahili but not isiZulu or isiXhosa, at a 72 percent launch discount that ends on 12 October. Meta started charging for WhatsApp Business replies sent through the API from 1 October, which matters to anyone running a WhatsApp bot. Shopify gave merchants a way to design a store by chatting with its AI. OpenAI's DevDay on 29 September brought a cheaper flagship-class model, always-on agents called Dots, and the start of an office suite. Cloudflare and Amazon released small "decision models" that pick an answer from a list instead of writing text, which suits routing and triage. Microsoft and Suno shipped speech tools, and ChatGPT added a virtual try-on button. Two big launches are not usable from South Africa yet - Google's Gemini 4 Argon and Meta's Muse for Small Business - and I have put them in a separate "not for us yet" section rather than the main list. Nine items made the list; one of them is a pricing change, not a tool.

---

## 1. Eleven v4 - a new ElevenLabs voice model, cheap for one more week

**What it is.** ElevenLabs announced [Eleven v4 and Eleven v4 Turbo on 28 September](https://elevenlabs.io/blog), describing them as bringing "emotional nuance, faster response times, and stronger voice cloning to text-to-speech", available across ElevenAgents, ElevenCreative and the API. The [model documentation](https://elevenlabs.io/docs/overview/capabilities/text-to-speech/eleven-v4) calls v4 "a net upgrade over Eleven v3, delivering better results in almost every case", with Turbo built for real-time agents.

**What it is good at.** Expressive narration and voice agents. The [API pricing page](https://elevenlabs.io/pricing/api) lists 90-plus languages and roughly 100 ms latency for Turbo, against 29 languages for the older Multilingual v2 model.

**Honest limitations.** The [v4 language list](https://elevenlabs.io/docs/overview/capabilities/text-to-speech/eleven-v4) includes Afrikaans and Swahili, but isiZulu, isiXhosa, Sesotho and Setswana are not on it. The same page says Style and Speed sliders are unavailable and SSML is not supported. Professional Voice Clone support was still "rolling out" when I read it.

**South African use cases.**
- Afrikaans and English explainer videos for a professional-services firm.
- A voice agent for after-hours bookings at a salon or clinic, in English.
- Swahili voiceovers for agencies with East African clients.

**Industries.** Agency and creative work, beauty and wellness, professional services, SaaS.

**Pricing.** The [API pricing page](https://elevenlabs.io/pricing/api) shows v4 at $0.022 per 1,000 characters (about R0.37) until 12 October, against a list price of $0.08 (about R1.33). [ElevenLabs on X](https://x.com/ElevenLabs/status/2104572138347004161) put Turbo at $11 per million characters (about R183) during the same two weeks. The [blog banner](https://elevenlabs.io/blog) adds "3x credits included on Creator+ until October 12".

**Access notes.** Same account and card process as current ElevenLabs plans. No South African restriction is stated.

**Link.** [elevenlabs.io/docs - Eleven v4](https://elevenlabs.io/docs/overview/capabilities/text-to-speech/eleven-v4)

---

## 2. WhatsApp Business Platform - replies are no longer free (pricing change, not a tool)

**What it is.** From 1 October 2026, [Wati's summary of the change](https://support.wati.io/en/articles/16954666-whatsapp-business-platform-api-pricing-changes-service-messages-and-click-to-message-ads) says "service messages, including free-form replies sent within the 24-hour customer service window, will be billed per message", and utility templates inside that window become billable again.

**Why it matters.** Any business running a WhatsApp chatbot or helpdesk through a provider such as Wati or 360dialog now pays for replies once the free allowance runs out. Wati says Meta provides 1,000 free service messages per month and that click-to-WhatsApp ad conversations get a free window of up to seven days from 28 September.

**Honest limitations.** I could not get the official Meta pricing page to load the new rules, so this rests on provider and press summaries. They disagree on one point: [Wati](https://support.wati.io/en/articles/16954666-whatsapp-business-platform-api-pricing-changes-service-messages-and-click-to-message-ads) says the 1,000 free messages are per WhatsApp Business Account, while [Business Standard](https://www.business-standard.com/world-news/whatsapp-business-pricing-changes-from-today-what-indian-firms-should-know-126100100165_1.html) says per phone number. I did not find the South African rate. Wati says the service rate equals the local utility-template rate.

**The good news.** Wati says the change applies to the API, and the free WhatsApp Business app used without the API "is not affected".

**South African use cases.**
- An immigration consultancy answering document queries through a bot should count last month's replies.
- A retailer running click-to-WhatsApp ads can lean on the seven-day free window.

**Industries.** Every SMB that uses a WhatsApp API provider.

**Pricing.** Per message after the allowance. The SA rate was not confirmed.

**Link.** [Wati - WhatsApp Business Platform pricing changes](https://support.wati.io/en/articles/16954666-whatsapp-business-platform-api-pricing-changes-service-messages-and-click-to-message-ads)

---

## 3. Shopify Canvas - design your store by chatting with Sidekick

**What it is.** [TechCrunch reported on 1 October](https://techcrunch.com/2026/10/01/shopify-debuts-canvas-a-way-to-build-online-stores-by-chatting-with-ai/) that Canvas "lets merchants set up their Shopify store by chatting with AI". You talk to Sidekick, Shopify's AI agent, and it edits the theme's real files while you watch. The [Shopify changelog](https://changelog.shopify.com/) dates the entry 1 October.

**What it is good at.** Getting a custom-looking store without paying a developer. TechCrunch says you can test full interactivity and view pages across screen sizes, and still click elements to edit directly.

**Honest limitations.** [TechCrunch](https://techcrunch.com/2026/10/01/shopify-debuts-canvas-a-way-to-build-online-stores-by-chatting-with-ai/) says "third-party theme support, app blocks and extensions, markets, translations, rollouts, and theme updates are all not part of the initial launch", and Canvas is desktop-only. Multi-language or multi-currency stores should wait.

**South African use cases.**
- A Joburg skincare brand reworking its product pages before the festive season.
- A small fashion label building a lookbook page without an agency.
- An agency doing quicker first drafts for Shopify clients.

**Industries.** Retail, beauty, agency work.

**Pricing.** No Canvas price was stated. Per [eSEOspace's summary of Shopify's help pages](https://eseospace.com/blog/shopify-sidekick-and-magic/), Sidekick "is included with your plan". Treat that as likely rather than confirmed for Canvas.

**Access notes.** Shopify operates in South Africa. No country restriction was stated for Canvas.

**Link.** [Shopify changelog](https://changelog.shopify.com/)

---

## 4. GPT-6.1 Sol and the Decisions API - OpenAI DevDay, for builders

**What it is.** At DevDay on 29 September, OpenAI's [recap](https://openai.com/index/devday-2026-recap/) described GPT-6.1 Sol as "a major upgrade to GPT-6 Sol with exceptionally strong performance on agentic coding" that "delivers near-Astra intelligence to everyone at a fifth of its standard input and output token prices". It replaces GPT-6 Sol, which I covered last week.

**What it is good at.** Coding agents and long documents. [DataCamp](https://www.datacamp.com/blog/gpt-6-1-sol) reports a 1,050,000-token context window.

**The Decisions API.** The [recap](https://openai.com/index/devday-2026-recap/) says it focuses Luna "on a specific set of user-defined questions with finite pre-defined answers" - classify, route, choose. It is "available in limited preview".

**Honest limitations.** [OpenAI's GPT-6.1 Sol page](https://openai.com/index/introducing-gpt-6-1-sol/) says it is in ChatGPT Work and Codex for Plus, Pro, Business, Enterprise and Edu, and "not yet available in Chat". [eesel](https://www.eesel.ai/blog/openai-decisions-api-pricing) reported on 2 October that no Decisions API price had been published.

**South African use cases.**
- A SaaS team pointing Codex at a messy codebase.
- A fintech using decisions to route support tickets once pricing is public.

**Industries.** SaaS building, fintech, professional services.

**Pricing.** [OpenAI's pricing page](https://openai.com/api/pricing/) lists $2 per million input tokens (about R33), $0.10 cached (about R1.67) and $10 output (about R167).

**Link.** [OpenAI - Introducing GPT-6.1 Sol](https://openai.com/index/introducing-gpt-6-1-sol/)

---

## 5. Dots, Space and Pages - ChatGPT moves into the office

**What it is.** [TechCrunch](https://techcrunch.com/2026/09/29/openai-launches-dots-its-bubbly-agentic-avatar/) describes Dots as "a new personal agentic assistant" that pursues goals "continuously in the background with minimal oversight", reachable through Slack and Teams. [A second TechCrunch piece](https://techcrunch.com/2026/09/29/openai-takes-on-microsoft-with-the-launch-of-what-feels-a-whole-lot-like-chatgpts-own-office-suite/) covers Space, a shared workspace, and Pages, a document editor built "for human and agent collaboration". Slides "will roll out to users in the coming weeks".

**What it is good at.** Small teams already living in ChatGPT get shared projects and documents in one place.

**Honest limitations.** Dots is only "for Pro and Business Premium users in eligible markets", per [TechCrunch](https://techcrunch.com/2026/09/29/openai-launches-dots-its-bubbly-agentic-avatar/), and no market list was given. Always-on agents with credentials are a security decision. [TechCentral reported on 28 September](https://techcentral.co.za/) that OpenAI agents leaked 53 ChatGPT user images.

**South African use cases.**
- A three-person agency drafting proposals together in Pages.
- A consultancy keeping client research in one Space.

**Industries.** Agency, professional services.

**Pricing.** Not stated for Dots, Space or Pages beyond plan tiers.

**Link.** [OpenAI DevDay 2026 recap](https://openai.com/index/devday-2026-recap/)

---

## 6. Cloudflare Clef and Amazon Strands Decider 2B - small models that only choose

**What it is.** On 1 October [Cloudflare's Workers AI changelog](https://developers.cloudflare.com/changelog/product/workers-ai/) introduced Clef (27B) and Clef-flash (9B), "decision models" that read an input and "return a probability for every allowed answer". The weights are open "under the Apache 2.0 license on Hugging Face". The same day, per [Digital Applied's tracker](https://www.digitalapplied.com/blog/ai-model-releases-october-2026-tracker), Amazon's Strands Labs released Decider 2B, a "2B decision model for local CPU or GPU" with weights, data and scripts.

**What it is good at.** Fast, cheap triage. Cloudflare reports a median of 38.8 ms for Clef-flash. The questions are yes/no, pick one or score on a rubric. There is no free text to parse.

**Honest limitations.** These models do not write replies. [Beri](https://www.beri.net/article/cloudflare-clef-amazon-strands-decider-open-weight-decision-models-vs-jev-benchmarks-pricing) says Decider 2B scores 0.505 on hard tasks.

**South African use cases.**
- Route WhatsApp messages to "booking", "complaint" or "human" before a costly model sees them.
- Flag incomplete visa document packs on your own hardware, keeping data local.

**Industries.** Immigration services, logistics, fintech, SaaS.

**Pricing.** [Cloudflare](https://developers.cloudflare.com/workers-ai/platform/pricing/) says Workers AI is included in the Free and Paid plans. [A Japanese developer write-up](https://note.com/dende2023/n/n45c36b444cd9) reports $0.24 per million input tokens for Clef (about R4) and $0.09 for Clef-flash (about R1.50), with no output charge. That is unconfirmed by Cloudflare in what I read. Decider 2B is free to run.

**Link.** [Cloudflare Clef docs](https://developers.cloudflare.com/workers-ai/models/clef/)

---

## 7. Microsoft MAI-Voice-2.1 and MAI-Transcribe-2-Streaming

**What it is.** Microsoft's [Foundry blog](https://techcommunity.microsoft.com/blog/azure-ai-foundry-blog/build-expressive-voice-experiences-with-new-mai-models-in-microsoft-foundry/4524637) introduced three models, dated 1 October by [Unite.AI](https://www.unite.ai/microsoft-launches-mai-transcribe-2-streaming-and-two-mai-voice-models/). MAI-Transcribe-2-Streaming "transcribes continuously across 60 languages", and MAI-Voice-2.1 speaks 23 languages with one consistent voice.

**What it is good at.** Live call transcription and voice agents for businesses already on Azure.

**Honest limitations.** The Foundry blog gives no full language list, so I could not confirm any South African language. No free tier or region availability was stated.

**South African use cases.**
- A call centre transcribing English calls live for quality checks.
- A clinic receptionist agent, with a human handover.

**Industries.** Professional services, logistics, BPO.

**Pricing.** [Microsoft](https://techcommunity.microsoft.com/blog/azure-ai-foundry-blog/build-expressive-voice-experiences-with-new-mai-models-in-microsoft-foundry/4524637) lists an introductory $0.54 per hour of audio (about R9) for transcription to year end, $22 per million characters (about R367) for MAI-Voice-2.1 and $15 (about R250) for Flash.

**Link.** [Microsoft Foundry blog](https://techcommunity.microsoft.com/blog/azure-ai-foundry-blog/build-expressive-voice-experiences-with-new-mai-models-in-microsoft-foundry/4524637)

---

## 8. ChatGPT virtual try-on

**What it is.** [TechCrunch reported on 1 October](https://techcrunch.com/2026/10/01/chatgpt-can-now-virtually-try-on-clothes-for-you/) "the global launch" of a Try On button in ChatGPT shopping results. You upload a selfie or full-body photo to see clothing or accessories on you. It uses the new Images 2.5 model.

**Why a business should care.** Shoppers will start asking ChatGPT what your product looks like on them. Clean product images and listings matter more.

**Honest limitations.** [ET Now](https://www.etnownews.com/technology/chatgpt-can-now-try-clothes-on-your-photos-heres-how-it-works-article-156272486) reports that uploaded photos are used for training by default. That is a privacy setting worth checking before you upload a body photo, and a reason not to use client photos.

**South African use cases.**
- A boutique checks how its items appear in ChatGPT shopping results.
- A stylist uses it for quick mood boards with their own photo.

**Industries.** Retail, fashion, beauty.

**Pricing.** Not stated.

**Link.** [TechCrunch](https://techcrunch.com/2026/10/01/chatgpt-can-now-virtually-try-on-clothes-for-you/)

---

## 9. Suno Speech (beta)

**What it is.** Per [AIReiter](https://aireiter.com/blog/suno-speech-beta-guide), Suno announced Speech on 1 October and opened the beta to everyone on web, iOS and Android. [Unite.AI](https://www.unite.ai/series/artificial-intelligence/) describes it as a model that generates "voice and music together".

**What it is good at.** Quick voice-and-music drafts for ads, intros and podcast stings.

**Honest limitations.** [AIReiter](https://aireiter.com/blog/suno-speech-beta-guide) says no Speech-specific price, quota or separate commercial terms were published. [Suno's pricing page](https://suno.com/pricing) says the free plan carries "No commercial rights".

**South African use cases.**
- An agency drafting a radio-style spot for a client to approve before paying for a voice artist.
- A creator making a podcast intro.

**Industries.** Agency and creative work.

**Pricing.** Suno's [free plan is $0](https://suno.com/pricing) with 50 credits a day. Use a paid plan for anything commercial.

**Link.** [Suno pricing](https://suno.com/pricing)

---

## Not for us yet

- **Gemini 4 Argon.** [India Today](https://www.indiatoday.in/technology/news/story/google-launches-gemini-4-argon-its-most-powerful-ai-model-yet-3007056-2026-10-01) says it went first to "trusted cyber defenders" and the US government, with paid API and AI Ultra access later. No date was given, so a South African SMB cannot use it today.
- **Muse for Small Business.** [Meta's Muse business page](https://muse.ai/business) says it is "Available today to people in the US and Canada who are 18 and over."
- **Meta smart glasses in South Africa.** [TechCentral](https://techcentral.co.za/meta-smart-glasses-south-africa-launch/286809/) reported on 2 October that Ray-Ban Meta and Oakley Meta glasses get an official local launch "this year, but likely without Muse". [The Open Letter](https://theopenletter.io/p/meta-ai-glasses-south-africa) says 2027. The timing is unconfirmed.

## South African corner

**Exten AI.** [Disrupt Africa profiled](https://disruptafrica.com/2026/10/01/south-african-startup-exten-ai-helps-non-technical-founders-build-full-stack-apps-in-plain-language/) this South African app builder on 1 October. It provisions a full backend - database, storage and authentication - from plain-language prompts. It is not a new launch: it "launched earlier this year", is in closed-cohort testing, is piloting with the University of Fort Hare and is raising R1.5 million. Worth following, but not something to sign up for this week.

## Left out on purpose

- **n8n Agents** launched on [25 September](https://blog.n8n.io/introducing-n8n-agents/), three days before this window.
- **Tavus Griffin-Lite** is an early-tester research preview, per [Digital Applied](https://www.digitalapplied.com/blog/ai-model-releases-october-2026-tracker).
- **Product Hunt's weekly board** ([week of 28 September](https://www.producthunt.com/leaderboard/weekly/2026/40)) was mostly agent infrastructure with little SA relevance.

---

## What I'd actually try this week

1. **Eleven v4, before 12 October.** Generate one Afrikaans and one English script at the discounted rate and compare them with your current voice. Do not plan isiZulu or isiXhosa work on it - they are not on the list.
2. **Shopify Canvas, if you sell on Shopify.** Rebuild one product page by chat on a duplicate theme, never the live one, because TechCrunch lists theme updates among the things not supported at launch.

**And one check that is not a purchase:** if you run a WhatsApp bot through an API provider, ask them this week how many replies you sent in September and what you will pay from October.
