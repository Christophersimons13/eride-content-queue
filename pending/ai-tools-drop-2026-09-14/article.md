# AI Tools Drop - Week of 14 September 2026

Nine launches worth your attention, read from a Johannesburg desk.

Exchange rate used throughout: **R16.11 to the dollar**. That is the midpoint of four sources taken between 11 and 14 September, and the spread between them was 0.37 percent, the tightest since this series started ([XE at 16.11 on 13 September](https://www.xe.com/currencyconverter/convert/?Amount=1&From=USD&To=ZAR), [Bloomberg at 16.1372](https://www.bloomberg.com/quote/USDZAR:CUR), [Investing.com at 16.1399](https://za.investing.com/currencies/usd-zar), [Pluang at 16.1723](https://pluang.com/en/tools/currency-converter/usd-zar)). Google Finance was excluded again for printing a stale outlier two weeks running.

---

## This week in one paragraph

The theme picked itself. Nine tools launched, and if your requirement is that customer data stays inside South Africa, only two of them can honestly say yes, and both get there the same way: you host it or the model runs on the device. Not one shortlisted vendor offers African data residency. Not one names South Africa in a hosting policy. The best data posture of the week belongs to a nine-person Amsterdam outfit whose entire pitch is that nothing leaves the phone. Meanwhile the money that would fix this did move, twice, but to Lagos and to Cairo, not here. And for the sixth week running I found zero AI vendors publishing anything about POPIA compliance, while a random community member built a POPIA compliance checker as an n8n workflow template. The tooling is getting genuinely good. The local plumbing is not arriving with it. So this week's honest recommendation is defensive: pick the tools that do not need you to trust anyone's data centre.

---

## 1. Desert Ant Labs

**On-device models that never phone home, free to a hundred thousand devices.**

### What it actually is

An Amsterdam team shipped a family of small models built to run entirely on the device, published as one SDK across iOS, Android, web and embedded. Seven audio models, seven text models, four vision models. It landed at number eight on the Product Hunt daily board for [10 September](https://www.producthunt.com/leaderboard/daily/2026/9/10).

The standout is not a chat model. It is [Redact](https://desertant.com/models/redact/), a 23 million parameter model that strips personally identifiable information from text across 27 languages, on the device, before anything is transmitted. Twenty-three million parameters is small enough to sit in a mobile app without a meaningful download penalty.

### What it is genuinely good at

Structural privacy rather than promised privacy. Their [privacy policy](https://desertant.com/privacy) states that inference data is never sent to them, which is a different category of claim from "we do not train on your data". One is an architecture, the other is a policy that can change.

### Honest limitations

- **No African language support.** The language lists are European. Redact's 27 languages do not include Zulu, Xhosa, Afrikaans or Sesotho.
- **There is no published paid price.** Free up to 100,000 monthly active devices per platform, and then nothing. The URL `desertant.com/pricing` does not exist. If you cross the threshold you are negotiating blind.
- **No statement on model training** beyond the on-device claim.
- Small models are small. Do not expect frontier reasoning.

### South African use cases

1. **Immigration document intake.** Run Redact on the client's device before an uploaded passport scan or payslip reaches your server. The PII never crosses the wire, which changes your POPIA exposure from a processing question to a much narrower one.
2. **Fintech onboarding in low-connectivity areas.** On-device audio and vision models keep working through a signal drop and through load shedding, because there is no round trip to fail.
3. **Field services with intermittent data.** Logistics or security operators capturing notes and photos offline, with classification happening locally and only structured output syncing later.

### Fit

Immigration services, fintech, security and compliance, logistics, any regulated intake workflow.

### Pricing

Free up to 100,000 monthly active devices per platform. Paid pricing not published.

### Access from South Africa

An SDK, so no regional block and no card required at the free tier. The gap is linguistic, not geographic.

[desertant.com](https://desertant.com/models/redact/)

---

## 2. Relaticle

**A self-hostable AI CRM under AGPL, so the database can live in Johannesburg.**

### What it actually is

An open-source CRM with AI features built in, licensed AGPL and designed to be self-hosted. It reached number six on the Product Hunt board for [8 September](https://www.producthunt.com/leaderboard/daily/2026/9/8), with version 3.5.8 tagged on 12 September.

Be clear on what that launch was: this is an existing project with 2025 development history that ran a Product Hunt launch this week, not a new product. That does not make it less useful, but it is not a debut.

### What it is genuinely good at

It is the only tool on this list where you can put customer records on infrastructure you control, in this country, without asking a vendor's permission. Their [privacy policy](https://relaticle.com/privacy-policy) states that Relaticle does not train AI models on CRM data.

### Honest limitations

- **Self-hosting does not make it unmetered.** Their [pricing page](https://relaticle.com/pricing) states plainly that self-hosting does not disable credit metering. You get 300 AI credits a month. Host it yourself and you still hit the same ceiling on the AI features.
- **The cloud hosting location is not named** anywhere in the privacy policy. If you use their cloud you do not know where the data sits.
- The enterprise jump is brutal: Pro is 19 dollars a month, enterprise starts at 20,000 dollars a year. Nothing in between.
- Self-hosting means you own the upgrades, the backups and the security patching.

### South African use cases

1. **A compliance-sensitive practice** such as immigration consulting or legal services keeping client records on a local VPS, with AI enrichment capped at the free credit allowance and the sensitive processing done manually.
2. **A salon or clinic group** wanting customer history without a per-seat SaaS bill scaling with a large casual staff roster.
3. **An agency** running client CRM for several accounts where contractual terms forbid third-party cloud storage.

### Fit

Professional services, legal, immigration, beauty and wellness groups, agencies.

### Pricing

Self-host free forever, 300 AI credits a month. Cloud Pro 19 dollars a month billed yearly, roughly **R306**, or 24 dollars monthly, roughly **R387**. Enterprise from 20,000 dollars a year, roughly **R322,200** ([pricing](https://relaticle.com/pricing)).

### Access from South Africa

Self-hosting has no geographic barrier. Cloud billing is standard card.

[relaticle.com](https://relaticle.com/pricing)

---

## 3. Widgo

**An AI sales rep for your website, genuinely free at 500 sessions a month.**

### What it actually is

A US company shipped a conversational agent that sits on your website, qualifies visitors and hands off. It hit number two on the Product Hunt board for [8 September](https://www.producthunt.com/leaderboard/daily/2026/9/8).

### What it is genuinely good at

Disclosure. Of the nine tools here, Widgo's [privacy policy](https://www.widgo.ai/legal/privacy-policy) is the clearest: it names the processing regions, US and EU, names the subprocessors, and states that customer conversation content is not used to train foundation models. That is the standard the rest of this list should be held to.

The free tier is also real: 500 sessions a month, no card.

### Honest limitations

- **EU data residency is on request only**, and there is no African option at all.
- The pricing cliff is steep. Free, then 249 dollars a month, then 833. Nothing for a business doing 600 sessions.
- The "100 plus languages" claim is not verifiable from published documentation.

### South African use cases

1. **A wellness clinic or salon site** qualifying booking enquiries after hours, which in practice is when most enquiries arrive.
2. **An immigration consultancy** running first-line triage on visa-pathway questions, with a hard handoff to a human before anything that resembles legal advice.
3. **A B2B SaaS landing page** filtering enquiry volume before it hits a two-person sales team.

### Fit

Beauty and wellness, professional services, SaaS, retail, any site with unattended enquiry volume.

### Pricing

Free forever, 500 sessions a month, no card. Growth 249 dollars a month, roughly **R4,011**. Scale 833 dollars a month, roughly **R13,420** ([pricing](https://www.widgo.ai/pricing)).

### Access from South Africa

No block reported. Free tier needs no card.

[widgo.ai](https://www.widgo.ai/pricing)

---

## 4. Typewise Nova

**Outcome-based pricing for customer support AI, and a launch gift that expires on 20 September.**

### What it actually is

A Zurich company launched an AI customer experience operator on 10 September, dated in their own press release ("ZURICH, 10 September 2026", [press page](https://www.typewise.app/press)). It took number one on Product Hunt with 349 upvotes.

The interesting part is the billing model. You pay per resolution: a full resolution counts 1.0, a partial counts 0.5, and an unresolved ticket is free.

### What it is genuinely good at

Two things. The billing model puts the risk on the vendor, which is rare and worth rewarding. And the data commitments are the strongest written ones of the week: EU or US hosting, a statement that customer data is never used to train anyone's model, zero data retention configured on the LLM layer, AWS Frankfurt named ([pricing page](https://www.typewise.app/pricing)).

**Time-sensitive:** the launch gift is 1,000 resolutions plus three months with no base fee, no card required, and it expires on 20 September 2026. From publication of this piece that is six days.

### Honest limitations

- **No African hosting option**, and the documentation does not make clear which of EU or US applies to a South African customer by default. Ask before you sign.
- That launch gift is a trial, not a free tier. There is no free plan underneath it.
- Starter at 99 dollars a month is a real monthly commitment for a small operation, and extra users are 89 dollars each.

### South African use cases

1. **An e-commerce or retail operation** where support volume spikes seasonally, and the unresolved-is-free model means you are not paying for the tickets the AI fails.
2. **A fintech support desk** wanting a written zero-retention commitment on the model layer, which most competitors do not offer.
3. **Any support team of two to four people** using the launch gift to run a genuine three-month test before committing budget.

### Fit

Retail and e-commerce, fintech, SaaS, professional services with support desks.

### Pricing

Starter 99 dollars a month, roughly **R1,595**. Growth 599 dollars, roughly **R9,650**. Business 2,000 dollars a month, roughly **R32,220**. Additional users 89 dollars, roughly **R1,434** ([pricing](https://www.typewise.app/pricing)).

### Access from South Africa

No block. Launch gift needs no card, which makes the test genuinely zero-risk if you start before 20 September.

[typewise.app](https://www.typewise.app/pricing)

---

## 5. n8n 2.39.x

**The self-hosted automation workhorse moved to a new minor line, but stable has not caught up.**

### What it actually is

Four releases landed inside the window: 2.39.2 on 10 September, 2.39.3 and 2.39.4 on 11 September, and a 2.39.5 beta on 14 September ([GitHub releases](https://github.com/n8n-io/n8n/releases)).

One important caveat: **the stable channel is still 2.38.7**. The 2.39 line is available but not marked stable, and n8n's own [changelog](https://docs.n8n.io/changelog) has no 2.39 entry at all, which means any feature description you read about this line from a third party is unverified.

### What it is genuinely good at

Self-hosted automation with a real node ecosystem. If you run it on a local VPS, your automation data does not leave the country. In a week where no vendor offers African residency, that matters.

### Honest limitations

- **Do not put 2.39.x on anything that matters yet.** No stable tag, no vendor changelog.
- Self-hosting is real operational work: upgrades, backups, monitoring.
- Priced in euros, so the rand conversion in this piece does not apply.

### South African use cases

1. **Compliance document routing** where a POPIA posture requires the pipeline to stay on infrastructure you control. There is even a community-built [POPIA website compliance workflow template](https://n8n.io/workflows/18920-grade-popia-website-compliance-using-homepage-and-privacy-policy-html/) that grades a site's homepage and privacy policy. Worth noting that this is a user contribution, not a vendor compliance product, and it was the only POPIA artefact I found anywhere this week.
2. **Connecting a local payment provider** to accounting and messaging without routing transaction data through a foreign automation cloud.
3. **Internal operations glue** across Supabase, Telegram and email for a small team.

### Fit

Fintech, compliance, logistics, any SME with an internal operations layer.

### Pricing

Self-host community edition free. Cloud Starter 20 euros, Pro 50 euros, Business 667 euros.

### Access from South Africa

Self-hosting is unrestricted.

[github.com/n8n-io/n8n/releases](https://github.com/n8n-io/n8n/releases)

---

## 6. GoodLads

**A Google Ads manager charging a flat fee instead of a percentage of your spend.**

### What it actually is

An AI growth manager for Google Ads that took number seven on the [8 September](https://www.producthunt.com/leaderboard/daily/2026/9/8) board.

### What it is genuinely good at

The pricing structure, honestly. Flat monthly fees rather than a percentage of ad spend. For a South African advertiser running meaningful budget, a percentage model gets expensive fast, and a flat 100 dollars does not scale against you.

There is a Product Hunt promo code, MAKEITEASY, for 50 percent off, with no published expiry.

### Honest limitations

- **The trial requires a card.**
- **No country is named** in their [privacy policy](https://goodlads.cc/privacy-policy), so you do not know where campaign and customer data is processed.
- The training clause is narrowly worded, referring to "generalized or non-personalized" use, which is not the same as a commitment not to train.
- No expiry on the promo code means no urgency, but also no guarantee it survives.

### South African use cases

1. **A retail or e-commerce operator** spending 30,000 to 80,000 rand a month on Google Ads, where a 15 percent agency cut is far more than R1,611.
2. **A small agency** using the Agency tier to manage several client accounts under one flat fee.
3. **A service business** in beauty, wellness or professional services running always-on local search campaigns without a dedicated media buyer.

### Fit

Retail and e-commerce, agency and creative, beauty and wellness, professional services.

### Pricing

Pro 100 dollars a month, roughly **R1,611**. Agency 1,000 dollars, roughly **R16,110**. Enterprise 2,000 dollars, roughly **R32,220**. Annual billing costs six months ([goodlads.cc](https://goodlads.cc/)).

### Access from South Africa

No block. Card needed for the trial.

[goodlads.cc](https://goodlads.cc/)

---

## 7. Cognition SWE-2 in Devin

**A strong coding model, free until October, on a plan that trains on your code by default.**

### What it actually is

Cognition released SWE-2, a software engineering model, on 10 September ([announcement](https://cognition.ai/blog/swe-2)), and it appeared on the Product Hunt board for [13 September](https://www.producthunt.com/leaderboard/daily/2026/9/13). The headline number is 50.0 percent on FrontierCode 1.1. It is free in Devin Desktop and the Devin CLI through 10 October 2026.

The widely repeated claim that it is "64 percent cheaper than Fable 5.1" is a Product Hunt tagline and I could not verify it.

### This is the week's warning item

Read this before you point it at a client repository. Devin's [security documentation](https://docs.devin.ai/admin/security) states that by default, they may use your data for model training purposes. The opt-out is available on paid plans. So on the free tier, which is exactly the tier being promoted until 10 October, your code is training data and you cannot turn that off without paying.

Their infrastructure is AWS with no region named.

### What it is genuinely good at

Autonomous multi-step engineering work on a codebase, and the benchmark position is real. For personal projects and open-source work the free window is a genuine offer.

### Honest limitations

Beyond the training default: no named data region, an unverified cost comparison, and the free window closes on 10 October.

### South African use cases

1. **A solo founder prototyping** a greenfield project with no client data and no proprietary logic, using the free window deliberately.
2. **An engineering team on a paid plan** with the training opt-out switched on, doing migration and refactor work.
3. **Learning and evaluation**, on throwaway repositories, to judge whether the benchmark translates to your stack.

### Fit

SaaS building, agency development work, technical founders.

### Pricing

Devin Free 0 dollars. Pro 20 dollars a month, roughly **R322**. Max 200 dollars, roughly **R3,222**. Teams 80 dollars plus 40 dollars a seat ([pricing](https://devin.ai/pricing)).

### Access from South Africa

No block. The data default is the barrier, not geography.

[cognition.ai/blog/swe-2](https://cognition.ai/blog/swe-2)

---

## 8. Loqua

**Dictation that can see your screen, with a pricing page that has no prices.**

### What it actually is

A voice dictation tool that reads on-screen context to improve transcription accuracy, at number two on the Product Hunt board for [11 September](https://www.producthunt.com/leaderboard/daily/2026/9/11) with 406 upvotes.

Note that this was a relaunch. The original announcement was a [press release on 15 July](https://www.prnewswire.com/news-releases/voice-to-text-was-never-enough-meet-voice-that-sees-302826395.html). The Product Hunt appearance is new, the product is not.

### What it is genuinely good at

Screen-aware dictation is a real improvement over blind speech-to-text when you are dictating into a specific application, because the tool can use what is on screen to disambiguate names and terms.

### Honest limitations

- **There are no published prices.** The [pricing page](https://www.theloqua.ai/en/pricing.html) is live and lists tiers, but no amounts. The free tier is 5,000 words a week.
- **The marketing contradicts the policy.** The pricing page claims "Never trained on your data" and "Zero cloud data retention". The [privacy policy](https://www.theloqua.ai/en/privacy.html) says audio is sent to third parties including in the United States, and is silent on training. When the sales page and the legal page disagree, the legal page is the one that binds.

### South African use cases

1. **Consultation notes** in a wellness or professional services practice, on the free 5,000-word weekly tier, for non-sensitive content only.
2. **Content drafting** where speaking is faster than typing and nothing confidential is involved.
3. **Not for client or patient data**, given the policy contradiction. That is the honest recommendation.

### Fit

Professional services, content and creative work, with a hard limit on sensitive material.

### Pricing

Free tier 5,000 words a week. Paid tiers exist but no amounts are published.

### Access from South Africa

No block. Free tier available.

[theloqua.ai](https://www.theloqua.ai/en/pricing.html)

---

## 9. Live Captions by Subanana

**Fifty-two languages of real-time captioning, and one of them is African.**

### What it actually is

A Hong Kong company shipped real-time captioning, at number five on the Product Hunt board for [10 September](https://www.producthunt.com/leaderboard/daily/2026/9/10).

It is last on this list for a specific reason. The published accuracy table covers 52 languages, and Swahili at 61.8 percent is the only African language on it. No Zulu, no Xhosa, no Afrikaans, no Sesotho. A multilingual captioning product with 52 languages and none of ours is worth naming plainly.

### What it is genuinely good at

Verifiable infrastructure disclosure, which is rarer than it should be. Their [security page](https://subanana.com/en-HK/security) names AWS Singapore. You know where the data goes.

### Honest limitations

- **The language coverage excludes South Africa** in practice.
- **Live Captions is only on the Max tier** at 50 dollars a month. The cheaper tiers do not include it.
- **New individual accounts are opted in to training by default.** Team accounts are opted out. If you sign up as an individual, change that setting first.
- Singapore hosting means a long round trip for real-time work from here.

### South African use cases

1. **English-language webinars and conference streams** where accessibility captions are required and the audience is English-speaking.
2. **Recorded content subtitling** for international distribution, where Swahili coverage has some regional value.
3. **Team accounts only**, given the individual-account training default.

### Fit

Media and events, education, corporate communications, with English-only realism.

### Pricing

Free 0 dollars. Lite 9 dollars, roughly **R145**. Pro 18 dollars, roughly **R290**. Max 50 dollars, roughly **R806**, and Live Captions requires Max ([pricing](https://subanana.com/en/pricing)). Code PRODUCTHUNT20 works until 10 October.

### Access from South Africa

No block. Free tier available, but not for the captioning feature.

[subanana.com](https://subanana.com/en/pricing)

---

## The African compute story moved this week, twice, and not to South Africa

This deserves its own section because it is the structural answer to everything above.

**Digital Parks Africa announced NDC1 in Lagos on 8 September** at ITW Africa ([tech.africa](https://tech.africa/digital-parks-africa-lagos-ndc1/), [Nairametrics, 11 September](https://nairametrics.com/2026/09/11/digital-parks-africa-enters-nigerias-data-centre-race-with-lagos-facility/)). Digital Parks Africa is a South African operator, based at Samrand. This is their first facility outside South Africa. What pushed it there was regulation: the Central Bank of Nigeria issued a payment-data localisation mandate in June 2026, with full compliance required by 1 January 2027. A hard deadline created a market, and a South African company built for it.

South Africa has no equivalent mandate. That is the whole difference. Capacity and pricing for NDC1 are not published, and Digital Parks Africa's own [newsroom](https://www.dpa.host/category/news/) carries no dates.

**Cassava and Vodafone announced Egypt's first national AI factory on 8 September** ([Cassava](https://www.cassava.ai/2026/09/08/launch-of-egypt-first-national-ai-factory/)), a roughly one billion dollar project ([Business Insider Africa](https://africa.businessinsider.com/local/markets/zimbabwean-billionaire-strive-masiyiwas-cassava-joins-vodafone-in-dollar1-billion/0lvzjjg)).

For context on what is actually purchasable from Johannesburg today, [Stratos Lab](https://stratoslab.co.za/) publishes GPU pricing openly: A100 40GB at 1.12 dollars an hour, roughly R18.04. H100 80GB at 2.56 dollars, roughly R41.24. H200 at 3.58 dollars, roughly R57.67. B300 from 4.10 dollars, roughly R66.05, with expected availability in the third quarter of 2026. That listing is undated, so treat it as context rather than as a launch.

---

## What did not launch this week

Three honest notes, because the omissions are as informative as the inclusions.

**Lelapa AI added voice generation, on 5 September** ([iAfrica](https://iafrica.com/lelapa-ai-adds-voice-generation-and-looks-beyond-africa-we-built-a-technology-thats-beneficial-for-a-majority-world/)). Two days outside the window, so it is out on the date rule. It is also out on a second rule: the coverage describes stated intent, and [Vulavula's release notes](https://docs.lelapa.ai/overview/release-notes) stop at 12 August 2026, so there is no shipped artefact to point at. This is the sixth week this has come up unresolved.

**Tether TranslatePsy released AfriSLM**, offline open-source models covering 19 African languages including Zulu, Xhosa, Afrikaans, Tswana and Sotho, on [2 September](https://explainx.ai/blog/tether-translatepsy-offline-african-language-models-2026). Five days outside the window. This one hurts, because it is precisely the thing missing from every tool on this week's list, and the date rule put it out. If you build for South African language coverage, look at it anyway.

**Injini launched an AI for Education venture builder** in South Africa on [9 September](https://disruptafrica.com/2026/09/09/sas-injini-launches-ai-for-education-venture-builder-incubation-programme/), with applications open to 27 September. Inside the window and locally built, but it is an incubation programme, not a tool, so it does not qualify for the list. If you are building in education technology, that deadline is worth your diary.

Also worth a line: **OpenAI paused new Pro subscriptions** because of demand for Astra ([TechCrunch, 10 September](https://techcrunch.com/2026/09/10/openai-puts-pro-subscriptions-on-hold-due-to-astra-demand/)). And **Meta announced Muse**, a personal AI agent, on [8 September](https://about.fb.com/news/2026/09/introducing-muse-personal-ai-agent/), which is hard-blocked to the United States, has no published price, and defaults to opt-out training. Not available, not priced, not respectful of your data. Three reasons it is a footnote.

---

## The POPIA count is now six for six

For the sixth consecutive week, not one vendor covered in this series published anything referencing POPIA. Every privacy policy, data processing agreement and security page for all nine tools was checked, plus per-domain searches across fourteen domains. Nothing.

The only POPIA artefact found this week was that community-contributed n8n workflow template. A volunteer built a POPIA compliance grader before any vendor mentioned the Act.

Two more structural notes. Five of the vendors' `/privacy` paths returned HTTP client errors, and while most had working alternates, Desert Ant Labs and Cognition have no pricing page at all. And both [TechCentral's AI section](https://techcentral.co.za/category/sections/aiml/) and [TechCabal's AI category](https://techcabal.com/category/artificial-intelligence/) render entirely without dates, which makes them impossible to filter against a seven-day rule. That remains the biggest gap in this week's coverage and I am flagging it rather than pretending it does not exist.

---

## What I would actually try this week

**1. Desert Ant Labs Redact.** Free to a hundred thousand devices, runs on the phone, and the data genuinely never leaves. For an immigration or fintech intake flow, stripping PII on the client's device before upload changes the shape of your compliance problem rather than just documenting it. The missing South African languages are a real limitation, but PII detection on identity documents and payslips is mostly structural, not idiomatic. Start with one form.

**2. Typewise Nova, before 20 September.** A thousand resolutions plus three months with no base fee, no card. That is six days from now. Unresolved tickets are free under their billing model, which means a real test costs you nothing and tells you something. Ask them in writing whether a South African account lands on EU or US hosting before you go past the trial.

**And the thing to be careful with:** the Devin free tier. SWE-2 is free until 10 October and it is a strong model, but on the free plan your code may be used for training and the opt-out is behind a paid plan. Use it on throwaway repositories or pay. Do not point it at client work on the free tier.

---

*Sources are linked inline throughout. Every launch date in the numbered list was verified against a vendor-dated announcement or a dated Product Hunt daily leaderboard within 7 to 14 September 2026. Rand figures use R16.11 to the dollar and will move.*
