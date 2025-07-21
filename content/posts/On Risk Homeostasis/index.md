+++
title = 'On Risk Homeostasis'
date = 2025-01-03T09:09:00
summary = "Jump into my latest rabbit hole: risk homeostasis theory, or, why we can rethink risk in strategy (and software development)."
showSummary = true
categories = ["Blog",]
tags = ["risk theory", "strategy", "software development", "risk management", "behavioural economics"]
+++

Over this winter break, I went down a bit of a rabbit hole, prompted by this excellent talk by Peter van Hardenberg on why we can’t avoid writing complex software (video embedded after the break). In the talk, Peter brings up something I never heard before: risk homeostasis. As a keen cybernetician and strategist, my spidey senses tingled – mainly because of the shame of never coming across the term. Allow me a couple of definitions and references:

- The risk homeostasis theory posits, in essence, that a control mechanism analogous to the thermal homeostatic system in warm-blooded animals tends to keep risk per unit time constant, and, as a consequence, the number of traffic accidents per unit time of driving also tends to remain constant, essentially independent of changes in the traffic safety system. [Reference](https://doi.org/10.1111/j.1539-6924.1986.tb00196.x).
- In essence, the theory holds that it is the target level of risk, rather than the absolute level of environmental risk, that determines accident loss. RHT therefore posits a population-level closed-loop process in which target and actual risk are compared. [Reference](https://www.sciencedirect.com/science/article/abs/pii/0925753596000070).

In other words (and going beyond the transport safety subject), risk homeostasis suggests that each of us has a personal threshold for how much risk we’re comfortable taking. When something shifts our perception of safety, we tend to adjust our behaviour to maintain a steady level of what we consider “acceptable risk.”

Now, let’s talk about software. There’s this thing Peter calls “complexity homeostasis”. You start a new (obviously SaaS) product and ship it. Its codebase is neat and well-maintained. Then, you start adding features and teammates. At first, everything’s cool, but eventually, it becomes a tangled mess, and you refactor. So, you simplify things, and it feels great. But then, as you keep adding features or making changes, the complexity creeps back in, and you’re back where you started.

It’s like we have this internal threshold for how much complexity we’re willing to deal with. When things get too complicated, we take steps to simplify. But once it’s simple again, we don’t stop; we keep adding more until it gets complicated again. 

Just like with road safety and software development, it struck me that we might unconsciously maintain a certain level of complexity within organisations and in strategy. Organisations naturally accumulate layers of processes, policies, and teams as they scale. At first, this feels like progress – each new addition addresses a specific need or fills a perceived gap. But over time, communication slows, silos emerge, and decision-making becomes cumbersome, involving several decision-makers across the organisation. 

That’s when leadership calls for a “reorg,” shedding layers of complexity to regain agility – like a phoenix, to burn it all down (yes, yes, metaphorically) to reemerge nimble. But just like in software, this simplification is rarely permanent. Freed from their previous constraints, organisations soon begin layering on new complexities, repeating the cycle.

Contrast that with strategy, where complexity homeostasis plays out more abstractly. A strategy (hopefully) starts as clean and focused – a vision, a goal, a clear path forward. Over time, though, as market conditions shift or new opportunities emerge, the strategy often accrues “add-ons”. New KPIs, adjacent goals, and tangential initiatives creep in. Before long, the strategic vision is muddied by competing priorities and internal politics. 

At this point, companies might declare a strategy reset, reducing the clutter to refocus. The paradox is that while organisational design is constrained by structure and operations, strategy starts from ideas and intentions. Here, the risks of overcomplication are harder to detect.

You can see the bloated org chart or the sluggish workflows and identify them as symptoms of excess, whereas strategic complexity often hides in plain sight, cloaked in corpo-jargon and PowerPoint decks. A strategy might sound sophisticated because of its complexity, but in reality, it’s a word salad.
That said, perhaps both domains share an underlying driver: our discomfort with simplicity. In organisations, there’s often an implicit belief that “more” equals progress – more teams, more processes, more sophistication. In strategy, the allure of complexity can come from wanting to appear thorough or future-proof. Yet, in both cases, complexity isn’t inherently bad; it becomes problematic when it’s unconscious, unmanaged, or left unsaid.

When it comes to large companies, complexity isn’t just a side effect – it’s practically baked into the business model. After all, it takes a lot of people, processes, and politics to keep the corporate machine purring. But let’s get one thing straight: scale is not a virtue in itself. A big organisation isn’t inherently better; it’s just harder to steer. Yet somehow, we’ve arrived at a world where “how many employees we have” or “how many countries we operate in” is treated like a badge of honour. Spoiler alert: size alone isn’t a KPI - it’s a side effect. Outcomes and outputs should be the real focus, but they’re often buried under layers of quarterly reports.

Think about it: we don’t applaud a city for having more traffic lights than its neighbour; we measure it by its liveability. Why, then, do we celebrate companies for their headcount instead of their impact? A sprawling org chart might look impressive on LinkedIn, but what’s the point if it takes three meetings, two approvals, and a ritual sacrifice to deploy a minor product update?

The irony is that large companies often mistake activity for effectiveness. They’re so busy managing the machinery of their size that they forget why they scaled in the first place: to deliver value. When was the last time you heard a customer say, “I love this brand because they’ve got so many regional VPs”? Exactly.

Complexity in large organisations isn’t inherently evil but should serve a purpose. If complexity enables better outcomes – more resilient systems, faster innovation, broader impact – great. But more often than not, complexity serves complexity. Bureaucracy grows to support bureaucracy. Meetings beget meetings. Teams spring up to manage the mess created by other teams. And the worst part? We normalise it.
Here’s a snarky reality check: if your company’s biggest competitive advantage is its ability to staff a project team with 40 people in three time zones, you’re not competing - you’re compensating. A nimble startup with 10 people and a clear mission can run circles around that kind of inertia [(shameless plug for my previous post)]({{< relref "posts/on-institutional-inertia" >}}). 

The solution isn’t to downsize for the sake of downsizing or to fetishise the startup mentality. It’s to refocus on what matters: outcomes and outputs. Ask yourself: What’s the minimum structure we need to achieve our goals? How can we avoid the gravitational pull of unnecessary complexity? And, most importantly, how do we keep [insert your goal here] at the centre of everything we do?

Allow me to go back to the literature to conclude this ramble. Wilde’s RHT model [(1988, proposition 2)](https://www.tandfonline.com/doi/abs/10.1080/00140138808966691) outlines three paths to achieving this homeostasis: adjusting behaviours within the current environment, switching modes entirely (technically called mode migration), or outright avoidance.

In software, when systems become safer or simpler, we often “spend” that safety by layering on new features or risks until we hit our perceived threshold of complexity. Similarly, organisations toggle between adding structure and stripping it back, chasing a balance between agility and stability. And in strategy, we rub shoulders with complexity, only to periodically step back and reset when clarity is lost.

Wilde’s framework offers a compelling invitation to rethink this relationship with risk: it doesn’t remain an open wound; it scabs over and integrates into the fabric of our decisions. After the initial turbulence, systems - be they human or organisational - tend to stabilise. 

The real danger in strategy isn’t risk itself; it’s inertia. Playing it safe often leads to stagnation, missed opportunities, and an organisational culture that fears failure more than it values innovation.

Consider the behavioural adjustments Wilde mentions: when risk increases, we adapt. A driver in stormy weather might grip the wheel more tightly, lower their speed, or increase following distance. Similarly, a company exploring an adjacent market might acquire talent, test smaller initiatives, or build partnerships to reduce exposure (and, often, costs).

And then there’s mode migration. In strategy, this could mean pivoting from one business model to another, adopting new or more efficient technologies, or reimagining how value is delivered. These shifts may feel radical, but they’re often the very moves that define a company’s longevity (think of Netflix pivoting from DVD rentals to streaming or Apple’s leap from computers to a broader ecosystem of devices and services or even Nintendo switching from playing cards to - eventually - videogames and consoles).

Even avoidance has a place in strategy. But it should be a deliberate choice, not a knee-jerk reaction. Avoidance might mean walking away from an acquisition you FOMO’d in or intentionally exiting a market that no longer offers meaningful returns. 

Strategy isn’t about scrubbing risk out of existence - that’s just hitting pause on reality and hoping nobody notices[^1]. And if Wilde’s theory is correct, we can trust that equilibrium will find us once again. 

The talk I mentioned at the beginning:
{{< youtubeLite id="czzAVuVz7u4" label="Peter’s excellent talk on complexity in software development, which sent me down the RHT rabbithole." >}}

[^1]: There’s an interesting conversation to be had about the Nash equilibrium, but that’s for another time - for now, [check out this eloquently written paper](https://pmc.ncbi.nlm.nih.gov/articles/PMC384684/).
