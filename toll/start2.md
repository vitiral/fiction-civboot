```
Author: Garrett Berg (github.com/vitiral)
Perspective: Toll Bansha
Other characters: Maye Johnson
Time period: 3 months 2 days After Event
Primary Location: Civboot A, composite production
```

Well, I was right about maintenence being something we have to keep up with.
Maye and I spent the last two days cleaning up and taking stock of our
supplies. While doing so, we discovered that we were running out of toilet
paper. Turns out the automated machines that turn excess plant mater from our
verticle farms into ass wipes was all plugged up. Wonderful.

By the way, in case anyone is reading this -- yes I have gone from being a sobbing
drunk to being an insuferable snarky bastard. Vulgar jokes are a coping
mechanism okay? I'm not normally this unfeeling but it sure beats feeling sad
for myself all the time.

Anyway, since this whole Civboot is built to be "as simple as possible" you would
figure repairing a problem like this would be easy. "Easy for who?" is the
relevant question. You see, this tin can was built with the idea that there
would be lots of _experts_ living in it, each with eight or more years of
training the complexities related to their specialty. This particular issue
should be done by someone with training in designing or at least repairing
machines. Unfortunately our resident mechanical engineer checked out a few
months ago and is currently sleeping rent free in a compost heap.

Fuck him. Ya, in addition to being snarky I'm also angry at pretty much
everyone who's dead. Stages of grief okay?

So anyway, I start trying to figure out what is wrong with our shit paper
dispenser. This thing is way over-engineered if all you want to do is make
toilet paper. Which, by the way, is not all it can do. It can make sheets of
nearly any thickness from our verticle farm's plant matter. Think OSB boards
but with corn husks, hemp, and science. It heats the cellulose, also extracting
chemicals used to make a kind of glue. Then it re-combines them in different
programmable ratios depending on the properties you want. For toilet paper you
can immagine we want it to be as flexible as possible, so that means very
little glue. We also want it to be as thin as possible. All this is programmable
in the console.

Let's talk about the software in a Civboot. They are text based. The
really advanced ones have little drawings consisting of wire meshes. It's like
whoever built this place wanted to make it as retro-futuristic 70's as
possible. Having a PhD in computer science I know why they chose this, but
it still sucks sometimes. Like everything else in this place they wanted
everything to be "as simple as possible." The software is so basic that a
teenager could probably understand and modify it.

Anyway, to use this machine you get on the terminal and type `help`. It pops up
with

```
PAMELA: PlAnt MatEriaL mAker

PAMELA creates materials of configurable properties from plant matter.  See
`config` for directions on the configuration of a job.

Commands:
  config: view help on the config format for PAMELA.
  run: run a job a specified number of times.
  stop: stop the current job
  diagnose: diagnose the system.
  maintenance: update the maintenance log for a part.
```

In the worst possible Backronym I've ever seen, this thing is called a "PAMELA"
... loosly meaing "plant material maker". Whoever made this was waaay too into
Bay Watch reruns. Fortunately for me they had the good sense to include a
diagnostics mode. I type `diagnose`. Electric motors start sprining into
life, moving pieces of the machine one after another. I see the following
text scroll on the screen.

```
THICKNESS SENSOR A... OK, B... OK, C... OK
SAW MOTOR... OK
SAW POSITIONER... OK
COMPRESS MOTOR... OK
COMPRESS ACTION... WARN requres scheduled maintenance.
HORIZONTAL MOTOR... OK
HORIZONTAL ACTUATOR...  ERROR
  cannot actuate material.
  May be blocked or broken.
  Inspection needed.
OVERHEAD LIGHT... OK
```

It continued with most of the parts saying okay, some saying they required
scheduled maintenance. The Horizontal Actuator was apparently malfunctioning.
Pamala, you're a life saver.

