# AI Tools Drop - Week of 23 November 2026

Episode 16. Window: 16 to 23 November 2026. Written for South African founders and small businesses.

Rand figures use **R17.56 to the dollar**, the middle of three rates checked on 22 and 23 November: [XE](https://www.xe.com/currencyconverter/convert/?Amount=1&From=USD&To=ZAR) (17.5578 at 08:25 UTC on 22 November), [Trading Economics](https://tradingeconomics.com/south-africa/currency) (17.4346 on 23 November) and [Pluang](https://pluang.com/en/tools/currency-converter/usd-zar) (17.5826 on 22 November). The rand is weaker than last week's R16.92, so dollar subscriptions cost about 4 percent more this week. That makes this week's rand-priced pick more attractive than usual.

---

## This week in one paragraph

This was a week for small, practical tools rather than big announcements. A Cape Town hosting company, HOSTAFRICA, launched HCode, which puts an app you built by chatting with an AI on a South African server for R50 a month. OpenAI made ChatGPT's dictation type as you speak on every plan, added an accounting plugin that works with Xero and QuickBooks, and started rolling out Space, its page and presentation builder, to Plus users. Canva gave everyone a switch to hide its generative AI, which matters for agencies whose clients ask for human-made work. Bluedot started recording phone calls, Creatify launched an agent that runs paid ads with your approval, and Gemini Notebook can now turn your research into a small interactive website. Google's new Gemini 4 Neon model is for paying Pro and Ultra subscribers ([Google](https://blog.google/innovation-and-ai/models-and-research/gemini-models/introducing-gemini-4-neon/)). Several launches are not available here: free Tasks in Gemini, Zoho Desk's new AI agents and ChatGPT Health all skip South Africa for now.

---

## 1. HCode by HOSTAFRICA - put your AI-built app on a South African server for R50

**What it is.** HCode is app hosting from HOSTAFRICA, launched in Cape Town. You describe an app or a game to an AI assistant such as Claude or ChatGPT, test what it builds, and then type "Publish this app to HCode" in the same chat; HCode publishes it and gives you a link to share ([ITWeb](https://www.itweb.co.za/article/hcode-makes-it-easy-for-anyone-to-build-an-app-with-ai-launch-it-from-the-same-chat/Olx4zMkaJK2v56km)).

**What it is good at.** It removes the step that stops most non-technical founders: getting the thing online. HOSTAFRICA says the platform is built around South African infrastructure, runs apps in South Africa by default and keeps the managed PostgreSQL database in the same place as the app ([HOSTAFRICA](https://hostafrica.co.za/hcode/)). It is billed as "One flat price in Rands", so there is no exchange-rate surprise ([HOSTAFRICA](https://hostafrica.co.za/hcode/)). The Solo plan supports custom domains ([ITWeb](https://www.itweb.co.za/article/hcode-makes-it-easy-for-anyone-to-build-an-app-with-ai-launch-it-from-the-same-chat/Olx4zMkaJK2v56km)).

**Honest limitations.** The ITWeb article is marked "Issued by HOSTAFRICA", so it is the company's own announcement, not an independent review ([ITWeb](https://www.itweb.co.za/article/hcode-makes-it-easy-for-anyone-to-build-an-app-with-ai-launch-it-from-the-same-chat/Olx4zMkaJK2v56km)). HCode is hosting only; you still need an AI tool such as Claude or ChatGPT to build the app, and you connect it through HCode's MCP connector ([ITWeb](https://www.itweb.co.za/article/hcode-makes-it-easy-for-anyone-to-build-an-app-with-ai-launch-it-from-the-same-chat/Olx4zMkaJK2v56km)). Solo gives you 1 GB of memory and one database ([HOSTAFRICA](https://hostafrica.co.za/hcode/)), which is fine for a booking form or an internal tool, not for a busy shop. An app the AI built is not automatically secure: if it stores client details, someone who can read code should check it before real customer data goes in.

**South African use cases.**
- An immigration consultant publishing a simple document checklist tool for clients, with the data stored in South Africa.
- A salon building a small booking or loyalty page on its own domain.
- A logistics business putting an internal delivery log online for its drivers.

**Industries.** SaaS building, immigration services, beauty and wellness, logistics, professional services.

**Pricing.** Rand prices from the HCode page ([HOSTAFRICA](https://hostafrica.co.za/hcode/)):

| Plan | Monthly | Yearly | Projects | Databases | Memory |
|---|---|---|---|---|---|
| Solo | R50 | R550 | 3 | 1 | 1 GB |
| Developer | R200 | R2,200 | 5 | 3 | 4 GB |
| Pro | R499 | R5,499 | 10 | 5 | 8 GB |
| Team | R999 | R10,999 | 20 | 20 | 16 GB |

The international site lists it "From $3/mo" ([HOSTAFRICA](https://www.hostafrica.com/hcode/)). The launch offer gives the first two months free with the code HCODEFREE2026 ([ITWeb](https://www.itweb.co.za/article/hcode-makes-it-easy-for-anyone-to-build-an-app-with-ai-launch-it-from-the-same-chat/Olx4zMkaJK2v56km)).

**Access notes.** Local company, rand billing, no foreign card needed. The AI assistant you build with is billed separately, usually in dollars.

**Disclosure.** The writing pipeline behind this series uses Claude models, and HCode's instructions use Claude as the main example, so weigh my view accordingly.

**Link.** [HOSTAFRICA - HCode](https://hostafrica.co.za/hcode/)

---

## 2. ChatGPT Live Dictation - your words appear as you speak

**What it is.** "With Live Dictation, your speech turns into text as you talk, so you spend less time waiting for your message to finish transcribing" ([OpenAI Help Center](https://help.openai.com/en/articles/6825453-chatgpt-release-notes)).

**What it is good at.** It is quicker than typing for long instructions, and you can see mistakes while you are still talking. OpenAI also says "We've also removed the 10-minute recording limit" ([OpenAI Help Center](https://help.openai.com/en/articles/6825453-chatgpt-release-notes)), so you can talk through a whole client brief in one go.

**Honest limitations.** It is "rolling out gradually, so it may not be available for your account yet" ([OpenAI Help Center](https://help.openai.com/en/articles/6825453-chatgpt-release-notes)). OpenAI does not say how well it handles South African accents or mixing English with isiZulu or Afrikaans in one sentence, so test it with your own voice. Dictating in a shared office or taxi means other people hear your client's details.

**South African use cases.**
- A beauty therapist dictating treatment notes between clients and asking ChatGPT to tidy them.
- A freight forwarder talking through a shipment problem and turning it into a client email.
- A founder recording a 15-minute product idea on a walk, then asking for a one-page summary.

**Industries.** Beauty and wellness, logistics, professional services, SaaS building, all industries.

**Pricing.** No extra cost. "Live Dictation is rolling out globally to all ChatGPT plans on iOS, Android, web, and the desktop app" ([OpenAI Help Center](https://help.openai.com/en/articles/6825453-chatgpt-release-notes)), which includes the free plan.

**Access notes.** Global, so South Africa is included. Update the app if you do not see it.

**Link.** [OpenAI - ChatGPT release notes](https://help.openai.com/en/articles/6825453-chatgpt-release-notes)

---

## 3. ChatGPT Accounting plugin - reconciliations and month-end drafts with Xero

**What it is.** OpenAI calls it "An accounting assistant for work in your software and workbooks, from everyday bookkeeping to reporting and audits" ([OpenAI](https://openai.com/business/plugins/accounting/)). It was added on 18 November ([OpenAI Help Center](https://help.openai.com/en/articles/6825453-chatgpt-release-notes)).

**What it is good at.** OpenAI's examples include reconciling a bank statement against the general ledger and listing unmatched transactions, checking a month-end workbook for broken formulas and duplicate entries, and ranking the largest expense variances against budget ([OpenAI](https://openai.com/business/plugins/accounting/)). Supported apps include Xero, QuickBooks Online, FreshBooks, BILL and Oracle NetSuite ([OpenAI Help Center](https://help.openai.com/en/articles/20001709-using-chatgpt-for-accounting-work)). It prepares drafts for your review rather than posting on its own.

**Honest limitations.** Sage, a common choice for South African businesses, is not on the list of partner apps ([OpenAI Help Center](https://help.openai.com/en/articles/20001709-using-chatgpt-for-accounting-work)). It needs the ChatGPT desktop app and computer use set up ([OpenAI Help Center](https://help.openai.com/en/articles/20001709-using-chatgpt-for-accounting-work)). Xero's expanded ChatGPT integration announced on 19 November is described for US businesses ([Lilach Bullock](https://www.lilachbullock.com/ai-news-this-week-for-small-business-22-november-2026/)), so test what your South African Xero file allows. OpenAI warns that "A connection that lets you read transactions may have different permissions for entering records" ([OpenAI Help Center](https://help.openai.com/en/articles/20001709-using-chatgpt-for-accounting-work)). It does not know SARS rules unless you tell it, and your accountant still signs off.

**South African use cases.**
- A small bookkeeping practice reconciling client bank statements in Xero before month-end.
- A retail store checking its stock and sales workbook for duplicate entries.
- A payments startup comparing actual spend with budget before a board meeting.

**Industries.** Professional services, fintech and payments, retail, agency and creative.

**Pricing.** "The Accounting plugin is free to install. Access to the model, tools, and usage included with your plan can vary" ([OpenAI Help Center](https://help.openai.com/en/articles/20001709-using-chatgpt-for-accounting-work)). It sits in ChatGPT Business and Enterprise workspaces; OpenAI's pricing page did not show me a dollar price for Business, so check it in your account before you upgrade.

**Access notes.** OpenAI's pages do not name any regional restriction ([OpenAI Help Center](https://help.openai.com/en/articles/20001709-using-chatgpt-for-accounting-work)). In Business workspaces members can install it without admin approval; in Enterprise an admin approves it first ([OpenAI Help Center](https://help.openai.com/en/articles/20001709-using-chatgpt-for-accounting-work)). Client financial records are personal information under POPIA, so get your client's consent before you connect their books.

**Link.** [OpenAI - Accounting plugin for ChatGPT](https://openai.com/business/plugins/accounting/)

---

## 4. Canva AI controls - one switch to hide generative AI

**What it is.** Canva launched "a new switch to turn generative AI features on or off, and an option to limit AI-generated content shown in the Canva library" ([Mumbrella](https://mumbrella.com.au/canva-launches-new-ai-controls-for-creative-flexibility-945289)).

**What it is good at.** When the switch is off, generative AI features are hidden across Canva and can be turned back on at any time; it lives under Profile, Settings, Permissions. The second option, under Profile, Your account, AI Personalization, reduces AI-generated content in search results and recommendations without changing your existing designs ([Mumbrella](https://mumbrella.com.au/canva-launches-new-ai-controls-for-creative-flexibility-945289)). Background Remover and Magic Grab stay available with the switch off ([Ad Test Bench](https://adtestbench.com/news/canva-adds-a-switch-that-turns-off-most-of-its-generative-ai/)).

**Honest limitations.** It does not prove a design is human-made; it only hides tools and lowers how often AI content appears. Turning it on and off is per account, so an agency needs every designer to set it. If you rely on Magic tools for speed, turning them off will slow you down.

**South African use cases.**
- A creative agency giving a corporate client written assurance that its campaign used no generative AI imagery.
- A beauty brand keeping its Instagram templates to human-made stock only.
- A training company letting junior staff design without AI suggestions while they learn.

**Industries.** Agency and creative, beauty and wellness, retail, professional services.

**Pricing.** "Both of these features are available to everyone on Canva Free and Canva Pro from today, at no extra cost" ([Mumbrella](https://mumbrella.com.au/canva-launches-new-ai-controls-for-creative-flexibility-945289)).

**Access notes.** Available to everyone on Free and Pro, so South Africa is included.

**Link.** [Mumbrella - Canva launches new AI controls](https://mumbrella.com.au/canva-launches-new-ai-controls-for-creative-flexibility-945289)

---

## 5. Bluedot phone calls - AI notes from the calls you make

**What it is.** Bluedot, a meeting notetaker, "now records phone calls on iOS, Android, and the web, with AI notes automatically synced to your CRM, ATS, or AI assistants" ([Bluedot](https://www.bluedothq.com/blog/bluedot-2-2)).

**What it is good at.** You verify your number, dial from the Bluedot app, talk as usual, and when you hang up the transcript and summary are ready. Calls land in the same library as your online and in-person meetings ([Bluedot](https://www.bluedothq.com/blog/bluedot-2-2)). There is an optional spoken message that tells everyone the call is being recorded ([Bluedot](https://www.bluedothq.com/blog/bluedot-2-2)).

**Honest limitations.** Outgoing calls only, started inside the Bluedot app; calls from your normal dialler are not recorded ([Hackr Life](https://www.hackrlife.com/p/bluedot-phone-calls)). Bluedot does not publish a list of supported countries or say what international calls cost ([Hackr Life](https://www.hackrlife.com/p/bluedot-phone-calls)), so I could not confirm South African numbers work; test before paying for a year. The consent message is "optional and off by default" ([Bluedot](https://www.bluedothq.com/blog/bluedot-2-2)). In South Africa, turn it on and tell the client yourself; recording calls with client details brings in POPIA, and you should get advice if you plan to do it routinely.

**South African use cases.**
- An immigration adviser recording a consultation call, with the client's agreement, so nothing on the checklist is missed.
- A sales rep at a payments company getting call notes straight into the CRM.
- A recruiter keeping notes from phone screens.

**Industries.** Immigration services, fintech and payments, professional services, logistics.

**Pricing.** Phone call recording is "unlimited and available to all paid Bluedot users at no extra cost" ([Bluedot](https://www.bluedothq.com/blog/bluedot-2-2)). Per user per month ([Bluedot](https://www.bluedothq.com/pricing)):

| Plan | Billed yearly | Billed monthly |
|---|---|---|
| Free (no phone calls) | $0 | $0 |
| Basic | $14 (about R246) | $18 (about R316) |
| Pro | $20 (about R351) | $25 (about R439) |
| Business | $32 (about R562) | $39 (about R685) |

**Access notes.** Card payment in dollars. Country support for calling is not published.

**Link.** [Bluedot - Introducing Bluedot 2.2](https://www.bluedothq.com/blog/bluedot-2-2)

---

## 6. Creatify Max - an agent that runs your paid ads, with your approval

**What it is.** Creatify launched Max on 18 November, "an AI teammate for paid ads". It "watches your accounts around the clock, spots what's working, turns winners into creative briefs, makes the videos and sets up campaigns across Meta, Google, TikTok and more" ([Creatify](https://creatify.ai/blog/meet-creatify-max-ai-marketing-agent)).

**What it is good at.** It researches competitors' hooks and offers, makes video and image ads in the right sizes, drafts campaigns from a product link, and runs routines such as daily spend checks and Monday reports. Channels include Meta, Google Ads, TikTok, Snapchat, LinkedIn and Reddit ([Creatify](https://creatify.ai/blog/meet-creatify-max-ai-marketing-agent)). The safety rule is clear: "Nothing touches your account until a person clicks Approve, and the card records who did" ([Creatify](https://creatify.ai/blog/meet-creatify-max-ai-marketing-agent)).

**Honest limitations.** You can let a routine you trust act on its own ([Creatify](https://creatify.ai/blog/meet-creatify-max-ai-marketing-agent)); do not do that with budget changes. The cheapest plan includes one routine, and only Ultra and up can be added to Slack ([Creatify](https://creatify.ai/pricing)). The free plan does not list Max and exports carry a watermark ([Creatify](https://creatify.ai/pricing)). AI actors and accents may not sound South African, so check every ad before it runs.

**South African use cases.**
- An online beauty store testing three video ad hooks on Meta and TikTok before Black Friday.
- An agency getting a Monday performance report for each client brand.
- A retail chain watching competitors' ads in its category.

**Industries.** Agency and creative, retail, beauty and wellness, SaaS building.

**Pricing.** Annual plan prices per month ([Creatify](https://creatify.ai/pricing)):

| Plan | Price | Credits | Max routines |
|---|---|---|---|
| Free | $0 | 10 | Not listed |
| Standard | $10 (about R176) | 55 | 1 |
| Pro | $38 (about R667) | 280 | 3 |
| Ultra | $66 (about R1,159) | 730 | 10 |
| Business | from $136 (about R2,388) | 1,500 and up | Unlimited |

The page says the annual plan saves 30 percent ([Creatify](https://creatify.ai/pricing)). Your ad spend on Meta or Google is billed separately.

**Access notes.** Card payment in dollars. Max works through your own ad accounts, which you can run from South Africa.

**Link.** [Creatify - Meet Creatify Max](https://creatify.ai/blog/meet-creatify-max-ai-marketing-agent)

---

## 7. Gemini Notebook interactive sites - turn your research into a small website

**What it is.** "Starting today, Gemini Notebook can turn your sources into interactive sites to help you quickly make sense of complex information" ([Google](https://blog.google/innovation-and-ai/products/gemini-notebook/interactive-sites/)), posted on 16 November.

**What it is good at.** You type "make me a site" in the Notebook chat and describe what you want. Google's examples are visual explainers such as a timeline, dashboards for exploring data such as quarterly sales, and project trackers with tasks and deadlines. You can open the site in a new tab and share it ([Google](https://blog.google/innovation-and-ai/products/gemini-notebook/interactive-sites/)).

**Honest limitations.** Web only for now; the mobile app is "coming soon" ([Google](https://blog.google/innovation-and-ai/products/gemini-notebook/interactive-sites/)). Google does not state limits on size, usage or sharing ([Google](https://blog.google/innovation-and-ai/products/gemini-notebook/interactive-sites/)). The site is only as accurate as the sources you upload, so check the figures before you share it with a client.

**South African use cases.**
- An immigration practice turning its visa category notes into an interactive explainer for new staff.
- A logistics manager making a simple dashboard from a month of delivery data.
- An agency turning a client's research pack into a clickable project tracker.

**Industries.** Immigration services, logistics, agency and creative, professional services.

**Pricing.** No price is stated ([Google](https://blog.google/innovation-and-ai/products/gemini-notebook/interactive-sites/)).

**Access notes.** "This capability is rolling out globally on the web today for Gemini Notebook users (18+), including Google Workspace subscribers" ([Google](https://blog.google/innovation-and-ai/products/gemini-notebook/interactive-sites/)).

**Link.** [Google - Interactive sites in Gemini Notebook](https://blog.google/innovation-and-ai/products/gemini-notebook/interactive-sites/)

---

## 8. ChatGPT Space - pages and presentations, for Plus users

**What it is.** "Starting today, ChatGPT Space is rolling out globally to Plus users ages 18 and older." In Space you create interactive pages and presentations with ChatGPT and invite others to build on them ([OpenAI Help Center](https://help.openai.com/en/articles/6825453-chatgpt-release-notes)).

**What it is good at.** It works on the web, the desktop app and iOS and Android ([OpenAI Help Center](https://help.openai.com/en/articles/6825453-chatgpt-release-notes)), so a small team can draft a pitch deck together without a separate design tool.

**Honest limitations.** This is the big one: "To open a shared page or presentation, you need permission to view it and must be signed in to a Plus, Pro, Business, or Enterprise account with Space access" ([OpenAI Help Center](https://help.openai.com/en/articles/6825453-chatgpt-release-notes)). Free users cannot open shared pages and there are no public links yet ([Lilach Bullock](https://www.lilachbullock.com/ai-news-this-week-for-small-business-22-november-2026/)). So you cannot send a Space presentation to a client who does not pay for ChatGPT. When I checked OpenAI's pricing page, it still listed Space as unavailable on Plus ([OpenAI](https://chatgpt.com/pricing)), which suggests the rollout is still reaching accounts.

**South African use cases.**
- Two co-founders building an investor presentation together, then exporting it for the meeting.
- An agency team drafting a campaign proposal internally.

**Industries.** SaaS building, agency and creative, professional services.

**Pricing.** Included with ChatGPT Plus; no separate price is given ([OpenAI Help Center](https://help.openai.com/en/articles/6825453-chatgpt-release-notes)). Check the rand price of Plus in the app.

**Access notes.** Global for Plus, so South Africa is included, but treat it as an internal tool until public links arrive.

**Link.** [OpenAI - ChatGPT release notes](https://help.openai.com/en/articles/6825453-chatgpt-release-notes)

---

## Not for us yet

- **Free Tasks in Gemini (17 November).** Free in the US, India, Canada, Australia, Japan and Korea ([Gemini release notes](https://gemini.google/za/release-notes/?hl=en-GB)). South Africa is not on the list.
- **Zoho Desk Blended Agents (16 November).** AI customer-service agents on any paid Zoho Desk plan with no build cost, but available in India, the US, the EU, Japan, China and Australia, with Canada next ([Shashi](https://www.shashi.co/2026/11/zoho-desk-launches-blended-agents-at-no.html)).
- **ChatGPT Health.** "Health is available to Free, Go, Plus, and Pro users in the U.S." ([OpenAI Help Center](https://help.openai.com/en/articles/6825453-chatgpt-release-notes)).
- **Computer use in the Gemini Mac app (19 November).** English in the US first, on AI Plus, Pro or Ultra ([Lilach Bullock](https://www.lilachbullock.com/ai-news-this-week-for-small-business-22-november-2026/)).
- **Gemini GIFs.** Listed for the US, Canada, the UK, Japan, Korea and Australia ([The Verge](https://www.theverge.com/google)).

---

## South African corner

- **A proposed R100 million AI venture fund.** During his Silicon Valley visit, President Ramaphosa said: "We've come up with the idea that we should set up a venture capital fund that will start off with R100 million, as well as a credit guarantee fund that will help start-ups in our country in the AI and tech industry" ([SAnews](https://www.sanews.gov.za/south-africa/sa-eyes-r100m-venture-capital-fund-support-ai-start-ups)). Government would seek to match entrepreneurs' commitments. It is proposed, not yet set up, and there is no application process or date ([SAnews](https://www.sanews.gov.za/south-africa/sa-eyes-r100m-venture-capital-fund-support-ai-start-ups)). Worth watching, not worth planning around yet.
- **CAPEability AI in Western Cape libraries.** The Western Cape Government and Microsoft launched it on 17 November, using 83 provincial eCentres and 375 public library service points, with a focus on people aged 18 to 35 ([Western Cape Government](https://www.westerncape.gov.za/department-premier/article/western-cape-government-partners-microsoft-prepare-residents-ai-economy)). Pathways cover digital literacy, AI and Copilot, employability and entrepreneurship. The page does not say whether it is free or how to sign up ([Western Cape Government](https://www.westerncape.gov.za/department-premier/article/western-cape-government-partners-microsoft-prepare-residents-ai-economy)). If you hire junior staff in the Western Cape, ask your local library.
- **SA AI Index 2026.** More coverage this week: SABC reports that nearly a third of large enterprises have AI in live operations, yet fewer than half see measurable financial returns ([SABC News](https://www.sabcnews.com/sabcnews/nearly-a-third-of-sa-firms-use-ai-but-measurable-profits-lag-study/)). I could not confirm whether the full report came out on 23 November as planned.

---

## Follow-ups

- **ChatGPT Standard and Advanced voice retire on 11 December**, as covered last week ([Lilach Bullock](https://www.lilachbullock.com/ai-news-this-week-for-small-business-15-november-2026/)).
- **Gems are moving into Settings in the Gemini app** from 17 November. For Business and Enterprise accounts, skills fully replace Gems no sooner than 1 March 2027 ([Google Workspace](https://knowledge.workspace.google.com/admin/generative-ai/gemini-app/about-the-transition-to-skills)). If your team relies on Gems, start rebuilding them as skills, which we covered last week.
- **Google Vids now keeps your images, video and audio in an Assets section** for reuse within the same project ([Google Workspace Updates](https://workspaceupdates.googleblog.com/2026/11/)). Business Starter is eligible, and Scheduled Release domains start on 2 December ([Lilach Bullock](https://www.lilachbullock.com/ai-news-this-week-for-small-business-22-november-2026/)).
- **Gemini 4 Neon.** Pro and Ultra subscribers can pick it in the Gemini app; the API costs $3 per million input tokens and $15 per million output tokens ([Google](https://blog.google/innovation-and-ai/models-and-research/gemini-models/introducing-gemini-4-neon/)).

---

## Left out on purpose

- **Kling Image 4.0 (17 November).** Kling's new image model ([Kling AI](https://app.klingai.com/global/release-history)). Kling makes this series' animated clips, so I hold it to a higher bar, and it is a model update rather than a business tool.
- **Anthropic's Nasdaq listing.** News, not a tool, and not investment advice. Anthropic also makes the Claude models this series' writing pipeline uses.
- **Office in Copilot.** Generally available to "eligible subscribers" ([Microsoft](https://www.microsoft.com/en-us/copilot/blog/2026/11/17/copilot-at-microsoft-ignite-expanding-whats-possible-with-intelligence-built-for-work/)), but the announcement gives no plan names or prices, so I could not tell you what it costs here.
- **Gemini business tools and saved brand styles.** Reported this week ([Lilach Bullock](https://www.lilachbullock.com/ai-news-this-week-for-small-business-22-november-2026/)), but Google's own post is dated 20 October ([Google](https://blog.google/innovation-and-ai/products/gemini-app/new-tools-small-business-owners/)), outside this window.
- **Claude computer use.** Rolling out to Team and Enterprise organisations only ([Lilach Bullock](https://www.lilachbullock.com/ai-news-this-week-for-small-business-22-november-2026/)), and Claude is part of this series' own pipeline.

---

## What I'd actually try this week

1. **HCode.** If you have ever asked an AI to build a small tool and then not known how to put it online, this is the cheapest way I have seen to finish the job, and it is in rand. Use the free two months to publish one internal tool, a checklist or a booking form, with no client data in it. If it holds up, you have a R50 a month home for it on a South African server.
2. **ChatGPT Live Dictation.** It costs nothing extra and works on every plan. This week, dictate one long client email or brief instead of typing it, in your normal accent, and see how much you need to correct. If it handles your voice well, it saves you time every day.
