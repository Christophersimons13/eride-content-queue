# AI Tools Drop - Week of 21 September 2026

Ten launches from 14 to 21 September, read from a Johannesburg desk. Rand figures use R16.25 to the dollar, the midpoint of a five-source cluster on Monday morning ([XE](https://www.xe.com/currencyconverter/convert/?Amount=1&From=USD&To=ZAR), [Trading Economics](https://tradingeconomics.com/south-africa/currency), [Forbes Advisor](https://www.forbes.com/advisor/money-transfer/currency-converter/usd-zar/)).

---

## This week in one paragraph

Three things happened that matter to a South African business. First, a payments platform launched that actually lists South Africa as a supported merchant country with local bank transfer, which is rarer than it should be: Creem 2.0, out of Estonia on 17 September ([Creem supported countries](https://docs.creem.io/merchant-of-record/supported-countries)). Second, and this is the story of the week, Bolt.new launched Forge on 14 September as an explicit trade - you get frontier-grade app building, they get your code to train open models - and StackBlitz quietly updated its privacy policy the same day to create a brand-new, opt-out model-training and dataset-licensing right that carves out only the EEA, the UK and Switzerland ([StackBlitz privacy policy](https://stackblitz.com/privacy-policy)). South Africa is not in that carve-out. That regime goes live on 29 September, eight days from now. Third, after six weeks of reporting zero South African AI product launches, the streak broke: 22 On Sloane launched KUMii in Cape Town at the GEC+Africa Summit ([TechCabal, 16 September](https://techcabal.com/2026/09/16/22-on-sloane-launches-kumii/)). The rest of the week was developer tooling and Mac utilities, with an unusually high number of Product Hunt relaunches dressed as launches - five of them, the most this series has caught in one week.

Two counts stay where they have been for seven weeks running. No AI vendor published POPIA compliance material dated in this window. And no tool on this shortlist offers African data hosting - Appwrite's region list is Frankfurt, New York, Sydney, San Francisco, Singapore and Toronto, with nothing on the continent ([Appwrite regions](https://appwrite.io/docs/products/network/regions)). Self-hosting remains the only route to South African data residency, and it is a route you build yourself.

---

## 1. Creem 2.0 - the payments platform that names South Africa

**Hook:** A merchant of record that lists South Africa among 86 supported merchant countries, with local bank transfer, at a flat 3.9 percent.

**What it actually is.** Creem becomes the legal seller on each of your sales. It collects and remits VAT and sales tax in the buyer's country, issues the invoice, absorbs fraud and chargeback handling, and pays you out net. Version 2.0, launched 17 September, adds checkout on your own domain, usage-based billing with a configurable free allowance and a spend cap per meter, revenue splits for affiliates, free short links, and an API built for agents to call ([Creem 2.0 announcement](https://www.creem.io/blog/introducing-creem-2-0)). The company is based in Tallinn, Estonia, founded by Gabriel Ferraz and Alec Erasmus ([Creem about page](https://www.creem.io/about)), and announced 7 million euro in total funding alongside the launch ([@creem_io](https://x.com/creem_io/status/2100479871466020889)).

**What it is genuinely good at.** Removing the single hardest problem in selling software from South Africa, which is not building the product - it is being the tax-compliant seller of record to a customer in Germany or California. Creem's rate is flat: 3.9 percent plus 40 US cents per successful transaction, no monthly fee, no setup fee, no volume minimum ([Creem pricing](https://www.creem.io/pricing)). On a R1,000 sale that is roughly R46 total. The usage-based billing with a hard spend cap is the feature most SaaS founders end up building badly themselves.

**Honest limitations.** Payouts cost 7 euro or dollars, or 1 percent of the payout, whichever is higher, and run only on the 1st and 15th with a 50 dollar minimum balance ([Creem payouts doc](https://docs.creem.io/merchant-of-record/finance/payouts)). On a small month that payout fee is a real percentage. The bigger gap is paperwork: Creem's privacy notice names no hosting region at all, makes no statement either way about training on customer data, and publishes no named subprocessor list ([Creem privacy notice](https://www.creem.io/privacy)). Both `creem.io/security` and `creem.io/legal/dpa` return 404 ([security](https://www.creem.io/security), [DPA](https://www.creem.io/legal/dpa)). For a company handling your revenue, a missing DPA page is not a small thing - you will have to request one directly.

**South African use cases.**
- A Johannesburg SaaS selling to European customers stops guessing at EU VAT and lets Creem be the seller of record, with payouts landing by local bank transfer.
- A beauty or wellness platform selling subscription packages internationally uses the usage cap so a runaway API bill cannot outrun the plan price.
- An agency reselling a tool under its own brand uses custom-domain checkout plus revenue splits to pay a referring partner automatically.

**Industries:** SaaS building, agency and creative work, professional services, any product with cross-border customers.

**Pricing:** 3.9 percent plus $0.40 (about R6.50) per transaction, no monthly fee. Payout fee $7 or 1 percent, whichever is higher, roughly R114 minimum. Partner plan is custom-priced ([Creem pricing](https://www.creem.io/pricing)).

**SA access notes:** South Africa is explicitly on the supported merchant list with local bank transfer available, and Creem sells to customers in 190-plus countries ([supported countries](https://docs.creem.io/merchant-of-record/supported-countries), [creem.io](https://www.creem.io/)). No language list is published, and no South African language is mentioned.

**Link:** https://www.creem.io/

---

## 2. n8n 2.40 - the automation release with a 50 percent SMB discount

**Hook:** The self-hosted automation workhorse ships a new major line, and the start-up discount is the most under-used thing on its pricing page.

**What it actually is.** n8n 2.40 landed 15 September per the vendor's own changelog, with patches 2.40.1, 2.40.2 and 2.40.3 following on the 16th, 17th and 18th ([n8n release notes](https://docs.n8n.io/changelog/release-notes), [GitHub releases](https://github.com/n8n-io/n8n/releases)). The 2.40 line brings MCP toolkit execution to queue-mode workers and adds Confluence as a native agent tool, with the Force Tool Call on First Iteration option shipping off by default ([Pondero](https://pondero.ai/news/2026-09-18-n8n-mcp-oauth-session-fixes/)). Earlier lines - 2.37, 2.38 and 2.39 - were covered in previous episodes.

**What it is genuinely good at.** Being the automation layer you can host in Johannesburg. MCP execution on queue-mode workers matters if you are running agent workflows at any volume, because it means the tool calls no longer bottleneck on the main process.

**Honest limitations.** 2.40.x is still tagged pre-release on GitHub while 2.39.8 remains the stable tag ([GitHub releases](https://github.com/n8n-io/n8n/releases)). Do not put 2.40 on anything a client depends on this week. There is also no free cloud tier - the pricing page's answer to free is that a standard self-hosted build is on GitHub ([n8n pricing](https://n8n.io/pricing)). And n8n publishes no hosting region, no training statement and no subprocessor list on the pages I could read.

**South African use cases.**
- An immigration consultancy self-hosts n8n on a local VPS so client document workflows never leave the country, which is the closest thing to POPIA-comfortable automation available right now.
- A logistics operator wires delivery-status webhooks into WhatsApp notifications without a monthly per-task platform fee.
- A professional services firm with under 20 staff applies for the start-up plan and runs the Business tier at half price.

**Industries:** Every one of them. This is infrastructure.

**Pricing (in euro - do not convert at the dollar rate):** Starter 20 euro per month billed annually, Pro 50 euro, Business 667 euro self-hosted, Enterprise on request ([n8n pricing](https://n8n.io/pricing)).

**The offer worth acting on:** companies with under 20 employees can qualify for 50 percent off the Business plan. No expiry is stated ([n8n pricing](https://n8n.io/pricing)). That takes 667 euro to about 334 euro, roughly R6,400 a month, for SSO, Git version control and environments. Most South African SMBs reading this qualify on headcount and have never applied.

**SA access notes:** No country restrictions stated. Self-hosting means you choose the hosting country, which is the only African-residency answer on this list.

**Link:** https://n8n.io/pricing - releases at https://github.com/n8n-io/n8n/releases

---

## 3. Bolt Forge - a very good deal, and you should read what it costs

**Hook:** Fifty times the usage at no extra charge until 14 October. The payment is your code.

**What it actually is.** Forge is a new agent mode inside Bolt.new, launched 14 September, running on open-weight models - GLM 5.3 Flash and GLM 5.3, with Kimi K3 and DeepSeek v4 Pro experimental - on Bolt's own reserved hardware, with projects running in the browser on WebContainers ([Bolt blog](https://bolt.new/blog/what-is-bolt-forge)). It is a research preview running 14 September to 14 October 2026, confirmed in a dated press release ([Businesswire, 14 September](https://www.businesswire.com/news/home/20260914296571/en/Bolt.new-Launches-Forge-to-Widen-Who-Gets-to-Build-with-AI-and-to-Train-Open-Models-on-What-They-Make)). Bolt.new is built by StackBlitz, Inc. in San Francisco, with training partner Arcee AI ([StackBlitz privacy policy](https://stackblitz.com/privacy-policy)).

**What it is genuinely good at.** The economics. Pro is 25 dollars a month billed yearly, about R406, and during the preview it includes up to 50 times the Forge usage at no extra cost with no access code needed ([Bolt blog](https://bolt.new/blog/what-is-bolt-forge)). There is one monthly usage bar, no daily cap, and at 100 percent it falls back to Standard rather than billing you overage. For a founder prototyping several products, that is the best build-volume-per-rand on this list by a wide margin.

**The trade, in the vendor's own words.** Forge training is opt-in: "Training in Forge is opt-in," and the trade is that "builders who switch into Forge opt in to share de-identified build sessions." What gets shared is "your prompts, your code, your project files and configuration, the tool calls Bolt makes, and your edit histories, including the fix traces Bolt creates" ([Bolt blog](https://bolt.new/blog/what-is-bolt-forge)). That is a clear, honest deal and it is stated plainly.

**The part that is not in the marketing, and the reason this leads the episode.** StackBlitz updated its privacy policy on 14 September to create a separate right that is opt-OUT, not opt-in: "Unless you opt out and subject to the regional and consent rules below, we may use Bolt Model Development Content... to train, fine-tune, evaluate, benchmark, and improve artificial-intelligence models developed by or for StackBlitz." And separately: "unless you opt out... we may prepare datasets derived from Bolt Model Development Content... and license them, including for compensation, to third parties such as AI developers and researchers." Eligibility is date-fenced - only content created on or after 14 September 2026 qualifies - and the policy says no such use will happen before 29 September 2026. The regional carve-out reads: "No opt-out is needed for accounts located in the European Economic Area, the United Kingdom, or Switzerland" ([StackBlitz privacy policy](https://stackblitz.com/privacy-policy)).

South Africa is not in that list. A Johannesburg account sits in the opt-out regime by default. The opt-out is free, available on any plan, through account settings or privacy@stackblitz.com ([StackBlitz privacy policy](https://stackblitz.com/privacy-policy)). If you use Bolt.new and your code is client work, do that before 29 September.

**Honest limitations.** Beyond the above: Teams and Enterprise workspaces are excluded from Forge and from the data collection entirely ([Businesswire](https://www.businesswire.com/news/home/20260914296571/en/Bolt.new-Launches-Forge-to-Widen-Who-Gets-to-Build-with-AI-and-to-Train-Open-Models-on-What-They-Make)), so if you need the protection the answer is a paid workspace tier. The policy names no data-centre region, and refers to "trusted subprocessors" and "third-party inference providers" without naming them on the page. And `bolt.new/privacy`, `bolt.new/legal/privacy` and `support.bolt.new/privacy` all return errors - the governing policy is only reachable at stackblitz.com ([bolt.new/privacy](https://bolt.new/privacy)).

**South African use cases.**
- A solo founder prototypes three product ideas in a month on Pro while the 50X allowance runs, on throwaway code they do not mind contributing.
- An agency keeps client work off Forge entirely and opts out of model development, then uses Standard mode for billable builds.
- A team lead moves the company to a Teams workspace specifically to get the blanket Forge exclusion.

**Industries:** SaaS building, agency and creative work, anyone prototyping.

**Pricing:** Free $0, Pro $25 per month (about R406), Teams $30 per member per month (about R488), Enterprise custom, up to 28 percent off yearly ([Bolt pricing](https://bolt.new/pricing)). Bolt Lite at $9 per month, about R146, with codes released in waves from around 21 September ([Bolt blog](https://bolt.new/blog/what-is-bolt-forge)). Free tier gives 300,000 tokens daily and 1 million monthly, Bolt branding on sites, 10MB uploads, hosting and unlimited databases ([Bolt pricing](https://bolt.new/pricing)).

**SA access notes:** No country restrictions stated. The relevant restriction is legal, not technical, and it is the carve-out above.

**Link:** https://bolt.new/blog/what-is-bolt-forge

---

## 4. Higgsfield API - fifty generative models, one bill, and a training clause

**Hook:** Pay-per-second generative video and image via one API, with a discount you have to lock in inside seven days.

**What it actually is.** A single pay-per-use API fronting more than 50 generative image and video models - Seedance 2.5, Kling 3.0, Higgsfield's own Genjutsu motion transfer, Marketing Studio Image, Cinema Studio 4.0 - with no subscription, served from open.higgsfield.ai. The vendor announced it on 16 September ([@higgsfield](https://x.com/higgsfield/status/2100305266688610746), [Higgsfield API page](https://higgsfield.ai/api)). Higgsfield Inc. is in San Francisco, with a stated location in Kazakhstan ([Higgsfield privacy policy](https://higgsfield.ai/privacy-policy)).

**What it is genuinely good at.** Removing subscription risk from video production. If you produce campaign video in bursts - which most South African agencies do, because client budgets arrive in bursts - per-second billing beats a monthly seat you pay for in quiet months.

**Honest limitations.** Start with the pricing page, which exists and shows no amounts at all - every field is empty ([Higgsfield pricing](https://higgsfield.ai/pricing)). The real rates only appear on the API page, and they carry no currency label: from 0.144 per second for Seedance 2.5, from 0.159 per second for Genjutsu motion transfer, from 0.042 per second for Kling 3.0, from 0.0121 per image for Marketing Studio Image, from 0.2057 per second for Cinema Studio 4.0 ([Higgsfield API page](https://higgsfield.ai/api)). A third-party summary reads those as US dollars, but the vendor does not say so on its own page. Then the training clause, which agencies need to read: the policy reserves the right to use "your user-shared multimedia data, query and prompt data, and Inputs and Outputs... to train and improve our (and our affiliates') AI models and algorithms" ([Higgsfield privacy policy](https://higgsfield.ai/privacy-policy)). No default is stated, no toggle is described, and the only route offered is deletion - with the caveat that "Content already incorporated into our AI models before deletion cannot feasibly be removed." If you are generating a client's brand assets, that clause is a conversation you need to have with the client first.

**South African use cases.**
- An agency prices a campaign video per second of render rather than absorbing a monthly subscription between briefs.
- A retailer generates seasonal product stills at roughly 1.2 US cents each, about 20 South African cents, for catalogue and paid social.
- A wellness brand uses motion transfer to animate a single studio still into short-form vertical content, on non-confidential creative only.

**Industries:** Agency and creative work, retail and e-commerce, marketing.

**Pricing:** Per-unit rates above, currency unlabelled on the vendor page. Assume dollars and budget accordingly. No free tier is stated on the pricing page or homepage ([Higgsfield pricing](https://higgsfield.ai/pricing)).

**The offer, with a caveat:** the vendor says "Get up to 50% OFF discount on your 3 favorite models" and "Lock in your max-discount within 7 days" ([@higgsfield](https://x.com/higgsfield/status/2100305266688610746)). Seven days from 16 September lands on or about 23 September - that date is inferred from the vendor's wording, not quoted by them. A third-party write-up mentions 15 dollars in free credits, which I could not confirm on any Higgsfield page.

**SA access notes:** No country restrictions stated. One capability appears US-fenced per a launch thread - Seedance 2.5 with face inputs. Note that `higgsfield.ai/privacy` and `higgsfield.ai/terms` both error; the working path is `/privacy-policy`.

**Link:** https://higgsfield.ai/api

---

## 5. VoiceCap - the best data posture of the week, and it cannot hear your languages

**Hook:** A meeting notetaker with EU hosting, a named subprocessor list, an explicit no-training promise, 300 free minutes and no card. It just does not do a single South African language.

**What it actually is.** VoiceCap records, transcribes and summarises meetings, writing the summary, decisions and action items in the language the meeting was spoken in. It sends bots into Google Meet, Zoom, Teams and Webex, auto-records from Google and Outlook calendars, and exposes an MCP interface so Claude or ChatGPT can query your meeting history ([voicecap.ai](https://voicecap.ai/)). It is built by Idea Link, an EU company, with reporting placing it in Vilnius, Lithuania ([ChatGate](https://chatgate.ai/post/voicecap)). Dated 14 September on a Lithuanian news rail ([Unicorns Lithuania](https://unicorns.lt/en/news/eimin-lithuania-wins-65-million-eu-tender-countrys-first-artificial-intelligence-centre)), with a Product Hunt appearance on 19 September ([PH board](https://www.producthunt.com/leaderboard/daily/2026/9/19)). Worth stating plainly: the vendor's own site carries no dated announcement, so the date rests on a dated third-party rail plus a dated board, not a press release.

**What it is genuinely good at.** Paperwork you can show a client. Data is stored in EU data centres, reported as Frankfurt ([voicecap.ai](https://voicecap.ai/), [Product Hunt](https://www.producthunt.com/products/voicecap)). The training claim is unambiguous: "No training on your data" and "Your audio and transcripts are never used to train AI models" ([voicecap.ai](https://voicecap.ai/)). And it publishes a full named subprocessor list - Google Cloud EMEA Ireland, OpenAI, Groq, Eleven Labs, Recall.ai, AssemblyAI, AWS, Neon, Vercel, Stripe Payments Europe, Microsoft, Meta and LinkedIn, with non-EU transfers under Standard Contractual Clauses ([VoiceCap privacy policy](https://voicecap.ai/privacy)). That is the best disclosure on this shortlist and one of the best the series has seen. The billing model is also unusually fair: you pay per person who records, and viewers are free however many you invite.

**Honest limitations.** The language story does not hold up. The site claims "100-plus languages, detected automatically" and publishes no list ([VoiceCap pricing](https://voicecap.ai/pricing)), while the App Store listing says "over 30 languages" and boasts specifically about "Baltic, Scandinavian and the smaller European languages most global apps ignore" ([App Store](https://apps.apple.com/ca/app/voicecap-ai-meeting-recorder/id6791075444)). Those two numbers cannot both be right. No South African language - Zulu, Xhosa, Afrikaans, Sesotho, Setswana, isiNdebele, Sepedi, Xitsonga, Tshivenda or siSwati - is named anywhere I could read, and `voicecap.ai/languages` returns an error. There is also a small gap between marketing and paperwork: the no-training promise lives on the website and is not restated in the privacy policy, which is silent on training. Free-tier minutes are 300 total, not monthly.

**South African use cases.**
- A professional services firm records client calls conducted in English with EU hosting and a signed no-training claim it can put in front of a compliance officer.
- An immigration consultancy tests it on 300 free minutes with no card, specifically to check whether South African English accents transcribe cleanly before paying.
- A SaaS team invites the whole company as free viewers and pays for only the two people who actually run the recordings.

**Industries:** Professional services, immigration services, SaaS, any meeting-heavy business operating in English.

**Pricing (in euro - do not convert at the dollar rate):** Free 0 euro forever with 300 minutes total, 1 capture seat and unlimited free viewers. Pro 29 euro plus VAT per capture seat per month for 1,000 minutes. Business 49 euro plus VAT per capture seat for unlimited recording ([VoiceCap pricing](https://voicecap.ai/pricing)).

**SA access notes:** No country restrictions. No card needed for the free tier, which is the friction that usually stops South African trials. Billing is in euro plus VAT.

**Link:** https://voicecap.ai/

---

## 6. tiun - Swiss payments and auth in one command, with an empty subprocessor list

**Hook:** Auth, checkout, billing and merchant-of-record payouts in one install. It just will not tell you whether South Africa is supported.

**What it actually is.** tiun bundles authentication, checkout, payments, a customer database, a self-serve customer portal, automated invoicing and analytics into one system installable with a single command, with SDK and MCP integration. tiun acts as merchant of record and pays out monthly ([tiun.io](https://tiun.io/), [why tiun](https://tiun.io/why-tiun)). It appeared at number one on the 15 September Product Hunt board ([PH board](https://www.producthunt.com/leaderboard/daily/2026/9/15)). Important caveat: the company dates to 2023, founded in Zurich by Sandro Zweig and Christian Heiduschke out of ETH ([Swiss Startup Association](https://swissstartupassociation.ch/2023/10/27/meet-sandro-zweig-co-founder-and-ceo-at-tiun/)), and there is no dated vendor press release for 15 September. This is a Product Hunt debut of an existing platform, not a first release.

**What it is genuinely good at.** Collapsing four vendors into one. If you are starting a SaaS this month, the auth-plus-billing-plus-invoicing stack is usually three integrations and a week of work. The rates are also slightly better than Creem's on the transaction line.

**Honest limitations.** The one that matters for this audience: tiun publishes no supported-country list. The site says "a checkout that works in every country we support" and "We sell on your behalf worldwide" without naming the countries ([why tiun](https://tiun.io/why-tiun)), so whether a South African merchant can onboard could not be verified. Creem publishes its list; tiun does not. There is also a gap between marketing and policy - "tiun is hosted in Europe and GDPR compliant by default" on the site, versus the policy's "You must anticipate your data to be transmitted to any country in Europe and the USA" and recipients "located in any country worldwide" ([tiun privacy policy](https://tiun.io/privacy-policy)). And the policy's subprocessor section says "We currently use offers from the following service providers:" and then lists nothing at all. No training statement exists either way. The payout minimum is 200 dollars against Creem's 50.

**South African use cases.**
- A founder launching a new SaaS this quarter uses one install for auth and billing instead of wiring Supabase auth to Stripe to an invoicing tool.
- A fintech-adjacent product tests the free plan's per-transaction economics against Creem's before committing either way.
- Any South African founder emails tiun first to confirm merchant onboarding is available here, because the site does not say.

**Industries:** SaaS building, fintech-adjacent products, professional services selling online.

**Pricing (dollar amounts shown, currency never named on the page):** Free plan with 2.9 percent plus $0.30 per transaction, 0.5 percent on subscription payments, 1.5 percent on payouts, $15 per dispute, monthly payouts with a $200 minimum, 1 workspace, unlimited seats. Enterprise on request. AI-native analytics add-on $17 per month, about R276 ([tiun pricing](https://tiun.io/pricing)).

**SA access notes:** Unverified, as above. Note `tiun.io/privacy` errors; the policy is at `/privacy-policy`.

**Link:** https://tiun.io/

---

## 7. Appwrite 2.1 and 2.2 - S3-compatible storage lands on self-hosted

**Hook:** The open-source backend brings its S3 API to self-hosted instances, which is the practical path to South African data residency.

**What it actually is.** Appwrite is an open-source backend covering auth, five database types including a vector store, S3-compatible storage at `/v1/s3`, an OAuth 2.1 server, an embeddings API and functions and site hosting. The 2.1 post is dated 14 September in the vendor's blog index and brings the S3 API and AutoGravity to self-hosted instances plus TikTok and Kakao sign-in, with the 2.2.0 tag following on 15 September ([Appwrite blog](https://appwrite.io/blog/categories/products), [GitHub releases](https://github.com/appwrite/appwrite/releases), [changelog](https://appwrite.io/changelog)).

**Worth being precise about.** Product Hunt carried "Appwrite 2.0" on 16 September, but that announcement is dated 31 August - outside this window. The in-window, vendor-dated items are the 2.1 self-hosted post and the 2.2.0 tag. This is one of five relaunches caught this week.

**What it is genuinely good at.** Being a backend you can run on a South African server with an S3-compatible storage API, which means your existing S3 tooling works against data that never leaves the country. Nothing else on this list gets closer to a residency answer.

**Honest limitations.** Appwrite Cloud has no African region - the list is Frankfurt, New York, Sydney, San Francisco, Singapore and Toronto, with Bangalore, Amsterdam and London coming ([Appwrite regions](https://appwrite.io/docs/products/network/regions)). So the residency answer is self-hosting and the operational burden that comes with it. The pricing page states no free-tier limits at all. No statement exists anywhere about training on customer data. Payments are card-only - "Appwrite currently supports credit and debit card payments" - which matters if you are on a local business card with international-transaction limits. And `appwrite.io/blog/post/introducing-appwrite-2-1` errors, so the 2.1 announcement is only reachable via the index.

**South African use cases.**
- A health or wellness product self-hosts Appwrite locally so patient-adjacent records stay in South Africa, with S3-compatible storage for uploaded documents.
- An immigration consultancy runs the vector database on its own server for document search without sending client files to a US API.
- A logistics platform uses the functions layer for webhook processing instead of paying per-invocation elsewhere.

**Industries:** Health-adjacent products, immigration services, fintech, any business with data it should not export.

**Pricing (USD, cloud):** Serverless database compute at $0 fixed fee with plan quota then overage. Dedicated from $10 per month per database with $10 of compute credits included monthly. Tiers run Micro $10, Small $15, Medium $60, Large $110, XL $210, 2XL $410, 4XL $960 - roughly R163 to R15,600 a month. HA replicas add 50 percent of base each, point-in-time recovery adds 20 percent ([Appwrite pricing](https://appwrite.io/pricing)).

**SA access notes:** No country restrictions. Card-only payments. Self-hosted is free by licence.

**Link:** https://appwrite.io/changelog

---

## 8. KUMii - the first South African AI launch this series has landed

**Hook:** After six weeks of reporting zero, a South African AI product launched in Cape Town. It also has no published pricing, no privacy policy and a website that will not let a machine read it.

**What it actually is.** KUMii is an AI-powered platform that matches African startups and MSMEs with funders, tenders, mentors, learning resources and business tools. It was launched by 22 On Sloane, the South African startup campus in Bryanston, Johannesburg ([22 On Sloane](https://www.22onsloane.co/registrations-for-gecafrica-2026-are-in-full-swing/)), on the opening day of the GEC+Africa Summit in Cape Town ([TechCabal, 16 September](https://techcabal.com/2026/09/16/22-on-sloane-launches-kumii/)). A South African trade roundup dated 17 September reports more than 4,000 businesses already registered ([Business Tech Africa](https://www.businesstechafrica.co.za/article/breaking-news-today-thursday-17-september-2026)).

**Being honest about the date.** No exact calendar launch date is published by 22 On Sloane. The evidence is two dated third-party articles - TechCabal on 16 September and Business Tech Africa on 17 September - plus a dated event write-up. Not a dated press release. On the series' own standard that is enough to place it in the window, but it is a weaker evidence class than Creem or Bolt.

**What it is genuinely good at.** Matching, at a scale no individual founder can do manually. Tender discovery alone is a real problem for South African SMBs - public and corporate tenders are scattered across dozens of portals, and 4,000 registered businesses in under a week suggests the demand is real.

**Honest limitations.** Nothing is published. No pricing page exists in any source I could find. No hosting region, no training statement, no opt-out, no subprocessor disclosure - there is no privacy policy to read. And both kumii.africa and kumii.co.za refuse automated reading, so the product site could not be checked directly; only the ESD platform at esd.kumii.africa was readable, and it publishes no pricing either ([esd.kumii.africa](https://esd.kumii.africa/)). For a platform that will hold your company financials and funding history in order to match you to funders, that absence of published data handling is the thing to ask about before you upload anything.

**South African use cases.**
- An SMB looking for tenders registers to see whether the matching surfaces opportunities its current manual search misses.
- A founder raising a seed round uses the funder matching as a shortlist generator, then verifies each funder independently.
- A business in an enterprise-supplier-development programme checks whether its corporate partner already runs on the KUMii ESD platform.

**Industries:** All South African SMBs, particularly those chasing public or corporate tenders and enterprise supplier development.

**Pricing:** Not published anywhere. Ask before you register.

**SA access notes:** Built for African startups and MSMEs, so access is the point rather than the obstacle.

**Link:** https://esd.kumii.africa/ - the consumer domain kumii.africa blocks automated reading

---

## 9. Axari Twin - a security vendor with no reachable privacy policy

**Hook:** An AI teammate for security leaders that promises it never trains on your data, published on a site with no working privacy page, no security page and no pricing page.

**What it actually is.** Axari Twin is an AI twin for security and IT professionals that works inside Slack and Microsoft Teams - investigating, gathering context, coordinating, following up and handling routine execution across the security stack until human judgement is needed ([Axari on LinkedIn](https://www.linkedin.com/posts/axari-ai_introducing-axari-twin-your-ai-twin-for-activity-7505644734632136705-Lqep)). The company is in Santa Clara, United States ([Axari LinkedIn](https://www.linkedin.com/company/axari-ai)). It went live 15 September, and I will state the evidence weakness plainly: the LinkedIn post renders a relative timestamp rather than a calendar date, and the launch blog carries no date in its text ([Axari launch blog](https://www.axari.ai/blog/introducing-your-ai-twin-for-security/)). The date rests on a dated Product Hunt board plus a search index date.

**What it is genuinely good at.** The shape of the product is right. Small South African firms do not have a security operations centre; they have one person who also does IT. An agent that triages in Teams and escalates only what needs a human is exactly the gap.

**Honest limitations.** Every piece of paperwork that would let you trust it is missing. `axari.ai/privacy`, `/security`, `/trust` and `/pricing` all return errors, and no alternate path exists for any of them ([privacy](https://www.axari.ai/privacy), [security](https://www.axari.ai/security), [pricing](https://www.axari.ai/pricing)). The marketing claims "Never trained on your data. Your data stays yours" and "Zero data retention where applicable" ([Axari launch blog](https://www.axari.ai/blog/introducing-your-ai-twin-for-security/), [axari.ai](https://www.axari.ai/)) with no policy, DPA or security page behind any of it. Hosting region is not stated. No subprocessor disclosure. No price for any tier could be verified - the Product Hunt page shows only "Free Options" with no amounts. This is a security product asking for access to your security stack. Do not connect it to anything holding regulated South African data on this evidence.

**South African use cases.**
- A firm with one IT person trials it on the free credits in a sandbox workspace with no production connections, purely to judge the triage quality.
- A security lead uses the daily brief output as a template for their own reporting, without granting stack access.
- Any evaluation starts by emailing Axari for a DPA and a hosting-region statement, and stops if neither arrives.

**Industries:** Professional services, fintech, any business with a compliance obligation - with the caveat above applying most strongly to exactly those businesses.

**Pricing:** Could not be verified. No working pricing page exists. Free tier is 50,000 credits free for the first 7 days, with no credit card required ([axari.ai](https://www.axari.ai/)).

**SA access notes:** No restrictions stated, and no card is required, which removes the usual South African trial friction. The obstacle here is not access.

**Link:** https://www.axari.ai/

---

## 10. Ami AI by AiSDR - the priciest thing on the list, with no trial

**Hook:** An outbound sales agent starting at 250 dollars a month, roughly R4,063, with no free trial at all.

**What it actually is.** A go-to-market platform where Ami AI generates campaign ideas and plans, prospects from a native 300-million-plus lead database plus Sales Navigator, writes personalised email and LinkedIn outreach, runs omnichannel sequences, warms mailboxes and domains, syncs two-way with HubSpot and Salesforce, and adds AI call steps ([AiSDR pricing](https://aisdr.com/pricing)). It topped the 18 September Product Hunt board ([PH board](https://www.producthunt.com/leaderboard/daily/2026/9/18)). No dated vendor press release was found - the date rests on the dated board.

**What it is genuinely good at.** Volume outbound for a business selling into the United States or Europe, where the 300-million-record database has real coverage and the mailbox warming meaningfully affects deliverability.

**Honest limitations.** The price, for this market. Solo is 250 dollars a month or 2,400 a year, Explore is 900 a month on a quarterly contract paid in advance, Scale is 2,500 a month ([AiSDR pricing](https://aisdr.com/pricing)). At the entry tier that is about R4,063 monthly, and the page states plainly "We currently don't offer a free trial." Paying R4,000 a month to test an outbound motion you cannot preview is a hard ask for a South African SMB. On paperwork: hosting is not stated, there is no training statement, no opt-out and no subprocessor list - only integration partners are named. Given that this tool will hold your entire prospect list, that silence matters.

**South African use cases.**
- An SA SaaS already selling into the US commits to one quarter on Solo with a defined pipeline target, and cancels on the number.
- A B2B services firm uses the mailbox and domain warming alone, which is the component hardest to replicate cheaply.
- A founder prices this against a part-time local SDR at R4,000 a month and makes an honest comparison rather than assuming the tool wins.

**Industries:** SaaS building, B2B professional services, anyone selling outbound into the northern hemisphere.

**Pricing:** Solo $250 per month or $2,400 per year, about R4,063 monthly. Explore $900 per month or $8,640 per year, quarterly contract, optional managed service at $149 per campaign. Scale $2,500 per month or $24,000 per year, fully managed service at an extra $2,500 per month. Annual is 20 percent cheaper than quarterly ([AiSDR pricing](https://aisdr.com/pricing)). No free trial.

**SA access notes:** No country restrictions stated.

**Link:** https://aisdr.com/pricing

---

## The structural story: eight out of ten

This is worth its own section because it is not an accident. Of the ten tools above, eight have a broken legal, pricing or documentation path, checked this week:

- Bolt.new's `/privacy`, `/legal/privacy` and `support.bolt.new/privacy` all error; the policy lives on stackblitz.com ([bolt.new/privacy](https://bolt.new/privacy)).
- Higgsfield's `/privacy`, `/terms` and `/legal/privacy-policy` all error; the working path is `/privacy-policy` ([higgsfield.ai/privacy](https://higgsfield.ai/privacy)).
- tiun's `/privacy` and `/legal/privacy` error; the policy is at `/privacy-policy` ([tiun.io/privacy](https://tiun.io/privacy)).
- Axari's `/privacy`, `/security`, `/trust` and `/pricing` all error with no alternate ([axari.ai/privacy](https://www.axari.ai/privacy)).
- Creem's `/security` and `/legal/dpa` return 404 ([creem.io/security](https://www.creem.io/security)).
- VoiceCap's `/languages` errors ([voicecap.ai/languages](https://voicecap.ai/languages)).
- Appwrite's 2.1 announcement URL errors ([link](https://appwrite.io/blog/post/introducing-appwrite-2-1)).
- n8n's `docs.n8n.io/release-notes/` does not exist; the working path is `/changelog/release-notes` ([link](https://docs.n8n.io/release-notes/)).

Two pricing pages load with no amounts on them: Higgsfield's ([link](https://higgsfield.ai/pricing)) and Sider's ([link](https://sider.ai/pricing)). Two tools have no pricing page at all - Axari and KUMii.

The practical lesson for anyone doing supplier due diligence from South Africa: if a vendor's `/privacy` returns a 404, try `/privacy-policy` before concluding there is no policy. Three vendors this week hid a real, detailed policy behind a non-standard path. And the reverse holds too - a confident no-training claim in marketing copy is not a policy. VoiceCap makes the claim on its site and does not restate it in the policy. Axari makes it with no policy at all.

---

## Seven weeks, same two zeros

**POPIA: zero, for the seventh consecutive week.** No vendor on this shortlist mentions POPIA anywhere - Creem, tiun, StackBlitz, Higgsfield, VoiceCap and Appwrite all frame compliance around GDPR and EU Standard Contractual Clauses, and Axari publishes nothing. What did appear in the window is regulator activity and commentary, not vendor compliance documents: a 17 September piece noting that "Specific AI legislation is not imminent in 2026, but POPIA already provides a comprehensive framework for regulating wearable AI" ([Polity](https://www.polity.org.za/article/invisible-data-collection-through-a-privacy-lens-2026-09-17)), ITWeb on the Information Regulator unpacking AI complexities on 17 September ([ITWeb](https://www.itweb.co.za/article/inforeg-unpacks-regulatory-complexities-posed-by-ai/KA3WwMdzPryvrydZ)), and Information Regulator chair adv. Pansy Tlakula on the changed data environment on 19 September ([ITWeb](https://www.itweb.co.za/categories/j5alrvQgkY1MpYQk)). The regulator is talking. The vendors are not answering.

**African data residency: zero, for the seventh consecutive week.** Appwrite's regions are confirmed with no African option. VoiceCap is EU and Frankfurt. tiun says Europe and means worldwide. Bolt and Higgsfield are United States. Creem, Axari, KUMii, AiSDR and n8n Cloud do not state a region at all. The only near-miss is BrandAxis listing Cape Town among pinned proxy markets, which is query routing and not data hosting.

**Not a zero this week:** African infrastructure money moved. On 17 September the US International Development Finance Corporation announced an investment in WIOCC, the Johannesburg-headquartered digital infrastructure operator, that "could amount to around R2.5 billion (up to $155 million)", alongside Vision International Investment Company and the Africa Finance Corporation. WIOCC runs subsea cables, fibre and data centres across more than 30 African countries ([EWN, 17 September](https://www.ewn.co.za/2026/09/17/us-govt-agency-pouring-billions-into-african-digital-infrastructure-firm-with-hq-in-joburg)). That is the pipe into which any future African region would be plugged. It is not a product you can use on Monday, but it is the reason the residency answer might change.

---

## What did not launch this week

**Lelapa AI and Vulavula - unresolved for a seventh consecutive episode.** The release notes page was checked again. The newest entry is `vulavula.minor-2026.08.12-1`, dated 12 August 2026, and the entries before it jump back to 2025 ([Lelapa release notes](https://docs.lelapa.ai/overview/release-notes)). Nothing between 14 and 21 September. The Lelapa news that did appear in the window is coverage of an announcement that happened before it - CEO Pelonomi Moiloa told ITWeb TV on 4 September that Vulavula is adding text-to-speech and expanding beyond Africa ([ITWeb, 4 September](https://www.itweb.co.za/article/itweb-tv-lelapa-ai-eyes-faster-ambitious-growth/VgZeyvJlpbXMdjX9)), and ITWeb re-ran it as a video package indexed 19 September covering the 31 August to 5 September news week ([ITWeb video](https://www.itweb.co.za/videos/mYZRX79gb8kqOgA8)). That is exactly the trap this series keeps hitting: an in-window publication date carrying out-of-window news. The most interesting South African language AI still has no dated shipping artefact since 12 August.

**Five relaunches caught, the most in one week so far.** Appwrite 2.0 was announced 31 August and appeared on the 16 September board ([Appwrite blog](https://appwrite.io/blog/categories/products)). OpenAI's Agents API is dated 10 September on OpenAI's own site and turned up on the 15 September board ([OpenAI](https://openai.com/index/introducing-the-agents-api/)). Weave Router 2.0's vendor blog says "Published September 9, 2026" and it took the number one slot on 16 September with 337 upvotes ([Weave blog](https://weaveos.com/blog/introducing-weave-router-2-0)). Naoma AI Demo Agent V2 topped the 14 September board, but Naoma's own blog said V2 was "live for every customer" on 12 July ([Naoma blog](https://naoma.ai/zu/blog?category=fundamentals)). Oats, the on-device notetaker, launched on Product Hunt on 25 July and reappeared on 14 September ([Product Hunt](https://www.producthunt.com/products/oats/launches)). Oats is genuinely good on privacy - "Zero data leaves your device", free and open source ([ariso.ai/oats](https://ariso.ai/oats)) - but it is not new.

**A near-miss on the South African front.** BrandAxis put out a press release dated 15 September announcing that Cape Town entrepreneur Felix Norton had launched an AI-visibility analytics platform ([Beacon Journal](https://www.beaconjournal.com/press-release/story/234151/south-african-aeo-and-geo-expert-felix-norton-launches-brandaxis-to-make-ai-visibility-accessible-to-every-brand/)). An SA trade article announcing the public platform carries a search-index date of 10 June, and the vendor's own about page says "Founded 2025" ([BrandAxis about](https://brandaxis.ai/about/)). So it is a PR push, not a launch. It gets a mention anyway for one reason: it is the only tool found this week priced in rand, and it publishes an unambiguous training answer. Plans run Lite $19 a month at R349, Starter $69 at R1,249, Pro $169 at R2,999, Advanced $349 at R6,299, with a free tier of 5 prompts on ChatGPT only, and the pricing page states "No. Your prompts, brand data, and results are never used for training. We pay full API rates to the model providers." ([BrandAxis pricing](https://brandaxis.ai/pricing/)). A South African vendor publishing rand prices and a plain training answer is doing something the nine international tools above are not.

**Also just outside:** Askya's pan-African AI growth programme, announced 4 September with up to $200,000 and no equity, is out of window - but applications close 30 September, so it is still actionable if you are raising ([TechCabal](https://techcabal.com/2026/09/04/askya-launches-the-askya-ai-growth-platform-a-zero-equity-pan-african-program-with-up-to-200000-investment-for-startups/)). Nigeria's DataSync Africa launched AGROSYNC, a Yoruba conversational voice AI for farmers, with Hausa and Igbo planned ([TechCabal, 15 September](https://techcabal.com/2026/09/15/datasync-africa-launches-agrosync-yoruba-conversational-voice-ai-for-farmers/)) - in window, African, and a reminder that the continent's language AI is being built, just not for our eleven languages yet.

---

## What I would actually try this week

**First pick: Creem 2.0.** It is the only tool on this list that solved a specifically South African problem by naming South Africa. Being the tax-compliant merchant of record for cross-border software sales is the thing that stops South African founders selling internationally, and 3.9 percent plus 40 cents with local bank transfer payouts is a workable number ([Creem pricing](https://www.creem.io/pricing), [supported countries](https://docs.creem.io/merchant-of-record/supported-countries)). Do one thing before you commit: email them for a DPA, because the page that should host it returns a 404.

**Second pick: VoiceCap, on the free tier, as a test.** Three hundred minutes, one seat, no card, EU hosting, a named subprocessor list and an explicit no-training claim ([VoiceCap pricing](https://voicecap.ai/pricing), [privacy policy](https://voicecap.ai/privacy)). Spend the free minutes on one specific question: does it transcribe South African English accents accurately. If the answer is yes, it is the best-documented meeting tool this series has covered. If the answer is no, you have lost nothing and found out for free.

**And one action item that is not a purchase.** If you use Bolt.new and any of your code is client work, open your account settings and opt out of model development and dataset licensing before 29 September 2026. It is free, it works on any plan, and after that date content you create becomes eligible for training and for licensed datasets sold to third parties. European, British and Swiss accounts do not have to do this. South African accounts do ([StackBlitz privacy policy](https://stackblitz.com/privacy-policy)).

---

*Compiled 21 September 2026. Window: 14 to 21 September 2026. Rand conversions at R16.25 to the dollar, the midpoint of a five-source cluster with a 0.13 percent spread - the tightest this series has recorded. Euro prices are left in euro and not converted. Two consumer money-transfer pages, Wise and Revolut, were showing rates around 17.1 on Monday morning, roughly 5 percent off the live cluster - worth knowing before you convert anything.*
