# AI Tools Drop - Week of 27 July to 3 August 2026

**For South African founders and small business owners.**
Rand figures use a working rate of roughly R16.50 to the dollar ([Yahoo Finance USD/ZAR](https://finance.yahoo.com/quote/USDZAR=X/)). Check the live rate before you commit to anything.

---

## This week in one paragraph

This was a pricing week, not a launch week. The two things that actually move money for a South African business both happened on the cost side: OpenAI cut GPT-5.6 Luna by 80 percent and Terra by 20 percent ([OpenAI](https://openai.com/index/advancing-the-price-performance-frontier-with-gpt-5-6/)), and DeepSeek promoted V4-Flash out of preview at roughly a tenth of that again ([Hugging Face](https://huggingface.co/blog/ResterChed/deepseek-v4-flash-official-release)). If you have been sitting on an AI feature because the per-request cost did not work, the maths changed this week. On the product side, ElevenLabs put its agents onto SMS and Telegram ([ElevenLabs](https://elevenlabs.io/blog/new-channels)), Google shipped deck generation into Slides and confirmed Gemini Spark is worldwide ([Google Workspace](https://workspace.google.com/blog/product-announcements/july-2026-workspace-feature-drop), [blog.google](https://blog.google/products-and-platforms/products/gemini/gemini-drop-july-2026/)), and Notion closed the loop between meeting notes and automation ([Notion](https://www.notion.com/releases/2026-07-31)). Nothing launched locally. South African tech news this week was infrastructure and ecosystem announcements, not tools you can sign up for.

---

## 1. ElevenAgents - now on SMS, Telegram, Intercom and Freshdesk

**One AI agent, nine channels, configured once.**

**What it actually is.** ElevenLabs already let you build a voice and chat agent and put it on phone, web, WhatsApp, Slack and Zendesk. On 28 July they added SMS, Telegram, Intercom and Freshdesk, managed from a redesigned channels dashboard ([ElevenLabs](https://elevenlabs.io/blog/new-channels)).

**What it is genuinely good at.** You define the agent once - knowledge, tools, procedures, guardrails - and the same agent answers a phone call, a WhatsApp message and a support ticket with the same information ([ElevenLabs](https://elevenlabs.io/blog/new-channels)). You can tune behaviour per channel, so it goes terse on SMS and formal on a support ticket. And you can run channel-scoped simulations against evaluation criteria before anything goes live, which matters when the agent is talking to paying clients.

**Honest limitations.** Telegram, Intercom and Freshdesk are labelled Alpha by ElevenLabs themselves ([ElevenLabs](https://elevenlabs.io/blog/new-channels)). The free tier is 15 minutes a month, which is a prototype budget, not a reception desk ([ElevenAgents pricing](https://elevenlabs.io/pricing/agents)). Concurrency is capped low on the cheap tiers - four concurrent calls on Free, six on Starter.

**South African use cases.**
- A salon or spa running WhatsApp and SMS booking confirmations and no-show chasing off one agent, with the same agent picking up the phone after hours.
- An immigration practice running first-line intake: what visa are you on, what is your expiry date, which documents do you already have. Chasing outstanding documents by SMS is exactly the boring work this handles.
- An online retailer answering "where is my order" across WhatsApp and the website widget without duplicating the logic twice.

**Industries.** Beauty and wellness, immigration services, retail and e-commerce, any appointment-driven business.

**Pricing.** Free tier at 15 minutes a month. Starter is $6 a month for 75 minutes, roughly R99. Creator is $11, about R182. Pro is $99, about R1,634. Prices exclude tax ([ElevenAgents pricing](https://elevenlabs.io/pricing/agents)).

**Access notes for SA.** No region restriction is stated. Card requirements were not published, so treat that as unconfirmed.

**Link.** [elevenlabs.io/blog/new-channels](https://elevenlabs.io/blog/new-channels)

---

## 2. Model Council in Perplexity Computer

**Ask eight models the same hard question and have a ninth one referee.**

**What it actually is.** You assemble a council of between two and eight different AI models, give them one prompt, each works it independently, and a chair model synthesises where they agree and where they diverge ([The Register](https://www.theregister.com/ai-and-ml/2026/07/28/perplexitys-tokenmaxxing-model-council-gives-you-multiple-bot-perspectives/5279972)). As of 28 July it moved into Computer and down to the Individual Pro tier.

**What it is genuinely good at.** It is built for judgement calls rather than lookups - the positioning is explicitly legal questions, financial queries, corporate decisions, growth modelling and risk ([The Register](https://www.theregister.com/ai-and-ml/2026/07/28/perplexitys-tokenmaxxing-model-council-gives-you-multiple-bot-perspectives/5279972)). You pick the diversity yourself, mixing OpenAI, Anthropic and Google with open-weight models like GLM and Kimi. And the synthesis comes out as work-ready assets, with follow-ups available for confidence levels and stated assumptions.

**Honest limitations.** The capability is not new - Model Council launched in February, and what changed this week is access ([The Register](https://www.theregister.com/ai-and-ml/2026/07/28/perplexitys-tokenmaxxing-model-council-gives-you-multiple-bot-perspectives/5279972)). Cost is the real catch: Computer is usage-billed at 100 credits to the dollar and Perplexity did not publish credits per Council session. A heavy asset-generating task is quoted at up to 2,275 credits, about $22.75 or R375, for one run. Individual Pro gets 4,000 bonus credits with no recurring monthly allowance stated.

**South African use cases.**
- Stress-testing a POPIA compliance decision before you pay an attorney to confirm it. Where the models disagree is where you actually need the lawyer.
- Pricing a new SaaS tier for the local market, where you want the divergence between models rather than one confident wrong answer.
- Build-versus-buy calls on infrastructure, with the assumptions written out so you can argue with them later.

**Industries.** Professional services, fintech, SaaS building, anything with a real decision cost.

**Pricing.** No free tier. Individual Pro is $20 a month, roughly R330. Max is $200, about R3,300. Enterprise Pro is $34 per seat ([The Register](https://www.theregister.com/ai-and-ml/2026/07/28/perplexitys-tokenmaxxing-model-council-gives-you-multiple-bot-perspectives/5279972)).

**Access notes for SA.** Not published.

**Link.** [perplexity.ai](https://www.perplexity.ai/)

---

## 3. Google Workspace July Drop - Gemini in Slides, Docs and Vids

**Describe the deck, point it at an old deck for branding, get an editable deck.**

**What it actually is.** The 29 July Workspace drop, headlined by full deck generation in Slides, comment-actioning and visual generation in Docs, and digital-presenter avatars in Vids ([Google Workspace](https://workspace.google.com/blog/product-announcements/july-2026-workspace-feature-drop)).

**What it is genuinely good at.** The Slides feature is the one worth your time: you describe the deck, point it at an existing deck so it picks up your brand formatting, and it pulls context from your Docs, Sheets, PDFs and prior decks, asks clarifying questions, and produces a fully editable deck. In Docs it synthesises comment threads, drafts replies and suggests edits you accept in one click, plus generates images, diagrams and infographics inline. Vids will auto-storyboard, auto-script, put an avatar presenter on screen and voice it in eight languages, re-scriptable at any point ([Google Workspace](https://workspace.google.com/blog/product-announcements/july-2026-workspace-feature-drop)).

**Honest limitations.** Google did not say which plans get what in the drop post, and the pricing page shows Gemini in Docs, Sheets and Slides is not supported on Starter ([Workspace pricing](https://workspace.google.com/pricing)), so realistically you need Standard. There is no African language support - the eleven newly added Docs languages are Mandarin, Dutch, Malay, Hebrew, Polish, Turkish, Czech, Indonesian, Swedish, Danish and Norwegian. And data-region controls remain EU or US only, with no African data region, which is worth knowing if you are writing a POPIA data-flow register.

**South African use cases.**
- An agency turning a client brief and a spreadsheet of results into a monthly report deck that already matches the client's template.
- A consultancy where comment-heavy document review is the actual billable work, and triaging those threads is the bottleneck.
- Internal training or onboarding videos via Vids, where the alternative is nobody making them at all.

**Industries.** Professional services, agency and creative work.

**Pricing.** No free tier. Starter is $7 per user a month, about R116, but the AI features you want need Standard at $14, roughly R231. Plus is $22, about R363. Promotional rates of $5.60 and $11.20 were listed ([Workspace pricing](https://workspace.google.com/pricing)).

**Access notes for SA.** Not region-restricted, described as rolling out to Workspace customers now ([Google Workspace](https://workspace.google.com/blog/product-announcements/july-2026-workspace-feature-drop)).

**Link.** [workspace.google.com - July 2026 feature drop](https://workspace.google.com/blog/product-announcements/july-2026-workspace-feature-drop)

---

## 4. OpenAI cuts GPT-5.6 Luna by 80 percent

**The most commercially significant thing that happened this week.**

**What it actually is.** From 30 July, an 80 percent price cut on GPT-5.6 Luna and 20 percent on Terra, plus a new API Fast mode replacing Priority Processing ([OpenAI](https://openai.com/index/advancing-the-price-performance-frontier-with-gpt-5-6/)).

**What it is genuinely good at.** Luna now costs $0.20 per million input tokens and $1.20 per million output - roughly R3.30 and R19.80. Terra sits at $2 and $12, about R33 and R198 ([OpenAI](https://openai.com/index/advancing-the-price-performance-frontier-with-gpt-5-6/)). If you shelved an AI feature because the unit economics did not work at South African price points, run the numbers again. Both models also consume fewer credits in ChatGPT Work and Codex at unchanged subscription prices, so your existing seat stretches further. Fast mode gives up to 2.5 times the speed at twice the price with no intelligence change, and existing priority requests migrate automatically.

**Honest limitations.** Sol, the flagship, got no cut. Luna is not available on Free or Go in ChatGPT Work and Codex - those tiers get Terra only ([OpenAI](https://openai.com/index/advancing-the-price-performance-frontier-with-gpt-5-6/)). And this is a price change, not a capability release. Cheaper output, not better output.

**South African use cases.**
- Any product feature where you priced per-request cost against a R199 monthly subscription and it did not clear. Document classification, intake triage, summarisation.
- Bulk processing you have been doing manually because automation cost more than a junior's time. At R3.30 per million input tokens that calculus flips for a lot of workloads.
- Customer-facing chat where you previously capped usage to protect margin.

**Industries.** SaaS building, fintech and payments, anywhere volume decides whether a feature ships.

**Pricing.** Token-priced, no subscription figure published on the announcement. ChatGPT Work has a free tier that includes Terra ([OpenAI](https://openai.com/index/advancing-the-price-performance-frontier-with-gpt-5-6/)).

**Access notes for SA.** I could not verify a current supported-countries page, so I am not asserting South African eligibility or card requirements either way.

**Link.** [openai.com - advancing the price-performance frontier with GPT-5.6](https://openai.com/index/advancing-the-price-performance-frontier-with-gpt-5-6/)

---

## 5. DeepSeek-V4-Flash-0731

**Cheap agentic model with MIT open weights, which solves the data-residency problem for you.**

**What it actually is.** DeepSeek promoted its cheap agentic model out of preview on 31 July - 284 billion parameters with 13 billion activated - and published MIT-licensed open weights the same day ([Hugging Face](https://huggingface.co/blog/ResterChed/deepseek-v4-flash-official-release)).

**What it is genuinely good at.** Cost, first. It runs at $0.14 per million input tokens on a cache miss, $0.28 per million output, and $0.0028 on a cache hit ([DeepSeek API pricing](https://api-docs.deepseek.com/quick_start/pricing)) - roughly R2.31, R4.62 and about five cents. That is an order of magnitude below GPT-5.6 Terra. On capability, the 13-billion-active build beats the much larger V4-Pro preview on all nine agentic benchmarks DeepSeek publishes ([Hugging Face](https://huggingface.co/blog/ResterChed/deepseek-v4-flash-official-release)). And the MIT open weights mean no lock-in.

**Honest limitations.** DeepSeek's own changelog still calls the API public beta ([Hugging Face](https://huggingface.co/blog/ResterChed/deepseek-v4-flash-official-release)). It is the same architecture and size as the preview, only re-post-trained. V4-Pro remains preview. And the hosted API is China-hosted, which for POPIA-sensitive client data is a real consideration - the open weights are the answer there, if you can host them.

**South African use cases.**
- High-volume document parsing in a logistics or clearing operation, where the volume is what made it uneconomical before.
- Bulk first-pass document review in a legal or accounting practice, with a human doing the second pass.
- Self-hosted agent backends where client data cannot leave your infrastructure, which the MIT licence makes possible.

**Industries.** SaaS building, logistics, professional services.

**Pricing.** No free tier and no subscription. Token-priced at $0.14 input and $0.28 output per million ([DeepSeek API pricing](https://api-docs.deepseek.com/quick_start/pricing)).

**Access notes for SA.** Not published. The open weights sidestep the question entirely if you can host.

**Link.** [api-docs.deepseek.com - pricing](https://api-docs.deepseek.com/quick_start/pricing)

---

## 6. Gemini Drop - July 2026

**Gemini Spark goes worldwide, which is the rare vendor statement that explicitly includes us.**

**What it actually is.** The 31 July Gemini app drop: Gemini Spark, a persistent agent that keeps working after you close the laptop, going worldwide, plus Gemini 3.6 Flash and 3.5 Flash-Lite, voice control on macOS, and app linking ([blog.google](https://blog.google/products-and-platforms/products/gemini/gemini-drop-july-2026/)).

**What it is genuinely good at.** The word "worldwide" is doing real work here. Most vendors publish nothing about country availability, and Google stated it plainly for Spark ([blog.google](https://blog.google/products-and-platforms/products/gemini/gemini-drop-july-2026/)). Google also lists South Africa among supported countries for the Gemini web app ([Google Gemini support](https://support.google.com/gemini/answer/13575153)). The macOS voice control lets you dictate clean text into any active window, transform highlighted content and generate visuals at the cursor, which is genuinely useful if you draft a lot. And the new Flash models are faster and cheaper in the app.

**Honest limitations.** Personalised image generation is United States only - a direct exclusion for us ([blog.google](https://blog.google/products-and-platforms/products/gemini/gemini-drop-july-2026/)). The "help across apps" feature supports Dropbox, Zillow Rentals and Viator, and Zillow is meaningless in South Africa. Google did not state which plans get most of these features.

**South African use cases.**
- Dictation-first drafting on a Mac - proposals, client emails, scoping documents - without switching applications.
- Spark as a background research agent that keeps running on a market or competitor question while you are in meetings.
- Cross-industry, honestly. This is general-purpose.

**Industries.** Professional services and agency work most directly, but broadly applicable.

**Pricing.** Free tier exists for the Gemini app. Plan requirements for these specific features were not stated.

**Access notes for SA.** Confirmed usable from South Africa ([Google Gemini support](https://support.google.com/gemini/answer/13575153)), with Spark stated as worldwide.

**Link.** [blog.google - Gemini Drop July 2026](https://blog.google/products-and-platforms/products/gemini/gemini-drop-july-2026/)

---

## 7. Notion - meeting notes can now trigger Custom Agents

**The meeting ends, the tracker updates itself.**

**What it actually is.** A new trigger, shipped 31 July, that fires a Custom Agent the moment an AI Meeting Note finishes summarising ([Notion](https://www.notion.com/releases/2026-07-31)).

**What it is genuinely good at.** It kills post-meeting admin. The agent can update the project tracker, post a recap with decisions and next steps to Slack or email, and turn feedback into tickets ([Notion](https://www.notion.com/releases/2026-07-31)). Setup is three steps - open Custom Agent settings, add the trigger, choose which meetings fire it. And it fires selectively, so client calls and internal standups can behave completely differently.

**Honest limitations.** AI Meeting Notes sits on the Business plan at $20 per member a month ([Notion pricing](https://www.notion.com/pricing)), so this is not a free-plan trick. Custom Agents also burn Notion credits on top of the seat price, at $10 per 1,000 monthly credits after the trial. For a small team the combined cost adds up quickly in rand terms.

**South African use cases.**
- A consultancy where the recap email to the client is the deliverable that proves the hour was billable.
- A product team where standup decisions never make it into the tracker and then nobody remembers what was agreed.
- Client onboarding calls where the action items need to become tasks the same day.

**Industries.** Professional services, agency and creative work.

**Pricing.** Notion itself has a free tier, AI is trial-only there. Plus is $10 per member a month, about R165. The plan that includes AI Meeting Notes is Business at $20, roughly R330 per member, plus about R165 per thousand credits ([Notion pricing](https://www.notion.com/pricing)).

**Access notes for SA.** Not published.

**Link.** [notion.com - 31 July 2026 release](https://www.notion.com/releases/2026-07-31)

---

## 8. NudgeForMe

**It reads your sent folder, finds who never replied, and drafts the follow-up.**

**What it actually is.** An AI follow-up agent that scans your sent mail, identifies threads nobody answered, and drafts natural follow-ups inside your own mailbox. It launched this week and took the number one spot on Product Hunt for 1 August ([Product Hunt leaderboard](https://www.producthunt.com/leaderboard/daily/2026/8/1), [Product Hunt](https://www.producthunt.com/products/nudgeforme)).

**What it is genuinely good at.** Recovering dead threads - leads, deals, partnerships and customer conversations that simply went cold ([Product Hunt](https://www.producthunt.com/products/nudgeforme)). It starts in draft mode, so you review, adjust, approve or dismiss before anything sends, which is the right default. And it works with Gmail, Outlook and generic IMAP or SMTP. That last one matters here, because plenty of South African businesses are on a local host rather than Google or Microsoft.

**Honest limitations.** It does one thing and nothing else. It is a launch-week product with no track record beyond the founding team's previous email tool. And you are granting a third party read access to your sent mail, which deserves a moment's thought if that mailbox contains client matters.

**South African use cases.**
- An immigration practice chasing outstanding documents from applicants who went quiet. This is the single highest-value use of it on this list.
- Proposal follow-ups at an agency, where the second nudge is where the work actually gets won.
- Invoice and payment follow-ups where nobody has the appetite to send the third email.

**Industries.** Immigration services, professional services, agency and creative work.

**Pricing.** Product Hunt lists it as free. Paid tiers were not published.

**Access notes for SA.** Not published.

**Link.** [producthunt.com/products/nudgeforme](https://www.producthunt.com/products/nudgeforme)

---

## 9. MiniMax H3, also called Hailuo 3.0

**Fifteen seconds of 2K video with native audio, priced per second.**

**What it actually is.** An omni-modal model released 31 July that takes text, images, video and audio in one context and returns up to fifteen seconds of 2K video with native stereo audio ([MiniMax](https://www.minimax.io/blog/minimax-h3)).

**What it is genuinely good at.** MiniMax specifically calls out accurate text rendering and accurate brand rendering, plus video-to-video motion transfer ([MiniMax](https://www.minimax.io/blog/minimax-h3)). Text rendering has been the failure mode of AI video for years, so that claim is worth testing rather than assuming. It is aimed squarely at commercial work - advertising, branding, e-commerce, product design, animated posters. And it is cheap: from $0.13 per second of generated video, around R2.15, which puts a fifteen-second clip at roughly R32 ([NYU Shanghai RITS](https://rits.shanghai.nyu.edu/ai/minimax-releases-h3-2k-video-with-native-audio-open-weights-promised/)).

**Honest limitations.** The "open model" claim is a promise, not a delivery - weights were not on Hugging Face at publication and the licence terms are unknown ([NYU Shanghai RITS](https://rits.shanghai.nyu.edu/ai/minimax-releases-h3-2k-video-with-native-audio-open-weights-promised/)). Clips run four to fifteen seconds, extendable to about thirty. Parameter count, architecture, rate limits and the licence covering generated content were all unpublished at launch, and there was no independent arena scoring. Reference inputs are fiddly: twelve files maximum, fifteen seconds of combined reference, and audio references cannot be submitted alone.

**South African use cases.**
- Product and promotional video for an online store, at a price where you can afford to make ten and keep two.
- Social content for a salon or wellness brand that needs weekly output and cannot afford a shoot each time.
- Agency concept work, where you show a client the idea as motion rather than a storyboard.

**Industries.** Retail and e-commerce, agency and creative work, beauty and wellness.

**Pricing.** Usage-based from $0.13 per second of generated video. No subscription published, free tier not confirmed.

**Access notes for SA.** Not published. Available through the MiniMax platform API, the Hailuo consumer app, and third-party routers including OpenRouter as `minimax/hailuo-3` - the router is likely the easier payment path from here ([NYU Shanghai RITS](https://rits.shanghai.nyu.edu/ai/minimax-releases-h3-2k-video-with-native-audio-open-weights-promised/)).

**Link.** [minimax.io/blog/minimax-h3](https://www.minimax.io/blog/minimax-h3)

---

## 10. Adomate

**Turns competitor ads and customer reviews into ad concepts you can trace back to the data.**

**What it actually is.** A workflow tool launched this week that converts ad performance data, competitor ads and customer reviews into branded ad concepts, each traceable to the data point that produced it ([Product Hunt](https://www.producthunt.com/products/adomate), [Adomate](https://adomate.ai/)).

**What it is genuinely good at.** It mines reviews for angles, pulling from Trustpilot and Amazon alongside the Meta Ad Library and Meta Ads Manager, then finds the single review that best matches your criteria and builds a concept from it ([Product Hunt](https://www.producthunt.com/products/adomate)). The traceability is the real feature - every concept points back to the exact competitor ad, review line or metric that triggered it, so you are not arguing with a black box. Workflows are reusable and duplicable across brands, which suits an agency running several accounts.

**Honest limitations.** It is Meta-only and shaped for direct-to-consumer. Other platforms and B2B use are roadmap, not shipped. Generation starts from a single data point - steering by aggregated insight is also roadmap, as is video brief generation ([Product Hunt](https://www.producthunt.com/products/adomate)). And the review-mining engine depends on Trustpilot and Amazon depth, which most South African brands simply do not have. That guts the strongest feature locally.

**South African use cases.**
- An agency running multiple Meta accounts where the competitor-ad teardown is currently manual.
- A local e-commerce brand with genuine Trustpilot volume, which is a small group.
- Concept generation for a brand where the Meta Ad Library already has useful competitor coverage.

**Industries.** Retail and e-commerce, agency and creative work. Only if you are already spending on Meta.

**Pricing.** Both pages say free to start, but standard pricing is not published ([Product Hunt](https://www.producthunt.com/products/adomate), [Adomate](https://adomate.ai/)). Launch-week discount codes expired at the end of the week.

**Access notes for SA.** Not published. Requires a Meta ad account.

**Link.** [adomate.ai](https://adomate.ai/)

---

## What I would actually try this week

**One. Re-run your unit economics against the new OpenAI and DeepSeek prices.** This costs you an hour and no money. Luna at $0.20 per million input tokens ([OpenAI](https://openai.com/index/advancing-the-price-performance-frontier-with-gpt-5-6/)) and DeepSeek V4-Flash at $0.14 ([DeepSeek](https://api-docs.deepseek.com/quick_start/pricing)) mean features you costed six months ago and shelved may now clear. That is the highest-return thing on this page and it is not a new tool at all.

**Two. ElevenAgents on the $6 Starter tier.** Roughly R99 a month to put one agent across WhatsApp, SMS and phone with per-channel tuning ([ElevenAgents pricing](https://elevenlabs.io/pricing/agents)). For any appointment-driven business - salon, clinic, consultancy - the no-show chasing alone justifies it. Start on the free 15 minutes, prove the flow works, then upgrade.

**Worth a diary note.** If you use Claude in Slack, the legacy app switches over to Claude Tag on 3 August, and Tag is beta for Enterprise and Team only ([Slack Help Center](https://slack.com/help/articles/53532192117267-Use-Claude-in-Slack)). For a solo Pro or Max subscriber that is a loss of access, not a gain.

---

## What we deliberately left out

Three of this week's loudest headlines were not actually from this week. Claude Opus 5 released on 24 July, three days before our window, but still ran high on Product Hunt's weekly board ([Product Hunt weekly](https://www.producthunt.com/leaderboard/weekly/2026/31)). Framer 3.0 shipped on 16 June and simply bought placement all week. Canva Code 2.0 opened up in mid-July, with country rollouts still continuing ([Daily Tribune](https://tribune.net.ph/2026/07/28/canva-code-20-arrives-in-phl)).

Two in-window releases were dropped for being unbuyable from here. ByteDance's Seedance 2.5 launched 31 July with thirty seconds of 4K in a single pass ([ByteDance Seed](https://seed.bytedance.com/en/blog/one-take-creation-flexible-referencing-introducing-seedance-2-5)), but access runs through Jimeng AI and Doubao Pro with no published pricing or regional availability. Zinley topped Product Hunt on 2 August with an AI representative that gets its own phone number ([Product Hunt](https://www.producthunt.com/products/zinley)) - attractive for a salon, but nothing published says it can provision a South African number, and a US-only number is useless here.

**On the local front.** No new AI tool aimed at South African SMBs launched this week. What did happen was ecosystem news: Telkom committed R100 million to a Telkom AI Institute on 31 July ([Engineering News](https://www.engineeringnews.co.za/article/telkom-commits-r100m-to-launch-telkom-ai-institute-2026-07-31)), Google Cloud announced five Africa initiatives including a R3 million Soweto innovation centre with WeThinkCode ([Tech Review Africa](https://techreviewafrica.com/news/6154/google-cloud-unveils-five-major-ai-and-digital-infrastructure-initiatives-for-africa)), South Africa topped Africa's AI-readiness rankings ([ITWeb](https://www.itweb.co.za/article/sa-tops-africas-ai-readiness-rankings/5yONP7EroK5MXWrb)), and local IT spend is forecast to grow 19.8 percent to $28.1 billion this year ([TechCentral](https://techcentral.co.za/south-african-it-spending-surging-as-ai-boom-lands-locally/284295/)). Context, not tools.

---

*Compiled 3 August 2026. Every price and date above was verified against the linked source in the week of publication. Prices change. Check before you buy.*
