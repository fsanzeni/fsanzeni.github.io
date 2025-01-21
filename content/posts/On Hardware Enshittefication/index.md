+++
title = 'On Hardware Enshittefication'
date = 2025-01-21T12:33:00
summary = "A notoriusly good 3D printer manufacturer decided to alienate their customer base py pushing unnecessarily restrictive firmware updates."
showSummary = true
categories = ["Blog",]
tags = ["rambling","strategy","hardware"]
+++

Bambu Lab, a relatively recent darling of the 3D printing world, has joined the pantheon of tech companies adopting the tradition of hardware enshittefication. Their latest move - [a firmware update on January 16, 2025](https://blog.bambulab.com/firmware-update-introducing-new-authorization-control-system-2/) - introduced “security measures” so unconvincing they might as well have come with air quotes and a side of contempt (I’ll be using air quotes liberally throughout this post, please do read them with irony). Ostensibly designed to “protect users”, the update added an authentication mechanism that smells suspiciously like nerfing capabilities that customers paid for.  

The backlash was swift, as it always is when you poke a once-loyal, now-betrayed user community. The update sparked outrage over its potential to hobble third-party slicer software like the excellent [OrcaSlicer](https://github.com/SoftFever/OrcaSlicer). It left users wondering how long it would be before their shiny Bambu printers became cloud-dependent bricks. Enter Louis Rossman, YouTube’s consumer rights activist, [who wielded righteous indignation to rally the troops](https://youtu.be/aIyaDD8onIE). Faced with an angry mob, Bambu Lab scrambled to reassure everyone that their new “Bambu Connect” platform would still allow third-party software and offline operation - but you would still have to register to their online service to set up the printer. Also, most offline functionality is now locked behind an opt-in 'Developer Mode'.

I remember early discussions when their printers came to the market about their, let’s call them _less than ideal_ tactics: their automatic filament changing add-on has RFID readers to ‘verify’ matching tags in first-party filament spools. Foreshadowing much? Anyways, [that system has been reverse engineered too](https://www.reddit.com/r/BambuLab/comments/1gyf242/rfid_tag_encryption_reverse_engineered/?rdt=40735). 

{{< figure
    src="bambulabRFID.jpeg"
    alt="Teardown of Bambu Lab's AMS"
    caption="When you crack open Bambu Lab's AMS you'll be ~~pleasantly~~ surprised to see RFID readers (the circle-shaped copper coils on either side) to match the tags in the filament spool. I can stretch my thinking and understand that this feature allows for automatic profile/settings switching in the slicer, but in this case it was simply a foreshadowing of what would come down the line."
    >}}

Bambu Lab isn’t the first company to tread this path of undermining customer autonomy for a quick buck. It’s a cliche at this point: take a product that works perfectly fine, add unnecessary restrictions, call it “progress” or [insert corpo-speak here], and pray nobody notices.  

Remember when Apple unceremoniously ditched the headphone jack in 2016, insisting it was a brave leap forward? Sure, if by “brave”, they meant shoving millions of users into proprietary and absolutely unfixable (aka soon-to-be landfill) AirPods. Or take John Deere, which transformed tractors into DRM-riddled techno-prisons that farmers can’t repair without corporate blessing. Even Keurig introduced DRM on their coffee pods in 2014, trying to stop customers from using cheaper, white-labeled alternatives. Because nothing screams innovation like locking people out of their morning coffee.

{{< figure
    src="keurigDRM.webp"
    alt="Error message on a Keurig coffee machine when using alternative coffee pods."
    caption="I don't have much to add to this hilarious image."
    >}}

And let’s not forget the grand tragicomedy of printers - HP, Canon, Epson - who have all, at some point, decided that ink should cost more than blood. Firmware updates to block third-party cartridges? Check. Software that reports nonexistent maintenance issues to force you to buy replacements? Double check. It’s a masterclass in finding new ways to turn customers into hostages. [^1]

Allow me a rant. Everything from cars to toasters is now “smart,” which really means “we can turn it off whenever we feel like it” or “we can change the ToS and basically brick your device remotely”. Tesla owners found this out the hard way when the company started charging to unlock features already physically built into their cars. Similarly, the unfortunate trend in consoles and other videogame hardware is to remove options for physical disks (looking at you, PlayStation 5 Digital Edition) or, more in general, physical media.

The folly of moves like Bambu Lab’s is that they target the wrong audience. Your average 3D printing enthusiast isn’t some casual consumer who bought a gadget on a whim - they’re professionals, DIYers, and tinkerers who *chose* your product because it empowered them to make things their way. These folks will void warranties without skipping a beat if it means improving functionality. They’re not just customers; they’re collaborators, evangelists, and, critically, the people who shape the narratives around your brand.  

The same applies to farmers fighting John Deere’s repair lockdowns or prosumers who flocked to open-source platforms to escape the constraints of proprietary ecosystems (remember when Autodesk changed their licensing for Fusion360 and the exodus towards open-source alternatives?). These groups prize autonomy, transparency, and the ability to solve problems on their own terms. By locking down your ecosystem, you’re not offering security or innovation - you’re waving a red flag in the face of the very people who value your product for what it *could be*, not what you want to limit it to. 

At the heart of enshittefication is a paradox: companies implement these strategies to maximise profit, but they often erode the very customer loyalty that made them successful in the first place. What Bambu Lab (and its ilk) fail to grasp is that ecosystems feed on trust, not coercion. Definitely, [issuing a semi-gaslighting press release was not the most tactically savvy thing to do](https://blog.bambulab.com/updates-and-third-party-integration-with-bambu-connect/).

But no. Like so many others, they chose the path of least imagination and greatest irritation. The result is a cautionary tale for folks working in strategy and a grim reminder for users: the products we love don’t belong to us - they belong to the companies who see us less as customers and more as an ongoing revenue stream.  

Alienating your customer base _never_ ends up in meadows and rainbows. A bad move with tinkerers? They’ll reverse-engineer your hardware, fork your software, and post the workaround online before you’ve finished drafting your press release. Upset farmers? They’ll lobby lawmakers, file lawsuits, and spark a right-to-repair movement undermining your business model. Frustrate prosumers? They’ll flock to your competitors.  

Bambu Lab’s botched update is a sad reminder of how not to engage with a technically-minded audience. They could have strengthened their market position and maintained their following if they had leaned into _what their customers expect and bought the printer to begin with_ (wild concept, I know). Instead, they risk becoming just another name in the cautionary tales of enshittefication.  

So here’s to the next firmware update, the next subscription fee, and the next set of proprietary dongles. Enshittefication marches on, one locked door at a time.

[^1]: Of course, [clever people have devised ways to get around these artificial restrictions](https://hackaday.com/2024/09/28/man-in-the-middle-pcb-unlocks-hp-ink-cartridges/). Better yet, if I can offer modest advice, get yourself a laser printer that is a decade old - they’re built like tanks (albeit slower) and don’t have these silly DRMs.