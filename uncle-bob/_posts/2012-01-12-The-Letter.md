---
layout: post
title: The Letter
tags: ["Testing", "Craftsmanship"]
old_tags: ["TDD", "Professionalism", "Craftsmanship"]
---

We need to become a self-regulating and self-policing profession. The stakes are simply too high to allow software to remain in the current ad-hoc limbo of hackers, heroics, and hermits.

Consider how much software you interact with every day. Your alarm clock, your cell phone, the television and cable box, the remote control, your toaster oven, your watch, your car, the train to work, the cash register at Starbucks, the coffee maker at Starbucks, the elevator you ride, etc. etc. The list is virtually endless. Nearly every aspect of our daily lives, nearly ever corner of our civilization is somehow touched, controlled, managed, or influenced by software.

Think about that again. Virtually every aspect of our lives has a software component; and yet we exert absolutely no regulatory control over that writing of that software. Any Harry Hacker with a "J" in his name can get hired to write Java code. And the strongest likelihood is that Harry J. Hacker's code be crap, will be wrong, and will not be explicitly tested before it is shipped.

Plumbers are regulated. Electricians are regulated. Architects, lawyers, and doctors are regulated. Why aren't we? Don't get me wrong, I don't want government to be the regulator; I want us to self-regulate. But if we software developers don't figure out how to do that, then government will certainly step in. And then life will get *really* bad.

Yesterday I received a very scary, letter that underscores this point rather dramatically. I thought you'd like to read it. I worked with the developer to sanitize it so that the innocent people in this story are not punished. I regret that I can't splash the guilty parties' names all over twitter though.

> Hello "Uncle Bob",

<p/>
I'm a 34 year old freelance programmer who has been developing software for 15 years.

<p/>
Some time ago I was hired as a team leader for a safety critical embedded system that controlled a medical surgery device. Everything was fine during the first months. I put a great deal of architectural effort into safety. I used Active-Objects for safer threading, UML-Generated State-Machines for stateful safety-checks, simulation, and lots of Unit-Testing (though not with full coverage).

<p/>
Oh, things weren't perfect. We had been asked to finish a four year project in less than 1 year; so time pressure was very high. Even so I had a good feeling that the device would be safe for millions of treatments.

<p/>
Eventually it became clear that we could not deliver the full release on time. When we told our manager, he began to worry about his bonus. (At least that’s my personal suspicion). When I told him we couldn't meet the schedule, he told me I was not allowed to make any more estimates. He shouted a lot all day long and forced everyone to work 7 days a week. He was in such a rage that he even scared the validation team into concluding the official medical validation after just a few days; which was far too early.

<p/>
He knew that safety was the most important issue for me, so he began to cut my responsibilities. He eventually gave full control of the project to the
youngest and most impressionable programmer on my team. I continued to code in the main-branch of the project; so the manager made his own code branch and, together with the rookie, produced his own version of the software.

<p/>
So I terminated my contract with the company.

<p/>
A few days later the first bug occurred during a human trial. Fortunately, during the early days of the project, I had made the software robust enough that the bug didn’t harm the patient. The device just stopped operating before starting the automated surgery. You'd think that would have been a wakeup call, but the company didn’t even analyze the bug (not to mention stopping the unstable product). More bugs were found later. Even obvious bugs like mixing up the surgery directions (upwards/downwards) were found during the first human treatments. It is a real possibility, and one of my great fears, that tomorrow some patient will become severely disabled.

<p/>
The other programmers didn't quit. They told me: “the boss is the boss – we just do what he tells us – it's his responsibility.”. So I figured I must have been crazy for quitting. I felt weak and worthless, like I couldn't handle the pressure. But lately I started reading “Clean Coder”. And it's made me consider that, perhaps, I’m not weak – but the opposite: strong.

I am, of course, furious about the manager who drove his organization to such unprofessional depths. He is an idiot and a criminal, and I hope he winds up in prison. But I am even angrier at the developers. Not only were they accomplices to that criminal idiocy; they made the one guy who took a stand feel stupid and weak. They are the ones who are stupid and weak. They should not be programmers. Programmers are better than that.

Aren't we?
