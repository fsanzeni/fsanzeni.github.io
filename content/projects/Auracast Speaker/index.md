+++
title = 'Auracast Bluetooth Speaker'
date = 2025-01-02
summary = "Trials and tribulations in developing a Bluetooth speaker ecosystem."
showSummary = true
categories = ["Post","Project",]
tags = ["bluetooth", "audio development", "product design", "consumer electronics", "speaker technology"]
+++

# The Concept
I was rooting around my ideas backlog and, by pure coincidence, I happened to be working (in my day job) at a horizon scan and technology readiness audit piece. In both my catalogue and work one technology stood out: Auracast.

It's kinda fringe for now, mainly used in hearing aids and experimental concert venues. It's an extension of the Bluetooth stack and, unlike "traditional" Bluetooth, it allows for streaming audio from one source to multiple sinks without having to worry about synchronisation. Pretty cool.

Also, I might be a bit of an audiophile (the nerdy kind, not the oxygen-free cables kind). I listen to music for the vast majority of my waking time, but after a while I tend to change my headphones - going from in-ears to over-ears, so that I mix things up a bit (and because after a while my ears need a break from the warmth). 

I also work from home a bunch, which means that, technically, I could have a loudspeaker on. I do have a listening setup in the common room, but it's not exactly portable. To seal the deal, I recently purchased an IKEA outdoor light/speaker - the Vappeby - and I was honestly blown out by how good it sounds for its size and arrangement (single, bottom-firing driver).

So, obvious segue, I should design something similar that I could pepper throughout my house, so I don't have to lug speakers around. I'd also like the speaker to look nice and *demure* in the house. Or maybe a statement piece, I'm not sure yet.

Anyways, that's the background. My design constraints are:
- Simple construction
- Mono audio, stereo/surround when multiple devices are paired together
- Battery operated
- Decent (8-hour-ish) playback time

## Proof-of-concept
This is what I'm working on at the minute. I'm using the FSC-BT1038B module from Feasycom, mainly because I don't want to sink in the ECAD-time to whip up a IC bringup board. With just a few hours of work I have a sensible design to test. You can follow along in this GitHub repo:
{{< github repo="fsanzeni/FSC-BT1038B-Barebones-Breakout" >}}

A few considerations:
- I've used a bunch of odd components (namely, the USB port and tactile switches) mainly because I have them lying around. I got them from LCSC.
- The FSC-BT1038B datasheet asks for a specific LDO which I didn't have in stock. It's supposed to be very low noise at 300mA. I've substituted fros an AMS1117-3.3v as I have plenty of those.
- I've broken out *all* the pins and grouped them in headers to kinda make it easy to attach external modules. This means some pins are duplicated (e.g., the MIC/LINE ones). I still expect folks to give the datasheet a peruse to familiarise yourselves with which ports can be used at the same time.
- The boards are 4 layers (signal - ground - 3.3v - signal), just because I didn't want to spend too much time figuring out how to route the various power supplies in a sensible way. I'm sure the design could be optimised for a 2 layer board.
- I didn't bother using differential routing for the USB (also, the pins are criss-crossing for some reason). This shouldn't be a problem at all, since the speeds are really limited - but, yes, it's not best practice.

## Update #1
The board works. All peripherals, AT commands, voltage regulation, buttons, etc. One small issue: I jumped the gun. The BT1038B does not support receivinbg Bluetooth Classic while rebroadcasting BLE Audio. So it works perfectly as a Bluetooth (classic) streamer OR a BLE streamer. Not both. I'm re-designing a new board witrh another Feasycom SoM that should support both modes at the same time:
{{< github repo="fsanzeni/FSC-BT631D-Breakout" >}}

As some extra goodies, you'll find in the same repo the schematic and layout for a 30W amplifier based on the [TPA3129D2](https://www.ti.com/product/TPA3129D2) ic and a DSP board based on the [ADAU1701](https://www.analog.com/en/products/adau1701.html) ic.
