+++
title = 'On Supply Chain Fragility'
date = 2025-07-21T16:58:00
summary = "Reflecting on supply chain fragiliy (with examples) && the limits of decentralised manufacturing."
showSummary = true
categories = ["Blog",]
tags = ["rambling","strategy","hardware"]
+++

In April 2025, the Iberian Peninsula went dark. Days earlier, the world was still reeling from another round of semiconductor shortages. At first glance, these appear to be isolated incidents: one an energy infrastructure failure, the other a supply bottleneck. But they both point to a deeper fault line. Our finely tuned, globally distributed production system is brittle in all the wrong places.

We’ve been told for years that we live in an age of hyper-efficiency. That costs have been optimised, lead times slashed, and markets made more agile. But underneath that (fragile) veneer lies a system where critical components come from one place, made by one company, with no backup plan in sight.

Riffing on last week’s post on how hw is getting (well, already is) cheaper than sw, I reflect here on how the world has become more dependent on physical goods at precisely the moment those goods have become harder to build, ship, or replace. Sounds like a sweeping generalisation, but stick with me for the rationale.

There is only one company in the world that makes the machines needed for the most advanced semiconductor chips. It’s called [ASML](https://www.asml.com/en). It’s based in the Netherlands. And it controls the keys to modern computing.

These machines - [EUV lithography systems](https://www.youtube.com/watch?v=RmgkV83OhHA) - aren’t sold by the dozen. Each one takes years to build and costs hundreds of millions of dollars. Every NVIDIA AI accelerator, every smartphone processor, every piece of cutting-edge silicon depends on machines that exist in exactly one place on Earth, manufactured by a single company with a 30-year development timeline. When TSMC, which produces 54% of all semiconductors globally, depends entirely on ASML’s machines, we’re looking at a supply chain that would make a medieval guild master weep with envy. Classic [chokepoint]( https://chokepointcapitalism.com/).

This didn’t happen by divine right or superior business acumen. ASML’s dominance grew out of a mix of historical quirks, deep R&D funding, and long-term industrial policy. They were in the right place with the right partners at a time when everyone else was busy offshoring.

That monopoly has geopolitical weight. If (or, better, when) the Dutch government blocks ASML from exporting to China, the ripple effects stretch across geographical boundaries. The world’s reliance on ASML is not an accident. But it wasn’t exactly planned either. I’m not trying to be over-dramatic or grandiose, _but_, this situation represents a new form of technological sovereignty that transcends traditional military or economic power. Control the lithography machines, control the future of computing.

## Fragility in Plain Sight
The April 28, 2025, blackout across Spain and Portugal provides a perfect case study in how centralised infrastructure dependencies create cascading failures. Something somewhere failed, [and there are several potential explanations](https://www.theguardian.com/environment/2025/apr/29/what-caused-the-blackout-in-spain-and-portugal-and-did-renewable-energy-play-a-part). Within seconds, the electrical grid across Spain and Portugal collapsed. I’m not here to debate the merits of one theory vs another. What piqued my interest when reading about what happened, [was this specific article]( https://watt-logic.com/2025/05/09/the-iberian-blackout-shows-the-dangers-of-operating-power-grids-with-low-inertia/). Seriously, read the article – it’s beautifully written and goes into a lot of detail that I’m omitting here.

TL;DR – the grid, and specifically its transformers, needed upgrading. Better late than never, you might think, BUT… [Spain can’t source transformers quickly (or any other country in the world, to be honest)]( https://www.cea3.com/cea-blog/transformer-bottleneck). Not even close. Replacement units wouldn’t arrive for years.

_Years_.

These transformers aren’t optional. They are the foundation of the power grid. Without them, no electricity. And without electricity, no modern society. Yet global wait times for medium and high-voltage transformers have ballooned. In some cases, they now exceed 200 weeks.

## Localised Dominance, Global Risk
China’s dominance in transformer manufacturing reveals how what appears to be a diversified global supply chain can actually represent a single point of failure disguised as geographic distribution. [Sinovoltaics’ map of Chinese transformer factories shows 128 manufacturers across multiple provinces]( https://sinovoltaics.com/sinovoltaics-press-releases/march-2025/sinovoltaics-launches-mainland-china-transformer-factory-map-to-help-solar-developers-overcome-transformer-supply-bottlenecks/). Perhaps an impressive diversity, until you realise they’re all subject to the same government policies, trade restrictions, and supply chain bottlenecks.

The situation becomes even more problematic when considering supply chain security. Relatively recent investigations have revealed [Chinese-manufactured transformers with hidden backdoor capabilities]( https://www.forbes.com/sites/llewellynking/2021/01/28/how-the-supply-chain-in-heavy-bulk-power-equipment-is-vulnerable-to-undetected-cyberattack/) that allow remote shutdown from overseas. This isn’t paranoid speculation; it’s documented [in quite some detail, as you can read for yourself here]( https://securethegrid.com/chinese-transformer-complaint-filed-with-u-s-government/).

The security implications cascade beyond simple sabotage concerns. When transformers take three years to replace and the primary manufacturers are located in countries with complex geopolitical relationships, every grid operator faces an impossible choice: accept potential security vulnerabilities or accept potential multi-year recovery times from natural disasters or targeted attacks. Now replace ‘grid operator’ with whatever critical infrastructure you can think of.

In other words, this lose-lose situation creates _manufactured vulnerability_. In this situation, the pursuit of cost optimisation and global efficiency has created systemic risks that no individual actor can address through market mechanisms alone. Utilities can’t simply decide to buy American-made transformers if American manufacturers don’t exist or have even longer lead times. The same applies to UK companies, Italian ones, and so on.

## The Limits of Local Production
If you’ve read this blog before, you’ll know I am a huge supporter / proponent of decentralised manufacturing. Spread out production. Rely (or, even better, build!) on local manufacturing. In theory, this reduces risk.

There’s real appeal in that idea. A world filled with 3D printers, CNC mills, and local fabricators sounds flexible. It sounds empowering. It sounds like resilience.

In practice, this works well for phone cases, machine parts, or architectural models. But it doesn’t scale well to complexity. My own rhetoric does not scale to critical / national infrastructure.

Transformers require certified materials, decades of warranty-backed performance, and adherence to strict, regulated standards. No one’s building these in a garage, no matter how sophisticated the printer.
And semiconductors? Forget it. The tools needed to make chips depend on global supply chains that are even more intricate than the devices they produce. You can’t decentralise photolithography the way you can decentralise toy manufacturing.

The strength of the maker movement lies elsewhere. It creates breathing room. It builds small-scale autonomy. It offers backup paths when primary systems fail. These are safety nets ([remember the 3D-printed PPE during COVID?](https://www.sciencedirect.com/science/article/pii/S2666964121000370)).

## Supply Chains as Instruments of Power
Breaking free from these dependencies requires more than market solutions or technological fixes. It requires a fundamental rethinking of how we organise production, manage risk, and balance efficiency against resilience. The maker movement and distributed manufacturing represent important experiments (emphasis on the word _experiment_) in technological autonomy. Still, they’re not sufficient by themselves to address the systemic vulnerabilities of centralised production.

The real solution requires political interventions: conscious decisions to prioritise (technological) sovereignty over short-term cost optimisation, even when those decisions appear economically inefficient from a purely market perspective. The alternative is continued dependence on supply chains that can be disrupted by everything from natural disasters to geopolitical conflicts to corporate decisions made thousands of miles away. Or a boat jamming itself somewhere in the Suez Canal.

Upon reflection, the question isn’t _really_ whether decentralised manufacturing will replace centralised production, but whether communities and countries will build the institutional capabilities necessary to maintain technological autonomy in a world where supply chain control has become a weapon of statecraft.

Resilience now demands investment in _inefficient_ things. Domestic factories. Strategic reserves. Redundant suppliers. There’s no shortcut here. Only choices.