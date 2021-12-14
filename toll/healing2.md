```
Author: Rett Berg (github.com/vitiral)
Perspective: Toll Bansha
Other characters: Maye Johnson
Time period: 3 months 2 days After Event
Primary Location: Civboot A, composite production
```

Well, I was right about maintenance being something we have to keep up with.
Maye and I spent the last two days cleaning up and taking stock of our
supplies. While doing so, we discovered that we were running out of toilet
paper. Turns out the automated machines that make it are all plugged up.
Wonderful.

Since this whole Civboot is built to be "as simple as possible" you would
figure repairing a problem like this would be easy. "Easy for who?" is the
relevant question. You see, this tin can was built with the idea that there
would be lots of _experts_ living in it, each with eight or more years of
training for the complexities related to their specialty. This particular issue
should be done by someone with training in mechanical engineering.
Unfortunately our resident mechanical engineer checked out a few months ago and
is currently sleeping rent free in a compost heap.

By the way, in case anyone is reading this -- yes I have gone from being a sobbing
drunk to being an insufferable snarky bastard. Vulgar jokes are a coping
mechanism okay? I'm not normally this unfeeling but it sure beats feeling sad
for myself all the time. I'm not just snarky, I'm also angry at pretty much
everyone who's dead. I'm allowed to joke about the dead, seeing as I'm one of
the few left who's still alive. It's all in the stages of grief, go read about
it sometime.

So anyway, I start trying to figure out what is wrong with our shit paper
dispenser. This thing is way over-engineered if all you want to do is make
toilet paper. Which, by the way, is not all it can do. It can make sheets of
nearly any thickness and stiffness from our vertical farm's plant matter. Think
OSB boards but with corn husks, hemp, and science. It heats the cellulose, also
extracting chemicals used to make a kind of glue. Then it re-combines them in
different programmable ratios depending on the properties you want. For toilet
paper you can imagine we want it to be as flexible as possible, so that means
very little glue. We also want it to be as thin as possible. All this is
programmable in the console.

Let's talk about the software in a Civboot. It is text based. The really
advanced ones have little drawings consisting of wire meshes. It's like whoever
built this place really loved watching Tron and dreamed of a retro-futuristic
70's future. Having a PhD in computer science I know _why_ it is built this
way, but it still sucks. Like everything else in this place they wanted
everything to be "as simple as possible." The software is so basic that a
teenager could probably understand and modify it.

Anyway, to use this machine you get on the terminal and type `help` into a
keyboard. It pops up with:

```
PAMELA: PlAnt MatEriaL mAker

Pamela creates materials of configurable properties from plant matter. Pamela's
full manual can be read with `man pamela`

Commands:
  config: view help on the config format for pamela.
  run <configuration> <args>: run a config with certain parameters.
  stop: stop the current job.
  diagnose [component]: diagnose the system or a specific component.
  logs update: update the maintenance log for a part.
  logs view: view te maintence log for a part.
```

This may be the worst possible backronym I've ever seen. This thing is called a
"PAMELA" ... loosely meaning "plant material maker". Whoever made this was way
too into Bay Watch re-runs. Fortunately for me they still had the good sense to
include a diagnostics mode. I type `diagnose`. Electric motors come to life,
moving one piece of the machine after another. I see the following text scroll
on the screen over the next minute or so:

```
THICKNESS SENSORS... OK
SAW MOTOR... OK
SAW POSITIONER... OK
COMPRESS MOTOR... OK
COMPRESS ACTION... OK, NEED SCHEDULED MAINTENENCE
HORIZONTAL MOTOR... OK
HORIZONTAL ACTUATOR...  ERROR
  Found maintence logs. View with:
    logs view "HORIZONTAL ACTUATOR"
  Cannot actuate material.
  May be blocked or broken.
  Inspection needed.
OVERHEAD LIGHT... OK
LOTION DISPENSER...
```

What the `LOTION DISPENSER` is I have no idea. My guess is it's a Baywatch joke
and it's for the glue dispenser. The diagnostics continued with most of the
parts saying OK, some saying they required scheduled maintenance. The
Horizontal Actuator was apparently malfunctioning. Pamela, you're a real life
saver.

Re-reading the help menu I see there are actually maintenance logs for the failing
part. I type `logs view "HORIZONTAL ACTUATOR"` as suggested and see the
following logs from about a year ago:

```
1. reran diagnostics for failing part, watching motion
  Command: diagnose "HORIZONTAL ACTUATOR"
2. bed jerked, possible jam.
3. manually inspected by moving forward/backward
4. noticed bent arm piece. Not sure what caused.
5. manually bent piece back into place.
6. reran diagnostics again, came back OK
```

Well, that was all pretty clear. I followed the steps, found and fixed
the bent part and re-ran diagnostics. It came back with:

```
HORIZONTAL ACTUATOR...  WARN
  OK. PREVIOUS FAILURE DETECTED.
  UPDATE LOGS WITH:
    logs update "HORIZONTAL ACTUATOR"
```

I updated the logs to say to refer to the previous log. I then looked at the
configuration files and found the configuration for making toilet paper.  I
told pamela to make 20 days worth of toilet paper for five people. I also
updated the scheduled toilet paper production to be for only five people
instead of the previous six... I wonder how many places have the number of
inhabitants hard-coded and would need to be manually updated?

At this point I was starting to feel pretty good about living in this
particular tin can. There had been a problem with a system and it had been
solvable by the previous maintenance log with no expertise required. Why the
metal part kept getting bent was definitely something that should be looked
into...  but it had happened a year ago, there were more pressing matters. The
point was, maybe we were going to be able to survive in this Civboot after all.

I did have one more curiosity though. I typed `man pamela` and searched for
`LOTION`. I wish I hadn't.

```
The LOTION uses the configuration provided to adjust heat and other settings
for creating the glue which is an essential component of many materials
created by pamela. Pamela can apply a configured amount of LOTION to make
the wood harder.
```

Pamela applies lotion... to "make the wood harder". How much of the software
or other components are designed by teenage boys who are way too amused by
sex jokes? Never-mind about feeling good, we are totally and completely fucked.

[Next segment](./healing3.md)
