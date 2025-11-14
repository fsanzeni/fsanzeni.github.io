+++
title = 'On AI and Temporal Arbitrage'
date = 2025-11-14T11:29:00
summary = "Why prioritising market dominance and delayed profits collides with the brute physics of AI computation."
showSummary = true
categories = ["Blog",]
tags = ["AI Economics",
  "Market strategy",
  "Platform capitalism",
  "Computational density",
  "George Hotz",
  "Temporal arbitrage",
  "Digital infrastructure",
  "Venture capital",
  "Business models"]
+++

It's been a while since I've written one of these. At any rate, I've (unsurprisingly) been thinking about AI and how strange it all seems. But, besides being arguably a solution in search of a problem, it *feels* like there is something structurally wrtong going on. It kinda clicked when I was listening to an interview with geohot. Here are my reflections.

Tech's big thing lately (and by lately, I mean the last couple of decades) has been to lose money now to print money later. Dominate the market, and profitability will follow. In this short essay, I am to demonstrate how, for AI, this entire playbook is *structurally* impossible. TL;DR the underlying physics of computation makes [temporal arbitrage](https://journals.sagepub.com/doi/10.1177/1461444820913567) (i.e., trading short-term losses for long-term dominance) a category error.
## Market Share is an Outcome, Not a Lever
[MIT’s Wernerfelt](https://web.mit.edu/bwerner/www/papers/Therelationbetweenmarketshareandprofitability.PDF) captures this elegantly:

> Note, first, that if a firm finds itself in a stable, asymmetric equilibrium, a higher market share will correspond to a higher profit from that time on. Over- or under-shooting the equilibrium and trying to hold too big or too small a market share will, however, not lead to maximum profits. Trying to hold too big a market share, for example, will often involve charging prices that are too low. […] Trying to increase the value of the firm simply by increasing market share is like trying to put out a fire by blowing the smoke away.

Wernerfelt describes “stable, asymmetric equilibrium”—market structures where firms of different sizes coexist with different profitability levels. In mature industries, symmetric size distributions are unstable: small perturbations cause one firm to gain share while others lose it, eventually settling into asymmetric configurations where the large firm commands higher profits. Once you’re *in* this equilibrium, higher market share correlates with higher profit. But forcing your way to bigger share through unsustainable pricing destroys value.

The “blowing smoke away” metaphor is my favourite bit of the quote: market share is an *outcome* of competitive advantage, not a lever you can pull independently. Firms chasing share through predatory pricing aren’t building the underlying capabilities (i.e., lower costs, superior products, economies of scale) that would justify larger share at equilibrium prices. OpenAI, anyone?

The platform capitalism playbook was to ignore this warning entirely. Amazon, Meta, Uber, etc., all built multi-sided markets in which one platform connects distinct user groups (riders and drivers, buyers and sellers), deliberately maintaining a larger market share on both sides while extracting *lower* immediate profit per transaction than competitors.

This apparent inefficiency was strategically sound. By keeping prices artificially low (or even sometimes negative, subsidising one side entirely), platforms attracted users whose switching costs and behavioural lock-in became more valuable than the foregone revenue. In other words, these platforms bank on consumer surplus as future leverage. Uber’s ride-sharing dominance at below-profit prices became a structural advantage for dominating food delivery, freight logistics, and financial services (and a relatively short-lived foray in eVTOLs). In other words, unexploited consumer surplus in one market became an asset in adjacent markets.

This worked because cross-side network effects ([Parker & Van Alstyne, 2005](https://dl.acm.org/doi/10.1287/mnsc.1050.0400), [Rysman, 2009](https://www.aeaweb.org/articles?id=10.1257/jep.23.3.125)), where (in a nutshell) adding users on one side increases value for the other, create positive feedback loops that competitors with higher profit-per-transaction cannot match, even with superior unit economics. Uber took 15 years to become profitable, deliberately burning VC money to subsidise rides and undercut not just competitors but alternatives like public transit. That’s temporal arbitrage: operating on a timescale so long that competitors can’t afford to wait you out.
## When Physics Refuses to Cooperate
I recently came across [this interview with George Hotz](https://www.youtube.com/watch?v=AG2BHbaBrQI) (aka one of my favourites since his reverse-engineering of the PS3, aka the geohot I mentioned at the beginnign - the interview starts at 01:03:04), where he introduces a useful taxonomy that shows where the logic I briefly summarised above breaks down. His five-tier model of the AI stack:

- Tier 1: Electricity & data centres
- Tier 2: Fabrication (TSMC, ASML, Samsung)
- Tier 3: GPUs (NVIDIA, AMD)
- Tier 4: Model makers (OpenAI, Anthropic)
- Tier 5: Applications (Cursor, Windsurf, what he calls the “completely worthless things”)

Platform logic suggests value should pool at Tier 4, which devours Tier 5 through vertical integration, exactly as Facebook consumed Zynga and Google ate its ecosystem. But it seems that the computational economics are _*inverted_* for AI.

Where Gmail could serve 10,000 users from a single server at minimal marginal cost, AI models exhibit what Hotz calls “inverse economies of scale”. Serving one more power user on ChatGPT costs the platform multiples of the $200 monthly subscription fee. There’s unlimited demand for better, faster models, and unlike web services, you cannot compress the serving infrastructure.

This is what I call the Computational Density problem. OpenAI and Anthropic aren’t _*choosing_* to operate unprofitably to build market share like Amazon did. They’re structurally incapable of achieving web-era margins because serving AI requests at the edge requires massive computational expenditure per query. The underlying physics of computation refuses to cooperate with platform economics. Tier 4 companies burn capital on inference costs that grow linearly (or worse) with usage, preventing the gross margin expansion that made web platforms so obscenely lucrative.

No amount of market share will change this. No amount of strategic patience will overcome adverse unit economics.
## The Attention Economy Parallel
The [attention economy](https://dl.acm.org/doi/abs/10.1145/376625.376626) provides a useful parallel that clarifies what’s different. Traditional monopolies extract rents by raising prices or restricting output. But attention monopolies (i.e., Meta, Google) extract what researchers call [“algorithmic attention rents”](https://www.ucl.ac.uk/bartlett/sites/bartlett/files/algorithmic_attention_rents-_a_theory_of_digital_platform_market_power_final.pdf) by manipulating user behaviour, suppressing rival entry, and dominating flows of visibility, time, and communication. They don’t optimise for profit per user interaction, maximising instead the architectural control through which all interactions must flow.

Since around 2013, [35% of Amazon’s retail revenue is generated through recommendation algorithms](https://www.mckinsey.com/industries/retail/our-insights/how-retailers-can-keep-up-with-consumers), which represents algorithmic rent extraction, or, the ability to “disregard the full information content of its ecosystem and still profit” ([Strauss, O’Reilly, Mazzuccato, 2024](https://repository.uclawsf.edu/hastings_science_technology_law_journal/vol15/iss2/5/)). Dominance means the platform can be _*inefficient_* in information processing and still maintain its position through structural lock-in.

AI platforms cannot achieve this luxury. The architectural control that web platforms weaponised becomes computational liability when every ‘power user’ (I use the inverted commas here very ironically) haemorrhages money. Whereas web platforms tolerated inefficiency because serving costs approached zero, AI platforms’ value proposition inverts precisely when users engage most heavily.
## Value Drains Down the Stack
So if application and model layers are Sisyphean competitions, where does value go?

Down. It drains into areas with genuine, physical moats.

Value pools at Tier 3 (NVIDIA’s GPUs with their CUDA moat), Tier 2 (TSMC’s fabrication plants operating at [59.5% gross margins](https://focustaiwan.tw/business/202510160012#:~:text=Driven%20by%20strong%20global%20demand,points%20quarter%2Don%2Dquarter.) - and no, that’s not a typo), and Tier 1 (data centres, electricity infrastructure). These layers have massive capital intensity, genuine supply constraints, and manufacturing complexity that cannot be replicated with code.

In other words, when computational costs refuse to compress, value doesn’t aggregate to platforms but settles at the level of scarce physical resources (fabrication capacity, electricity, specialised manufacturing equipment). The “worthless” tier-five applications won’t fail because they lack patience or market share; they’ll fail because the entire value chain has inverted, and no amount of strategic forbearance can overcome adverse unit economics. The future belongs to whoever controls atoms, not bits (to invert [Negroponte’s famous quote](https://en.wikiquote.org/wiki/Nicholas_Negroponte)). I am not professing my nostalgia for industrial capitalism, but simply recognising that the Computational Density problem forces a re-materialisation of competitive advantage.

Market dominance and profit maximisation, it turns out, operate on different temporal registers *and* different technological substrates. In markets with computational density constraints and unfavourable marginal cost curves, dominance may be structurally impossible to translate into profitability at the application layer. The companies that survive won’t be those who achieved platform dominance through temporal arbitrage, but those who controlled the atoms on which all the bits depend. Or, to go back to the old adage:
> When Everyone Digs for Gold, Sell Shovels