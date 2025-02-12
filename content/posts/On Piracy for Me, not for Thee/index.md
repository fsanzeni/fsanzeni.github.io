+++
title = 'On "Piracy for Me, not for Thee"'
date = 2025-02-12T14:19:54
summary = "LLMs, institutionalised piracy and other good things all add up to slop. Let's dissect Meta's latest blunder."
showSummary = true
categories = ["Blog",]
tags = ["rambling","genAI","innovation"]
+++
# The Context
Meta [torrented 81.7 terabytes of pirated books](https://arstechnica.com/tech-policy/2025/02/meta-torrented-over-81-7tb-of-pirated-books-to-train-ai-authors-say/) from shadow libraries like Z-Library, LibGen, and Anna’s Archive to train its AI models like LLaMA. This wasn’t a one-off - [court documents reveal Meta previously downloaded another 80.6TB from LibGen alone](https://cdn.arstechnica.net/wp-content/uploads/2025/02/Kadrey-v-Meta-Plaintiffs-Motion-for-Relief-2-5-25.pdf). To put this in perspective, that’s equivalent to approximately 45e+10 (that reads as more than forty-five billion) pages of scanned books[^1]. 

But Meta, besides riding the 777 seas, didn’t just download - they actively concealed their tracks. Employees avoided using company servers, switched to VPNs, and joked about the illegality. One engineer wrote, “Torrenting from a corporate laptop doesn’t feel right”, while others debated ethics, comparing LibGen to The Pirate Bay. Even CEO Mark Zuckerberg was implicated: internal emails show the decision to use pirated data was escalated to him, contradicting his public denials.

{{< youtubeLite id="gKNvLyxHTmg" label="I know that the reference to those '777 seas' is obscure at best, so here's the reference. Razor 1911's work on cracktros is some of the finest put there. And this tune is straight up bangin." >}}

## The Power Imbalance: Internet Archive vs. Meta’s Corporate Piracy

This news (scandal?) highlights the hypocrisy in how copyright laws are enforced. The [Internet Archive](https://archive.org/), a nonprofit digital library, has faced relentless lawsuits for lending scanned books under controlled “digital borrowing” models. Publishers like [Hachette, HarperCollins, Wiley, and Penguin Random House sued it for “mass copyright infringement,” arguing that even limited lending harms sales](https://www.eff.org/cases/hachette-v-internet-archive). Yet Meta - a trillion-dollar corporation - downloaded terabytes of pirated content with near-impunity, adding insult to injury by masking its actions to avoid accountability. Irony? More like corporate kleptocracy.

The Archive’s crime? Letting you “borrow” a PDF like it’s 1989. Meta’s crime? Swiping literal billions of pages to feed the AI machine that spits out derivative slop, threatening the same writers whose work it regurgitated. The takeaway, _ça va sans le dire_, is that if you’re a trillion-dollar company, piracy isn’t theft - it’s R&D. If you’re a grad student downloading a textbook? Straight to copyright jail.

{{< figure
    src="straight-to-jail-meme.jpg"
    alt="Straight to jail meme."
    caption="Pirate a book? Straight to jail."
    >}}

Meta’s internal communications read like a dark comedy. Employees debated ethics while torrenting, with one researcher calling it “beyond our ethical threshold”. Yet they proceeded, operating in so-called _stealth mode_ to avoid detection. The company even messed with their Torrent client settings to avoid seeding, ensuring they wouldn’t redistribute content - making them not just pirates, but _leeches_. In Torrent parlance, that’s like taking the last slice of pizza and ghosting the chat. For a company built on “community”, their P2P etiquette is worse than a live-action adaptation of an anime[^2].

## Leechers in Suits and the Hypocrisy Machine

Meta’s actions are part of a broader trend. OpenAI, Nvidia, StabilityAI and others face lawsuits for training AI on copyrighted works ([see here for an up-to-date tracker of all the lawsuits happening at the moment](https://www.bakerlaw.com/services/artificial-intelligence-ai/case-tracker-artificial-intelligence-copyrights-and-class-actions/)). The stakes are - to the risk of sounding bombastic - _existential_ for writers: AI models trained on pirated books can churn out derivative stories, obviously endangering livelihoods with machine-generated slop.

Worse, AI could enable corporations to bypass human creators entirely. Imagine studios using AI to generate entire fictional universes - à la Harry Potter or Bionicle - then monetising toys, films, and merch without paying a single author. Yes, this is speculation, [as a judge dismissed claims on risks of future damage to intellectual property as too speculative](https://www.theverge.com/2024/2/13/24072131/sarah-silverman-paul-tremblay-openai-chatgpt-copyright-lawsuit). Yet, I argue this future isn't too far away or inconceivable.

I'm not trying to crystallise the debate into a binary good/evil. The underlying issue is, well, complicated: who gets to profit from humanity’s collective knowledge? Shadow libraries like LibGen emerged to bypass paywalls and democratise access to knowledge, but Meta (and I'm pretty sure all the other GenAI companies) co-opted them for corporate gain.

## LLMs and [checks script] _Innovation_?

Let’s cut the techno-optimist crap. AI trained on pirated books is copyright sleight-of-hand. As a side effect, writers aren’t just competing with AI, they’re competing with their own pirated words. Romance novels [(18% of adult fiction sales)](https://fortune.com/2021/08/21/rom-com-pandemic-book-sales-romance-bookstore-day/) are [low-hanging fruit for algorithms](https://www.bbc.co.uk/news/business-64975524)[^3], but even academic papers aren’t safe. 

Imagine a future where Elsevier charges $29 (or more) for a paper written by a bot trained on pirated research. Oh wait, [that’s already happened](https://www.sciencedirect.com/science/article/pii/S2468023024002402).

## Chokepoint Capitalism and Fighting Back

Meta’s piracy spree is a masterclass in chokepoint capitalism. For the uninitiated, chokepoint capitalism is the art of monopolising markets by controlling critical bottlenecks, squeezing workers and creators dry while hoarding profits ([I din't invent the term, Giblin and Doctorow did. Their book is well worth a read](https://chokepointcapitalism.com/)). Think Amazon strangling book publishing, Spotify finessing musicians, or Live Nation monopolising concert venues.

Meta’s playbook is classic chokepoint strategy:

1.  Lock in the supply by filling your digital coffers with scraped data in an effort to monopolise training data for AI models.
2.  Eliminate competition by arguing that scraping copyrighted works is “fair use,” a legal loophole smaller players can’t afford to exploit[4^].
3.  Extract value by getting paid for a service you built on others' work, all while Zuckerberg schmoozes with politicians to keep regulators at bay.

The real crime here isn't Meta doing it - but if they got away with it. But there is hope. The Internet Archive still fights. Authors are suing. We must demand radical transparency from AI companies, insisting they disclose the precise sources of their training data instead of hiding behind “fair use” hand-waving. At the same time, writers, coders, and creatives need to unite - whether through forming unions or coordinating collective legal action - to secure fair licensing deals or to challenge corporate overreach by suing en masse. And finally, we must decentralise control by supporting independent libraries, not as piracy hubs, but as vital antidotes to corporate domination.

*This work licensed under CC BY 4.0. Pirate responsibly.*

[^1]: This is calculated as [an average of 2kb per page of text - corresponding to about 500 words (if ASCII-encoded. The difference with UTF-8 should be minimal)](https://superuser.com/questions/351791/what-is-a-general-rule-of-thumb-for-file-sizes-in-kb-mb-gb-etc)

[^2]: I still shudder thinking about ~~_that_ adaptation of Dragon Ball~~.

[^3]: But how much money are we talking about here, really, I hear you cry from the back of the room. You'd be surprised to learn (at least, I was) that (18% of the global fiction market corresponds to roughly $2 billion)[https://www.thebusinessresearchcompany.com/report/fiction-books-global-market-report].

[^4]: For a very thorough read on the subject, I cannot recommend Sobel's article [Artificial Intelligence's Fair Use Crisis](https://www.bensobel.org/files/articles/41.1_Sobel-FINAL.pdf). Just to note, _this essay was published in 2017, the same year in which Google's [Attention is All You Need](https://arxiv.org/abs/1706.03762), the paper that introduced Transformers - the architecture that enables virtually all modern GenAI systems - came out._ People have been shouting about the very issues I discuss here for *a very long time*.