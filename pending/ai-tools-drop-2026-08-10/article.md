# AI Tools Drop - Week of 4 to 10 August 2026

**For South African founders and small business owners.**

Rand figures use a working rate of roughly R16.20 to the dollar ([Xe](https://www.xe.com/en-us/currencyconverter/convert/?Amount=1&From=USD&To=ZAR)). Worth noting the rand firmed over the week, from around R16.50 last Monday to R16.13 by Friday ([Trading Economics](https://tradingeconomics.com/south-africa/currency)). Every dollar-priced subscription on this page got about two percent cheaper without anyone doing anything. Check the live rate before you commit.

---

## This week in one paragraph

Ten launches verified inside the window, and the two at the top are worth your Monday. OpenAI removed the daily text-chat cap on the ChatGPT free tier entirely and made GPT-5.6 Luna the default there ([TechCrunch](https://techcrunch.com/2026/08/06/openai-brings-unlimited-chatgpt-text-chats-to-free-users/)), which for a lean team that has been rationing prompts is a bigger deal than most paid upgrades. And ElevenLabs opened its dubbing model as an API with **Afrikaans in the supported language table** ([ElevenLabs](https://elevenlabs.io/docs/overview/capabilities/dubbing))  -  the first thing in weeks that is genuinely shaped for a country with eleven official languages. Below that the week is developer-heavy: Keystroke, Cloudflare OS and Meta's Muse Code are all agent infrastructure, useful if you build, irrelevant if you do not. Three entries on this list are priced or gated in ways that make them marginal for a small South African business, and I have said so in each case rather than dressing them up. Locally it was quiet. Two SA stories worth reading, neither of them a tool.

---

## 1. ChatGPT - the 6 August update

**Unlimited text chats on the free tier, and the free model got materially more accurate.**

**What it actually is.** A model and interface refresh across ChatGPT, dated 6 August on OpenAI's own release document ([GPT-5.6 August Updates](https://cdn.openai.com/pdf/GPT_5_6_August_Updates.pdf)). GPT-5.6 Luna becomes the default for Free and Go accounts with unlimited text chats, while Plus and Pro get a retuned Sol with a continuous reasoning-effort slider.

**What it is genuinely good at.** The daily text-chat cap on the free tier is gone entirely ([TechCrunch](https://techcrunch.com/2026/08/06/openai-brings-unlimited-chatgpt-text-chats-to-free-users/)). If you have staff who hit the limit at eleven in the morning and stop using the tool, that problem just disappeared at no cost. The accuracy improvement is also real and measured: OpenAI's internal evaluation reports factual errors 62 percent less common for Luna and 68 percent less common for Sol against GPT-5.5 Instant ([TechCrunch](https://techcrunch.com/2026/08/06/openai-brings-unlimited-chatgpt-text-chats-to-free-users/)). And on paid tiers the effort slider replaces model-picker guesswork  -  you dial thinking effort up for planning or research and down for quick drafting ([OpenAI release notes](https://releasebot.io/updates/openai)).

**Honest limitations.** Free users get Luna, the cheapest tier, not the flagship Sol. The Think button gives Luna more time but does not upgrade you ([Windows Forum](https://windowsforum.com/windows-news.4/chatgpt-free-gets-gpt-5-6-luna-not-flagship-sol.441885/)). Unlimited applies to text only  -  file uploads, image generation and voice keep their own separate limits ([OpenAI release notes](https://help.openai.com/en/articles/6825453-chatgpt-release-notes)). The rollout is staggered, with unlimited chats and Think pushed to the week of 10 August, so account availability still varies. And if your team works in Codex or ChatGPT Work, this release does nothing for you  -  both are explicitly unchanged ([OpenAI](https://cdn.openai.com/pdf/GPT_5_6_August_Updates.pdf)).

**South African use cases.**
- Any team where you have been quietly limiting who gets a paid seat. The free tier just became viable for real daily work.
- Immigration or legal admin where document summarisation is high-volume and the accuracy gain matters more than the model tier.
- Training junior staff without provisioning licences first.

**Industries.** All of them.

**Pricing.** Free tier yes. Go is $8 a month, about R130. Plus is $20, roughly R324. Pro is $200, around R3,240 ([The Next Web](https://thenextweb.com/news/chatgpt-free-unlimited-text-chats-gpt-5-6-luna-default)).

**Access notes for SA.** ChatGPT is available here and this is a tier-level rollout rather than a regional launch. No region gating was stated on any source I checked.

**Link.** [help.openai.com - ChatGPT release notes](https://help.openai.com/en/articles/6825453-chatgpt-release-notes)

---

## 2. ElevenLabs Dubbing API

**Afrikaans is in the language table. That is the headline for us.**

**What it actually is.** Programmatic access to the emotion-preserving dubbing model, opened on 6 August ([ElevenLabs](https://elevenlabs.io/blog/dubbing-api), [Tech Times](https://www.techtimes.com/articles/323588/20260807/elevenlabs-opens-dubbing-api-emotion-preserving-ai-localization-now-programmable.htm)). You send audio, you get back audio in another language with the original speaker's tone and delivery intact.

**What it is genuinely good at.** It is audio-to-audio rather than transcribe-translate-resynthesise, which is why the emotion survives, across 90-plus languages ([ElevenLabs](https://elevenlabs.io/blog/dubbing-api)), reported as 92 by [Chosun Biz](https://biz.chosun.com/en/en-it/2026/08/10/FGUVJVXIU5FDPE5DQBQCJPCTL4/). Afrikaans is supported, and the table goes to dialect level elsewhere  -  Mexican Spanish separated from Castilian, for instance ([ElevenLabs dubbing docs](https://elevenlabs.io/docs/overview/capabilities/dubbing)). One API covers translation, voice cloning, dubbing and sync, handles background music and multi-speaker audio, and enterprise customers can supply their own transcripts and regenerate only the edited segments.

**Honest limitations.** The API is in alpha ([ElevenLabs](https://elevenlabs.io/blog/dubbing-api)). Output is audio only, not finished video, so you still need an editor to remux. Free-tier dubs are watermarked automatically. And the model itself is not new  -  it shipped inside ElevenCreative on 28 May. What is new this week is programmatic access, which matters if you want it in a pipeline rather than a browser tab.

I could not confirm the per-minute dubbing rates on a first-party page. [Tech Times](https://www.techtimes.com/articles/323588/20260807/elevenlabs-opens-dubbing-api-emotion-preserving-ai-localization-now-programmable.htm) reports $0.33 per source minute watermarked and $0.50 without, roughly R5.35 and R8.10, but treat those as second-hand until ElevenLabs publishes them.

**South African use cases.**
- Producing one campaign video and shipping it in English and Afrikaans without a second shoot or a second voice artist.
- An immigration practice recording a single process explainer and putting it out in three languages, where the client understanding the tone matters as much as the words.
- Retail or wellness brands localising social content for different provincial audiences.

**Industries.** Agency and creative work, beauty and wellness, immigration services, retail marketing.

**Pricing.** Free tier yes, at $0 with 10,000 credits a month. Starter is $6, about R97, and adds the commercial licence, instant voice cloning and Dubbing Studio. Creator is $11, roughly R178. Pro is $99, around R1,604 ([ElevenLabs pricing](https://elevenlabs.io/pricing)).

**Access notes for SA.** No region restriction stated on any ElevenLabs page I checked.

**Link.** [elevenlabs.io/blog/dubbing-api](https://elevenlabs.io/blog/dubbing-api)

---

## 3. Keystroke

**n8n for people who would rather write TypeScript than drag boxes.**

**What it actually is.** An open-source platform for building internal AI agents and automation workflows as plain TypeScript inside your own repository, deployed to a managed web app. Launched 5 August on Product Hunt with a same-day [Y Combinator launch page](https://www.ycombinator.com/launches/RNB-keystroke-open-sourcing-our-internal-agents-automations-platform).

**What it is genuinely good at.** The team pitch it as what n8n would be if it were built for Claude Code and Cursor ([Product Hunt](https://www.producthunt.com/products/keystroke-2)), which means your automation lives in your repo under version control rather than trapped in someone's canvas. Given your stack is already GitHub and Vercel, that is a natural fit. It ships with over a thousand integrations plus any REST API or MCP server, and memory, filesystem, code execution, web search, triggers, schedules, webhooks and approvals are built in ([Keystroke](https://keystroke.ai/)). The code is on [GitHub](https://github.com/keystrokehq/keystroke) under Elastic License 2.0, so you are not locked into the hosted product.

**Honest limitations.** Open alpha, so expect breakage. Elastic License 2.0 is source-available rather than OSI-open, which carries commercial hosting restrictions  -  read them if you were planning to resell anything built on it. It assumes you write TypeScript, so a non-technical ops person cannot pick this up the way they could n8n's canvas. And the Hobby tier caps runs at ten minutes ([MakerStack](https://makerstack.co/reviews/keystroke-review/)), which kills longer agent jobs.

**South African use cases.**
- Internal ops automation across a multi-product setup, where the workflows need to be reviewable in a pull request rather than clicked together.
- Fintech back-office jobs where you want the automation logic auditable and versioned for compliance reasons.
- Any agency running repeatable client onboarding that currently lives in someone's head.

**Industries.** SaaS building, fintech and payments operations, professional services back-office, agency work.

**Pricing.** Free forever Hobby tier with roughly $1 a month of usage credit, about a hundred agent runs, and a ten-minute timeout. Pro is $20, about R324, including $20 of usage credit, 50 GB storage and a thirty-minute timeout ([MakerStack](https://makerstack.co/reviews/keystroke-review/)).

**Access notes for SA.** Self-hostable from the public repo, so no regional dependency on the open-source path.

**Link.** [keystroke.ai](https://keystroke.ai/)

---

## 4. Aveiro

**Site, blog and newsletter in one subscription, with agents drafting and a human approving.**

**What it actually is.** An AI-native publishing workspace covering website, blog, newsletter and eventually social, launched 6 August ([Product Hunt](https://www.producthunt.com/products/aveiro)). AI agents draft, a human approves before anything goes live.

**What it is genuinely good at.** ChatGPT, Claude or Cursor can write directly into the workspace over MCP, with approval gating publication ([Aveiro](https://www.aveiro.app/)). Subscriber list, email campaigns and analytics are bundled, so you are not paying for a separate newsletter tool on top. And custom domain and branding removal are available even on the trial tier ([Aveiro pricing](https://www.aveiro.app/pricing)).

**Honest limitations.** The "Free" plan is a 14-day trial, not a permanent free tier, and when it ends live sites pause until you upgrade ([Aveiro pricing](https://www.aveiro.app/pricing)). That is a meaningful difference and the pricing page does not lead with it. Trial caps are tight: one site, ten pages, one editor, a thousand one-time AI credits, a hundred emails a month. Social publishing is not really shipped  -  only X appears on the trial tier and the rest is marked coming soon. And it is a brand new product with no track record.

**South African use cases.**
- A consultancy or immigration practice that needs a content site and a client update newsletter but does not want three subscriptions to manage.
- A wellness or beauty brand where the owner writes the content and wants an agent to do the first draft.
- Replacing a WordPress plus Mailchimp setup that nobody enjoys maintaining.

**Industries.** Professional services, immigration services, beauty and wellness, agency work.

**Pricing.** 14-day trial. Starter is $12 a month, about R194, discounted from $15.60 under a beta discount. Creator is $29, roughly R470. Professional is $99, around R1,604 ([Aveiro pricing](https://www.aveiro.app/pricing)).

**Access notes for SA.** Not published.

**Link.** [aveiro.app](https://www.aveiro.app/)

---

## 5. AdAnt AI

**Flat thirty-nine dollars, no tier games, aimed at social video ads.**

**What it actually is.** A set of creative agents that research, produce and iterate on social video ads for TikTok, Instagram and YouTube. It took the number one spot on Product Hunt for 5 August ([Product Hunt](https://www.producthunt.com/products/adant-ai)).

**What it is genuinely good at.** Competitor and viral-pattern research feeds directly into ad creation, so it is not generating in a vacuum. Product profiles store your brand positioning and assets and get referenced inline with @ mentions, which keeps output on-brand across campaigns. And there are over a hundred AI avatars with no watermark on paid output ([Product Hunt](https://www.producthunt.com/products/adant-ai)).

**Honest limitations.** It is credit-based and credits go quickly on video. The $39 monthly reportedly buys only 150 credits ([MakerStack](https://makerstack.co/reviews/adant-ai-review/)). The dedicated pricing page returned an error for at least one reviewer, which tells you something about how finished the commercial side is. The ChatGPT and Claude plugins are announced but not shipped. And there is a done-for-you Studio tier at $100 to $200 per video with a $5,000 monthly minimum  -  irrelevant to you, but worth knowing the upsell exists so it does not surprise you in a sales call.

**South African use cases.**
- A salon or wellness brand that needs weekly social video and currently pays a freelancer per asset.
- Retail promotional cycles where you need five variants of the same offer and only have budget for one shoot.
- An agency testing creative angles before committing production spend.

**Industries.** Beauty and wellness, retail, agency and creative work.

**Pricing.** No permanent free tier, but 50 free trial credits and at least one free video before purchase. $39 a month, about R632, one plan, with pay-as-you-go top-ups. Annual is reported at $32.50 a month billed $390 a year with 1,800 credits ([SaaSpicious](https://saaspicious.com/blog/adant-ai-vs-creatify/)).

**Access notes for SA.** Not published.

**Link.** [adant.ai](https://adant.ai/)

---

## 6. Wispr Flow Notetaker

**No bot joins your call. Excellent product, but Mac-only and English-only.**

**What it actually is.** A meeting notetaker released 5 August that captures Mac system audio directly rather than joining your call as a participant ([Wispr Flow Notetaker](https://wisprflow.ai/notetaker)).

**What it is genuinely good at.** No bot in the room, which sidesteps the awkward moment where a client asks who the extra participant is. Speaker identification pulls from your calendar, Gmail and Slack so notes attribute correctly. And your notes are readable directly from Claude, ChatGPT or Cursor over MCP, with a one-step Granola import. It works across Google Meet, Zoom, Teams, Slack huddles and in-person meetings.

**Honest limitations.** macOS 14.4 or later only, with no Windows version at launch. English only, which is a genuine constraint for a Johannesburg team where meetings drift between languages  -  note the separate dictation feature does support a hundred-plus languages, but the notetaker does not. Processing is cloud, not on-device, which is worth a thought if you handle POPIA-sensitive client conversations. It is not on Enterprise plans yet, with Wispr committing to no later than September ([Enterprise FAQ](https://docs.wisprflow.ai/articles/6858284702-notetaker-for-enterprise-faq)). And the free plan has a weekly meeting cap that Wispr does not publish, which is an odd thing to hide.

**South African use cases.**
- Client consultations in a legal or accounting practice where the recap is billable and the bot is unwelcome.
- Immigration intake calls where you need an accurate record and the client is already nervous.
- Only if your team is on Macs and your meetings run in English. Otherwise skip it this round.

**Industries.** Professional services, immigration services, SaaS building.

**Pricing.** Free tier yes, including Notetaker with an unpublished weekly cap. Flow Pro is $15 per user monthly, about R243, or $12 billed annually, roughly R194 ([Wispr Flow pricing](https://wisprflow.ai/pricing)).

**Access notes for SA.** No region restriction stated.

**Link.** [wisprflow.ai/notetaker](https://wisprflow.ai/notetaker)

---

## 7. Cloudflare OS

**Open source agent workspace with the governance layer everyone else skips.**

**What it actually is.** An open-source, browser-based AI agent workspace and personal-app platform that runs inside your own Cloudflare account. Cloudflare's [press release](https://www.cloudflare.com/press/press-releases/2026/cloudflare-os-is-the-first-ai-workspace-built-around-how-companies-actually-work/) is dated 4 August, the [blog post](https://blog.cloudflare.com/cloudflare-os/) and coverage land on 5 August.

**What it is genuinely good at.** Capability-based security is the standout  -  agents start with zero access and are granted capabilities explicitly ([Cloudflare](https://blog.cloudflare.com/cloudflare-os/)). That is a materially better default than most agent platforms, which start permissive and hope. It is model-agnostic through Cloudflare AI Gateway with per-person, per-team and per-app spend visibility, budgets and rate limits. Given how quickly agent spend gets away from people, that governance layer is arguably the real product. And it is Apache 2.0, genuinely self-hostable, runs locally on workerd and supports Ollama ([GitHub](https://github.com/cloudflare/cloudflare-os)).

**Honest limitations.** The repository README describes it as early access with many rough edges. There is no hosted version yet  -  managed dashboard deployment is coming soon. Community reports, not confirmed by Cloudflare, suggest Dynamic Workers require a paid Workers plan, which would undercut the free-and-open framing ([ExplainX](https://explainx.ai/blog/cloudflare-os-open-source-agent-platform-august-2026))  -  verify that before you plan around it. And setting this up is a real engineering exercise, not an afternoon.

**South African use cases.**
- Running agents against client data where you need the spend and permission boundaries documented for a compliance review.
- Self-hosted agent infrastructure where data residency is the constraint.
- Fintech operations where per-team AI spend needs to be attributable.

**Industries.** SaaS building, fintech and payments, compliance-heavy professional services.

**Pricing.** Software is free under Apache 2.0. Underlying Cloudflare Workers costs apply and the paid-plan requirement is unconfirmed.

**Access notes for SA.** Self-hostable, so no regional gate on the code.

**Link.** [blog.cloudflare.com/cloudflare-os](https://blog.cloudflare.com/cloudflare-os/)

---

## 8. Meta Muse Code

**Capable, cheap on tokens, and the cheap tier trains on your prompts.**

**What it actually is.** A terminal-based AI coding agent for large codebases, launched in beta on 5 August, powered by the new Muse Spark 1.2 model ([TechCrunch](https://techcrunch.com/2026/08/05/meta-launches-muse-code-an-ai-agent-for-large-code-bases/)).

**What it is genuinely good at.** Persistent background sub-agents run in isolated git worktrees, so parallel work does not collide ([The Register](https://www.theregister.com/ai-and-ml/2026/08/06/meta-wants-to-get-inside-your-terminal-with-its-new-coding-agent/5283717)). Benchmarks are strong  -  82.9 percent on Terminal-Bench 2.1, 59.3 percent on DeepSWE v1.1, with a one-million-token context window ([DataNorth](https://datanorth.ai/news/meta-releases-muse-spark-1-2-and-muse-code)). And it is safe by default, with sandbox and approvals on, plus a local event log for crash recovery ([Codersera](https://codersera.com/blog/muse-code-complete-guide-2026/)).

**Honest limitations.** Read this one carefully. macOS and Linux only, WSL2 on Windows, no desktop app. The cheap contributor tier means **Meta trains on your prompts and completions**, and your rate limit collapses from 3,000 requests per minute to 60 ([Barchart](https://www.barchart.com/story/news/3691953/meta-enters-the-terminal-coding-agent-race-with-muse-code-as-contributor-pricing-raises-new-data-use-questions)). For client code under NDA, that tier is simply unusable, and the price difference is designed to tempt you. Contributor access is also limited to selected countries and South Africa's inclusion is unconfirmed. Muse Spark 1.2 has closed weights, so there is no self-hosting escape hatch. And it is beta.

**South African use cases.**
- Large-codebase refactoring on your own products, on the standard tier only.
- Not for client work under NDA on the contributor tier. That is not a nuance, it is a hard line.

**Industries.** SaaS building only.

**Pricing.** No free tier, token-priced. Standard is $1.25 per million input tokens, about R20, $0.15 per million cached, and $4.25 per million output, roughly R69. Contributor drops to $0.10, $0.002 and $0.20 per million with the data and rate-limit trade-offs above ([Barchart](https://www.barchart.com/story/news/3691953/meta-enters-the-terminal-coding-agent-race-with-muse-code-as-contributor-pricing-raises-new-data-use-questions)).

**Access notes for SA.** Contributor tier availability here is unconfirmed. Install is a one-line curl from dev.meta.ai ([9to5Mac](https://9to5mac.com/2026/08/05/meta-launches-muse-code-ai-coding-agent-for-macos-and-linux/)).

**Link.** [techcrunch.com - Meta launches Muse Code](https://techcrunch.com/2026/08/05/meta-launches-muse-code-an-ai-agent-for-large-code-bases/)

---

## 9. Omniwork

**Whole content pipeline in one desktop app. The pricing page contradicts itself.**

**What it actually is.** A desktop creative agent operating system with specialist agents for research, scripts, images, video editing, music and social posting. Launch of the Day on Product Hunt for 9 August ([Product Hunt](https://www.producthunt.com/products/omniwork-2/awards)). Note it was in invite-only beta from around May, so this is the public launch rather than first availability.

**What it is genuinely good at.** One desktop surface across the whole content pipeline, research through to posting, instead of stitching five tools together ([Omniwork](https://omniwork.ai/)). Over a hundred agents are available on the free Starter tier, so you can evaluate the range before paying anything. The desktop-pet companion that surfaces idle, working, done and error states is gimmicky, but it does make long-running agent jobs legible at a glance, which is a real problem.

**Honest limitations.** The free tier allows five deep tasks a month, which is enough to try and not enough to use. The pricing page contradicts itself on the Pro tier, stating roughly ninety deep tasks a month in one place and "30+ deep tasks/month" in a bullet on the same page ([Omniwork](https://omniwork.ai/)). Get that clarified in writing before you subscribe. And $69 a month is a hard sell against AdAnt at $39 or Aveiro at $12 unless you genuinely need the full pipeline.

**South African use cases.**
- An agency producing end-to-end content for several clients where the tool sprawl is the actual cost.
- A beauty or wellness brand doing weekly video where research, script and edit currently sit in three places.

**Industries.** Agency and creative work, beauty and wellness content, retail marketing.

**Pricing.** Free Starter tier with 100-plus agents and five deep tasks monthly. Pro is $69, about R1,118. Ultimate is $1,999 a year, roughly R32,380 ([Omniwork](https://omniwork.ai/)).

**Access notes for SA.** Not published.

**Link.** [omniwork.ai](https://omniwork.ai/)

---

## 10. Rindler

**Logs into portals for you. Highest price floor on this list.**

**What it actually is.** Browser automation that logs into the sites your team already uses by hand and completes tasks, returning structured records rather than raw page dumps. Launched 7 August ([Product Hunt](https://www.producthunt.com/products/rindler)).

**What it is genuinely good at.** It handles login-gated sites, which is exactly where generic automation falls over ([Rindler](https://rindler.ai/)). Output is structured, so results drop straight into a database instead of needing parsing. And the billing model is honest  -  one run equals one finished task equals one dollar, and failed runs are not charged ([Rindler pricing](https://rindler.ai/pricing)).

**Honest limitations.** $100 a month minimum, about R1,620, with no cheaper tier. Starter covers only one custom site mapped, so a second portal pushes you to Teams at $1,000 a month, roughly R16,200. Billing is annual, billed monthly, with the first month as a pilot  -  that is a year-long commitment dressed as a monthly plan, and you should read it that way. And whether it copes with South African government portals specifically is entirely untested.

**South African use cases.**
- An immigration practice where staff spend hours logged into Home Affairs and VFS portals doing the same lookups. This is the use case, and it is also the untested one.
- Logistics operations checking multiple carrier portals daily.
- Only worth it if you can name the portal, count the hours, and the maths clears R1,620 a month.

**Industries.** Immigration services, professional services, logistics, fintech back-office.

**Pricing.** No free tier, but a 7-day trial and a free public playground with a few sites requiring no signup. Starter $100 a month for 100 runs. Teams $1,000 for 1,000 runs plus scheduled automations and ten login-gated sites ([Rindler pricing](https://rindler.ai/pricing)).

**Access notes for SA.** Not published.

**Link.** [rindler.ai](https://rindler.ai/)

---

## What I would actually try this week

**One. The ElevenLabs Dubbing API on the free tier.** Afrikaans support is the first genuinely South-Africa-shaped thing to land in weeks ([ElevenLabs docs](https://elevenlabs.io/docs/overview/capabilities/dubbing)). Take one existing piece of content, dub it, and listen to whether the tone survives. It costs nothing to find out, and if it works you have doubled your addressable audience on every video you have already made. Free-tier output is watermarked, so this is a test, not production  -  but the test is the point.

**Two. Audit who on your team is still on a paid ChatGPT seat they do not need.** The free tier now has unlimited text chats and a model that is measurably more accurate ([TechCrunch](https://techcrunch.com/2026/08/06/openai-brings-unlimited-chatgpt-text-chats-to-free-users/)). If someone is paying R324 a month and only ever types text prompts, that is a seat you can drop. Keep Plus for whoever actually needs file uploads, images, voice or Sol-grade reasoning. This is the rare week where the recommendation is to spend less.

**And one to avoid.** Do not put client code through Meta Muse Code's contributor tier. Meta trains on your prompts and completions on that tier ([Barchart](https://www.barchart.com/story/news/3691953/meta-enters-the-terminal-coding-agent-race-with-muse-code-as-contributor-pricing-raises-new-data-use-questions)). The pricing gap between contributor and standard is roughly twelve to one, which is precisely the kind of gap that makes people click the wrong button on a Friday afternoon.

---

## What we deliberately left out

Two products I wanted to include did not make it on pricing grounds. Soloop, an approval-first agent system for solo founders, placed second on Product Hunt on 7 August, but its pricing page would not resolve and the aggregators contradict each other badly  -  one says a single $100 tier, another describes a free tier with fifteen credits ([Stork.ai](https://www.stork.ai/en/soloop), [LinkGo](https://linkgo.dev/tools/soloop-ai-agents-2026-08-08)). Worth a second look next week. Hey Noah topped Product Hunt on 4 August as an SMS-first AI executive assistant, but publishes no pricing at all and its SMS-first design almost certainly assumes a US number ([Product Hunt](https://www.producthunt.com/products/hey-noah)).

Anthropic shipped self-hosted environments for Claude Code on 6 and 7 August, but Team and Enterprise plans only ([Anthropic](https://claude.com/blog-category/announcements)), so there is no path for a small business. Qwen3.8-Max missed the window by a single day. And n8n did ship v2.34.0 on 4 August, but it is patches and fixes  -  the AI-builder orchestrator step ceiling went from 5 to 60, plus credential and OAuth handling fixes ([n8n changelog](https://raw.githubusercontent.com/n8n-io/n8n/master/CHANGELOG.md)). Worth knowing if you self-host, not worth a segment.

I checked Google Gemini and Workspace properly and found nothing date-verifiable inside the window. The Workspace blog lists recent items but renders no dates, so I could not place them.

**On the local front.** Two South African stories worth your time, neither of them a tool. Discovery is deliberately pacing its adoption of AI coding agents, reporting 20 to 25 percent efficiency gains in some areas but declining to rush ([TechCentral](https://techcentral.co.za/why-discovery-is-going-slow-on-ai-coding-agents/284618/))  -  useful calibration if you are ever pitching AI tooling into a large SA corporate, because the buyer wants evidence, not velocity. And Disrupt Africa's third Diversity Dividend report shows female-founded African startup funding trending the wrong way: the share of funded startups with a female co-founder fell from 26.3 percent in 2023 to 18.3 percent so far in 2026, and female-CEO-led ventures captured just 2.8 percent of total funding this year against 8.2 percent in 2023 ([Disrupt Africa](https://disruptafrica.com/2026/08/05/worrying-trend-for-funding-for-female-founded-startups-in-african-tech/)). The report is free to download.

Just outside the window but worth a note: Domains.co.za launched self-hosted n8n VPS hosting on local South African infrastructure ([TechCentral](https://techcentral.co.za/domains-co-za-launches-self-hosted-n8n-vps-hosting/284434/)). If you have been wanting automation running on SA soil for POPIA reasons, that is the local option now.

---

*Compiled 10 August 2026. Every price and date above was verified against the linked source in the week of publication. Where a figure came only from a third-party reviewer rather than the vendor, the text says so. Prices change. Check before you buy.*
