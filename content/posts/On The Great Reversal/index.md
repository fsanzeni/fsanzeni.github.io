+++
title = 'On The Great Reversal'
date = 2025-07-14T18:25:00
summary = "In my latest rabbit hole, I explore whether hardware development has actually become cheaper than software development."
showSummary = true
categories = ["Blog",]
tags = ["rambling","strategy","hardware"]
+++

The other week I was caught in another rabbit hole (intensly fuelled by algorithmic suggestions on good ol' YouTube) and came across [this video interview with Jeffrey Lipton](https://www.youtube.com/watch?v=IYUN104W3Io). In it, Lipton explains how academia is one of the few remaining 'feudal' systems today - a disussion that warrants a whole other post. 

It was a much smaller snippet that caught my attention. Lipton suggests that hardware is becoming cheaper than software. As someone who likes to dabble in hw design, that's not been my experience, but it's also true that I'm a single (read: limited, n00b) data point. So, I did a bit of research  and maths to figure out whether the claim can be reproduced. Now the following discussion can be a little dense, so here's the TL;DR: yes, hardware is less expensive than software on the medium- to long-term and presents a better bang/buck ratio.

As this is me being me, I couldn't resist touching on some of the deeper contradictions of our current techno-economic moment. Main discussion after the break.

{{< youtubeLite id="IYUN104W3Io" label="Prof Jerry Lipton interviewed by Leon." >}}

-----------
I'm going to start with the raw numbers, because they tell only part of the story. My (admittedly, surface-level) analysis of the current UK market[^1] suggests that software engineers earn an average of £63,638 per annum, compared to hardware and mechanical engineers' respective averages of £63,942 and £50,376. Not that much of a difference, I hear you whisper in the back.

But as any good [Bullshit Jobs](https://www.penguin.co.uk/books/295446/bullshit-jobs-by-graeber-david/9780141983479) evangelist would tell you, salaries often have an inverse relationship to actual social utility. The actual question is whether that money represents genuine productivity or simply [captures rent](https://www.sciencedirect.com/topics/social-sciences/rent-seeking) from an increasingly financialised (read: decoupled) economy.

Here's where Lipton's observation piqued my interest: the operational overhead for software development has exploded beyond sanity/recognition. A single H100 GPU costs £32,050 to purchase or around £2 per hour to rent in the cloud. Run that continuously for a year, and you're looking at roughly £17,520 (not including the _exorbitant_ electricity/cooling/sysadmin costs associated) just for the privilege of accessing the computational resources that modern ~~slop~~ software development increasingly requires. 

Meanwhile, CAD software licenses that once represented a significant barrier to entry in mechanical engineering now cost between [$0-$3,000 annually](https://interscale.com.au/blog/cad-software-cost/), a rounding error compared to the compute costs that software teams now treat as routine operational expenses.

Yes, there are ancillary costs. Yet, digital fabrication costs are going down YoY while GPU costs are experiencing what I can only describe as a supply-side coup, [with NVIDIA raising prices 10-15% across the board due to geopolitical tensions and manufacturing bottlenecks](https://www.tomshardware.com/pc-components/gpus/nvidia-reportedly-raises-gpu-prices-by-10-15-percent-as-manufacturing-costs-surge-tariffs-and-tsmc-price-hikes-filter-down-to-retailers). To trivialise slightly, the nuts and bolts are cheaper than the ephemeral bits needed to hallucinate your next image featuring a mashup of a famous person with distincitvely pope-esque clothing.

--------------

As promised, now allow me a bit of an analysis. to understand why hardware is becoming relatively cheaper, we need to examine what software has actually become. Starting from [Enshittification](https://www.versobooks.com/en-gb/products/3341-enshittification): platforms first serve users well, then abuse users to benefit business customers, then abuse everyone to maximise short-term profits. 

Consider the operational overhead that Lipton alludes to. Modern software development doesn't just require more computational power; it requires participation in [what Shoshana Zuboff calls "surveillance capitalism"](https://www.hbs.edu/faculty/Pages/item.aspx?num=56791). Every API call to a cloud service, every dependency on a SaaS platform, every integration with a third-party tool is, in all intents and purposes, a surrender of agency to what [Bentham would have recognised as a perfect panopticon](https://www.brown.edu/Departments/Joukowsky_Institute/courses/13things/7121.html). 

Software developers, ironically, have become the inmates of their own digital prison, constantly monitored and optimised by the very platforms they depend on to do their work.

This creates a peculiar form of what Graeber would identify as "spiritual violence", the psychological harm that comes from knowing your work serves no genuine purpose beyond feeding the great data-extraction machine. The software engineer writing yet another A/B testing framework, the DevOps specialist optimising cloud costs that exist primarily to extract rent from computational scarcity, the full-stack developer building "user engagement" features designed to maximise attention capture - these are the modern equivalents of Graeber's "box tickers" and "taskmasters", trapped in roles that feel both essential and fundamentally hollow.

On the flip side, I see the democratisation of digital fabrication tools as a rare example of technology serving human agency rather than undermining it. Unlike software platforms that lock users into proprietary ecosystems, these tools produce tangible outputs that exist independently of their creators' business models.

Hardware development is becoming less hierarchical, less dependent on massive capital investments, and more accessible to individual practitioners. A mechanical engineer with a low-cost 3D printer and open-source CAD software can prototype and iterate on physical designs in ways that would have required entire manufacturing facilities just two decades ago.

When a hardware engineer designs a physical object, they create something that exists-in-the-world, regardless of whether the company that employs them continues to exist, whether the platform they use remains profitable, or whether their subscription remains active. Software, by contrast, has become increasingly ephemeral, dependent on vast networks of digital infrastructure that can disappear with a change in ToS.

The conventional narrative frames this as a productivity story: AI tools make software developers more efficient, so companies need fewer of them; therefore, salaries might plateau, while those of hardware engineers maintain their value. But this misses the deeper point. The (questionable) efficiency gains from AI coding assistants come at the cost of increased dependency on proprietary platforms and computational infrastructure. [Not to mention that so-called _vibe coders / AI-enabled devs_ actually are around 19% slower than their counterpart](https://metr.org/blog/2025-07-10-early-2025-ai-experienced-os-dev-study/).

Case and point, so-called vibe coder platforms quietly raise prices overnight, upsetting the vibe crowd (and no-code startups).

One final riff on Lipton's argument. Hardware isn't just becoming cheaper than software in absolute terms. It's becoming a more effective way to capture and realise value in an economy increasingly dominated by rent-seeking platforms. Physical products can't be enshittified in the same way digital products can (that doesn't mean they categorically cannot - looking at you [Sonos](https://en.community.sonos.com/controllers-and-music-services-229131/app-update-broke-the-system-tech-supported-admitted-the-features-are-broken-6894331)). 

If hardware development offers a path toward less alienated forms of (technical) work, then the relative shift in costs represents a political opportunity. The maker movement, the open-source hardware community, and the distributed manufacturing networks that Lipton alludes to are alternative social relations, not necessarily outside of the capitalistic/neoliberalist framework, but arguably an improvement on it.

This doesn't mean software development is doomed or that all digital work is inherently alienated. But it does suggest that the current trajectory toward ever-greater computational requirements, platform dependency, and surveillance integration is neither inevitable nor sustainable. The same AI tools that are making software developers more "productive" are also making them more replaceable, more monitored, and more dependent on infrastructure they don't control.

Lipton's observations encapsulate a symptom of what happens when an economy becomes too abstract, too divorced from material reality, too dependent on artificial scarcity and platform control. Software, which began as a tool for human empowerment, has become a system of human control. Hardware, which was once the domain of massive industrial capital, is becoming accessible to individuals.

I'd go as far as saying that the future belongs not to those who can manipulate the most abstract symbols but to those who can create things that actually work in the real world, while restoring meaningful work as a radical alternative to digital feudalism.

[^1]: I've used Indeed.com average salary calculator, set to Greater London. I know, not exactly profeshunal, but good enough for back-of-the-napkin calculations.