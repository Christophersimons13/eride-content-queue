# AI Tools Drop - Week of 7 September 2026

Covering launches from 31 August to 7 September 2026. South African founder and SMB lens.

All USD figures converted at **R15.97 per dollar**, the rate on 6 September 2026 ([XE](https://www.xe.com/currencyconverter/convert/?Amount=1&From=USD&To=ZAR), cross-checked against [Bloomberg at 15.9730](https://www.bloomberg.com/quote/USDZAR:CUR), [Investing.com at 15.9842](https://za.investing.com/currencies/usd-zar) and [Pluang at 15.98](https://pluang.com/en/tools/currency-converter/usd-zar)). Note that the public rate sources disagree badly this week - [Google Finance was showing 17.7101](https://www.google.com/finance/quote/USD-ZAR) off a stale 25 August stamp, an 11 percent spread against the live cluster. If you are quoting a client in rand, pull your own live rate. Round to R16 for mental maths.

---

## This week in one paragraph

This was a frontier-model week, not a small-tools week. Google shipped Gemini 3.8 Flash on 2 September at $0.75 per million input tokens with a genuinely free tier, and buried in the pricing page is the single most important line for any South African business handling client data: on the paid tier, your prompts are not used to improve their products. On the free tier they are. OpenAI shipped GPT-6 Astra on 3 September and rated it Critical for cyber capability - their own safety document says it finds previously unknown security flaws and builds working exploits without a person guiding each step. That is not a product feature, it is a change to your threat model. Anthropic shipped Claude Fable 5.1 with a one-million-token context by default and a cache-read price 75 percent below the old one, though the Mythos variant is restricted to United States organisations. On the smaller end, ThunderPhone put a voice-agent platform out at two US cents a minute that switches language mid-call across forty-plus languages, which matters more here than almost anywhere. And exactly one launch this week was built in South Africa: Syspro, out of Johannesburg, launched Torque, an industrial AI platform that puts auditable no-code agents inside a manufacturing ERP. It has no published price and is not generally available. Across all ten tools on this week's shortlist, not one vendor mentions POPIA anywhere in their documentation. Every data-handling answer below is inferred from GDPR-shaped language written for Europe.

---

## 1. Gemini 3.8 Flash - the cheap workhorse just got a compliance answer

**What it is.** Google's fast, cheap model tier, updated on 2 September 2026 and listed in the [Gemini API changelog](https://ai.google.dev/gemini-api/docs/changelog) alongside a [launch post on the Google blog](https://blog.google/innovation-and-ai/models-and-research/gemini-models/3-8-flash-and-3-8-flash-cyber/). It is the model you build production features on when you are paying per call and the volume is real.

**What it is genuinely good at.** Price-to-capability at scale. Paid tier runs **$0.75 per million input tokens and $3.75 per million output** ([pricing page](https://ai.google.dev/gemini-api/docs/pricing)) - roughly **R12 in and R60 out per million tokens**. For a document-processing or classification workload that is close to free relative to what the same job cost eighteen months ago. There is also a free tier that is actually free, not a trial.

The more important thing is on that same pricing page. There is a row headed "Used to improve our products" with two values: **Free Tier: Yes. Paid Tier: No.** That is the clearest statement of the free-versus-paid data bargain any major vendor publishes, and it is the line that lets you have an honest conversation with a client about whether their information trains anyone's model.

**Honest limitations.** Search grounding is not available on the free tier, so free-tier answers cannot be anchored to live web results. Pricing is time-boxed: the $0.75 and $3.75 rates hold **through 31 December 2026 and then double to $1.50 and $7.50 on 1 January 2027** ([pricing page](https://ai.google.dev/gemini-api/docs/pricing)). Build your unit economics on the 2027 number, not the promotional one. And there is no African data residency option - Google's [API terms](https://ai.google.dev/gemini-api/terms) say data may be stored transiently or cached in any country.

**South African use cases.**
- Bulk document classification and field extraction in an immigration, conveyancing or debt-review practice, on the paid tier so client files are not training data.
- Customer-message triage across WhatsApp and email for a retail or services SMB, routing by intent before a human touches it.
- Product description and catalogue generation for an e-commerce operation with thousands of SKUs, where per-item cost has to be near zero.

**Industries.** Professional services, legal and immigration, retail and e-commerce, logistics, fintech operations, anyone building SaaS.

**Access from South Africa.** Straightforward. Google account, API key, no US card required for the free tier. Paid tier needs a card that Google Cloud accepts, which most South African business cards are.

**Link.** [ai.google.dev/gemini-api/docs/pricing](https://ai.google.dev/gemini-api/docs/pricing)

---

## 2. ThunderPhone - voice agents at R0.32 a minute, in your caller's language

**What it is.** A voice-AI agent platform that launched on 1 September and placed 14th on that day's [Product Hunt leaderboard](https://www.producthunt.com/leaderboard/daily/2026/9/1). You build a phone agent, point it at a number, and it handles calls.

**What it is genuinely good at.** Two things. First, price: the Spark tier is **$0.02 per minute** ([pricing](https://thunderphone.com/pricing)) - about **R0.32 a minute**, or roughly **R19 an hour of talk time**. Bolt is $0.05 and Storm is $0.09. Second, and more relevant here: it supports **more than forty languages including switching language mid-call**. South Africa has twelve official languages and a real-world call centre problem that most voice AI ignores. An agent that can start in English and move to isiZulu when the caller does is not a gimmick here.

**Honest limitations.** There is **no free tier** - you pay from the first minute. The advertised per-minute price is a floor, not a price: add-ons stack fast. Verbal acknowledgement adds $0.02, supervision adds $0.08, premium voices add $0.03 and a text-to-speech upcharge adds another $0.03 ([pricing](https://thunderphone.com/pricing)). A fully-featured Spark agent can cost more than double the headline. Demo numbers are United States only at $1 a month, though bringing your own SIP trunk is free - which is what you would do here anyway with a local provider.

On data: **hosting location is not stated** on either the [security page](https://thunderphone.com/security) or the [privacy policy](https://thunderphone.com/privacy). The only no-training commitment I could find is narrowly scoped to Google. For recorded customer calls under POPIA, that is not enough to sign off on without asking them directly.

**South African use cases.**
- After-hours booking line for a salon, clinic or workshop, taking appointments in the caller's language instead of dropping them to voicemail.
- Outbound payment-reminder calls for a debt collector or a body corporate, with the script and consent language fixed and logged.
- First-line qualification for an immigration or insurance practice, capturing details before a consultant spends an hour on someone who does not qualify.

**Industries.** Beauty and wellness, healthcare admin, debt collection and credit, logistics dispatch, professional services, any business with an unanswered phone.

**Access from South Africa.** Sign-up is open. Use your own SIP trunk with a local number rather than the US demo number. Budget in dollars.

**Link.** [thunderphone.com/pricing](https://thunderphone.com/pricing)

---

## 3. Syspro Torque - the only South African launch this week

**What it is.** Syspro, the manufacturing ERP company headquartered in Johannesburg, launched Torque on 2 September. It is an industrial AI platform that lets you build no-code agents that act inside the ERP itself, via MCP, rather than sitting beside it giving advice ([press release](https://www.syspro.com/press_release/syspro-launches-torque-the-industrial-ai-platform-that-transforms-manufacturing-decisions-into-auditable-automatic-action/), [AI solutions page](https://www.syspro.com/solutions/artificial-intelligence/)).

**What it is genuinely good at.** Auditability, which is the thing that usually kills AI in a regulated factory. Syspro calls it the "Glass House": every action an agent takes is logged with the rule that fired, the data it used, and why. It also gives you an upfront cost estimate per workflow before you run it, so an agent cannot quietly spend your token budget. For a manufacturer who has to explain a decision to an auditor or a customer, that logging is the whole product.

**Honest limitations.** **No published price.** Syspro describes it as usage-based and says nothing more, which means a procurement conversation, not a signup. It is **not generally available** - this is controlled availability, with participants capped around $2 billion revenue, and it requires Syspro 8 2026 R1. So if you are not already a Syspro customer on a current version, this is not available to you this quarter.

And here is the part worth saying out loud: despite the Johannesburg headquarters, **there is no African data residency**. The [privacy policy](https://www.syspro.com/privacy-policy/) says data may go outside your country of residence, "such as the United States". A South African company selling to South African manufacturers still routes the data offshore. That is the state of the market, not a criticism of Syspro specifically - but it does mean the local-vendor advantage you might assume you are buying is not a data-location advantage.

They are showing it at IMTS in Chicago from 14 to 19 September if you want to see it running.

**South African use cases.**
- Automated reorder and supplier-selection agents in an automotive component plant, with every decision logged for the OEM's audit trail.
- Production-schedule adjustment when a load-shedding stage changes, acting inside the ERP rather than in a spreadsheet next to it.
- Quality-hold and batch-release workflows in food or pharmaceutical manufacturing where the why has to be recoverable years later.

**Industries.** Manufacturing, automotive components, food and beverage production, industrial distribution.

**Access from South Africa.** Local company, local sales team, but gated to existing Syspro 8 2026 R1 customers in controlled release. Ask your account manager.

**Link.** [syspro.com/solutions/artificial-intelligence](https://www.syspro.com/solutions/artificial-intelligence/)

---

## 4. Stitch AI by Dynamic Mockups - embroidery digitising in fifteen seconds, free right now

**What it is.** An embroidery digitising agent, launched 2 September and 12th on that day's [Product Hunt leaderboard](https://www.producthunt.com/leaderboard/daily/2026/9/2). You give it artwork and in about fifteen seconds you get a photoreal mockup, a Tajima DST stitch file, a production sheet and a stitch count ([product page](https://dynamicmockups.com/stitch/)).

**What it is genuinely good at.** Collapsing a cost line that most people outside the trade do not know exists. Manual digitising runs **$10 to $50 per design**, and the desktop software that does it in-house runs **$100 to $3,000**. Stitch AI is **free right now** with no stated expiry and no card required. For a small merch or uniform business quoting jobs, that is the difference between a same-day quote and a two-day turnaround.

It also has the **best data disclosure of anything on this week's list**: the [privacy policy](https://dynamicmockups.com/privacy-policy/) states processing takes place in the EU or other regions where AWS operates. That is a real answer, not a shrug.

**Honest limitations.** Narrow. If you are not in apparel, merch, uniforms or promotional goods, this does nothing for you. "Free right now" with no expiry stated is a launch-window price, not a commitment - the parent product's free plan is 50 credits with no card and Pro is $15 a month, about **R240**, which is probably where this lands. And there is **no statement on whether your uploaded artwork trains their models**, which matters if you are digitising a client's logo.

**South African use cases.**
- A Johannesburg uniform supplier quoting school and corporate embroidery jobs on the same call instead of sending artwork out to be digitised.
- A township or market-based merch operation producing sample mockups for client approval before buying blanks.
- A promotional-goods reseller checking stitch counts to price accurately instead of guessing and eating the margin.

**Industries.** Apparel and textiles, promotional products, school and corporate uniforms, print and embroidery shops.

**Access from South Africa.** Open signup, no card, free at time of writing. Browser-based.

**Link.** [dynamicmockups.com/stitch](https://dynamicmockups.com/stitch/)

---

## 5. Claude Fable 5.1 and Mythos 5.1 - a million tokens as standard, and a much cheaper cache

**What it is.** Anthropic's model update on 1 September ([announcement](https://www.anthropic.com/claude-fable-and-mythos-5-1), [API release notes](https://docs.anthropic.com/en/release-notes/api), [newsroom](https://www.anthropic.com/news)). One million tokens of context by default and 128 thousand tokens of output.

**What it is genuinely good at.** Long-document work without chunking. A million-token context handles a full contract set, a year of correspondence or an entire codebase in one pass. The commercial change worth noticing is the **cache read price at $0.25 per million tokens, 75 percent below the previous rate** - about **R4 per million**. If your product re-reads the same large document across many queries, which is exactly what a compliance or document-review tool does, your cost profile just changed materially. Input is $10 and output $50 per million, roughly **R160 and R799**.

**Honest limitations.** **Mythos 5.1 is restricted to United States organisations**, so half the launch is not available to you. There is a breaking API change: `tool_choice` set to `any` or `tool` now returns a 400 error, so check your existing integrations before you upgrade. Consumer Pro is $17 a month on annual billing, about **R272**.

**Access from South Africa.** The direct API needs a card Anthropic accepts. The better route if that is a problem: Fable 5.1 is available through Amazon Bedrock, Google Cloud and Microsoft Foundry, so you can consume it on an existing cloud account and pay through infrastructure billing you already have.

**South African use cases.**
- Contract and lease review across a full document set for a law firm or property manager, one pass, no chunking.
- A compliance assistant that keeps a whole regulatory corpus cached and answers against it cheaply, which is where the $0.25 cache read pays for itself.
- Codebase-wide refactoring and review for a small development team without a dedicated senior reviewer.

**Industries.** Legal, property, compliance and audit, immigration practices, software development.

**Link.** [anthropic.com/claude-fable-and-mythos-5-1](https://www.anthropic.com/claude-fable-and-mythos-5-1)

---

## 6. GPT-6 Astra - the warning item, and it is not about the price

**What it is.** OpenAI's new frontier model, released 3 September ([announcement](https://openai.com/index/gpt-6-astra/), [ChatGPT release notes](https://help.openai.com/en/articles/6825453-chatgpt-release-notes)). It builds documents, spreadsheets and presentations from templates, which is the headline consumer feature.

**Why it is the warning item.** This is **OpenAI's first model rated Critical for cyber capability** under their own preparedness framework. Their [safety overview](https://openai.com/index/safety-overview-gpt-6-astra/) states it finds previously unknown security flaws and develops new ways to exploit them across many well-protected systems, without a person guiding each step.

Read that as a defender, not as a customer. The capability that OpenAI is gating is the same capability that will show up in less careful hands. If your security posture assumes that finding a novel flaw in your stack requires a skilled human spending weeks, that assumption has a shorter shelf life than it did last month. The practical response for a small South African business is unglamorous and immediate: patch faster, turn on multi-factor authentication everywhere, and know what you have exposed to the internet.

Which connects directly to the housekeeping item further down - n8n shipped fixes for two CVEs this week. If you self-host anything, this is the week to patch it.

**Honest limitations as a product.** Rollout is limited, so you may not have it yet. Pricing is **$10 per million input and $50 per million output** ([API pricing](https://openai.com/api/pricing/)) - about **R160 and R799** - with cached input at $1. Fast mode doubles the rate. It is labelled "Promotional pricing" with no expiry stated, so treat it as temporary. There is **no African data residency region**: the [data residency guide](https://platform.openai.com/docs/guides/your-data) lists the United States, EU, Australia, Canada, Japan, India and Singapore only. Zero data retention is available on request, which is the control to ask for if you are handling client information.

**South African use cases.**
- Generating first-draft proposals, financial models and client decks from your own templates, which is the feature that actually saves an afternoon.
- Internal security review: pointing it at your own configuration and asking what an attacker would try, before someone else does.
- Board and investor reporting packs built from a spreadsheet each month.

**Industries.** Professional services, finance and accounting, anyone with an internet-facing system, which is everyone.

**Link.** [openai.com/index/safety-overview-gpt-6-astra](https://openai.com/index/safety-overview-gpt-6-astra/)

---

## 7. Tadata - an AI employee in Slack that asks before it sends

**What it is.** Launched 6 September and second on that day's [Product Hunt leaderboard](https://www.producthunt.com/leaderboard/daily/2026/9/6). It sits in Slack, gives you a morning brief, and drafts follow-ups ([tadata.com](https://www.tadata.com/)).

**What it is genuinely good at.** The approval gate. Their own copy says nothing is sent until you approve it, which is the correct default for a tool with access to your inbox and it is not the default everywhere. The morning brief plus drafted follow-ups is a real fit for a founder doing their own sales admin.

**Honest limitations.** The free offer is **$50 or 1,000 credits, one time only, no card** ([pricing](https://www.tadata.com/pricing)) - that is a trial, not a free tier. After it, Lite is $39 a month, Pro $149 and Scale $299, so about **R623, R2,380 and R4,775**. Critically, **what a credit buys is not defined anywhere**, so you cannot forecast your monthly spend before you commit. Hosting location is not stated.

**South African use cases.**
- A solo founder's morning brief pulling overnight email and Slack into one list before the day starts.
- Drafted follow-ups on a sales pipeline where the deals are worth more than R600 a month of tooling.
- Handover notes between a founder and a part-time assistant, generated rather than written.

**Industries.** Agencies, B2B sales teams, small SaaS, consultancies. Only worth it if you are already living in Slack.

**Link.** [tadata.com/pricing](https://www.tadata.com/pricing)

---

## 8. AI Toolbox 3.0 - the best data disclosure of the week, and a lifetime price

**What it is.** A browser extension that adds folders, search and export across ChatGPT, Gemini, Claude and Grok, updated 6 September and top of that day's [Product Hunt leaderboard](https://www.producthunt.com/leaderboard/daily/2026/9/6).

**What it is genuinely good at.** Finding the conversation you had three weeks ago. If you are using AI for client work, your chat history is a working record and none of these products give you a usable filing system. This does, across four of them.

And it wins the disclosure prize this week: the [privacy policy](https://www.ai-toolbox.co/privacy-policy) states plainly that servers are hosted with DigitalOcean in Frankfurt, Germany. Naming the provider and the city is more than almost any vendor on this list manages.

**Honest limitations.** That Frankfurt statement covers the **ChatGPT module only** - the disclosure is weaker for the other three platforms. It is **priced per module** at $9.99 a month each, $59 a year, or $99 lifetime, with All Access Lifetime at $199 ([pricing](https://www.ai-toolbox.co/pricing)) - about **R160 a month, R942 a year, R1,581 lifetime per module, or R3,178 for everything forever**. Read the per-module structure carefully or you will buy one thing and expect four. Chromium browsers only, so no Safari. The free tier is tight.

**South African use cases.**
- An immigration or legal practice keeping a searchable record of AI-assisted drafting per client matter, which is a file-note obligation in practice.
- An agency separating client work into folders so a handover does not require reading six months of chat.
- Exporting a conversation trail as evidence of how a decision was reached.

**Industries.** Legal, immigration, accounting, agencies, consultancies, anyone billing for AI-assisted work.

**Access from South Africa.** Extension install, card payment, no regional block. The $199 lifetime is a one-off in dollars, so exchange-rate exposure is once rather than monthly.

**Link.** [ai-toolbox.co/pricing](https://www.ai-toolbox.co/pricing)

---

## 9. MagiCrew - the only real residency answer on this list

**What it is.** An open-source, Apache-licensed multi-agent platform, third on the [Product Hunt leaderboard for 3 September](https://www.producthunt.com/leaderboard/daily/2026/9/3) ([magicrew.ai](https://www.magicrew.ai/)).

**What it is genuinely good at.** One thing that nothing else here can do: because it is Apache-licensed and self-hostable, **you can run it on infrastructure you control**. If a client contract or a POPIA assessment requires that data does not leave a machine you own, this is the only tool on this week's list that gives you a path. Everything else on this page routes offshore.

**Honest limitations.** Several, and they matter. Paid tiers run Plus $9.99, Pro $24.99, Max $49.99 and Ultra $99.99 ([pricing](https://www.magicrew.ai/pricing)) - the Plus tier is listed at 66 percent off a $29 list price with no expiry stated, which is a permanent discount and therefore a fictional list price. **There is no free tier on the pricing page.** "Points" are the billing unit and are not defined. The demo interface shows prices in yuan, so the primary market is likely Chinese, which affects support and documentation quality. And it is a Product Hunt launch of an existing project - the [GitHub repository](https://github.com/dtyq/magic) has activity going back through 2025, so this is a marketing moment, not a new codebase. That is not a problem; it is arguably reassuring. But it is not new.

**South African use cases.**
- Self-hosted agent workflows for a client whose contract prohibits offshore processing, run on a local VPS or on-premise box.
- An internal automation layer for a business that has already decided not to send its data to a US API.
- Evaluating multi-agent architecture without a subscription, since you can read and run the code.

**Industries.** Regulated sectors, government-adjacent work, financial services, anyone with a data-location clause in their contracts.

**Link.** [magicrew.ai](https://www.magicrew.ai/)

---

## 10. Video Agent by Fotor - number one on Product Hunt, and I cannot tell you what it costs

**What it is.** An AI video agent from Fotor, launched 31 August, which took **first place on that day's [Product Hunt leaderboard with 377 upvotes](https://www.producthunt.com/leaderboard/daily/2026/8/31)** - the biggest community response of the week ([fotor.com/video](https://www.fotor.com/video/)).

**What it is genuinely good at.** Fotor's existing tooling is competent and the free plan gives you 50 AI Agent chats and one task, which is enough to judge whether the output is usable for your content. If you are producing social video for a small brand, the free allowance is a real test drive.

**Honest limitations, and they are unusual.** I could not verify the price. **Fotor's own [pricing page](https://www.fotor.com/pricing/) renders no readable paid price** - it shows dashes and a literal unrendered `{credits}` placeholder where the numbers should be, and a screenshot showed empty loading skeletons. The only figures I have are second-hand: [G2 reports Pro at $8.99 and Pro+ at $19.99](https://www.g2.com/products/fotor-photo-editor/pricing). Treat those as unconfirmed, because they are.

Worse, **their privacy policy returned a 403 error on two attempts**, so the data posture is unverified. I am not saying it is bad. I am saying I could not read it, and you should not upload client footage to a service whose privacy terms you cannot open. It is also beta and web-only, and the free plan watermarks output.

**South African use cases.**
- Testing whether AI-generated social video clears the quality bar for your brand, on the free allowance, before committing budget.
- Short-form product clips for a retail or hospitality account where the alternative is no video at all.

**Industries.** Retail, hospitality, agencies, creator businesses.

**Access from South Africa.** Web signup, no block. Do not put anything sensitive through it until the privacy policy loads.

**Link.** [fotor.com/video](https://www.fotor.com/video/)

---

## Also this week, briefly

- **Dial** - an AI phone product at $3 a month per number plus $0.13 to $0.22 a minute ([pricing](https://getdial.ai/pricing)), so roughly seven times ThunderPhone's floor, with no free tier. Its iMessage integration is close to irrelevant in an Android-majority market. Skip it here.
- **Lyria 3.5** - Google's music generation model, updated 3 September. Useful for royalty-free background audio on social video.
- **Agentic video understanding** - shipped 1 September, cutting token use on long video by about 88 percent. The unglamorous South African application is reviewing hours of retail or warehouse CCTV without the cost being absurd.
- **n8n 2.37.x and 2.38.x** - bug-fix releases from 1 to 4 September including a fix for **CVE-2026-73088 and CVE-2026-73089** ([releases](https://github.com/n8n-io/n8n/releases)). If you self-host n8n, patch it this week. This is the most actionable item on the page for anyone running their own automation stack.
- **ChatGPT platform features** - Zendesk and OneNote plugins in beta, and Sites can now be shared externally, from 31 August and 3 September ([release notes](https://help.openai.com/en/articles/6825453-chatgpt-release-notes)).
- **Anthropic `ant` CLI 1.30.0** - 3 September, for developers on the Claude toolchain.
- **CleanShot 5.0** - a good screenshot tool, Mac only, so limited relevance for a mostly-Windows local market.

## Worth knowing, but it did not launch this week

Three things came up in research that people are calling new and are not. Saying so is the point of doing this weekly.

- **Refiant Protea**, a South African-founded model line with a ten-million-token context window, is being circulated as fresh. Their [own announcement is dated 8 July 2026](https://www.refiant.ai/article/refiant-launches-10-million-token-context-window-model-as-long-context-ai-race-heats-up). A recycled index page made it look current.
- **Framer AI Agents** - actually [16 June](https://www.framer.com/blog/ai-credits-simpler-plans-and-lower-prices/).
- **Stratos Lab, ECOBLOX and Digital Parks Africa** announced what they describe as Africa's most powerful AI cloud on [26 August](https://ecoblox.com/blog/news/stratos-lab-ecoblox-and-digital-parks-africa-partner-to-launch-most-powerful-african-ai-cloud/) - five days outside this window, so it does not qualify. But given that every single tool above routes your data offshore, African compute deserves its own segment soon rather than a footnote.

**Lelapa AI and Vulavula**, the South African multilingual speech work, kept surfacing but I could not date-verify a release inside this window, so it stays off the list. It is the local one I would most like to cover properly.

---

## What I would actually try this week

**One. Gemini 3.8 Flash, on the paid tier.** Not because it is the most exciting thing that shipped, but because it is the one where the numbers work and the data answer is written down. R12 per million input tokens, and a pricing page that states in a table that paid-tier data is not used to improve their products. Move one real workload onto it - document classification, message triage, catalogue text - and price it at the January 2027 rate of $1.50 and $7.50, not the promotional rate, so the business case survives the change.

**Two. AI Toolbox 3.0, on the free tier first.** Because it fixes a problem you have and have not named: your AI chat history is a working client record with no filing system. Test the free tier for a week on real client work. If it holds, the All Access Lifetime at $199, about R3,178, is a single exchange-rate hit rather than a monthly subscription, and Frankfurt hosting on DigitalOcean is a more specific data answer than most vendors will give you.

**And one thing to do rather than buy.** If you self-host n8n, patch it. Two CVEs were fixed this week, and the same week OpenAI shipped a model their own safety team rated Critical for finding novel exploits without human guidance. Those two facts belong in the same sentence.

---

*Prepared for Eride Technologies. Launch dates verified against primary sources; anything I could not date-verify inside the 31 August to 7 September window is listed as such rather than included. No vendor on this shortlist mentions POPIA in their documentation - every data-handling assessment above is inferred from GDPR-oriented language.*
