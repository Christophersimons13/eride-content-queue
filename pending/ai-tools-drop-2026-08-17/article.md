# AI Tools Drop - Week of 10 to 17 August 2026

Weekly AI tool review for South African founders and small business owners. Every launch date, price and claim below was verified against a source page during research, and the source is linked at the point of use.

Rand conversions use USD/ZAR at about **R16.20** and EUR/ZAR at about **R18.75**. The dollar rate is flat on the week ([Xe, 17 August](https://www.xe.com/currencyconverter/convert/?Amount=1&From=USD&To=ZAR) at 16.16, [Investing.com](https://www.investing.com/currencies/usd-zar) at 16.18). The euro rate is drawn from [Xe on 17 August](https://www.xe.com/currencyconverter/convert/?Amount=1&From=ZAR&To=EUR) at 18.73. Rand figures are indicative, not exact, and exclude your bank's card fee.

---

## This week in one paragraph

This was a thin week for products and a heavy week for models, and I am going to say so rather than pad the list. Product Hunt's leaderboards from 10 to 16 August were dominated by developer infrastructure - evaluation harnesses, agent sandboxes, command-line tools - with very little a non-technical business could pick up and use. Nine items are verified inside the window and only about four of them are genuinely adoptable by a Johannesburg SMB without a developer on hand. The week's most useful item is not a startup at all: **Google shipped Gemini 3.7 Flash** on 13 August at a price that is deliberately temporary, and the fine print matters more than the benchmark scores. The best free tier on the list is **Dograh**, an open-source voice phone agent platform that handles 70-plus languages with mid-call switching, which is unusually relevant to a business fielding English, isiZulu, Sesotho and Afrikaans callers on one number. There is also a genuine pattern worth naming: **vendor pricing pages were unusually broken this week.** Vizard renders zeros where its paid prices should be, Z.ai shows two different prices for every tier, and xAI puts a "get started for free" button next to a 300 dollar per month plan. Where a vendor could not state its own price, I have said the price is unverifiable rather than borrowing a number from a review site and presenting it as fact. And the most important South African story of the week was not a tool: TechCentral reported that only about a quarter of surveyed SA firms are running AI in production at all.

---

## 1. Gemini 3.7 Flash

**The hook:** the cheapest frontier-adjacent model you can put into production this week, at a price that nearly doubles on 1 January 2027.

**What it actually is.** Google's mid-tier general-purpose model, now generally available. The [Gemini API changelog](https://ai.google.dev/gemini-api/docs/changelog) records "August 13, 2026 - Gemini 3.7 Flash generally available (GA)", confirmed by the [DeepMind model card](https://deepmind.google/models/model-cards/gemini-3-7-flash/) and [Reuters](https://www.reuters.com/business/google-unveils-gemini-37-flash-ai-model-coding-agent-workflows-2026-08-13/). It carries a 1 million token context window, 64k output, and selectable thinking levels, under the model ID `gemini-3.7-flash` ([model docs](https://ai.google.dev/gemini-api/docs/latest-model)). It replaces the previous Flash release just three weeks after that one shipped ([Ars Technica](https://arstechnica.com/ai/2026/08/google-announces-gemini-3-7-flash-just-three-weeks-after-previous-release/)).

**What it is genuinely good at.**

1. Coding and agentic work. DeepSWE v1.1 moved from 49.0 to 65.3 percent and FrontierCode 1.1 from 34.4 to 43.6 percent against the prior Flash ([9to5Google](https://9to5google.com/2026/08/13/gemini-3-7-flash-launch/)).
2. Long documents at low cost. A 1 million token input window with context caching at 0.075 dollars per million tokens, about R1.22 ([Gemini API pricing](https://ai.google.dev/gemini-api/docs/pricing)). That is the number that matters for immigration case files, lease agreements and policy documents.
3. Business process automation. AutomationBench rose from 17 to 30.4 percent and GDP.pdf from 22 to 34 percent ([Ars Technica](https://arstechnica.com/ai/2026/08/google-announces-gemini-3-7-flash-just-three-weeks-after-previous-release/)).

**Honest limitations.**

1. **The price nearly doubles in about four months.** The 0.75 and 3.75 dollar per million rate applies only "through 31 Dec 2026", then 1.50 and 7.50 dollars ([Gemini API pricing](https://ai.google.dev/gemini-api/docs/pricing)). Any 2027 budget built on this week's number is wrong.
2. **The free tier trains on your data.** The pricing page states free-tier usage "is used to improve Google products" ([Gemini API pricing](https://ai.google.dev/gemini-api/docs/pricing)). For client documents under POPIA, that is a compliance problem, not a preference.
3. Batch and Flex tiers and Google Search grounding are all excluded from the free tier ([Gemini API pricing](https://ai.google.dev/gemini-api/docs/pricing)), so the cheapest bulk-processing route requires billing enabled.
4. Knowledge cutoff is March 2026 ([model docs](https://ai.google.dev/gemini-api/docs/latest-model)), so it does not know recent South African regulatory changes without grounding.
5. Consumer app rollout has regional footnotes. Second-hand from [DataNorth](https://datanorth.ai/news/google-releases-gemini-3-7-flash): 160-plus countries, with the EEA, UK, Switzerland and Nigeria excluded and the Spark surface requiring AI Pro or Ultra. I could not confirm those exclusions on a Google-owned page.

**South African use cases.**

- Run first-pass review over an immigration case file bundle with context caching, so the same document set is not re-billed on every question.
- Batch-process a month of supplier invoices or delivery notes at the Batch rate of 0.375 dollars per million input tokens, about R6.08 ([Gemini API pricing](https://ai.google.dev/gemini-api/docs/pricing)).
- Draft and revise client correspondence at volume in an agency, on the paid tier only, so your client text is not feeding model training.

**Industries:** immigration services, fintech, professional services, SaaS building, agency work.

**Pricing** (from [ai.google.dev/gemini-api/docs/pricing](https://ai.google.dev/gemini-api/docs/pricing)):

| Tier | Input per 1M | Output per 1M |
|---|---|---|
| Standard, to 31 Dec 2026 | 0.75 USD, about R12.15 | 3.75 USD, about R60.75 |
| Standard, from 1 Jan 2027 | 1.50 USD, about R24.30 | 7.50 USD, about R121.50 |
| Priority | 1.35 USD, about R21.87 | 6.75 USD, about R109.35 |
| Batch | 0.375 USD, about R6.08 | 1.875 USD, about R30.38 |
| Flex | 0.375 USD, about R6.08 | 1.875 USD, about R30.38 |
| Context caching | 0.075 USD, about R1.22 | - |
| Cache storage | 0.50 USD per 1M per hour, about R8.10 | - |

**Free tier:** yes, with the training caveat above.

**SA access:** API and AI Studio access is not region-gated for South Africa on the pricing page. A card is needed only to leave the free tier. No phone requirement published.

**Link:** https://ai.google.dev/gemini-api/docs/latest-model

---

## 2. Dograh

**The hook:** open-source voice phone agents, free forever if you host it yourself, with mid-call language switching across 70-plus languages.

**What it actually is.** A BSD-2 licensed platform for building and running voice AI phone agents, positioned as an alternative to Vapi. It ranked **number one on Product Hunt for 12 August 2026** ([Product Hunt](https://www.producthunt.com/leaderboard/daily/2026/8/12)). It ships a visual flow builder, telephony, human transfer, monitoring and QA, integrations with 30-plus models including local ones, and 70-plus languages with switching mid-call ([dograh.com](https://www.dograh.com/)).

**What it is genuinely good at.**

1. Removing per-minute platform lock-in. The Open Source plan is described as "free forever, full platform, self-hosted, no limits" under BSD-2 ([Dograh pricing](https://www.dograh.com/pricing)).
2. Multilingual call handling. 70-plus languages with mid-call switching ([dograh.com](https://www.dograh.com/)). For a South African business taking calls in four languages on one line, this is the feature that matters, not the benchmark.
3. A cheap hosted entry point. Pay-as-you-go is a 1 cent per minute platform fee, roughly 16 South African cents per minute, with credits from 5 dollars, about R81, and 10 concurrent calls included ([Dograh pricing](https://www.dograh.com/pricing)).

**Honest limitations.**

1. **Two different enterprise prices are published.** The HTML pricing page says "custom", while [dograh.com/pricing.md](https://www.dograh.com/pricing.md) says on-prem enterprise "starts at 2,500 dollars per month", about R40,500, with expert help at 2,000 to 6,000 dollars, roughly R32,400 to R97,200. That is self-contradictory and worth raising with them before signing anything.
2. **The 1 cent per minute fee is not your total cost.** You still pay the underlying model and telephony providers, and the pricing page does not total it for you ([Dograh pricing](https://www.dograh.com/pricing)).
3. **No local number answer.** No region, card or KYC terms appear anywhere on the pricing page ([Dograh pricing](https://www.dograh.com/pricing)). For a telephony product, South African number availability is the single unanswered question and it is not addressed.
4. Self-hosting is the only genuinely unlimited path, which means you own the infrastructure, the uptime and the POPIA handling for recorded customer calls. That is a real operational cost, not a free lunch.

**South African use cases.**

- Immigration services intake: an agent that answers in English, switches to isiZulu when the caller does, captures the pathway and passport details, and hands to a consultant on request.
- Beauty and wellness no-show recovery: an outbound agent that confirms tomorrow's appointments and rebooks cancellations, at roughly 16 cents a minute of platform fee on the hosted tier.
- Fintech collections reminders, where the call recording stays on infrastructure you control because you self-hosted it.

**Industries:** immigration services, beauty and wellness, fintech, logistics, professional services.

**Pricing** ([Dograh pricing](https://www.dograh.com/pricing)): Open Source free forever, self-hosted, no limits, BSD-2. Pay-as-you-go 1 cent per minute platform fee, credits from 5 dollars, about R81. Custom volume and Enterprise are quoted as custom, but see the 2,500 dollar figure in [pricing.md](https://www.dograh.com/pricing.md).

**Free tier:** yes, and the strongest on this list - the full platform, self-hosted, no usage limits.

**SA access:** not published. Self-hosting sidesteps any signup gate. The hosted tier's card and region requirements are not stated.

**Link:** https://www.dograh.com/ - code at https://github.com/dograh-hq/dograh

---

## 3. BetterClaw

**The hook:** a genuine zero-rand, no-card-required way to run one AI agent in production and find out whether the idea works.

**What it actually is.** A hosted agent deployment platform, pitched as "deploy AI agent, 60 seconds and 0 dollars forever". It ranked **number two on Product Hunt for 11 August 2026** ([Product Hunt](https://www.producthunt.com/leaderboard/daily/2026/8/11)), with the launch discussion at [producthunt.com/p/betterclaw](https://www.producthunt.com/p/betterclaw). You configure an agent, connect data sources, and it runs on their infrastructure with a kill switch and a sandbox. The free tier is bring-your-own-key ([BetterClaw pricing](https://www.betterclaw.io/pricing)).

**What it is genuinely good at.**

1. A real no-card free tier: 0 dollars per month forever, explicitly "no credit card", with 1 agent, 500 credits per month, 3 connectors, 7-day memory, kill switch, sandbox and AES-256 ([BetterClaw pricing](https://www.betterclaw.io/pricing)). For an SA founder without a US card, that removes the usual evaluation blocker entirely.
2. Transparent overage pricing. Extra agents 12 dollars per month on Pro or 8 on Business, extra credits 5 dollars per 1,000-credit pack on Pro or 4 on Business, extra seats 10 or 8 dollars ([BetterClaw pricing](https://www.betterclaw.io/pricing)). Very few agent platforms publish this at all.
3. A cost unit you can actually reason about: 1 credit equals 1 minute of agent machine uptime ([BetterClaw pricing](https://www.betterclaw.io/pricing)).

**Honest limitations.**

1. **Three different free-tier definitions are in circulation.** The vendor's pricing page says 500 credits per month ([BetterClaw pricing](https://www.betterclaw.io/pricing)) and so does [betterclaw.io/free-plan](https://www.betterclaw.io/free-plan), but the [Product Hunt launch post](https://www.producthunt.com/p/betterclaw) describes "100 tasks, daily crons, 1 agent" and [Capterra](https://www.capterra.com/p/10044070/BetterClaw/) lists 100 tasks per month. Trust the vendor page and expect surprises.
2. Paid pricing is inconsistent second-hand too. Capterra lists Pro at 19 dollars per user per month against the vendor's 49 dollars ([Capterra](https://www.capterra.com/p/10044070/BetterClaw/) versus [BetterClaw pricing](https://www.betterclaw.io/pricing)).
3. **7-day memory on the free tier is a hard functional cap.** An agent that forgets a client after a week cannot track an immigration case. You need Pro's 90-day memory for that ([BetterClaw pricing](https://www.betterclaw.io/pricing)).
4. Bring-your-own-key on free means you pay model costs separately ([BetterClaw pricing](https://www.betterclaw.io/pricing)). Free covers the orchestration, not the inference.
5. No region, card-country or phone terms are published ([BetterClaw pricing](https://www.betterclaw.io/pricing)). A launch promotion of three months of Pro for 49 dollars with code PH3 is reported by [Complete AI Training](https://completeaitraining.com/ai-tools/betterclaw/) and is not confirmed on the vendor site.

**South African use cases.**

- Prove out one internal agent at no cash cost - for example, a daily agent that reads your support inbox and writes a triage summary - and only pay once it earns its keep.
- Run a short-lived agent task where 7-day memory is not a constraint, such as a weekly competitor price check for a retail line.
- Use the 500 free credits, about 500 minutes of uptime, as a monthly evaluation budget across a few ideas before committing to Pro at 49 dollars, about R794.

**Industries:** SaaS building, professional services, agency and creative work.

**Pricing** ([BetterClaw pricing](https://www.betterclaw.io/pricing)): Free 0 dollars per month forever. Pro 49 dollars per month, about R794, or 39 dollars annually, about R632, for 5 agents, 12,000 credits, unlimited connectors, 90-day memory and 2 seats. Business 149 dollars per month, about R2,414, or 119 dollars annually, about R1,928, for 25 agents, 40,000 credits, 5 seats and a dedicated instance. Enterprise custom. Seven-day money-back guarantee.

**Free tier:** yes, no card.

**SA access:** not published, but the no-card free tier removes the usual blocker for evaluation.

**Link:** https://www.betterclaw.io/

---

## 4. n8n 2.35.0

**The hook:** the AI Assistant finally reaches self-hosted installs, which is the release note that matters if you run n8n on your own infrastructure in South Africa.

**What it actually is.** The weekly release of the open-source automation platform. The [n8n changelog on GitHub](https://raw.githubusercontent.com/n8n-io/n8n/master/CHANGELOG.md) records "[2.35.0] (2026-08-11)". This one brings AI Assistant onboarding to self-hosted and Community installs, enables the `instance-ai` module by default, adds Agent Builder test runs with human-in-the-loop, and adds Discord as an agent chat channel ([n8n changelog](https://raw.githubusercontent.com/n8n-io/n8n/master/CHANGELOG.md)).

**What it is genuinely good at.**

1. Closing the self-hosted gap. The AI Assistant was previously a Cloud-tier feature and is now available on Community and self-hosted ([n8n changelog](https://raw.githubusercontent.com/n8n-io/n8n/master/CHANGELOG.md)). If you kept your automation on local infrastructure for data-residency reasons, you no longer pay a capability penalty for it.
2. Safer agent development, with Agent Builder test runs that keep a human in the loop, plus improved human-in-the-loop over Slack and Telegram ([n8n changelog](https://raw.githubusercontent.com/n8n-io/n8n/master/CHANGELOG.md)).
3. Cost visibility on local models, via local agent token counting ([n8n changelog](https://raw.githubusercontent.com/n8n-io/n8n/master/CHANGELOG.md)).

**Honest limitations.**

1. **The official changelog site does not list 2.35.0.** [docs.n8n.io/changelog](https://docs.n8n.io/changelog/) showed 2.34 dated 4 August as the latest stable while listing 2.35.3 in beta. GitHub and the docs disagree, so check which build you are actually installing before you upgrade production.
2. n8n Agents is still preview and beta - on Cloud from 2.32.3, in beta for self-hosted, and explicitly **not available for self-hosted Enterprise** ([n8n community announcement](https://community.n8n.io/t/introducing-n8n-agents-a-new-way-to-build-agents-you-set-up-once-and-use-anywhere/306323)).
3. **No USD pricing is published.** [n8n.io/pricing](https://n8n.io/pricing/) quotes euros only. For an SA buyer that means a euro card charge and the associated FX cost on every invoice.
4. Trial terms are not stated on the pricing page ([n8n.io/pricing](https://n8n.io/pricing/)).

**South African use cases.**

- If you already run n8n on a local VPS for POPIA reasons, upgrade and use the AI Assistant to build workflows without moving to Cloud.
- Wrap a human approval step around any workflow that touches customer money, using the improved human-in-the-loop over Telegram.
- Use local agent token counting to work out whether a local model is actually cheaper than an API call before you commit.

**Industries:** all of them, since this is infrastructure. Most directly SaaS building, fintech operations, logistics and professional services.

**Pricing** ([n8n.io/pricing](https://n8n.io/pricing/), euros not dollars): Starter 20 euros per month, about R375. Pro 50 euros per month, about R938. Business 667 euros per month billed annually, about R12,500. Enterprise contact sales. The self-hosted Community Edition is free from GitHub.

**Free tier:** yes, as the self-hosted Community Edition. No hosted free tier is described.

**SA access:** not published for Cloud. Self-hosting has no region gate.

**Link:** https://n8n.io/

---

## 5. Lettertrace

**The hook:** find out whether Claude, ChatGPT and Gemini mention your business when someone asks about your category - for free, with your data staying in your own database.

**What it actually is.** An MIT-licensed, bring-your-own-key tool that tracks whether and how your brand appears in answers from Claude, ChatGPT and Gemini, plus Google AI Overviews. It ranked **number three on Product Hunt for 12 August 2026** ([Product Hunt](https://www.producthunt.com/leaderboard/daily/2026/8/12)). It reports visibility, share of voice, prominence, sentiment and competitor comparison ([lettertrace.com](https://lettertrace.com)).

**What it is genuinely good at.**

1. Costing essentially nothing. Free end-to-end under MIT, with you supplying your own API keys ([lettertrace.com](https://lettertrace.com)). Hosted competitors in this category charge subscription money for the same question.
2. Keeping your data yours. API keys encrypted at rest and results stored in your own Supabase instance ([lettertrace.com](https://lettertrace.com)) - a real POPIA advantage over a hosted tracker.
3. Multi-engine coverage in one view: Claude, ChatGPT, Gemini and Google AI Overviews together ([lettertrace.com](https://lettertrace.com)).

**Honest limitations.**

1. No paid tier and no vendor support commitment. Second-hand from [MakerStack](https://makerstack.co/reviews/lettertrace-review/): there is no paid plan and running it costs roughly 3 dollars in token spend, about R49. That figure is MakerStack's, not the vendor's.
2. **Bring-your-own-key means three separate API accounts** with three separate cards before you see a single report ([lettertrace.com](https://lettertrace.com)). The word "free" understates the setup work.
3. **You must run your own Supabase** ([lettertrace.com](https://lettertrace.com)). Fine for a technical founder. A hard blocker for a salon owner.
4. No signup, card or region terms are published ([lettertrace.com](https://lettertrace.com)), so there is nothing to verify for SA access either way.

**South African use cases.**

- Check whether an immigration consultancy shows up when someone asks an assistant "how do I get a South African work visa" - and whether a competitor does instead.
- Run it monthly for an agency client as an add-on deliverable, at roughly R49 of token spend per run.
- Track sentiment about your brand in model answers as a leading indicator, before it shows up in enquiry volume.

**Industries:** agency and creative work, retail, SaaS building, professional services marketing.

**Pricing:** free, MIT licence, no paid tier published ([lettertrace.com](https://lettertrace.com)). The roughly 3 dollar token estimate is second-hand from [MakerStack](https://makerstack.co/reviews/lettertrace-review/).

**Free tier:** the whole product is free.

**SA access:** not published. Self-hosted and bring-your-own-key, so no region gate is implied.

**Link:** https://lettertrace.com

---

## 6. Vizard Agent

**The hook:** a conversational agent that turns long recordings into social clips - with a pricing page that currently cannot tell you what it costs.

**What it actually is.** A conversational surface on top of Vizard's video repurposing engine, at agent.vizard.ai. You describe the outcome and it handles clipping, captioning, reframing and scheduling instead of you driving an editor ([Vizard blog](https://vizard.ai/blog/the-next-shift-in-ai-is-coming-to-video)). Vizard's own blog dated 10 August says it "is available today"; it appears at rank 8 on the [Product Hunt leaderboard for 11 August](https://www.producthunt.com/leaderboard/daily/2026/8/11). Either date is in window.

**What it is genuinely good at.** Turning long recordings into clips at volume, with the free plan alone allowing 60-minute uploads at 1080p ([Vizard pricing](https://vizard.ai/pricing)). Paid plans manage 6 to 20 connected social accounts with scheduling and a brand kit. The cost unit is legible: 1 credit equals 1 minute of uploaded video.

**Honest limitations.** **The pricing page is broken.** As fetched, [vizard.ai/pricing](https://vizard.ai/pricing) renders Creator and Business as "0 dollars, 50 percent off, 0 dollars billed yearly", and seats as "plus 0 dollars per month per seat". Paid pricing is therefore unverifiable from the vendor's own page. Second-hand, [MakerStack](https://makerstack.co/reviews/vizard-review/) reports Creator at 29 dollars per month, about R470, and Business at 39 dollars, about R632 - treat those as MakerStack's numbers, not Vizard's. The free tier watermarks output and caps you at one social account, 720p export and 3-day storage ([Vizard pricing](https://vizard.ai/pricing)), which makes it unusable for client work. Free API access is throttled to 1 request per minute. Business storage lasts only "as long as you are subscribing" - cancel and the archive goes.

**South African use cases.** Cut a recorded workshop or webinar into shorts for TikTok and Reels. Repurpose a founder interview into a week of clips. Both on a paid tier only, because of the watermark.

**Industries:** agency and creative work, beauty and wellness marketing, retail.

**Pricing:** Free 0 dollars with 60 credits per month, verified on [vizard.ai/pricing](https://vizard.ai/pricing). Paid prices not verifiable from the vendor.

**Link:** https://agent.vizard.ai/

---

## 7. Grok Bot

**The hook:** xAI's agent app, at 200 to 300 dollars a month, in beta, with no published free tier. Included for completeness, not as a recommendation.

**What it actually is.** xAI's agentic assistant as a desktop and iOS application for top-tier subscribers, in beta. [x.ai/news/introducing-grok-bot](https://x.ai/news/introducing-grok-bot), dated 11 August 2026, states it is "available today for SuperGrok Heavy, Cursor Ultra, and Cursor Teams Premium subscribers on desktop and iOS", with an enterprise waitlist. It also ranked number two on the [Product Hunt leaderboard for 12 August](https://www.producthunt.com/leaderboard/daily/2026/8/12).

**What it is genuinely good at.** Very little is verifiable from first-party sources, and that is itself the finding. Confirmed: desktop and iOS availability from day one, and bundling with an existing Cursor Ultra or Cursor Teams Premium subscription at no extra purchase ([x.ai](https://x.ai/news/introducing-grok-bot)). Broader platform coverage is second-hand from [Fello AI](https://felloai.com/grok-bot/).

**Honest limitations.** [x.ai/bot](https://x.ai/bot) lists Ultra at 200 dollars per month, about R3,240, SuperGrok Heavy at 300 dollars, about R4,860, and Premium Teams at 120 dollars per seat, about R1,944. **The same page shows a "get started for free" call to action with no free-trial terms stated anywhere.** It is beta software, enterprise access is waitlist-only, and no launch date or region information appears on the product page at all. Related, same window: xAI also shipped Grok 4.6, whose API pricing is second-hand from [Releasebot](https://releasebot.io/updates/xai) and could not be confirmed on an x.ai page.

**South African use cases.** Honestly, at R3,240 to R4,860 a month with no free tier and beta status, this is hard to justify for an SA SMB. The one defensible case is a SaaS team already paying for Cursor Ultra, where access is included.

**Industries:** SaaS building only, and only on the bundled path.

**Link:** https://x.ai/bot

---

## 8. GLM-5.3

**The hook:** a low-cost coding model whose vendor pricing page shows two different prices for every tier and never states that the new model is included.

**What it actually is.** Zhipu's updated flagship coding model, pitched as a coding improvement from scaled post-training on the same base. [models.dev](https://models.dev/models/zhipuai/glm-5.3) records a 2026-08-14 release date, and South African outlet [Memeburn](https://memeburn.com/glm-5-3-is-here-benchmarks-pricing-coding-and-whats-new/) reported the same date on 16 August. It ranked number two on the [Product Hunt leaderboard for 15 August](https://www.producthunt.com/leaderboard/daily/2026/8/15).

**What it is genuinely good at.** Coding, per its own positioning and the benchmark framing in [Memeburn's writeup](https://memeburn.com/glm-5-3-is-here-benchmarks-pricing-coding-and-whats-new/). Billing is subscription rather than per-token, with Lite including 10,000 credits per week ([z.ai/subscribe](https://z.ai/subscribe)), which is predictable against a fixed monthly budget, and quarterly billing is 20 percent off with yearly 30 percent off.

**Honest limitations.** **The pricing page shows two prices for every tier** - Lite at both 12.60 and 18 dollars per month, Pro at both 56 and 80 dollars, Max at both 117.60 and 168 dollars ([z.ai/subscribe](https://z.ai/subscribe)). At R16.20 that spread is roughly R204 versus R292 on Lite and R907 versus R1,296 on Pro. **Worse, the page does not say GLM-5.3 is included** - its own copy references GLM-5.2 and GLM-5-Turbo. You cannot confirm from the vendor that a subscription buys you the model that launched this week. Per-token API pricing is not published. No open weights or model card at launch; a roughly two-week weights release pending safety review is second-hand from [explainX](https://explainx.ai/blog/glm-5-3-launch-cyber-defense-benchmarks-august-2026). No free tier is stated.

**South African use cases.** A fixed-budget coding subscription for a small development team, if and only if you get written confirmation of which model and which price applies. Nothing is published about SA payment rails either way, so I am not asserting a problem, but a Chinese-vendor card charge is worth testing with a small amount first.

**Industries:** SaaS building, agency and creative development work.

**Link:** https://z.ai/subscribe

---

## 9. Claude text watermarking - a policy change, not a tool

**The hook:** if you draft client work with Claude, that text now carries a detectable marker, globally, with no opt-out.

**What it actually is.** Anthropic now embeds a statistical watermark in text generated by Claude models launched on or after 2 August 2026, applied globally with no opt-out, plus C2PA signed provenance metadata on generated image files. Older models will be retrofitted "over coming months", and a text-detection API was announced ([Anthropic, 14 August](https://www.anthropic.com/news/claude-text-watermark)). The underlying policy change was reported on 11 August by [TechCrunch](https://techcrunch.com/2026/08/11/anthropic-says-it-will-watermark-text-generated-by-its-ai-models/), [Fortune](https://fortune.com/2026/08/11/anthropic-claude-watermark-ai-text-police-ai-slop/) and [Euronews](https://www.euronews.com/next/2026/08/11/eu-compliance-delivered-globally-anthropic-to-watermark-claudes-output-worldwide).

**Why an SA business should care.**

1. **It applies to you whether you want it or not.** Global, no opt-out ([Anthropic](https://www.anthropic.com/news/claude-text-watermark)). Client deliverables drafted with Claude carry the marker.
2. **It is EU compliance delivered worldwide** ([Euronews](https://www.euronews.com/next/2026/08/11/eu-compliance-delivered-globally-anthropic-to-watermark-claudes-output-worldwide)). This is how EU AI Act obligations reach South African users - through vendor policy, not through South African law. Expect more of it.
3. **It cannot do what people will assume it does.** Anthropic states the watermark "cannot distinguish 'Claude wrote this' from 'Claude heavily edited this'" ([Anthropic](https://www.anthropic.com/news/claude-text-watermark)). South African experts told [ITWeb on 14 August](https://www.itweb.co.za/article/claude-ai-watermarking-is-not-definitive-evidence-say-sa-experts/kYbe9MXbZK6vAWpG) the same thing: it is not definitive evidence of anything.

**The practical action:** decide now what you tell clients about AI assistance in written deliverables, and put it in the engagement letter. Do not wait for a client to run a detector and ask you about it.

**Pricing:** not applicable. This is platform behaviour, not a purchase.

**Link:** https://www.anthropic.com/news/claude-text-watermark

---

## What I would actually try this week

**First pick: Dograh.** It is the only item on this list that is free forever with no usage cap, and its headline feature - mid-call switching across 70-plus languages ([dograh.com](https://www.dograh.com/)) - maps directly onto a South African reality that overseas voice platforms do not price or plan for. Self-host it, point it at a test line, and see whether it handles a caller switching from English to isiZulu mid-sentence. The unanswered question is South African number availability, which the vendor does not address ([Dograh pricing](https://www.dograh.com/pricing)), so make that your first question to them rather than your first surprise.

**Second pick: BetterClaw's free tier.** Not because the product is remarkable, but because a 0 dollar, no-credit-card tier ([BetterClaw pricing](https://www.betterclaw.io/pricing)) is the cheapest honest way for an SA founder to find out whether an agent idea works. The 7-day memory cap decides what you can test - short tasks, not long-running case tracking. Treat 500 credits a month as a free evaluation budget and nothing more.

**One to avoid: Grok Bot.** At 200 to 300 dollars a month, roughly R3,240 to R4,860, in beta, with no published free-trial terms next to a "get started for free" button ([x.ai/bot](https://x.ai/bot)), there is no version of the SA SMB case that works. Skip it unless Cursor Ultra already covers you.

**And one thing to do that costs nothing:** if you use Claude for client work, write your AI-assistance disclosure into your engagement terms this week ([Anthropic](https://www.anthropic.com/news/claude-text-watermark)).

---

## What we deliberately left out

The instruction on this series is to cover fewer tools in more depth rather than pad a thin week, so here is what was considered and dropped, and why.

**Outside the window.** FLUX 3 Video went GA on 4 August ([BFL release notes](https://docs.bfl.ml/release-notes)); Bland Speech v3 on 4 August; Decart Anywear on 5 August; OpenAI's GPT-5.6 Sol improvements on 6 August ([OpenAI](https://openai.com/index/improving-gpt-5-6-sol-in-chatgpt/)). The genuinely painful near-miss is **Domains.co.za launching self-hosted n8n VPS hosting inside South Africa** ([ITWeb](https://www.itweb.co.za/article/domainscoza-launches-self-hosted-n8n-vps-hosting-for-ai-workflow-automation/DZQ587V8mP3qzXy2)) - the single most relevant item on the whole shortlist to a Johannesburg n8n operator, and dated 29 July, twelve days out of window. If you run n8n locally, look at it anyway.

**In window but pricing unverifiable.** **Lexi**, billed as "the operating system for legal work" and launched 11 August, would have been the best immigration-services fit on the list, but its pricing page does not resolve. Flagged for re-check next week. **Chert**, an iMessage and FaceTime AI agent from 16 August, is a strong concept undone by channel: iMessage-only is a fatal mismatch in a WhatsApp-first market. **Zetik**, a "chief of staff in your pocket" from 16 August, publishes no website URL or pricing on its Product Hunt page.

**In window but developer-only.** The bulk of the week. Product Hunt's daily winners included **oqoqo** on 10 August, an LLM evaluation harness, **Kane CLI** on 13 August, and **Inferock Bench** on 15 August, an LLM API receipts tool. Also dropped: Tines, Xirp, Unsloth Desktop, LaraCopilot, Gitar, Octomind, and roughly forty others across the week - all developer tooling or single-platform utilities with no SA SMB use case. **Talvo** was rejected on an explicit region mismatch: European banks only. **CostLogic**, AI construction takeoffs from 16 August, is a plausible SA construction fit with no verified pricing.

**Raw model releases with no product surface.** DeepSeek V4 Pro 0813, Wan 3.0 public beta, Qwen3.8-Max, MiniMax H3 open weights, LTX-2.5, Nemotron 3.5 Lightning and about a dozen others from [ThursdAI's August index](https://thursdai.news/releases/2026-08). Weights and API endpoints, not products. **OpenAI previewed "Ultrafast" mode on 13 August** ([OpenAI](https://openai.com/index/previewing-ultrafast/)), which is in window but waitlisted and restricted to work accounts, so there is nothing to sign up for.

---

## South African context this week

The most important local story was not a launch. TechCentral reported on 12 August that of roughly 100 South African tech decision-makers surveyed, **only about 25 percent are running AI in production**, 43 percent are still piloting, and 16 percent have plans they have not started ([TechCentral](https://techcentral.co.za/only-a-quarter-of-sa-firms-are-running-ai-for-real/284770/)). About 55 percent plan AI-driven cloud migrations within 18 months, Azure is in use or under consideration at roughly 79 percent against AWS at 53 percent, and about one in five are weighing local providers such as Liquid or Xneelo.

Read alongside the free tiers in this week's list, that survey is the actual opportunity. The gap between piloting and production is not usually a tooling gap - two of this week's items cost nothing to run.

Also worth your attention:

- Discovery's CIO told TechCentral on 13 August that the group measures only about 20 to 25 percent efficiency gains from AI coding tools, with heavy spend on guardrails ([TechCentral](https://techcentral.co.za/meet-the-cio-derek-wilcocks-on-how-ai-personalised-vitality/284809/)). A useful corrective to vendor productivity claims.
- ITWeb's 11 August AI lead was AI deepfake fraud threatening efforts to rebuild investor trust after South Africa's FATF grey-list exit, on a page that also carries Netcare's SAHPRA application to license an AI clinical-deterioration algorithm ([ITWeb](https://www.itweb.co.za/categories/j5alrvQgkY1MpYQk)).
- Cape Town's mayor set an AI condition for salary increases, referencing the city's AI investment concierge ([MyBroadband, 12 August](https://mybroadband.co.za/news/ai/662071-cape-towns-mayor-has-one-interesting-condition-for-salary-increases.html)).

One correction worth making, because the story is circulating: DeepSeek's steep API price increase was reported by **TechCentral.ie, an Irish outlet**, not South Africa's techcentral.co.za ([TechCentral.ie, 10 August](https://www.techcentral.ie/deepseek-announces-steep-price-increase-due-to-rising-demand-for-low-cost-ai-models/)). It is not South African coverage.

---

## Verification note

Every launch date, price and feature claim above was checked against a source page during research for this edition, and the source is linked at the point of use. Where a figure appears only on a third-party review or aggregator rather than the vendor's own site, it is labelled second-hand and the reviewer is named. Where a vendor publishes nothing about South African access, the entry says "not published" rather than offering an estimate. Rand figures are indicative conversions at about R16.20 to the dollar and R18.75 to the euro, and exclude bank and card fees. Prices move; check the vendor page before you commit budget.
