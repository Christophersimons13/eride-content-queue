# AI Tools Drop - Week of 28 September 2026

Ten items from 21 to 28 September, read from a Johannesburg desk. Rand figures use R16.43 to the dollar, the midpoint of a three-source cluster on Monday morning ([XE](https://www.xe.com/currencyconverter/convert/?Amount=1&From=USD&To=ZAR), [Trading Economics](https://tradingeconomics.com/south-africa/currency), [Pluang](https://pluang.com/en/tools/currency-converter/usd-zar)).

---

## This week in one paragraph

This was a frontier-model week, and it is worth being honest about what that means. Four of the largest AI labs shipped or repriced inside five days: xAI's Grok 4.7 on 21 September ([xAI](https://x.ai/news/grok-4-7)), Anthropic's Claude Opus 5.5 and OpenAI's GPT-6 Sol and Luna on 22 September ([Anthropic](https://www.anthropic.com/news), [OpenAI](https://openai.com/index/introducing-gpt-6-sol-and-luna/)), and Google's Gemini 3.8 text-to-speech models on 23 September ([Google](https://blog.google/innovation-and-ai/models-and-research/gemini-models/gemini-3-8-text-to-speech/)). Microsoft rebuilt Copilot on 25 September and, in a partner notice most small businesses will never read, made usage-based billing the default for new Copilot Business licences from 2 November ([Microsoft Partner Center](https://learn.microsoft.com/en-us/partner-center/announcements/2026-september)). Genuinely new small-business tools with verified in-window dates were scarce - most of the Product Hunt board was relaunches or products that shipped earlier in the month. So this list leans on platform changes, and three entries are exactly that. The headline for South Africa is Google's speech model, whose published language list includes Afrikaans, isiZulu, isiXhosa, siSwati, Sepedi and Sesotho ([Gemini API docs](https://ai.google.dev/gemini-api/docs/models/gemini-3.8-flash-tts)). That is the first voice release in this series to name our languages.

Two long-running counts moved this week, both only slightly. For the first time in eight weeks a vendor referenced South Africa's privacy law: Relativity's 23 September press release says its expansion "helps companies abide by South Africa's Protection of Personal Information Act and The Cybercrimes Act" ([Relativity](https://www.relativity.com/news-events/press-release-relativity-partners-with-deloitte-and-control-risks-to-launch-relativityone-in-south-africa/)). And RelativityOne is the first tool on any shortlist in this series with a documented South African hosting region - though, as covered below, that region is not new.

---

## 1. Gemini 3.8 Flash TTS and Flash-Lite TTS - the first voice model here that names our languages

**Hook:** Studio-grade speech in the Gemini API for about 22 cents a minute, with six South African languages on the published list.

**What it actually is.** Two text-to-speech models released 23 September. Flash TTS is the flagship for voice design, acting and long-form audio; Flash-Lite TTS is the high-volume, low-latency model for voice agents ([Google](https://blog.google/innovation-and-ai/models-and-research/gemini-models/gemini-3-8-text-to-speech/)). Google says the models maintain voice quality "across hours of continuous audio" with minimal speaker drift, support two-speaker scenes from a single script, and accept cues such as laughs and sighs ([Google](https://blog.google/innovation-and-ai/models-and-research/gemini-models/gemini-3-8-text-to-speech/)). Voice replication from your own recording is available in Google AI Studio, gated by a verbal consent recording from the voice owner, and every clip is watermarked with SynthID ([Google](https://blog.google/innovation-and-ai/models-and-research/gemini-models/gemini-3-8-text-to-speech/)).

**What it is genuinely good at.** Language coverage and price. The model page says it detects the input language automatically and supports "over 130 languages", and the list printed there includes Afrikaans, Zulu, Xhosa, Swati, Northern Sotho and Southern Sotho, alongside Swahili and Nyanja ([Gemini API docs](https://ai.google.dev/gemini-api/docs/models/gemini-3.8-flash-tts)). On price, Flash TTS is $0.50 per million text tokens in and $9.00 per million audio tokens out through 31 December 2026, and Google states that equals $0.00225 per 10 seconds of audio ([Gemini pricing](https://ai.google.dev/gemini-api/docs/pricing)). That works out to about 1.35 US cents a minute - roughly R0.22 - or about R13 for an hour of finished speech. Flash-Lite TTS is $6.00 per million audio tokens out, about R0.15 a minute ([Gemini pricing](https://ai.google.dev/gemini-api/docs/pricing), [CellCog](https://cellcog.ai/blog/gemini-3-8-flash-tts/)).

**Honest limitations.** Four of them. First, a language being on a list is not the same as a language sounding right. Nothing published this week tests isiZulu or isiXhosa output quality; you have to listen. Second, Setswana, Xitsonga, Tshivenda and isiNdebele do not appear on the list we read ([Gemini API docs](https://ai.google.dev/gemini-api/docs/models/gemini-3.8-flash-tts)). Third, prices double from 1 January 2027 - Flash TTS goes to $18.00 per million audio tokens ([Gemini pricing](https://ai.google.dev/gemini-api/docs/pricing)). Fourth, and this matters for client work: on the free tier, the pricing page's "Used to improve our products" row reads "Yes"; on the paid tier it reads "No" ([Gemini pricing](https://ai.google.dev/gemini-api/docs/pricing)). Do not put client scripts or personal information through the free tier. Voice replication is also unavailable in the EEA, UK, Switzerland, India, Illinois and Texas ([Google](https://blog.google/innovation-and-ai/models-and-research/gemini-models/gemini-3-8-text-to-speech/)); South Africa is not on that exclusion list, but Google does not state South African availability either.

**South African use cases.**
- A clinic, salon or municipality-facing service records appointment reminders and IVR menus in isiZulu, isiXhosa and Afrikaans instead of English only.
- An immigration or legal-services firm produces plain-language explainer audio in a client's home language, with a human reviewing every script first.
- A content agency narrates long-form training or YouTube material at a fraction of per-minute voice costs, then spends the savings on native-speaker review.

**Industries:** professional services, beauty and wellness, agency and creative work, education, customer service, any business speaking to customers outside English.

**Pricing:** Free tier for testing. Paid Flash TTS $0.50 in and $9.00 out per million tokens (about R8 and R148) through 31 December 2026, doubling on 1 January 2027. Flash-Lite TTS $0.50 in and $6.00 out (about R8 and R99) ([Gemini pricing](https://ai.google.dev/gemini-api/docs/pricing)).

**SA access notes:** Available in the Gemini API and Google AI Studio from 23 September ([Google](https://blog.google/innovation-and-ai/models-and-research/gemini-models/gemini-3-8-text-to-speech/)). No hosting region or South African availability statement is published. Use a paid billing account for anything involving personal information.

**Link:** https://ai.google.dev/gemini-api/docs/models/gemini-3.8-flash-tts

---

## 2. The new Microsoft Copilot - and the billing change hiding in a partner notice

**Hook:** Copilot gets a persistent agent called Autopilot and a coding surface. New Copilot Business licences bought through a reseller switch to pay-as-you-go by default on 2 November.

**What it actually is.** On 25 September Microsoft reorganised Copilot into Home, which combines Chat and Cowork with editing inside Word, PowerPoint and Excel; Code, for building apps; and Autopilot, the new name for Scout, an agent with its own identity, memory and workspace inside your Microsoft 365 tenant that you assign an objective and a role ([VentureBeat](https://venturebeat.com/technology/microsoft-revamps-its-copilot-ai-with-a-persistent-autopilot-agent-and-hosting-for-ai-generated-apps)). Autopilot's private preview expands at the end of September, and Code arrives first for Frontier programme users ([VentureBeat](https://venturebeat.com/technology/microsoft-revamps-its-copilot-ai-with-a-persistent-autopilot-agent-and-hosting-for-ai-generated-apps), [Reuters](https://www.reuters.com/technology/microsoft-revamps-copilot-with-code-generation-agentic-ai-tools-2026-09-25/)).

**What it is genuinely good at.** If your business already lives in Outlook, Teams and Excel, Autopilot is the first Microsoft agent designed to keep working on a responsibility over days rather than answer one prompt. Microsoft's demonstration had an Autopilot pull email, Teams threads, Dynamics 365 inventory and spreadsheets together to find a shipment problem affecting 18 stores ([VentureBeat](https://venturebeat.com/technology/microsoft-revamps-its-copilot-ai-with-a-persistent-autopilot-agent-and-hosting-for-ai-generated-apps)).

**Honest limitations.** The billing. Microsoft's partner notice states that "Starting November 2, 2026, new Microsoft 365 Copilot Business licenses that you purchase through Cloud Solution Provider (CSP) include usage-based billing by default", with pay-as-you-go covering Copilot Cowork, Work IQ APIs and GitHub Copilot Harness ([Bechtle](https://www.bechtle.com/gb/news/bechtle-blog-uk/software-updates/microsoft-news-september-2026), [Microsoft Partner Center](https://learn.microsoft.com/en-us/partner-center/announcements/2026-september)). Most South African SMBs buy Microsoft 365 through a CSP reseller, so this lands on you through your reseller, not through Microsoft directly. Separately, from 1 October 2026 Microsoft applies "a 5% cost-of-capital uplift to annual-term CSP software subscriptions billed monthly" ([Bechtle](https://www.bechtle.com/gb/news/bechtle-blog-uk/software-updates/microsoft-news-september-2026)). That is three days away. Most of the headline features are preview-only for now.

**South African use cases.**
- A 20-person accounting or logistics firm assigns an Autopilot to month-end supplier follow-ups inside Outlook and Teams, with a named human approving every outbound message.
- A retailer on Dynamics 365 uses the stock-exception pattern Microsoft demonstrated ahead of Black Friday.
- Any SMB on a monthly-billed annual Microsoft plan asks its reseller this week whether the 1 October uplift applies to it.

**Industries:** professional services, retail, logistics, any Microsoft 365 business.

**Pricing:** Copilot Business on Microsoft's US page is $18 per user per month paid yearly on a first-year promotion valid 1 July to 31 December 2026 (about R296), down from $21 (about R345), or $25.20 monthly (about R414) ([Microsoft](https://www.microsoft.com/en-us/microsoft-365-copilot/pricing)). Local reseller pricing in rand will differ. Agent usage is metered on top.

**SA access notes:** Microsoft 365 is sold in South Africa through local CSP partners. The usage-billing default applies to new licences from 2 November; ask your reseller to set a spending cap before you enable agent features.

**Link:** https://learn.microsoft.com/en-us/partner-center/announcements/2026-september

---

## 3. GPT-6 Sol and Luna - half the price, and Luna is free on desktop

**Hook:** OpenAI's new workhorse models cost 50 percent less in the API than the models they replace, and the small one is free in the ChatGPT desktop app.

**What it actually is.** Two models released 22 September in ChatGPT Work, Codex and the API. Sol is the mid-tier model; Luna is the fast, cheap one. OpenAI says Luna at higher effort levels "matches GPT-5.6 Sol at about a hundredth its cost" and that GPT-6 Astra remains its top model ([OpenAI](https://openai.com/index/introducing-gpt-6-sol-and-luna/)).

**What it is genuinely good at.** Unit cost for automation. Sol is $2 per million input tokens and $10 per million output (about R33 and R164); Luna is $0.10 and $0.50 (about R1.64 and R8.21) ([OpenAI](https://openai.com/index/introducing-gpt-6-sol-and-luna/)). Batch and Flex processing are half the standard rate, and cached input drops to $0.20 for Sol and $0.01 for Luna ([TechWire Asia](https://techwireasia.com/2026/09/openai-gpt-6-sol-luna-prices/)). For a business running thousands of classification, extraction or reply-drafting calls a day, Luna is priced low enough that the model is no longer the main cost.

**Honest limitations.** The $2 and $10 Sol rates apply to prompts up to 272,000 input tokens ([TechWire Asia](https://techwireasia.com/2026/09/openai-gpt-6-sol-luna-prices/)). Fast mode costs double. The launch page does not state a data-hosting region or restate a training policy ([OpenAI](https://openai.com/index/introducing-gpt-6-sol-and-luna/)); rely on your existing OpenAI business terms. And OpenAI said at launch that "These models are not yet available in Chat" ([OpenAI](https://openai.com/index/introducing-gpt-6-sol-and-luna/)).

**South African use cases.**
- A fintech or payments business runs every inbound support message through Luna for triage and routing for a few rand a day.
- An e-commerce store regenerates thousands of product descriptions in Batch at half price.
- A founder on the Free plan uses Luna in the desktop app as a daily drafting assistant without paying in dollars.

**Industries:** fintech and payments, retail, SaaS building, customer service.

**Pricing:** Sol $2 / $10, Luna $0.10 / $0.50 per million tokens ([OpenAI](https://openai.com/index/introducing-gpt-6-sol-and-luna/)). Luna is available to Free and Go users in the desktop app ([OpenAI](https://openai.com/index/introducing-gpt-6-sol-and-luna/)).

**SA access notes:** No country restrictions stated. ChatGPT and the OpenAI API are already used from South Africa with local cards.

**Link:** https://openai.com/index/introducing-gpt-6-sol-and-luna/

---

## 4. Claude Opus 5.5 - the expensive tier got cheaper

**Hook:** Anthropic says its new Opus performs at the level of its larger Fable model on most work and costs 40 percent less to run than Opus 5.

**What it actually is.** Released 22 September. Anthropic's words: it "performs at the level of Claude Fable 5.1 on most work and costs 40% less to run than Opus 5" ([Anthropic](https://www.anthropic.com/claude/opus)). It has a 1M-token context window by default and 128k maximum output ([Claude Platform release notes](https://docs.anthropic.com/en/release-notes/api)). TechCrunch notes Anthropic says it is "setting a new state-of-the-art in coding and knowledge work performance" ([TechCrunch](https://techcrunch.com/2026/09/22/anthropic-releases-opus-5-5-with-lower-prices-and-fable-level-performance/)).

**What it is genuinely good at.** Long-running agent work where cache reads dominate the bill. The API price is $4 in and $20 out per million tokens, down from $5 and $25 for Opus 5 ([Claude Platform release notes](https://docs.anthropic.com/en/release-notes/api)), and cache reads fell from $0.50 to $0.20 ([TechWire Asia](https://techwireasia.com/2026/09/openai-gpt-6-sol-luna-prices/)). Anthropic published a worked cost breakdown on 25 September ([Claude blog](https://claude.com/blog/what-a-task-costs-on-opus-5-5)).

**Honest limitations.** It is still the premium tier: $20 out is double GPT-6 Sol's $10. A Japanese reseller's plan guide says Opus 5.5 is on Pro, Max, Team and Enterprise and not on Free ([fyve](https://fyve.co.jp/claude-code/articles/claude-opus-5-5-plan-availability)). Anthropic also announced subscription-limit changes for Pro, Max and Team alongside it ([Windows Forum](https://windowsforum.com/news/claude-opus-5-5-launches-with-20-lower-rates-60-cache-read-cut.445446/)) - check your own limits rather than assuming they went up.

**South African use cases.**
- A software house runs multi-hour refactors or code reviews on client repositories at a lower cost per task.
- A legal or compliance team reviews long contracts or regulatory packs inside a single 1M-token context.
- An agency builds a research agent that reuses the same cached brief across many runs.

**Industries:** SaaS building, professional services, legal and compliance, agency work.

**Pricing:** $4 / $20 per million tokens (about R66 and R329), cache reads $0.20 (about R3.29) ([Claude Platform release notes](https://docs.anthropic.com/en/release-notes/api), [TechWire Asia](https://techwireasia.com/2026/09/openai-gpt-6-sol-luna-prices/)).

**SA access notes:** Available on the Claude API, Amazon Bedrock, Google Cloud and Microsoft Foundry ([Claude Platform release notes](https://docs.anthropic.com/en/release-notes/api)). No new hosting region announced.

**Link:** https://www.anthropic.com/claude/opus

---

## 5. Amazon Seller Assistant workflows - a free agent for marketplace sellers, with a big question mark

**Hook:** An always-on agent that watches your pricing, stock and ratings and can act inside limits you set. Free. Not yet confirmed for amazon.co.za.

**What it actually is.** Announced 23 September. Seller Assistant can now run workflows that monitor a seller's business and either recommend or take action, with an audit trail of every action and seller-set limits and approval requirements ([Retail Gazette](https://www.retailgazette.co.uk/blog/2026/09/amazon-launches-always-on-ai-agent-for-marketplace-sellers/), [Reuters](https://www.reuters.com/business/retail-consumer/amazon-rolls-out-new-agentic-ai-third-party-sellers-2026-09-23/)). It has persistent memory of a seller's pricing patterns, inventory cycles and growth goals. Amazon also launched a Selling Partner plugin that connects seller data to external AI tools, through Amazon Quick and in beta with Anthropic's Claude ([Retail Gazette](https://www.retailgazette.co.uk/blog/2026/09/amazon-launches-always-on-ai-agent-for-marketplace-sellers/)).

**What it is genuinely good at.** Control design. You choose whether it "simply makes recommendations or takes action on their behalf", everything is logged, and you set approval thresholds ([Retail Gazette](https://www.retailgazette.co.uk/blog/2026/09/amazon-launches-always-on-ai-agent-for-marketplace-sellers/)). That is the right shape for a small seller who cannot watch prices at 2 AM.

**Honest limitations.** No coverage says which marketplaces get the new workflows; Reuters says it is for sellers on Amazon's "main e-commerce site" ([Reuters](https://www.reuters.com/business/retail-consumer/amazon-rolls-out-new-agentic-ai-third-party-sellers-2026-09-23/)), and the Selling Partner plugin is "initially available in beta to sellers operating on Amazon's US marketplace" with an international rollout to follow ([Retail Gazette](https://www.retailgazette.co.uk/blog/2026/09/amazon-launches-always-on-ai-agent-for-marketplace-sellers/)). Treat South African availability as unconfirmed until it appears in your Seller Central.

**South African use cases.**
- A Durban homeware brand on amazon.co.za sets price-matching rules with an approval step above a set discount, if and when the feature reaches the SA marketplace.
- A South African brand selling on amazon.com through FBA gets the full feature now.
- A small electronics reseller uses stock alerts to avoid stock-outs over Black Friday.

**Industries:** retail and e-commerce, logistics.

**Pricing:** Free to sellers. Separately, Amazon South Africa is offering new Professional sellers "a R1 monthly selling fee (regular price R400)" until 31 March 2027 ([Amazon Seller Central SA](https://sellercentral.amazon.co.za/)).

**SA access notes:** Not confirmed for amazon.co.za. Check Seller Central before planning around it.

**Link:** https://www.retailgazette.co.uk/blog/2026/09/amazon-launches-always-on-ai-agent-for-marketplace-sellers/

---

## 6. Old Mutual ZakaChat - South African, on WhatsApp, in all our languages

**Hook:** A South African insurer launched an AI money-questions tool on WhatsApp that works in every South African language.

**What it actually is.** ZakaChat, launched during Heritage Month, is "an interactive, AI-powered tool available through WhatsApp" for financial education ([Bizcommunity, 23 September](https://www.bizcommunity.com/article/ask-learn-understand-old-mutual-brings-financial-education-to-whatsapp-419239a)). It answers questions on budgeting, saving and debt "in all South African languages", is built to work on "slower devices and connections", and needs no extra app ([Sunday World, 24 September](https://sundayworld.co.za/business/old-mutual-brings-financial-education-in-your-own-language-on-whatsapp/)).

**What it is genuinely good at.** It is the pattern more than the product. A large South African brand put a multilingual AI assistant on the channel South Africans actually use, designed for low bandwidth, with a clear boundary: it "is not intended to replace personalised financial advice" ([Sunday World](https://sundayworld.co.za/business/old-mutual-brings-financial-education-in-your-own-language-on-whatsapp/)). That boundary is the FAIS-aware way to do this.

**Honest limitations.** It is a consumer education tool, not something you can build on. No pricing, data-handling or language-by-language detail was published in the coverage we read.

**South African use cases.**
- A stokvel or savings-club organiser points members to it for plain-language budgeting help.
- A fintech founder studies it as a reference design: WhatsApp-first, low data, all languages, explicit "information not advice" framing.
- An HR team in a retail or mining business shares it as a free financial-wellness resource.

**Industries:** fintech and payments, financial services, HR and employee wellness.

**Pricing:** Not stated. Consumer-facing.

**SA access notes:** South African by design. Old Mutual's general WhatsApp service line is 0860 933 333 ([Old Mutual](https://www.oldmutual.co.za/contact-us/)); coverage did not confirm whether ZakaChat runs on that same number.

**Link:** https://www.bizcommunity.com/article/ask-learn-understand-old-mutual-brings-financial-education-to-whatsapp-419239a

---

## 7. Financial Cents AI agents - three free document agents for bookkeeping firms

**Hook:** Rename, validate and file client uploads automatically, free on every plan.

**What it actually is.** Launched 24 September by the accounting practice-management platform Financial Cents: AI File Renaming applies the firm's naming convention on upload; AI File Validator checks each document against the request and accounting period and tells the client in the portal if it looks wrong; AI File Routing files a copy into the best-fit client folder ([Yahoo Finance](https://finance.yahoo.com/small-business/articles/financial-cents-launches-ai-agents-150000016.html)). Low-confidence decisions go to staff for review.

**What it is genuinely good at.** Catching the wrong bank statement before it reaches your team. The validator gives the client feedback at the moment of upload, which removes a whole round of emails ([Yahoo Finance](https://finance.yahoo.com/small-business/articles/financial-cents-launches-ai-agents-150000016.html)).

**Honest limitations.** The launch describes "thousands of accounting and bookkeeping firms across North America" ([Yahoo Finance](https://finance.yahoo.com/small-business/articles/financial-cents-launches-ai-agents-150000016.html)); nothing about South African tax documents or SARS formats. Pricing is in US or Canadian dollars ([Financial Cents pricing](https://financial-cents.com/pricing/)).

**South African use cases.**
- A small bookkeeping practice in Pretoria stops chasing clients who upload the wrong month's statement at provisional-tax time.
- A payroll bureau enforces one naming convention across hundreds of client uploads.
- A tax practitioner routes supporting documents into the right client folder without a junior filing them by hand.

**Industries:** accounting, bookkeeping, payroll and professional services.

**Pricing:** Agents free on every plan. Plans from $19 per user per month billed annually (about R312), with Team at $69 per user monthly (about R1,134) and a 14-day trial ([Financial Cents pricing FAQ](https://help.financial-cents.com/en/articles/6079564-pricing-faq-s), [Yahoo Finance](https://finance.yahoo.com/small-business/articles/financial-cents-launches-ai-agents-150000016.html)).

**SA access notes:** SOC 2 certified with encryption in transit and at rest ([Yahoo Finance](https://finance.yahoo.com/small-business/articles/financial-cents-launches-ai-agents-150000016.html)). No hosting region stated. Client financial records are personal information under POPIA; get a data processing agreement before uploading.

**Link:** https://financial-cents.com/

---

## 8. Hemory - always-on listening memory for your agents, and a consent question

**Hook:** Your phone or Apple Watch listens all day and turns what you hear into searchable memory your AI agent can read.

**What it actually is.** Hemory took the number one Product Hunt slot on 26 September with 352 votes ([Nodus](https://nodus-ai.app/it/ph/today)). It listens "on the phone or Apple Watch you already own", splits the day into moments with speaker labels, and connects to Claude, Codex, Cursor or any agent over MCP ([Product Hunt](https://www.producthunt.com/products/hemory)).

**What it is genuinely good at.** Audio handling. The company says "Original audio stays on the recording device; audio sent to the cloud for processing is discarded after processing", and that what is kept is text ([Product Hunt](https://www.producthunt.com/products/hemory)). Only detected speech counts against the usage quota.

**Honest limitations.** You are recording other people. Hemory itself says "We'd always encourage asking before recording a conversation" ([Product Hunt](https://www.producthunt.com/products/hemory)). Text memories are stored in the cloud, with no hosting region and no training statement published. No pricing was on the page. For any business that meets clients, this needs a policy before it needs a subscription.

**South African use cases.**
- A founder uses it only for their own voice notes and internal planning sessions, with the team's agreement.
- A field-sales rep captures their own post-visit debriefs, not the client conversation.
- Not recommended for client consultations in immigration, health or legal work.

**Industries:** founder productivity, internal operations.

**Pricing:** Not stated.

**SA access notes:** App Store availability; no country statement. POPIA applies to any identifiable voice you capture.

**Link:** https://www.hemory.com/

---

## 9. RelativityOne South Africa - the first vendor POPIA reference in eight weeks

**Hook:** A legal e-discovery platform partnered with Deloitte and Control Risks to push its South African service, citing the POPI Act and the Cybercrimes Act.

**What it actually is.** Relativity's 23 September press release announces partnerships with Deloitte and Control Risks to "Launch RelativityOne in South Africa", saying the expansion "helps companies abide by South Africa's Protection of Personal Information Act and The Cybercrimes Act" ([Relativity](https://www.relativity.com/news-events/press-release-relativity-partners-with-deloitte-and-control-risks-to-launch-relativityone-in-south-africa/)).

**What it is genuinely good at.** In-country hosting for legal review. RelativityOne's technical overview lists a "South Africa (North)" region, short code zano, with Azure South Africa North and West endpoints ([Relativity technical overview](https://help.relativity.com/RelativityOne/Content/Getting_Started/RelativityOne_technical_overview.htm)).

**Honest limitations.** The region is not new. Relativity's own 2023 blog celebrated "Relativity's recent data centre launch of RelativityOne in South Africa" ([Relativity blog](https://www.relativity.com/blog/understanding-south-africas-e-discovery-landscape-and-celebrating-the-global-relativity-community/)). This week's news is the partnership. No pricing is published; this is enterprise software sold through partners.

**South African use cases.**
- A law firm handling a large commercial dispute keeps disclosure review in-country.
- A company responding to a regulator or forensic investigation uses Deloitte or Control Risks as the service provider.
- A compliance officer uses it as a benchmark question for other vendors: where exactly is my data hosted.

**Industries:** legal, forensic, compliance, corporate investigations.

**Pricing:** Not stated.

**SA access notes:** South African region documented. Access through partners.

**Link:** https://www.relativity.com/news-events/press-release-relativity-partners-with-deloitte-and-control-risks-to-launch-relativityone-in-south-africa/

---

## 10. Claude plugin directory portal - a route to market for South African builders

**Hook:** Developers on paid Claude plans can now submit plugins and MCP connectors to the Claude directory and track them through review.

**What it actually is.** Announced 25 September. Plugins "package MCP connectors, Agent Skills, or both" and are now "the main way to build third-party extensions for Claude". You can submit a single remote MCP server or a GitHub-hosted bundle; submissions are auto-validated and safety-scanned, and approved plugins get usage analytics ([Claude blog](https://claude.com/blog/build-plugins-for-claude)).

**What it is genuinely good at.** Distribution. A South African SaaS with an API can now put a connector in front of Claude users without a partnership deal.

**Honest limitations.** Paid Claude plan required to submit ([Claude blog](https://claude.com/blog/build-plugins-for-claude)). Listing does not mean users; review times are not published.

**South African use cases.**
- A local accounting or payroll SaaS ships a connector so Claude can read a client's figures with permission.
- A logistics platform exposes shipment tracking as an MCP connector.
- An agency packages its client-onboarding skills as a plugin.

**Industries:** SaaS building, agencies, fintech.

**Pricing:** Portal included with paid Claude plans.

**SA access notes:** No country limits stated.

**Link:** https://claude.com/blog/build-plugins-for-claude

---

## The structural story: a price war you can actually use

Put the four frontier releases side by side, per million tokens in and out: Grok 4.7 at $2 and $6 ([xAI](https://x.ai/news/grok-4-7)), GPT-6 Sol at $2 and $10, GPT-6 Luna at $0.10 and $0.50 ([OpenAI](https://openai.com/index/introducing-gpt-6-sol-and-luna/)), and Claude Opus 5.5 at $4 and $20 ([Claude Platform release notes](https://docs.anthropic.com/en/release-notes/api)). Every one of them either held or cut price. Grok 4.7 is served "at the same price and speed as Grok 4.6" ([xAI](https://x.ai/news/grok-4-7)); OpenAI halved; Anthropic cut 20 percent and took 60 percent off cache reads.

For a South African business paying in dollars, this matters more than any single feature. When the rand weakens - it moved from R16.25 to R16.43 in a week - a price cut on the dollar side absorbs it. The practical move is to price your AI features on the cheapest model that passes your own test set, not on the brand you started with, and re-check every quarter.

The other structural signal is language. On 21 September the Gates Foundation convened 60 organisations, including Anthropic, Google and the OpenAI Foundation, to make AI "more accessible in underrepresented languages", aiming to reach more than 3 billion people over five years ([ABC News](https://abcnews.com/Technology/wireStory/gates-foundation-launches-coalition-build-representative-language-data-136622214)). Cassava Technologies and South Africa's Lelapa AI are among the named members ([Billionaires.Africa](https://www.billionaires.africa/2026/09/25/zimbabwean-billionaire-strive-masiyiwa-joins-amazon-and-google-in-an-african-languages-ai-pact/)). Two days later Google shipped a speech model listing six South African languages, and Old Mutual shipped a WhatsApp assistant in all of them. That is not coincidence of intent, even if it is coincidence of timing.

---

## Eight weeks: the two zeros move, a little

**POPIA: one reference, after seven weeks of none.** Relativity's press release names South Africa's Protection of Personal Information Act ([Relativity](https://www.relativity.com/news-events/press-release-relativity-partners-with-deloitte-and-control-risks-to-launch-relativityone-in-south-africa/)). It is a press-release sentence, not a compliance document, but it is the first time in this series a vendor has written the law's name in launch material. Every other tool this week stayed silent on it.

**African data residency: one documented region, and it is old.** RelativityOne's South Africa (North) region is documented in its technical overview ([Relativity technical overview](https://help.relativity.com/RelativityOne/Content/Getting_Started/RelativityOne_technical_overview.htm)) and dates back to at least 2023 ([Relativity blog](https://www.relativity.com/blog/understanding-south-africas-e-discovery-landscape-and-celebrating-the-global-relativity-community/)). None of the week's new AI releases - OpenAI, Anthropic, Google, Microsoft, Amazon, Hemory, Financial Cents - announced an African hosting region.

---

## What did not launch this week

**A correction on Lelapa AI.** Last week this piece said Vulavula's release notes had nothing between 14 and 21 September. They now show `vulavula.minor-2026.09.16-1`, a fix for Live API sessions that "could incorrectly fail with HTTP 429" ([Lelapa release notes](https://docs.lelapa.ai/overview/release-notes)). Either it was posted after we checked or we missed it; either way, last week's line was wrong. It is a bug fix, not the text-to-speech launch the CEO previewed, and it is outside this week's window.

**Earlier than it looked.** Base44's AI phone calls got TechRadar coverage on 22 September, but TechRadar says the feature "launched earlier this month" ([TechRadar](https://www.techradar.com/pro/hi-its-ai-speaking-base44-just-launched-ai-that-can-handle-phone-calls)); the in-window changelog entries are follow-ups ([Base44 changelog](https://docs.base44.com/changelog/product)). Reinventing.AI's eight MIT-licensed "AI Employees" were released 19 September ([Beacon Journal](https://www.beaconjournal.com/press-release/story/237049/reinventing-ai-releases-eight-open-source-ai-employees-on-github-under-mit-license/)). TypeSafe AI's Jev decision model was covered on 19 September ([MarkTechPost](https://www.marktechpost.com/2026/09/19/typesafe-ai-releases-jev/)). Solid's 23 September Product Hunt appearance is its second launch there ([The Dollar Craft](https://www.thedollarcraft.com/2026/09/solid-ai-agents.html)).

**Not for us yet.** Google's "Call for Me", where Gemini phones businesses for you, rolls out first to Pixel 11 owners with a paid Gemini subscription in the US ([TechCrunch](https://techcrunch.com/2026/09/24/google-tests-letting-gemini-make-phone-calls-initially-for-us-pixel-owners/)).

---

## What I would actually try this week

**First pick: Gemini 3.8 Flash TTS.** It is the first voice model in this series that publishes our languages, and at about R0.22 a minute the test costs almost nothing ([Gemini API docs](https://ai.google.dev/gemini-api/docs/models/gemini-3.8-flash-tts), [Gemini pricing](https://ai.google.dev/gemini-api/docs/pricing)). Write one 30-second script in isiZulu, isiXhosa and Afrikaans, generate it, and play it to a first-language speaker. Their reaction is the only benchmark that matters. Use a paid billing account for anything real, because the free tier's data is used to improve Google's products.

**Second pick: GPT-6 Luna.** At $0.10 in and $0.50 out, run your highest-volume automation through it for a week and compare quality and cost against what you use now ([OpenAI](https://openai.com/index/introducing-gpt-6-sol-and-luna/)).

**And one action item that is not a purchase.** If you pay for Microsoft 365 on an annual term billed monthly through a reseller, ask them today whether the 5 percent uplift from 1 October applies to you, and before 2 November ask them to set a spending cap on any new Copilot Business licence ([Bechtle](https://www.bechtle.com/gb/news/bechtle-blog-uk/software-updates/microsoft-news-september-2026)).

---

Compiled 28 September 2026. Window: 21 to 28 September 2026. Rand conversions at R16.43 to the dollar, the midpoint of a three-source cluster with a 0.25 percent spread. Two of the usual five sources did not return a readable rate this week, so the cluster is thinner than usual.
