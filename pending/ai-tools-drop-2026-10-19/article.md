# AI Tools Drop - Week of 19 October 2026

Episode 11. Window: 12 to 19 October 2026. Written for South African founders and small businesses.

Rand figures use **R16.47 to the dollar**, the midpoint of [XE](https://www.xe.com/currencyconverter/convert/?Amount=1&From=USD&To=ZAR) (16.4747 at 09:02 UTC on 19 October), [Trading Economics](https://tradingeconomics.com/south-africa/currency) (16.4762) and [Pluang](https://pluang.com/en/tools/currency-converter/usd-zar) (16.4585). The rand is slightly stronger than last week's R16.55.

---

## This week in one paragraph

This week's useful launches were about running AI on your own machine, and about voice. Hugging Face released a free Windows app that runs AI models on your own PC with nothing sent to the cloud. Datalab released a tiny free document reader (OCR) that runs on an ordinary processor. Google's Gemini 4 Argon, which I listed under "not for us yet" two weeks ago, is now available globally, including on South African Google AI Pro plans. ChatGPT got a slides tool for paid business plans, and Microsoft brought legal skills into Copilot worldwide. On the voice and audio side: xAI shipped a cheaper, faster voice model for phone agents, Fish Audio released a voice model you direct with plain-English instructions, and ElevenLabs released a tool that adds music and sound effects to a video in one pass. Meta's big new models are real but not practically usable from here yet. Eight items made the main list.

---

## 1. Llama Windows - run AI models on your own PC, free

**What it is.** On 13 October [Hugging Face announced](https://huggingface.co/blog/huggingface/llama-windows) Llama Windows, "a free and open source app that puts llama.cpp in your Windows 11 tray". You pick an open model from the Hugging Face Hub, download it in one click and chat with it locally.

**What it is good at.** Privacy. Hugging Face says "everything runs on device, so your prompts and data stay on your PC", with "no internet connection needed". It also runs a local server with an "OpenAI-compatible API", so tools you build can talk to it, and it needs "no admin rights".

**Honest limitations.** Windows 11 only, and [the announcement](https://huggingface.co/blog/huggingface/llama-windows) gives no minimum hardware. Small local models are much weaker than ChatGPT or Claude, and an older office laptop will be slow. No language list is given, so test Afrikaans or isiZulu yourself.

**South African use cases.**
- An immigration practice summarising client documents without uploading them anywhere.
- A wellness practitioner drafting session admin notes on a laptop that never leaves the practice.
- A SaaS builder testing an AI feature locally before paying for an API.

**Industries.** Immigration services, wellness, professional services, SaaS building.

**Pricing.** Free.

**Access notes.** You download it from llama.app on any Windows 11 PC. Models are separate downloads and can be several gigabytes, so it is worth doing on uncapped Wi-Fi.

**Link.** [Hugging Face - Introducing Llama Windows](https://huggingface.co/blog/huggingface/llama-windows)

---

## 2. Indra OCR - a tiny, fast document reader that runs on a normal CPU

**What it is.** [Datalab's Indra](https://github.com/datalab-to/indra) is "a 1M-parameter OCR model that reads up to 49 pages per second on CPU", turning PDFs and images into markdown, plain text or JSON. [ThursdAI](https://thursdai.news/releases/2026-10) listed it among the 15 October releases.

**What it is good at.** Bulk, private document reading. The [GitHub page](https://github.com/datalab-to/indra) says it needs no GPU, and its local viewer keeps "files stay on your machine". It covers Latin script (about 50 languages), which includes the alphabet South African languages use.

**Honest limitations.** [Datalab](https://github.com/datalab-to/indra) says it is not for complex tables, handwriting or degraded scans. Afrikaans and isiZulu are not individually listed. Installing it needs Python 3.10 or newer, so you need someone technical.

**South African use cases.**
- Turning a stack of scanned passports, bank statements and employer letters into searchable text for an immigration file.
- A bookkeeper extracting supplier invoices into text before capture.
- A logistics firm reading printed delivery notes in bulk.

**Industries.** Immigration services, professional services, logistics, fintech.

**Pricing.** The code is Apache 2.0. The model weights are free for "startups under $20M funding/revenue" (about R329 million) under a modified OpenRAIL-M licence, per [GitHub](https://github.com/datalab-to/indra). The managed platform gives "$5 in free credits".

**Link.** [Indra OCR on GitHub](https://github.com/datalab-to/indra)

---

## 3. Gemini 4 Argon - Google's top model, now available here

**What it is.** On 13 October [Google said](https://blog.google/innovation-and-ai/models-and-research/gemini-models/introducing-gemini-4-argon/) Gemini 4 Argon "is now globally available" through the Gemini API, and in the Gemini app and AI Mode for Google AI Pro and Ultra subscribers. Two weeks ago it was limited to cyber defenders and US government users.

**What it is good at.** Long, multi-step work. [Google](https://blog.google/innovation-and-ai/models-and-research/gemini-models/introducing-gemini-4-argon/) lists coding, finance, legal and document analysis, with a 1 million token limit through the API.

**Honest limitations.** It is not on the free Gemini plan. The API needs the paid tier, and the introductory price doubles after 30 November.

**South African use cases.**
- A professional services firm comparing two long contracts clause by clause.
- A fintech founder stress-testing a financial model.
- A SaaS builder using it for harder coding tasks.

**Industries.** Professional services, fintech, SaaS building.

**Pricing.** API: $2 per million input tokens (about R32.94) and $10 output (about R164.70) until 30 November 2026, then $4 / $20 (about R65.88 / R329.40), per [Google](https://blog.google/innovation-and-ai/models-and-research/gemini-models/introducing-gemini-4-argon/). The [South African Google One page](https://one.google.com/intl/en_za/about/) says Google AI Pro "includes Gemini 4 Argon"; [News24](https://www.news24.com/business/tech/google-offers-sa-higher-ed-students-a-year-of-free-premium-ai-access-20251008-0884) put Google AI Pro at "almost R350 a month".

**Link.** [Google - Introducing Gemini 4 Argon](https://blog.google/innovation-and-ai/models-and-research/gemini-models/introducing-gemini-4-argon/)

---

## 4. ChatGPT Slides - presentations inside ChatGPT

**What it is.** On 16 October [OpenAI's release notes, via Releasebot](https://releasebot.io/updates/openai/chatgpt), said "Slides is rolling out to eligible Pro, Business, and Enterprise users with Space access on the web and in the desktop app."

**What it is good at.** First drafts of decks. You ask ChatGPT in Work to create a presentation, and "on the web, export to PowerPoint, PDF, or Google Slides".

**Honest limitations.** Not on Free, Go or Plus. It is a rollout, so it may not appear on your account yet.

**South African use cases.**
- A founder turning investor notes into a first-draft pitch deck.
- An agency drafting a client proposal deck, then finishing it in PowerPoint.
- A logistics manager building a monthly operations review.

**Industries.** Agency and creative work, professional services, logistics.

**Pricing.** Included in eligible Pro, Business and Enterprise plans. I did not verify current plan prices this week.

**Link.** [ChatGPT updates on Releasebot](https://releasebot.io/updates/openai/chatgpt)

---

## 5. Grok Voice 3.0 - a cheaper, faster voice model for phone agents

**What it is.** On 14 October [xAI announced](https://x.ai/news/grok-voice-3) Grok Voice 3.0 for its Voice Agent API, claiming it "sets a new record for resolving customer support calls" with "latency at under one second".

**What it is good at.** Answering phone calls. [xAI's docs](https://docs.x.ai/developers/model-capabilities/audio/speech-to-speech) list phone-call support (SIP), tool calling, custom voices and pronunciation replacements.

**Honest limitations.** The [docs](https://docs.x.ai/developers/model-capabilities/audio/speech-to-speech) list 20 languages, including English, but no South African languages, and other languages have "varying degrees of accuracy". Test it with South African accents. Recording or automating calls also raises POPIA consent questions.

**South African use cases.**
- A salon answering after-hours booking calls.
- A logistics company answering "where is my delivery" calls.
- A fintech handling first-line card queries before passing to a person.

**Industries.** Beauty and wellness, logistics, fintech, retail.

**Pricing.** $0.08 per minute (about R1.32), or $4.80 per hour (about R79), per [xAI](https://x.ai/news/grok-voice-3).

**Link.** [xAI - Introducing Grok Voice 3.0](https://x.ai/news/grok-voice-3)

---

## 6. Fish Audio Drama 3 - an AI voice you direct in plain English

**What it is.** On 13 October [Fish Audio released Drama 3](https://fish.audio/blog/fish-audio-drama-3/), its "most emotive text-to-speech model", on fish.audio, its apps and the API. It is "open-weight rather than open source".

**What it is good at.** Directing a performance. You add directions in square brackets, change the read mid-line and tag specific words. Fish Audio claims "83 languages".

**Honest limitations.** The [docs](https://docs.fish.audio/features/text-to-speech/drama-3) do not mention Afrikaans, isiZulu or isiXhosa, and say language tags "are experimental". The licence "bans cloning a real person's voice without their consent".

**South African use cases.**
- An agency producing radio-style ads with several characters.
- A training provider voicing course videos with a natural delivery.
- A brand testing an alternative to its current AI voice.

**Industries.** Agency and creative work, education and training, retail marketing.

**Pricing.** The API is $50 per million characters (about R823.50), with a launch price of $10 (about R164.70) until 12 November 2026, per [Fish Audio](https://fish.audio/blog/fish-audio-drama-3/). The weights are free for commercial use under $500,000 annual revenue (about R8.2 million).

**Link.** [Fish Audio - Drama 3](https://fish.audio/blog/fish-audio-drama-3/)

---

## 7. ElevenLabs Instant Soundtracks - music and sound effects for a video in one pass

**What it is.** On 15 October [ElevenLabs launched Instant Soundtracks](https://elevenlabs.io/blog/introducing-instant-soundtracks?ref=aiposthub.com): "Generate a soundtrack and synchronized sound effects for any video you upload in ElevenCreative."

**What it is good at.** Short-form social video. It places effects on separate timeline layers and shifts the music mood across scenes. Through the API it can return music and effects as separate files.

**Honest limitations.** ElevenLabs gives no price or plan details. Limits are "up to 10 videos per request, combined up to 200 MB and 10 minutes of video". Check the licensing terms for music before using it in paid ads.

**South African use cases.**
- A beauty brand scoring product Reels without searching stock music libraries.
- An agency adding sound to silent client screen recordings.
- A property agent adding music to walkthrough videos.

**Industries.** Beauty, agency and creative work, property, retail.

**Pricing.** Not stated. It runs on ElevenLabs credits in ElevenCreative.

**Link.** [ElevenLabs - Introducing Instant Soundtracks](https://elevenlabs.io/blog/introducing-instant-soundtracks?ref=aiposthub.com)

---

## 8. Microsoft Copilot for legal - legal skills inside Word and Copilot

**What it is.** On 15 October [Microsoft announced](https://techcommunity.microsoft.com/blog/microsoft-copilot-blog/introducing-microsoft-copilot-for-legal/4564246) "more than 20 purpose-built legal skills" plus partner plugins, "generally available to Microsoft Copilot customers worldwide today".

**What it is good at.** In Word, it proposes "agreement edits as native tracked changes" and drafts from approved precedents. In Cowork, it tracks obligations and deadlines and builds case chronologies.

**Honest limitations.** No price or plan is stated, and you need a Microsoft Copilot licence. It is a drafting aid, not legal advice. A qualified attorney still signs off.

**South African use cases.**
- A small law firm redlining a supplier agreement as tracked changes.
- An immigration practice tracking permit deadlines across client files.
- A company secretary turning meeting notes into minutes and resolutions.

**Industries.** Professional services, immigration services.

**Pricing.** Not stated. It requires a Microsoft Copilot licence.

**Link.** [Microsoft - Introducing Copilot for legal](https://techcommunity.microsoft.com/blog/microsoft-copilot-blog/introducing-microsoft-copilot-for-legal/4564246)

---

## Not for us yet

- **Meta Muse Wonder.** [TechCrunch](https://techcrunch.com/2026/10/12/meta-releases-its-first-frontier-model-muse-wonder/) reports that Meta released it on 12 October at $4 / $20 per million tokens through the Meta Model API, with the Full version only for Muse Code subscribers. Country availability is not stated, and Muse itself is still [US and Canada only](https://muse.ai/business).
- **Meta Muse Spark Open.** Open weights, released 15 October, but [TechCrunch](https://techcrunch.com/2026/10/15/meta-launches-an-open-weight-model-that-runs-on-macs/) says local use needs "at least 1 terabyte of RAM".
- **OpenAI's Rosalind Academic Plan.** Applications are open only "to labs at U.S. universities", per [Releasebot](https://releasebot.io/updates/openai/chatgpt).

## South African corner

- **Funda Nam.** On 16 October [ITWeb reported](https://www.itweb.co.za/article/non-profit-rolls-out-trilingual-ai-study-aid/o1Jr5qxP3lZqKdWL) that ORT South Africa launched a trilingual AI study companion in English, isiZulu and isiXhosa, trained on its own big data analytics curriculum. It is for programme students only, but it is a good local model of an AI tutor built on your own material.
- **Vodacom and UJ.** On 12 October [Vodacom reported](https://www.vodacom.com/news-article.php?articleID=17039) that its AI for Africa Hackathon with the University of Johannesburg and AWS ran at Vodacom World, with student teams working on health, safety, youth employment and water security.
- **Coming up.** [AI Expo Africa](https://www.engineeringnews.co.za/article/obsidian-brings-practical-enterprise-ai-into-focus-at-ai-expo-africa-2026-2026-10-08) returns to the Sandton Convention Centre on 28 and 29 October.

## Follow-ups from last week

- The Eleven v4 launch discount ended on 12 October; [ElevenLabs' v4 page](https://elevenlabs.io/blog/eleven-v4) was last updated that day.
- The Gemini agent is still enterprise-only. I will cover it when small businesses can sign up.

## Left out on purpose

- **Canva AI 2.0.** It was recirculated this week, but [the release](https://www.martechcube.com/canva-unveils-canva-ai-2-0-reimagining-how-the-world-designs-and-works/) dates from April.
- **Shopify agent checkout.** [TechCrunch reported it on 28 September](https://techcrunch.com/2026/09/28/shopify-opens-checkout-to-browser-based-ai-agents/).
- **Microsoft-Decision-1.** [Microsoft's post](https://commandline.microsoft.com/microsoft-decision-1-model-foundry/) is dated 9 October, outside this window.
- **Mistral Large 4.** It [launched on 6 October](https://mistral.ai/news/mistral-large-4/).
- **Claude Code Review.** It became [generally available](https://claude.com/resources/articles/code-review-is-now-generally-available) on 15 October, but only for Claude Team and Enterprise, and it is a developer tool.

---

## What I'd actually try this week

1. **Llama Windows, if you have a Windows 11 PC.** Install it, download one small model and ask it to summarise a non-sensitive document. Then decide whether a local model is good enough for your private documents.
2. **Indra OCR, if you have someone technical and a pile of scans.** Run 20 scanned pages through it and check the output against the originals before trusting it with client files.
