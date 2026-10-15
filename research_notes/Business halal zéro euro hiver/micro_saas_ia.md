# Micro-SaaS / web tools / extensions built with AI coding agents (Claude Code) at 0 €: realistic for a French non-developer beginner starting October 2026?

Research date: 2026-10-15. About 18 searches and fetches. Many web sources are vendor blogs that cite each other, so weak sources are flagged. Revenue figures for famous founders are mostly self-reported or third-party estimates.

## 1. What expert indie hackers show: concrete numbers, medians vs outliers

### Takeaway
The famous examples (levelsio, Marc Lou, Tony Dinh, Danny Postma) earn $50K–$150K+ per month, but they had years of audience-building and dozens of failed products behind them. The best 2026 median data points to about $145 MRR (global, revenue-generating SaaS) and about 500 € MRR (29 verified French-speaking bootstrappers). About 55% of the French sample earns under 1,000 €/month, and only about 6–7% clear $10K or 20K €. The likely outcome for a beginner is 0 € to a few hundred euros per month in the first year.

### Cited Findings
- **levelsio, Photo AI:** an IndieHackers case study (sourcing vague) cites $132–138K MRR as of November 2025 — [IndieHackers](https://www.indiehackers.com/post/photo-ai-by-pieter-levels-complete-dive-case-study-0-to-132k-mrr-in-18-months-3a9a2b1579). A May 2026 teardown says "~$150K MRR neighbourhood" from earlier public snapshots, with about $20K/month GPU cost — [openaitoolshub](https://www.openaitoolshub.org/ai-product-research/photo-ai). Latka estimates only about $744K revenue in 2023, so the figures don't reconcile — [Latka](https://getlatka.com/companies/photoAI). A widely repeated narrative is that this came "after 70 failed startups" — [PPC Land](https://ppc.land/how-one-photo-ai-app-generates-132k-monthly-after-70-failed-startups/).
- **levelsio, fly.pieter.com (vibe-coded game, started 22 Feb 2025):** self-reported "$1M ARR in 17 days" — [levels.io](https://levels.io/full-multiplayer-python-websockets-game-ai). Press reported $87K in its first 30 days, mostly from selling ad slots at about $5K/month each plus in-game purchases — [VGTimes](https://vgtimes.com/tech-and-hardware/122582-dutch-startup-founder-creates-game-using-ai-in-180-minutes-and-earns-87000-in-one-month.html). 404 Media's headline: "makes $50,000 a month, yours probably won't" — [404 Media](https://404media.co/this-game-created-by-ai-vibe-coding-makes-50-000-a-month-yours-probably-wont). This success rests on his roughly 600K+ X audience (my inference, but central to the 404 Media framing).
- **Marc Lou:** now runs TrustMRR, a database of Stripe-verified startup revenues. He claims a "$1.2B database of verified startup revenues" and says he is a solo founder with no VC money — [TrustMRR](https://trustmrr.com/why-sell-on-trustmrr). A scraped record shows ShipFast at about $8.9K MRR as of March 2025 (old data) — [Apify scraper](https://apify.com/zerobreak/trustmrr-startup-scraper). I found no reliable 2026 figure for his total revenue.
- **Tony Dinh, TypingMind:** Latka estimates about $817K revenue in 2024, up from about $360K in 2023, with about 3 staff by 2026. Most revenue is from one-time licences — [Latka](https://getlatka.com/companies/typingmind); [AIBase](https://news.aibase.com/news/14433) (reports $1M in 20 months).
- **Danny Postma, HeadshotPro:** a secondary source says it passed $1M/year as a solo founder before a seven-figure sale. Unverified — [teahose](https://www.teahose.com/companies/9313).
- **Global median (2026):** BigIdeasDB "Revenue Intelligence" tracks 8,699 SaaS, of which 3,787 have revenue. Average $4,298 MRR, **median $145 MRR**, and about 6.1% above $10K MRR (July 2026). It is a vendor dataset with self-selection — [BigIdeasDB](https://bigideasdb.com/micro-saas-examples-2026) (fetch returned 429; figures via search summary).
- **French-speaking median (most relevant):** Journal du Net, 13 Aug 2026, covers 29 francophone bootstrapped founders whose revenue is verified with Stripe screenshots (Founder Trace) — [JDN](https://www.journaldunet.com/start-up/1553695-combien-gagnent-vraiment-les-fondateurs-bootstrappes-francophones/).
  - **Revenue:** median MRR is **500 €** (on 15 precise cases). 16 of 29 earn 0–1,000 €/month, 6 earn 1–5K €, 4 earn 5–20K €, and 2 earn more than 20K €.
  - **Time to first euro (15 cases):** 5 took under 30 days, 7 took 30–60 days, and 2 took more than 12 months.
  - **Main acquisition channels:** LinkedIn (10), cold outreach (9), word of mouth (9), paid ads (3), **SEO only 2 of 29**.
  - **Bias:** the sample leans toward founders who are already visible on LinkedIn.
- A widely repeated claim of a French developer making $1.03M in 2025 from solo SaaS appears only on secondary sites and is unverified (search summary, [pasqualepillitteri](https://pasqualepillitteri.it/fr/news/3086/stack-indie-hacker-france-2026)). Indiemakers.fr is cited as the main francophone bootstrapper community — same source.

### Inferences
- **Survivorship bias is extreme.** The experts are outliers with large audiences and years of failures. levelsio's "12 startups in 12 months" era produced only a few winners.
- **Realistic target for a beginner's first 3–6 months:** first euro possible, but 0–200 €/month is the most likely range. The French data suggests first revenue in 30–60 days for founders who succeed, but these are mostly experienced profiles.
- **The French data contradicts the "SEO/passive" narrative.** Revenue came mainly from LinkedIn, cold outreach and word of mouth, which are active, not passive.

### Gaps
- No primary 2026 figure for Marc Lou's total revenue, Danny Postma's current revenue, or Arvid Kahl's current projects. TrustMRR pages need a login or direct visit.
- No data on outcomes specifically for *non-developer* beginners (as opposed to developers).

## 2. Vibe coding reality for non-coders (Claude Code, Cursor, Lovable, Bolt), including security

### Takeaway
Non-coders can ship working web tools with AI agents. Most of the hard data on outcomes is anecdotal, though, and security is the main documented risk: many vibe-coded apps leak data through misconfigured Supabase or auth. **Claude Code is not free.** It needs at least the Claude Pro plan (about $20/month, about $17/month billed annually), which breaks the strict 0 € constraint unless an existing subscription or free alternative is used.

### Cited Findings
- **Pricing:** Claude Code is included in Pro at $20/month or $200/year. The Max plans cost $100/$200 per month. Claude Code and chat share the Pro quota. Sources conflict on whether the free plan includes any Claude Code access, and most say no — [noqta](https://www.noqta.tn/blog/claude-code-pricing-2026); [heyuan110](https://www.heyuan110.com/posts/ai/2026-02-25-claude-code-pricing/); [costbench](https://costbench.com/software/ai-computer-use/claude-code/).
- **Security, Replit study (May 2025):** 170 of 1,645 Lovable-built apps exposed sensitive user data, including names, emails, financial data and API keys. The cause was missing Supabase row-level security and ownership checks, cataloged as CVE-2025-48757 — [The Next Web](https://thenextweb.com/news/lovable-vibe-coding-security-crisis-exposed).
- **Security, single app (Feb 2026):** one Lovable-hosted app exposed 18K users and had 16 vulnerabilities, 6 of them critical — [The Register](https://www.theregister.com/2026/02/27/lovable_app_vulnerabilities).
- **Security, platform flaw (2026):** a Lovable broken-object-level-authorization flaw stayed open for 48 days — [TNW](https://thenextweb.com/news/lovable-vibe-coding-security-crisis-exposed).
- **Security, RedAccess:** a scan of Lovable, Replit, Base44 and Netlify apps found more than 5,000 apps without basic auth, about 40% of which leaked private data — [TNW](https://thenextweb.com/news/lovable-vibe-coding-security-crisis-exposed).
- **Time to revenue (blog estimates, weakly sourced):** one guide estimates about 95 hours over about 12 weeks to a paying-customer SaaS for a non-technical founder — [aibuilderclub](https://www.aibuilderclub.com/blog/vibe-coding-non-technical-founders). Another claims "about 70% of first builds need a full restart," which is unverified — [questera](https://www.questera.ai/blogs/vibe-coding-statistics-2026).
- **Custom domains:** only 7.6% of startups still on a vibe-coding platform subdomain report MRR, versus 44.1% on their own domain. This is correlation, not causation — [bigideasdb](https://bigideasdb.com/how-to-vibe-code) (via search summary).
- **Anecdote:** Modest Mitkus reported a vibe-coded SaaS reaching +$23K MRR in October 2025, his first SaaS built without knowing how to code. This is self-reported, and he already had a large audience — [Substack](https://iamjohnellison.substack.com/p/the-vibe-coding-wave-is-here-5-builders).

### Inferences
- **For a beginner, the safest products avoid storing user data.** Client-side calculators, static tools and Chrome extensions without a backend largely sidestep the Supabase/auth leak class of bugs.
- Anything with accounts or payments should use a hosted checkout (Stripe Payment Links or a merchant of record) rather than custom payment code.

### Gaps
- No rigorous success or failure rate for non-coders shipping with Claude Code specifically. There is no Reddit-sourced dataset on time to first customer.

## 3. Zero-cost stack: hosting, database, payments, fixed costs

### Takeaway
Hosting and database can be free:
- **Cloudflare Pages/Workers:** commercial use apparently allowed, but this comes from a secondary source.
- **GitHub Pages and Netlify:** free hosting options.
- **Supabase free:** pauses after 7 days of inactivity.
- **Vercel Hobby:** officially **non-commercial only**, so a monetized site should not use it.

Payments have no monthly fee, only per-transaction fees: Stripe at about 1.5% + 0.25 € on EU cards, or a merchant of record (Lemon Squeezy/Paddle at about 5% + $0.50) that handles EU VAT. Unavoidable fixed costs are the domain (~10 €/yr) plus store fees if relevant (Chrome $5 once, Google Play $25 once, Apple $99/yr). The AI tool itself (~$20/month) is the biggest hidden cost.

### Cited Findings
- **Vercel Hobby:** "non-commercial, personal use only." Commercial use needs Pro at about $20/seat/month — [Vercel docs](https://vercel.com/docs/plans/hobby); [Vercel Terms](https://vercel.com/terms).
- **Cloudflare Pages free:** up to 20,000 files and 25 MiB per asset — [Cloudflare docs mirror](https://9a51ac8b.previews.developers.cloudflare.com/pages/platform/limits/index.md). Workers free is about 100K requests/day (secondary). Commercial use is listed as allowed in a secondary comparison — [agentdeals](https://agentdeals.dev/hosting-free-tier-comparison-2026). This was not confirmed against Cloudflare's terms.
- **Supabase free:** 2 projects, 500 MB DB, 1 GB file storage, 50K MAU. Projects pause after 1 week of inactivity. Egress is 5 GB per one source and 500 MB per another (conflicting) — [automationatlas](https://automationatlas.io/answers/supabase-free-tier-limits-2026/); [jetadmin](https://www.jetadmin.io/blog/supabase-pricing-2026-guide-to-plans-limits-and-real-world-costs/).
- **Stripe France:** about 1.5% + 0.25 € for French cards, about 1.4% + 0.25 € for other EEA cards, and about 3.25% + 0.25 € for non-EU cards (secondary; the official page was not parsed) — [hayot-expertise](https://hayot-expertise.fr/blog/frais-stripe-paypal-mollie-klarna-comparatif-optimisation-ecommerce-2026); [kolonell](https://kolonell.com/fr/blog/paiement-en-ligne-pme-stripe-mollie-payplug-frais-2026). With Stripe direct, the seller handles VAT themselves.
- **Lemon Squeezy:**
  - Fees: 5% + 50¢, with reported surcharges of +1.5% on international transactions and +0.5% on subscriptions. One example works out to about 8.6% total on a $20 sale into France — [learnwithhasan](https://learnwithhasan.com/payment-gateways/lemonsqueezy/); [rework](https://resources.rework.com/tools/billing-revenue/paddle-vs-lemon-squeezy).
  - Ownership: Stripe acquired it in July 2024, with reports of slower support and approvals.
  - Stripe Managed Payments: Stripe's own merchant-of-record product covers tax in 80+ countries. Its fee is unconfirmed (one source says 3.5% on top of Stripe fees) — [dodopayments](https://dodopayments.com/blogs/lemon-squeezy-vs-stripe/); [devtoollab](https://devtoollab.com/blog/best-merchant-of-record-platforms).
- **Store fees:** Chrome Web Store $5 one-time; Google Play $25 one-time; Apple $99/year — [extensionbooster](https://extensionbooster.net/blog/chrome-web-store-developer-registration-fee-2026-guide/); [splitmetrics](https://splitmetrics.com/blog/google-play-apple-app-store-fees/).
- **French legal/tax:** thresholds, VAT and ACRE rules reportedly changed on 1 July 2026 (unverified; check URSSAF) — [pasqualepillitteri](https://pasqualepillitteri.it/fr/news/3086/stack-indie-hacker-france-2026).

### Inferences
- **Cheapest compliant path for a French individual:**
  1. Register a micro-entreprise (free).
  2. Host on Cloudflare Pages or GitHub Pages.
  3. Take payments through a merchant of record for international or EU digital sales (it handles EU VAT OSS), or through Stripe Payment Links for French customers only.
- **Mobile apps are the least zero-budget format.** Apple's $99/yr fee plus the review burden make them the worst first project. A PWA, web tool or Chrome extension is better.

### Gaps
- Whether Stripe or Lemon Squeezy require a SIRET from a French individual. Most likely yes for Stripe, since a business entity is needed, but I did not confirm it.
- Exact Stripe Managed Payments fees.
- Cloudflare's commercial-use terms from the primary source.

## 4. Zero-budget distribution: what gets first users

### Takeaway
For first users, active channels beat SEO: personal network, LinkedIn, Reddit or communities, cold outreach. SEO and programmatic SEO are slow (months) and weakened by AI Overviews and Google's "scaled content abuse" policy. Free-tool sites remain a proven long-term traffic play, but mostly for established domains.

### Cited Findings
- **French verified founders' main channels:** LinkedIn 10/29, cold outreach 9, word of mouth 9, paid ads 3, SEO 2 — [JDN](https://www.journaldunet.com/start-up/1553695-combien-gagnent-vraiment-les-fondateurs-bootstrappes-francophones/).
- **AI Overviews (secondhand):** reportedly cut position-1 CTR by 58% on keywords where they appear (Ahrefs, Dec 2025). Semrush reportedly found 93% of AI Mode sessions end without a click — [quickseo](https://quickseo.ai/blog/programmatic-seo-stats-2026-is-pseo-still-viable-in-the-ai-search-era) (vendor; not verified against Ahrefs or Semrush).
- **Google policy:** the March 2024 "scaled content abuse" policy targets mass auto-generated pages — same source. G2 reportedly lost about 80% of its organic traffic by late 2025 — same source (unverified).
- **Free-tool traffic leaders:** Smallpdf, MXToolbox and Ahrefs' free tools rank among the top bootstrapped sites by organic traffic (March 2026, third-party estimates) — [tryanalyze](https://www.tryanalyze.ai/blog/top-bootstrapped-saas-companies).
- **Launch spikes:** Marc Lou's Unicorne launched on Product Hunt on 9 Feb 2026 with 507 upvotes. Results like this come from founders who already have an audience — [hunted.space](https://hunted.space/dashboard/unicorne/launches/unicorne).
- **Validation advice:** guides recommend mining Reddit, X and forums for recurring complaints — [aibuilderclub](https://www.aibuilderclub.com/blog/vibe-coding-non-technical-founders).

### Inferences
- **For a beginner with no audience:**
  - First users come from niche communities where the person already belongs. For this user, French-speaking Muslim WhatsApp, Telegram and Facebook groups, local mosque networks and Reddit (r/islam, r/france) fit, with careful respect for self-promotion rules.
  - Build in public on X or LinkedIn compounds slowly.
  - SEO is a 6–12 month bet, not a winter plan.
- **"Passive" is mostly a late-stage result.** Early months require daily distribution work.

### Gaps
- No rigorous comparative data on Product Hunt, Reddit and directories for first users in 2026. YouTube's effectiveness for micro-tool launches was not researched.

## 5. Ideas with demand (francophone, Muslim audiences) and halal monetization

### Takeaway
Muslim-utility apps have proven mass demand: Muslim Pro passed 150M downloads (2023) and charges about $35/yr for premium. The space is crowded with free, entrenched tools, though. Mawaqit is free, ad-free, and widely used by French mosques, so a generic prayer-time app is a poor bet. Niche French-language tools are less contested and better suited to a web-tool beginner, but checking accuracy with scholars is essential:
- Islamic inheritance calculators following French law and fiqh
- zakat calculators
- Ramadan or Hajj planners
- Arabic or Quran learning helpers

Monetization: ads are permissible per several fatwas *if the ad content is halal*. AdSense gives limited control, so some scholars advise avoidance. Subscriptions, one-time sales and halal affiliate links are cleaner.

### Cited Findings
- **Muslim Pro:**
  - Downloads: more than 150M globally, about 12M from Malaysia (June 2023, older data) — [NST](https://www.nst.com.my/amp/business/home/2023/06/922652/muslim-pro-app-exceeds-150mil%C2%A0downloads-globally).
  - Premium: about $34.99/yr per a competitor-authored comparison. The same source repeats the 2020 report that Muslim Pro sold location data to US military contractors, which created distrust and an opening for privacy-first alternatives — [islamtics](https://islamtics.com/?p=21176).
- **Mawaqit:** free, no ads, no personal data collection. Times are set by each mosque's imam (publisher claims) — [App Store FR](https://apps.apple.com/FR/app/id1460522683); [Clubic](https://www.clubic.com/telecharger-fiche555681-mawaqit.html). No reliable user count for France was found.
- **Inheritance (farāʾiḍ) calculators:** search results were dominated by low-quality spam pages. That suggests search demand exists and a quality French-language tool might stand out, but it is my inference. These pages warn that one misidentified heir invalidates the whole calculation, so results need checking by a scholar or notary — [example page](https://production.matthewmarks.com/?p=21514) (low quality).
- **Ads, fiqh views:**
  - Darul Ifta Birmingham: AdSense income is acceptable if the ads are not unethical. It advises avoiding AdSense on videos because scholars differ — [Darul Ifta Birmingham](https://daruliftabirmingham.co.uk/is-income-from-google-adsense-halal/).
  - Shaykh Irshaad Sedick (SeekersGuidance): selling ad space is like renting, but if you have no control it is best avoided where possible — [IslamQA.org](https://islamqa.org/shafii/seekersguidance-shafii/237230/is-it-permissible-to-collect-ad-revenue-from-online-services/).
  - Muftionline: permissible if the ads are of a permissible nature — [IslamQA.org](https://islamqa.org/hanafi/muftionline/128166/earning-through-google-adsense/).
  - 2025 Indonesian journal: permissibility depends on content and ad type, and zakat is due on the income — [UIN Bukittinggi](https://ejournal.uinbukittinggi.ac.id/jilaw/article/view/9638).
- **Model example:** fly.pieter.com earned from directly sold sponsor slots (about $5K/month each), giving full control over the advertisers. That model is more compatible with halal constraints than programmatic ads — [VGTimes](https://vgtimes.com/tech-and-hardware/122582-dutch-startup-founder-creates-game-using-ai-in-180-minutes-and-earns-87000-in-one-month.html).
- **TypingMind:** earns mostly from one-time licences, which shows non-subscription models can work — [AIBase](https://news.aibase.com/news/14433).

### Inferences
- **Halal-friendly monetization, in order of preference:**
  1. One-time payment or "pay what you want" for a premium version (via a merchant of record).
  2. Small subscriptions for B2B tools: mosques, Islamic schools and associations, e.g. class management or donation-free admin tools, but **avoid handling donations or finance**.
  3. Directly sold sponsor slots to halal businesses.
  4. Halal affiliate links: books, Islamic courses, modest fashion, Hajj/Umrah-adjacent but non-financial.
  5. AdSense or programmatic ads only with strict category blocking, and this is the most doubtful option.
- **Excluded by the user's constraints:** zakat and inheritance tools are fine as calculators, but products touching finance, interest, crypto, gambling, dating or adult content are out. Islamic inheritance and zakat tools carry religious-accuracy and reputational risk, so citing a madhhab and getting a scholar's review is necessary.
- **The B2B angle is more likely to produce first euros than B2C apps** competing with free giants. The French data shows LinkedIn and cold outreach work, and mosque or association admin tools are a reachable niche. This is an inference, not validated demand.

### Gaps
- No search-volume data for French queries such as "calcul héritage islam", "calcul zakat" or "horaires prière". The Ubersuggest connector was not authorized.
- No revenue data for small Muslim-niche indie tools.
- No 2025–2026 market-size figures for Islamic apps.
