# AI Tools Drop  -  Week of 24 to 31 August 2026

**For South African founders and small businesses. Compiled Monday 31 August 2026, Johannesburg.**

---

## This week in one paragraph

Quiet at the frontier, busy at the coalface. Neither OpenAI nor Anthropic shipped a new product this week  -  Anthropic published a hardware-standard preview, a scientist-support programme and evaluation funding ([Anthropic news](https://www.anthropic.com/news)), and the only datable OpenAI material was three ChatGPT feature notes ([ChatGPT release notes](https://help.openai.com/en/articles/6825453-chatgpt-release-notes)). Google did ship two real milestones: Gemini 3.5 Transcribe went generally available on 26 August at roughly half a US cent per minute, and Gemini Omni Flash went GA on 27 August at roughly six dollars a minute of video ([Gemini API changelog](https://ai.google.dev/gemini-api/docs/changelog)). The most locally relevant launch of the week is South African: Telviva put out Viva, a voice and WhatsApp agent hosted in SA data centres ([TechCentral](https://techcentral.co.za/telviva-launches-viva-a-digital-agent-built-for-south-african-businesses/285458/)). Beyond that, the week's real theme is support automation that bills per outcome instead of per seat  -  three separate tools tried it, and two of them will not tell you the rate. Two housekeeping notes before we start, both of which affect what you are about to read: Product Hunt's daily leaderboards would not render for four of the seven days in this window, so this is honest coverage rather than exhaustive coverage; and the rand is currently being quoted four different ways by four different sources, spanning a 9.7 percent range.

---

## Before the tools: two disclosures

### 1. Four of seven days are under-covered

Product Hunt's daily leaderboards for 26, 28, 29 and 30 August would not render full rankings. The 26 August board gave a partial list on the first attempt and timed out on retry; 28, 29 and 30 August each returned a single stray entry and then timed out on every retry. Direct product-page fetches for x1, Screenify Studio and Jotform AI Data Assistant each returned HTTP 403.

The consequence is plain: anything that launched on 28, 29 or 30 August is very likely missing from this piece. That is a gap, not a judgement. Padding the list with older releases to hide it would be worse.

### 2. The rand has no agreed price this week

Four sources, four answers, a 9.7 percent spread:

| Source | USD/ZAR | Date on the page |
|---|---:|---|
| [XE](https://www.xe.com/currencyconverter/convert/?Amount=1&From=USD&To=ZAR) | 16.16758 | 11:56 UTC, 30 August |
| [Investing.com](https://www.investing.com/currencies/usd-zar) | 16.1690 | 28/08 |
| [Wise](https://wise.com/gb/currency-converter/usd-to-zar-rate) | 17.11 | not stated |
| [Google Finance](https://www.google.com/finance/quote/USD-ZAR) | 17.7101 | 25 August |
| [X-Rates](https://www.x-rates.com/table/?from=USD&amount=1) | 16.150572 | 1 January 2026  -  stale |

**Every rand figure below uses USD/ZAR 16.17**, because that is the only value with two independently dated sources in agreement  -  XE at 16.16758 on 30 August and [Investing.com](https://www.investing.com/currencies/usd-zar) at 16.1690 on 28/08. Google Finance's 17.7101 is both the outlier and the stalest live quote. X-Rates' figure is dated 1 January and should not be used at all. No source carried a quote timestamped 31 August; the freshest available was 30 August.

Treat every rand number in this piece as approximate. If you are budgeting, use the dollar figure and your own bank's rate on the day.

---

## 1. Telviva Viva

**A South African voice and WhatsApp agent, hosted in South African data centres.**

**What it actually is.** A digital agent sold in four tiers by Telviva, an established SA cloud telephony provider. Starter is a voice-only digital receptionist doing 24/7 inbound answering, presence checking and routing. Business adds WhatsApp and web chat, answering from your website or an uploaded FAQ. Professional connects to your existing CRM knowledge base as the source of truth. Enterprise does live CRM and ERP lookups, returning account balances, order status and contract dates ([TechCentral](https://techcentral.co.za/telviva-launches-viva-a-digital-agent-built-for-south-african-businesses/285458/), [Telviva](https://telviva.co.za/elevate-your-cx-24-7-introducing-digital-agent-viva/)).

**What it is genuinely good at.** Voice and WhatsApp for Business natively  -  the two channels South African customers actually use, rather than the web-chat widget most foreign tools assume. It resolves end to end where it can and hands over to a human with the full conversation context passed across ([Telviva](https://telviva.co.za/elevate-your-cx-24-7-introducing-digital-agent-viva/)). Telviva says it resolves more than 40 percent of inbound contact centre volume without a human in its own implementations ([Telviva](https://telviva.co.za/elevate-your-cx-24-7-introducing-digital-agent-viva/)).

**Honest limitations.** There is no published price anywhere. Pricing is described only as "a fixed monthly fee for unlimited simultaneous interactions" ([TechCentral](https://techcentral.co.za/telviva-launches-viva-a-digital-agent-built-for-south-african-businesses/285458/)). I fetched both the vendor page and the press release; neither publishes a figure in rands or dollars. It is sales-led, so budget for a quote cycle. The 40 percent resolution claim is vendor-reported and unaudited. Live CRM and ERP lookups are Enterprise-tier only. There is also a date question: TechCentral's article metadata says 27 August 2026, but the [Telviva product page](https://telviva.co.za/elevate-your-cx-24-7-introducing-digital-agent-viva/) carries no date at all and a search index dated that same page to 18 August. If the vendor page really went live on 18 August, only the press coverage falls inside this week's window.

**South African use cases.**
- An immigration practice puts Starter on the main line so visa-status callers get routed at 19:00 instead of hitting voicemail.
- A Sandton beauty and wellness group runs Business tier on WhatsApp for bookings, pricing and location questions answered from an uploaded FAQ.
- A lender or fintech runs Enterprise so a customer can ask "what is my balance" on WhatsApp, with a live core-system lookup that never leaves the country.

**Industries.** Fintech and payments, retail, logistics, professional services, immigration services, beauty and wellness.

**Pricing.** Not published. No monetary figure appears on any page I fetched.

**Access notes for SA.** The strongest in this week's list by a distance. Built and hosted locally, with "local POPIA-compliant deployment, with infrastructure hosted in South African data centres" plus enhanced private-cloud options for financial services, healthcare and legal ([TechCentral](https://techcentral.co.za/telviva-launches-viva-a-digital-agent-built-for-south-african-businesses/285458/)). No foreign card, no KYC wall, no US phone number. Telviva's core business is local numbers, though I did not find a page stating Viva's number-provisioning terms specifically, so treat that as unverified.

**Link.** [telviva.co.za](https://telviva.co.za/elevate-your-cx-24-7-introducing-digital-agent-viva/)

---

## 2. Gemini 3.5 Transcribe  -  now generally available

**Speech to text at about half a US cent a minute, with speakers separated.**

**What it actually is.** Google's transcription model reaching GA on 26 August ([Gemini API changelog](https://ai.google.dev/gemini-api/docs/changelog)). It does automatic language detection, speaker diarization, word-level timestamps and custom vocabulary biasing. A sibling model, `gemini-3.5-transcribe-live`, handles low-latency bidirectional streaming over WebSockets ([Gemini API pricing](https://ai.google.dev/gemini-api/docs/pricing)).

**What it is genuinely good at.** Cheap, high-volume transcription with speakers separated  -  which is the hard part of turning a recorded call into a usable file note. Custom vocabulary biasing matters more here than most places: generic speech recognition mangles South African names, place names and industry terms, and this lets you bias against that.

**Honest limitations.** On the free tier, Google's own pricing page marks "Used to improve our products: Yes", and "No" for the paid tier ([Gemini API pricing](https://ai.google.dev/gemini-api/docs/pricing)). For client audio, that is a direct POPIA problem  -  the free tier is for your own test recordings, not a client's intake interview. Grounding with Google Search is listed as not supported on both Transcribe models. And this is an API, not an app, so you need a developer to put it to work.

**South African use cases.**
- An immigration consultancy transcribes client intake interviews with diarization so consultant and applicant statements are separated in the file note  -  paid tier only.
- An agency turns recorded client briefs into scopes. At the blended rate, an hour of audio is about $0.30, roughly R4.85.
- A logistics operator turns driver voice notes into ticket text.

**Industries.** Professional services, immigration services, agency and creative, logistics, SaaS building.

**Pricing** ([Gemini API pricing](https://ai.google.dev/gemini-api/docs/pricing)). `gemini-3.5-transcribe` paid tier: input $2.00 per million tokens or $0.003 per minute of audio; output $12.00 per million tokens or $0.002 per minute of text. Google's own footnote gives an effective blended rate of about $0.005 per minute, roughly 8 South African cents. `gemini-3.5-transcribe-live` paid tier: input $0.005 per minute, output $0.004 per minute, blended about $0.009 per minute, roughly 15 cents. Free tier is free of charge on both models, with limited model access  -  and your content used to improve Google's products.

**Access notes for SA.** Google AI Studio and the Gemini API are reachable from South Africa on an ordinary card. No page I fetched stated a US-only card or phone requirement. The POPIA-safe path is the paid tier, and at these rates the paid tier is cheap enough that there is no real argument for the free one on client work.

**Link.** [ai.google.dev/gemini-api/docs/pricing](https://ai.google.dev/gemini-api/docs/pricing)

---

## 3. Jotform AI Data Assistant

**Talk to your form submissions. The free tier is real and published to the digit  -  the new product's price is not published at all.**

**What it actually is.** An AI workspace inside Jotform Tables that turns submitted data into tables, insights and charts, announced 25 August ([Jotform](https://www.jotform.com/blog/announcing-jotform-ai-data-assistant-for-teams/)). Listed capabilities: create tables, analyse, visualise, automate work, collaborate, follow up, manage submissions, run bulk actions, customise tables, discover insights, and speak your request instead of typing it ([Jotform](https://www.jotform.com/ai/data-assistant/)). It ranked fourth with 246 votes on the [Product Hunt board for 25 August](https://www.producthunt.com/leaderboard/daily/2026/8/25).

**What it is genuinely good at.** Closing the gap between collecting data and understanding it, without exporting to a spreadsheet first. If your team already runs intake, quotes or bookings through Jotform, this is a zero-migration upgrade rather than a new system.

**Honest limitations.** It only sees what is already in Jotform  -  this is not a general business intelligence tool. More awkwardly, the [product page](https://www.jotform.com/ai/data-assistant/) publishes no pricing, no free-tier limits, no data-training statement and no residency statement, and the [pricing page](https://www.jotform.com/pricing) never names "AI Data Assistant" at all; it lists "AI Agents" limits instead. So there is no vendor page anywhere stating what this new product costs or which plan includes it. Free-tier forms also carry Jotform branding.

There is a second oddity worth knowing about. Jotform serves two materially different pricing pages at two URLs. [jotform.com/pricing](https://www.jotform.com/pricing) renders full amounts. The same page with a trailing slash renders tier names and terms but no monetary amounts at all. The two renders even disagree on company scale  -  over 40 million users on one, over 35 million on the other. Use the version without the trailing slash.

**South African use cases.**
- An immigration practice runs client intake through a Jotform, then asks which document types most often cause rework.
- A Joburg salon group collects post-visit feedback and asks for the top complaint themes per branch, with no dashboard built.
- A retailer runs supplier onboarding forms and asks which submissions are missing B-BBEE or tax documents.

**Industries.** Immigration services, beauty and wellness, retail, professional services, agency and creative.

**Pricing** ([jotform.com/pricing](https://www.jotform.com/pricing)). Starter $0. Bronze $39 per month or $408 per year, about R631 monthly. Silver $49 per month or $468 per year, about R792 monthly. Gold $129 per month or $1,188 per year, about R2,086 monthly. Enterprise custom. Jotform charges euros to users in Europe and US dollars to the rest of the world, so South Africa is billed in USD ([Jotform pricing](https://www.jotform.com/pricing/)). Note again that none of these tiers is stated to include the AI Data Assistant.

**Free tier.** Yes, and published precisely: one user, 5 active forms, 100 monthly submissions, 10,000 monthly form views, 100 MB upload space, 500 total stored submissions, 10 payment submissions a month, 10 signed documents a month, 100 fields per form, 5 active AI agents, 100 monthly AI agent conversations, 3,000 monthly AI agent voice minutes and 250 monthly AI agent SMS ([Jotform pricing](https://www.jotform.com/pricing)). No HIPAA features, Jotform branding included.

**Access notes for SA.** Card or PayPal, 30-day money-back guarantee, tax applied per local regulation and removable with a valid Tax ID ([Jotform pricing](https://www.jotform.com/pricing/)). No US-only requirement stated. Data-protection posture is unresolved: neither the product page nor the pricing page states whether the free tier trains on your data, so read the DPA before you put client personal information through it.

**Link.** [jotform.com/ai/data-assistant](https://www.jotform.com/ai/data-assistant/)

---

## 4. x1  -  AI App Studio

**Idea to App Store submission for iPhone, on a free tier that needs no card  -  and paid users get the source code out.**

**What it actually is.** A guided build workflow that plans screens and flows, designs brand and layout, builds step by step, then prepares App Store assets including screenshots, descriptions, subtitles and keywords, and handles release prep, analytics and monetisation. Output is real React Native. You preview on device through Expo Go, run beta through TestFlight, then submit. Paid plans export the full React Native source as a ZIP ([x1](https://x1.new/)). It sat at number one on the [Product Hunt board for 26 August](https://www.producthunt.com/leaderboard/daily/2026/8/26), described as "Lovable for iPhone apps".

**What it is genuinely good at.** Getting a non-engineer founder from idea to a submittable iOS app, and  -  this is the part that matters  -  not locking you in, because the paid tiers hand over the source. That turns it from a walled garden into a head start.

**Honest limitations.** iPhone only; no Android path is stated. An Apple Developer account is required ([x1](https://x1.new/)), which is a separate annual cost x1 does not cover and carries its own identity verification. It is credit-based, so heavy iteration burns budget. Nothing on the page addresses whether x1 trains on your project data, or where that data sits. The site itself states no launch date, and a direct fetch of its Product Hunt product page returned HTTP 403, so the leaderboard is the only date source I have.

**South African use cases.**
- A Joburg beauty and wellness chain ships a simple loyalty and booking app without hiring an iOS developer.
- An SME logistics operator builds a driver proof-of-delivery app, tests it with ten drivers through TestFlight, then exports the source to hand to a local dev shop.
- A professional-services firm ships a client-portal app as a retention play.

**Industries.** SaaS building, beauty and wellness, retail, logistics, agency and creative.

**Pricing** ([x1.new](https://x1.new/)). Free tier of 100 credits. Paid plans at $20, $50 and $100 per month, billable monthly, quarterly or yearly. The $20 tier is about R323 a month.

**Free tier.** Yes and genuinely usable: 100 credits, no credit card required, credits never expire, enough to validate an idea, generate a plan, explore designs and build a first milestone ([x1](https://x1.new/)).

**Access notes for SA.** No card required to start, which removes the usual first barrier. No region block, KYC or US phone requirement stated. The real local friction is the Apple Developer account you need to publish.

**Link.** [x1.new](https://x1.new/)

---

## 5. Screenify Studio 2.0

**Cinematic product demos on a Mac, processed on-device. The best data posture in this week's list.**

**What it actually is.** A native macOS cinematic screen recorder and mockup studio: auto-zoom on clicks, cursor smoothing, 3D iPhone, iPad, MacBook and Mac mini mockups, multi-device 3D scenes, callouts, transitions, captions, voiceover, backgrounds and device frames, plus iOS Simulator or real-iPhone recording and a CLI for recording AI web demos. Optimised for Apple Silicon through Metal and the Neural Engine. An 80 MB app on macOS 13 and up ([Screenify Studio](https://www.screenify.studio/)). It appeared on the [26 August Product Hunt board](https://www.producthunt.com/leaderboard/daily/2026/8/26); the site says "we're live on Product Hunt today" and flags "New in 2.0  -  Multi-Device Mockup Studio", but prints no calendar date.

**What it is genuinely good at.** Local processing. "Nothing leaves your Mac unless you choose to share." Captions run Whisper locally, and translation, background removal and smart clipping run on the Apple Neural Engine, with recordings staying on device ([Screenify Studio](https://www.screenify.studio/)). It is also one-time-purchase software, which beats subscription arithmetic when the rand is weak.

**Honest limitations.** macOS only and Apple Silicon-optimised, so useless in a Windows shop. The free tier watermarks exports, caps resolution at 1080p, caps duration at five minutes, excludes all AI features, and its share links expire after seven days. And the pricing page shows two different prices for each paid tier simultaneously  -  Pro at both $149 one-time and "$179 Early Access price", Pro+ at both $249 and "$299 Early Access price". Which one you actually pay is not resolvable from the page. The page's competitive comparison section is also dated "based on publicly available information, February 2026"  -  six-month-old claims on a launch-week page.

**South African use cases.**
- An agency produces client-facing walkthroughs of work in progress without uploading unreleased client screens to a foreign cloud. That is a real POPIA and NDA win, not a marketing line.
- A Joburg SaaS founder records a polished 4K demo for a pitch deck for one payment of $149, about R2,409, instead of another monthly subscription.
- A fintech records internal SOP videos containing customer-facing screens entirely on-device.

**Industries.** Agency and creative, SaaS building, fintech and payments, professional services.

**Pricing** ([screenify.studio](https://www.screenify.studio/)). Free forever at $0. Pro $149 one-time, about R2,409, including one year of updates then an optional $39 a year. Pro+ $249 one-time, about R4,026, with lifetime updates, five devices and 100 GB cloud storage. Pro users can pay a fixed $100 to upgrade to lifetime updates. 30-day money-back guarantee. Note the duplicate Early Access prices above.

**Free tier.** Yes, and specific: unlimited recording with no time limit, unlimited local export, 1080p export cap, exports up to five minutes, watermark on exports, three share links expiring after seven days, AI features excluded  -  but the full editing suite, 3D mockups, multi-window recording and iPhone recording all included. No card required ([Screenify Studio](https://www.screenify.studio/)).

**Access notes for SA.** One-time purchase, no card requirement for the free tier, no region block stated. Because the AI runs locally, this has the cleanest data-protection posture of anything in this week's list.

**Link.** [screenify.studio](https://www.screenify.studio/)

---

## 6. ify

**Resolution AI on top of the helpdesk you already have, billed per resolved ticket  -  at a rate it will not publish.**

**What it actually is.** A layer over Freshdesk, Zendesk, Salesforce or HubSpot, working across email, chat, WhatsApp and Slack. It builds its own knowledge base by reading your sites and documentation, and generates SOPs from release notes and past ticket resolutions ([Product Hunt](https://www.producthunt.com/products/ify-2)). Billing is outcome-based: your bill equals resolved tickets, and a resolution counts whether the AI or a human closed it ([ify pricing](https://useify.ai/pricing)). Launched 26 August on the [Product Hunt board](https://www.producthunt.com/leaderboard/daily/2026/8/26).

**What it is genuinely good at.** Not forcing a helpdesk migration, which is the single biggest reason small businesses never adopt support AI. WhatsApp coverage is the correct channel choice for this market. Seat cost is genuinely zero, so the whole team can be inside the tool.

**Honest limitations.** The rate per resolved ticket is not published. The pricing page says "talk to us for a rate" ([ify pricing](https://useify.ai/pricing)). That makes budgeting impossible before a sales call, and the rule that a resolution counts regardless of who closed it means you pay for tickets your own people handled. No statement on data privacy or training appears on the pricing page. And auto-generating a knowledge base by reading your docs needs a human review pass before it answers customers unsupervised.

**South African use cases.**
- An e-commerce retailer already on Zendesk adds AI resolution on WhatsApp for "where is my order" without changing systems.
- An immigration firm lets it handle document-checklist and status questions from generated SOPs, escalating anything substantive to a consultant.
- A fintech deflects password, limit and fee questions across chat and email.

**Industries.** Retail, fintech and payments, logistics, immigration services, professional services, SaaS building.

**Pricing** ([useify.ai/pricing](https://useify.ai/pricing)). $0 per agent, $0 per seat, $0 to add a teammate. Agents always free. Resolved tickets: talk to us for a rate.

**Free tier.** None. A 14-day free trial, setup under 20 minutes, cancel anytime ([ify pricing](https://useify.ai/pricing)).

**Access notes for SA.** Not stated. No page I fetched addresses card requirements, KYC, region availability or billing currency. WhatsApp is a supported channel, but no page says whether ify provisions numbers or expects you to bring your own WhatsApp Business number. Since pricing is sales-led anyway, ask all of this on the call.

**Link.** [useify.ai](https://useify.ai/)

---

## 7. MCP-Builder.ai

**Point it at your legacy database or ERP and it hosts a production MCP server  -  with an EU residency option and an entry tier that is really a demo.**

**What it actually is.** A hosted MCP-server service. You describe the use case; it builds, secures and hosts a production MCP server reachable at one URL. It connects modern APIs, legacy databases, ERP systems, storage and custom systems to Claude, ChatGPT, Microsoft Copilot, Mistral, Cursor, Windsurf, Gemini, Perplexity, LangChain, n8n, Zapier and any MCP client. It claims more than 5,000 servers built, under five minutes from prompt to live, and 99.9 percent hosted uptime ([MCP-Builder.ai](https://mcp-builder.ai/)). Listed on the [26 August Product Hunt board](https://www.producthunt.com/leaderboard/daily/2026/8/26).

**What it is genuinely good at.** The hardest step in small-business AI adoption  -  getting an assistant to safely read the ugly system the business actually runs on. Its stated data posture is unusually strong for a launch-week tool: no data stored on server, data read at request time and forwarded rather than persisted, TLS on all connections, credentials encrypted at rest, OAuth, API key and JWT auth, full audit logs on every tool call, EU hosting and EU data residency available, and an on-premise option to run the whole server inside your own infrastructure ([MCP-Builder.ai](https://mcp-builder.ai/)).

**Honest limitations.** No free tier. Entry is $29 a month and that tier allows only 100 requests a month, which is a demo allowance rather than a working one  -  and requests are counted per account, not per server. The residency options are EU, not South African: useful for a cross-border transfer argument under POPIA, but not local. The page offers to "try it risk-free for 7 days" while listing no free tier, which means a refund window rather than free usage. And the Launch tier lists "100 Requests" and "100 Requests / month" as two separate line items, which reads as padding.

**South African use cases.**
- A logistics operator exposes its legacy consignment database as an MCP server so ops staff can query shipment status in plain language.
- An accounting or professional-services firm wires its practice-management system into ChatGPT for fee and WIP queries, using the on-premise option to keep client data in-house.
- A retailer connects its ERP so a stock-availability agent can answer without a custom integration project.

**Industries.** Logistics, retail, professional services, fintech and payments, SaaS building.

**Pricing** ([mcp-builder.ai](https://mcp-builder.ai/)). Launch $29 a month, about R469: one server, 100 requests a month, five tools, API-key auth. Pro $75 a month, about R1,213: three servers, 1,000 requests, 15 tools. Scale $290 a month, about R4,689: 20 servers, 100,000 requests, unlimited tools, priority support. Enterprise custom, with on-premise or hosted, OAuth 2.0 and custom identity provider, custom domain, bring-your-own LLM key, team management and an observability stack.

**Access notes for SA.** No region block, KYC or US card requirement stated. Currency shown is USD. EU residency and the on-premise option are the POPIA-relevant levers here.

**Link.** [mcp-builder.ai](https://mcp-builder.ai/)

---

## 8. Skydive

**Cloud agents with a $0 no-card workspace, model costs passed through at cost, and a hard spend cap.**

**What it actually is.** A subscription agent platform where the plan fee converts one for one into a dollar usage-credit balance. Agents spend that balance on model usage billed at cost with provider rates passed through, on sandbox time for browsing, running code and hosting apps, and on metered services like search and email ([Skydive pricing docs](https://www.skydive.com/docs/account/pricing)). It was number one on the [27 August Product Hunt board](https://www.producthunt.com/leaderboard/daily/2026/8/27) as "build cloud agents that work across your tools".

**What it is genuinely good at.** Cost transparency, which is not a phrase I use often. Model usage is passed through at cost, you can set a monthly cap at any time, and pay-as-you-go workspaces have no overdraft cushion  -  agents stop rather than running up a bill. For a rand-denominated business buying in dollars, a hard stop is worth more than a discount.

**Honest limitations.** The subscription fee is the credit, so $20 a month buys $20 of agent work; heavy use exceeds it and bills at plan rate. The free tier caps at two seats. No statement on data privacy or training appears in the pricing docs. And it appears to have launched twice in eight days: a Skydive with a different tagline, "AI coworkers that actually get work done", sits on the [20 August board](https://www.producthunt.com/leaderboard/daily/2026/8/20). So treat this week's item as a major feature launch on an existing product, not a new company.

**South African use cases.**
- An agency runs a research-and-drafting agent for client pitches at a hard $20 a month cap, avoiding surprise dollar spend.
- A professional-services firm has an agent monitor a shared inbox and pre-draft replies, with the monthly cap acting as the budget control.
- A small SaaS team uses sandbox time to have agents build and host internal tools without provisioning infrastructure.

**Industries.** Agency and creative, professional services, SaaS building, fintech and payments.

**Pricing** ([Skydive pricing docs](https://www.skydive.com/docs/account/pricing)). Free $0 a month pay-as-you-go, up to two seats. Starter $20 a month, about R323, giving $20 monthly credit, unlimited agents, up to five seats and email support  -  or $240 a year with $264 of usage credit. Team $200 a month, about R3,234, giving $200 credit, unlimited agents and seats, priority support  -  or $2,400 a year with $2,640 credit. Enterprise custom with SSO and SAML, advanced security and audit logs. Yearly plans give a 10 percent bonus credit; the yearly fee itself is exactly twelve times monthly with no discount.

**Free tier.** Yes: $0 a month, no card required, up to two seats, agents enabled, auto-refill when the balance runs low, and a settable monthly cap ([Skydive pricing docs](https://www.skydive.com/docs/account/pricing)).

**Access notes for SA.** No card required for the free workspace. No region block, KYC or US phone requirement stated. Data posture is not addressed anywhere in the pricing docs.

**Link.** [skydive.com/start](https://www.skydive.com/start)

---

## 9. Speko

**One API in front of every speech model, benchmarked language by language, at $0.09 a minute all in.**

**What it actually is.** Two parts. Router is a hosted, provider-neutral speech-to-text, LLM and text-to-speech data plane at `router.speko.dev` with typed contracts and managed routing. Gateway is an open customer-side runtime for LiveKit and Pipecat with provider-direct streaming and local bring-your-own-key credentials. Public OpenAPI and AsyncAPI contracts, an MCP endpoint, Y Combinator-backed ([Speko](https://speko.ai/)). Fourth on the [27 August Product Hunt board](https://www.producthunt.com/leaderboard/daily/2026/8/27) as "OpenRouter for Voice".

**What it is genuinely good at.** Per-language benchmarking, which is exactly the axis that matters in a multilingual market. It publishes word error rate alongside price per minute for 16 speech-to-text models, 13 LLMs and 22 text-to-speech models, and routes with pre-response failover so a provider outage does not take down your voice app ([Speko pricing](https://speko.ai/pricing)).

**Honest limitations.** Both the Router and Speko-infra tiers are in public preview with no SLA ([Speko pricing](https://speko.ai/pricing)). There is no free tier, only signup credit. The 5 percent Router markup stacks on top of provider rates. No statement on data privacy, training or residency appears on the pages I fetched. And I found no page confirming whether its benchmarks cover isiZulu, Afrikaans or South African English specifically  -  the language-by-language claim is generic on the homepage, so verify it against your own audio before you commit.

One more thing worth crediting: Speko publishes other vendors' contradictions on its own comparison page, including a note that one competitor's pricing page contradicts its model page and that the vendor "never publishes an exact rate". That is useful honesty, but it also means every provider rate on Speko's table is second-hand relative to that provider's own page. Quote them as Speko's benchmark, not as the provider's price.

**South African use cases.**
- A fintech building a voice IVR benchmarks speech-to-text accuracy on SA-accented English before committing to a provider, then routes with automatic failover.
- A logistics company runs driver voice notes through the cheapest acceptable model. Per Speko's own table the spread on the same task runs from $0.0010 to $0.0170 a minute  -  a seventeen-fold difference ([Speko](https://speko.ai/)).
- An agency prototypes a voice product at $0.09 a minute all in without signing three separate vendor contracts.

**Industries.** Fintech and payments, logistics, retail, agency and creative, SaaS building.

**Pricing** ([speko.ai/pricing](https://speko.ai/pricing)). Router adds 5 percent to the provider's published rate. Speko infra is $0.09 per minute all in across speech-to-text, LLM and text-to-speech  -  about R1.46 a minute. Enterprise is custom and locked for the term with a committed monthly minimum.

**Free tier.** None stated. $100 in signup credit applies to every account, applied before paid usage, with no expiry stated ([Speko pricing](https://speko.ai/pricing)).

**Access notes for SA.** Not stated. No page addresses card requirements, KYC, region availability or number provisioning. It is a model router rather than a carrier, so numbers come from LiveKit, Pipecat or your own provider.

**Link.** [speko.ai/pricing](https://speko.ai/pricing)

---

## 10. Helply

**A dollar a ticket with unlimited free seats. Clean arithmetic, but a $250 a month floor.**

**What it actually is.** An AI-native B2B helpdesk with per-ticket pricing. Every ticket includes an AI teammate and every seat is free. Included on every ticket: resolve issues, take action, escalate intelligently, detect churn, surface upsell opportunities, find bugs, capture feature requests, generate documentation. Platform features cover unlimited agents and seats, shared inbox, email, chat and messaging, AI triage, AI replies, AI actions, workflow automation, smart escalations, knowledge base, analytics, API access, onboarding and premium support ([Helply pricing](https://helply.com/pricing)). On the [24 August Product Hunt board](https://www.producthunt.com/leaderboard/daily/2026/8/24) with the tagline "65% AI resolution rate in 90 days, or you pay nothing". Search coverage suggests Helply pricing pages existed in June, so this may be a relaunch; I could not verify that from a vendor page.

**What it is genuinely good at.** Pricing that scales with your customers rather than your headcount, which is a real advantage when your staff costs are in rands and your software costs are in dollars. Unlimited free seats means everyone who touches a customer can be in the tool.

**Honest limitations.** The $250 a month minimum is the killer for a small business. You pay for 250 tickets whether you have them or not, and the minimum annual contract is $3,000. "Any customer conversation processed through Helply counts as a ticket", so the meter is broad. Most customers go live within two weeks, so it is not a same-day switch. And no statement on data privacy or AI training appears on the pricing page.

**South African use cases.**
- A mid-size e-commerce retailer with 400-plus monthly queries drops a seat-based helpdesk and puts warehouse and customer service staff in for free.
- A fintech with spiky support volume pays for the volume it actually gets rather than for peak-season headcount.
- An agency running white-glove client support gives every account manager a seat at no marginal cost.

**Industries.** Retail, fintech and payments, logistics, SaaS building, agency and creative.

**Pricing** ([helply.com/pricing](https://helply.com/pricing)). Starting at $1 per ticket, minimum 250 tickets a month, which is a $250 a month floor  -  about R4,042. Minimum annual contract $3,000, about R48,510. No seat fees, unlimited agents and seats, AI usage unlimited and included. Volume discounts for larger teams.

**Free tier.** None stated. No free tier or trial figure appears on the pricing page.

**Access notes for SA.** Not stated. No page addresses card, KYC, region or billing currency. Assume dollars and assume a sales conversation for the annual contract.

**Link.** [helply.com/pricing](https://helply.com/pricing)

---

## Also launched this week, weaker fit

**Gemini Omni Flash went GA on 27 August** ([Gemini API changelog](https://ai.google.dev/gemini-api/docs/changelog))  -  Google's next-generation video generation and editing model, available to developers on the paid tier only. Input $1.50 per million tokens; output $9.00 for text and $17.50 for video per million tokens, billed at 5,792 tokens per second of 720p video, which works out to roughly $0.10 per second, about $6 a minute or R1.62 per second ([Gemini API pricing](https://ai.google.dev/gemini-api/docs/pricing)). Free tier: not available. At that rate a 30-second social clip is about $3 in generation alone before you iterate. This is an agency tool, not a small-business tool.

**Lightfield, an AI-native CRM, launched 26 August** ([Product Hunt](https://www.producthunt.com/leaderboard/daily/2026/8/26))  -  an agentic CRM building a living model of every customer from calls, emails and meetings, with an agent SDK, call recording and MCP connectivity ([Lightfield](https://lightfield.app/)). Pro is $1,000 a month, about R16,170 ([Lightfield pricing](https://lightfield.app/pricing)). It misses the cut on arithmetic from its own FAQ: budget roughly 37,000 credits a month per active seller, "about $1,450 per month per seller", which is about R23,447 per seller per month. The "5,000 free credits" Starter tier is therefore around 13 percent of one seller's monthly need. Its trust block also lists ISO 27001 as "Soon", which is a badge for a certification not yet held.

**Three ChatGPT feature notes landed in-window** ([ChatGPT release notes](https://help.openai.com/en/articles/6825453-chatgpt-release-notes)). On 28 August, connecting multiple Gmail, Google Calendar and Google Contacts accounts in one conversation, globally on supported Plus, Pro, Business and Enterprise plans. On 27 August, more controls in temporary chat, including optionally personalised temporary chats and the ability to save one. On 25 August, scheduled tasks in ChatGPT Work triggerable by webhooks on new Gmail messages, Slack channel messages and GitHub pull request activity, for Plus and Pro. The 27 August item is the POPIA-relevant one: a non-personalised temporary chat uses no memory, no custom instructions and no plugins, and creates no memories, which is the closest thing to a clean-room mode for client data. These are features on an existing product, not launches.

**Vercel shipped several things between 27 and 30 August** ([Vercel changelog](https://vercel.com/changelog)), and one of them is the most immediately useful item in this whole section for a cost-constrained developer: **Ling 3.0 Flash Fin is free on AI Gateway through 25 September** via a `-free` model ID that stops serving rather than billing when the allowance runs out. A model that stops instead of billing is a hard budget guarantee, not a discount. Also in-window: building and deploying eve agents from the Vercel dashboard, Hy4 Preview on AI Gateway, expanded CLI for DNS, domains and projects, and MiniMax H3 at 50 percent off on AI Gateway through 13 September.

**Alibaba relaunched Qoder on 27 August** as an intelligent agent workspace rather than an AI programming IDE, with a Programming mode for developers and a General mode letting non-technical users build prototypes, manage data and troubleshoot without code, plus cross-session long-term memory, hierarchical permissions and a tool whitelist. **Second-hand flag:** this comes from [AIBase](https://www.aibase.com/news/30691), an aggregator, not from Alibaba's own page, and no monetary price is published for any tier. Treat the date and all detail as unverified.

---

## What I would actually try this week

**First: Telviva Viva.** Get a quote. It is the only tool on this list built for the channels South African customers actually use, hosted inside the country, by a vendor whose core business is already local telephony. Voice plus WhatsApp with POPIA-compliant local hosting is not something a foreign vendor can offer you, at any price. Go in knowing that no price is published anywhere, so you are negotiating blind  -  ask for the fixed monthly fee across all four tiers in writing, ask what "unlimited simultaneous interactions" excludes, and ask them to substantiate the 40 percent resolution claim with a reference customer in your sector.

**Second: Gemini 3.5 Transcribe on the paid tier.** At an effective half a US cent a minute, transcription with speaker separation and custom vocabulary is now cheap enough that there is no reason for a professional-services or immigration practice not to have a proper record of every client call. Pay for it. The free tier trains on your content, and for client audio that is not a trade-off you should be making.

**One to be careful with: Helply.** The $1-per-ticket headline is genuinely clean and the free seats are genuinely valuable, but the $250 a month floor and the $3,000 minimum annual contract mean you are committing about R48,500 a year before you know whether the AI resolves anything. If your monthly ticket volume is not comfortably above 250, this is a seat-based helpdesk with extra steps. Run the arithmetic on your actual volume first.

**If you write code: take the free Ling 3.0 Flash Fin model ID on Vercel AI Gateway before 25 September.** A model that refuses to serve rather than quietly billing you is the safest way to let a team experiment with agents in a rand-denominated business.

---

## What we deliberately left out, and why

**Playcall** would have been an excellent fit  -  open source, self-hostable on Vercel and Supabase for free, keeps call data on your own infrastructure, scores calls against MEDDPICC, BANT, SPIN or your own playbook, and supports OpenAI, Anthropic, Gemini, Mistral, Groq, Cohere, Perplexity and Together AI. It is excluded on a date conflict: it appears on the [26 August leaderboard](https://www.producthunt.com/leaderboard/daily/2026/8/26) but its Product Hunt launch page is indexed at 14 August, and its own site states no date and no pricing. I could not resolve the date from a vendor page, so it is not counted as a launch this week. Worth watching regardless.

**Perplexity's Portable Computer** is out because I could not verify it. [perplexity.ai/pricing](https://www.perplexity.ai/pricing) returned HTTP 403 and the product page timed out. The subscription figures circulating  -  Pro at $20 a month, Max at $200  -  are second-hand from [Cryptobriefing](https://cryptobriefing.com/perplexity-portable-computer-nvidia-dgx-spark/), a news site, not from Perplexity. That same source gives no specific launch date, and it runs on separately purchased NVIDIA DGX Spark hardware with Linux support only at first. I am not presenting second-hand prices as vendor prices.

**TechCrunch and VentureBeat were unusable this week.** [TechCrunch's AI section](https://techcrunch.com/category/artificial-intelligence/) rendered headlines with no publication dates at all, and [VentureBeat's AI section](https://venturebeat.com/category/ai/) rendered neither headlines nor dates. Neither was used to source a launch, because nothing on either page could be date-bounded to the window.

**n8n 2.36.0** is real and confirmed in the [official changelog](https://raw.githubusercontent.com/n8n-io/n8n/master/CHANGELOG.md), but it is dated 18 August  -  outside the window. It is in the catch-up section below.

**A second-hand-source blocklist was applied.** MakerStack, explainX, Releasebot, visalytica, onei.ai, aikaptan, efficient.app, ahoy.ai, eesel.ai, kompozy, ProductCool and completeaitraining all surfaced in search and were excluded from every pricing claim in this piece. The only second-hand figures anywhere above are the Perplexity subscription prices and the Alibaba Qoder details, and both are labelled as such.

---

## Catch-up: 17 to 24 August

The scheduled run for that week did not produce, so here are the four launches from it I could date-verify. These are not part of this week's list.

- **Grok 4.6, 20 August**  -  "frontier intelligence for long-running agents", on the [20 August leaderboard](https://www.producthunt.com/leaderboard/daily/2026/8/20). Distinct from Grok Bot. Pricing not verified; [x.ai/news](https://x.ai/news) rendered nothing dated for the period.
- **Origin by Cursor, 19 August**  -  "the Git forge built for the age of coding agents", third on the [19 August leaderboard](https://www.producthunt.com/leaderboard/daily/2026/8/19). Pricing not verified.
- **The New Calendly, 20 August**  -  "handle all of the work before, during, and after meetings", on the [20 August leaderboard](https://www.producthunt.com/leaderboard/daily/2026/8/20). Relevant to South African professional-services and beauty and wellness bookings. Pricing not verified.
- **n8n 2.36.0, 18 August**  -  confirmed in the [official n8n changelog](https://raw.githubusercontent.com/n8n-io/n8n/master/CHANGELOG.md). Self-hostable, which makes it the POPIA-friendly automation option for a South African business that would rather not send workflow data abroad.

---

## The South African read on this week

Three things stand out.

**The channel gap keeps closing from the local side, not the foreign side.** Telviva Viva is a local vendor solving voice-plus-WhatsApp-plus-POPIA in one product because it already owned the telephony. Meanwhile ify supports WhatsApp as one channel among several and will not tell you what it costs. When the local option and the foreign option are close on capability, the local one wins on data residency and on billing you in a currency you earn.

**Outcome pricing arrived this week and it is not automatically cheaper.** Three tools tried per-ticket or per-resolution billing. Helply publishes $1 a ticket and a $250 floor, so you can at least do the arithmetic. ify publishes $0 seats and no rate at all. Skydive converts the subscription into credit at cost with a hard cap. Only two of those three let you build a budget before a sales call, and only one of them lets an agent stop instead of spending.

**On-device is becoming a real competitive axis.** Screenify Studio's whole pitch is that nothing leaves your Mac. MCP-Builder's is that no data is stored on its servers. Both of those are POPIA arguments dressed as feature bullets, and both are more useful to a South African business than another point of model benchmark. When a vendor cannot tell you where your data sits  -  which is the case for ify, Skydive, Speko and Helply this week  -  that silence is the answer.

---

## Verification note

Every price, date and feature above was read from a page fetched during research on 31 August 2026. Where a figure could not be confirmed from a vendor page it is written as not published or not stated, rather than estimated. Where a figure came from a news site rather than the vendor, it is labelled second-hand. Rand conversions use USD/ZAR 16.17 as set out at the top, and are approximate by design  -  no rand figure here is exact.

Product Hunt coverage for 26, 28, 29 and 30 August is incomplete because those leaderboards would not render. Neither OpenAI nor Anthropic launched a product in this window. If you see a claim elsewhere that they did, check the date on it.
