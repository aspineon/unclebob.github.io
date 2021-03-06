---
layout: post
title: The Barbarians are at the Gates
tags: ["Coding"]
---


There's a revolution coming. I wonder if anyone has noticed. It's not subtle. It won't be sublime, or easy to integrate. Indeed, it'll probably muck up everything for a long long time. But it's coming nonetheless, and you'd better be strapped in and ready for the impact.

The challenge for computing is *power*. How much processing can you get done per unit of time. Over the last fifty years we've seen this power increase by a scale that we usually reserve for thermonuclear weapons, supermassive black holes, or core-collapse supernovae. We might characterize that power increase with the following formula:

> Power-increase = speed-increase \* memory-increase \* disk-increase \* watts-decrease \* volume-decrease \* cost-decrease.

This formula is woefully incomplete. We could add memory speed, and disk speed, and network interconnectivity, and a whole range of other power multipliers. But never mind that; the formula is already scary enough. When I use this formula to compare my current laptop to the PDP-8 that I used 40 years ago, I get *twenty-two orders of magnitude*. My little laptop is at least *ten septillion* (10,000,000,000,000,000,000,000) times more powerful than that PDP-8.

What do we do with those 22 zeros? A lot! I can watch HD video on my laptop streaming down from the web, and it barely utilizes one of it's four cores. I can edit high resolution video at 32,000 feet over the Atlantic, while sipping a scotch and checking twitter. I can play Dungeon's and Dragons, with dazzling video effects on three high resolution screens, in real time with dozens of people scattered around the world. So, yeah, 22 orders of magnitude seems about right.

Where has all that power come from? It's come from the hardware! The hardware designers have steadily improved our machines. For the last fifty years they've made them faster, smaller, cheaper, and better. They've created miracles in technology. They've doubled, or more than doubled the capabilities of our computers every 18 months or so[1].

In the last fifty years the hardware of computers has undergone revolution after revolution after revolution. From Vaccuum Tubes, to Transistors, to Integrated Circuits, to Solid State Ram, to Winchester disks, to Liquid Crystal and LED displays, to Ethernet, to Wifi and bluetooth. I could go on, and on.

And we software people...what have we done with all that power? Has it driven us through similar revolutions? **NO!** Quite the opposite in fact. All that dramatic increase in hardware power has allowed us software people to *avoid* any similar major revolution. We software developers have had a virtually infinite reserve of computer power laid out in front of us by the hardware developers. Every time we needed more capability, they were there with the answer. And so *our* technology -- the technology of software development, has changed very little.

You might disagree with that at first. You might object and say that software development has changed a lot over the last fifty years. And it's true, of course, that software development nowadays is quite a bit different from the 1960s. Or is it?

Consider this. Take a computer hardware designer from 1960 and transport him to 2011. Could he design modern processor chips without years of re-education? Clearly not. The technological gulf between those two eras is so vast, that the poor hardware engineer would need to start his career over from very close to the beginning.

Now do that thought experiment with a software developer from 1960. Transport him to 2011. It would take him a day or so to get over the shock. Perhaps he'd need another day or two to learn vim, or Eclipse. He might need a few weeks to learn Java or C\#. But then he'd start in writing if statements, assignment statements, and while loops just like the rest of us. He'd have to learn HTML, and XML, and Maven, and a whole suite of other tools; but he could do that on the job like the rest of us. He'd be at a disadvantage, there's no doubt about that; but he wouldn't have to start his career over; because he knows how to code; and coding just hasn't changed that much in the last fifty years. We all still use the same old tools: sequence, selection, and iteration.

The Sapir-Whorf trap
--------------------

Our computer languages are all geared towards the same thing. They view the computer as a single, hyperfast, hyperaccurate, clerk. Computer languages are simply the languages we use to direct the operation of that clerk. What's more, the most popular computer languages map cleanly to the hardware. They create an abstract image of that hardware; but are strongly related to it.

Did you know, for example, that the ++ operator in C, C++, Java, and C\# derived from the fact that there were special registers in early computers that automatically incremented their contents every time you accessed them? The compiler tried to make use of these auto-increment registers whenever you used a ++ operator.

Consider the data types in C++: int, double, char. These are, or are very closely related to, the data types of the hardware. The data types in Java and C\# are only slightly more abstract and still have a strong correlation to the underlying hardware.

The assignment statements, if statements, and loop operators in our languages are all easily mappable to machine instructions in the hardware.

In short, our languages are projections of the hardware. Some languages are more abstract projections than others; but the most popular languages, C, Pascal, C++, Delphi, Java, and C\# are very closely related to the hardware. Even langauges like Smalltalk, Python, and Ruby, while more abstract than the others, still show their hardware roots.

The reason for this is clear. The closer you are to the hardware, the faster your programs execute. Why is so much embedded work done in C and C++? Speed. Why are DSPs programmed in assembler, or C? Speed. Why is Java closely related to the hardware, even though it executes in a virtual machine? Speed.

And so our languages, like it or not, have been constrained to stay close to the hardware by (ahem) the need for speed[2]. But this leads us into a trap. The Sapir-Whorf hypothesis tells us that our view of the world is strongly affected by the languages we use. When we think in a given language, that language acts as a filter. Concepts it can't express are removed from our awareness. Our mode of expression constrains us to only those thoughts and concepts that can easily be expressed within it.

And that should make you wonder. Since we've been constrained by these close-to-hardware languages for the last fifty years, what have we been missing? What concepts have eluded us? How warped is our world view?

We're about to find out.

There's a Freight Train Coming.
-------------------------------

A few years ago hardware engineers hit a brick wall known as the speed of light. Signals can propagate at 3E8 meters per second at most. That's about 1ns per foot. For the last fifty years clock rates had been doubling every 18 months; but in the early 2000s that stopped cold, and it'll never start up again. From now on, computer chips will *not* be getting much faster. Oh we might see some new materials that give us a speedup. -- Maybe. But the exponential curve of 2X every 18 months is over. It'll never be back.[3]

But density is another matter entirely. Chips are still getting exponentially denser, even if they aren't getting much faster. What's more, there's no reason that density has to be limited to a chip. If we have to, we can cram lots of chips on boards, and lots of boards in boxes, and lots of boxes in rooms. And we have lots and lots of rooms. So the amount of computer power a room can contain is vast. We haven't even begun to scratch that surface.

But this leads to the dilemma. This is why the barbarians are at the gates. This is why those languages that have served us so well are about to become anchors around our necks.

In the coming decades, if you want your program to run fast, you are going to have to write it so that it shares thousands of processors. Not two. Not four. Thousands. -- *Thousands.*

Imagine an XBox with 1024 processors, each running at a ghz. Imagine your laptop with 2048 cores. Or a server farm in a room, and each server has 4096 cores. If the next 50 years is to see another 22 orders of magnitude increase in power, *that's* where that power is going to have to come from. Not just one hyperfast, hyperaccurate clerk; but thousands upon thousands; all sharing the load; all with programs written to share the load.

How are we going to write that code? What language are we going to use to express the concepts that execute in thousands of machines.

Of course the current answer to that is "Functional Programming". OK, maybe -- *maybe*. But I gotta tell ya, the new functional languages out there aren't looking too good to me. Scala and F\# are still closely tied to the hardware. Scala *is* java with a few cute twists. And F\#? Is it really the language that's going to take us into the next age? My fear is that these languages suffer from the Sapir/Whorf trap. Their mode of expression does not sufficiently change our world view. They are too much like Java and C\# and all the other old languages.

Clojure
-------

The only language I've seen so far that comes close to a different[4] mode of expression, and that is capable for use in the enterprise, is Clojure; which, after all, is just Lisp. But writing code in Lisp *is* different. It's a different mode of expression, and it makes you see concepts that are difficult, if not impossible, to conceive of in Java, or C. The Clojure data types[5], the control structures, the state management, the homoiconicity, and just the overall mathematical flavor; make this language different from what most Java/C\#/Ruby programmers are used to.

Is Clojure the language that will take us into the massively-multicore regime? I don't know. In fact, I rather doubt it. What I am reasonably sure of, however, is that it will be an important step on the way. It is different enough that, by using it, we might break out of the Sapir-Whorf trap and get a glimmer of the real solution.

[1] Moore's Law.

[2] I feel the need.

[3] You can talk to me about quantum computers when we manage to get more than a handful of qbits stable for more than a few seconds.

[4] Notice I didn't say "new".

[5] Recently some compromises have been made in Clojure, tying it a bit closer to the hardware for the sake of speed.
