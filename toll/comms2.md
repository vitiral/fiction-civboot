```
Author: Rett Berg (github.com/vitiral)
Perspective: Toll Bansha
Other characters: Maye Johnson, Taylor (Tay) Jong
Time period: 5 months 3 days After Event
Primary Location: Civboot A
```

I was some insomnia tonight. While trying to go to sleep my mind slipped back to
before the nucs fell, to a video I'd watched when I was trying to avoid working.
It had been about how a guy had hacked into like 30 devices or something. Some
had been through UART ports, some had been just connecting to it and using a
password of "password"... but then others had been where they discovered some
web APIs were implemented with bash, and they could actually _inject_ bash
commands.

I leapt out of bed and fired up my laptop. Just in case this wasn't clear
before, we do have regular hardware and software -- not just Civboot stuff. It's
mostly supposed to be for communicating with the outside world and the large
database of information and software we have in our archive. I open up the
Web-UI on IP address `192.168.1.1`.

I've actually never tried to hack into anything before. Maybe that's
embarrassing for a Computer Science PhD, but I've never been one to take many
risks.  "Okay...  now what" I think as I stare at the Web UI. "Assuming this
thing is written using bash... how do I do bash injection?"

I've used surprisingly little bash, but I know a bit about it. Bash is a weird
language, if you write `cat /etc/passwd` that will print the contents of
`/etc/passwd` to the screen. Ah, but you can do `echo "$(cat /etc/passwd)"` and
it will also print the contents of `/etc/passwd`, the important point being that
the `$(cat /etc/passwd)` is running code and is injected into the string to be
echoed. So if they had something like `echo "<inserted string from API>"` I
could run literally anything I wanted.

To start I just want to whether whether what I'm doing is working without
breaking anything. How about just inserting `$(echo YOUWIN)` into a few spots?
If I get `YOUWIN`, or even if I get back certain weird errors, I know that
_something_ is working.

So I start with just the UI, inserting `$(echo YOUWIN)` into any text box
I can find. All of them respond as expected, with an error that the string I
entered isn't valid or just writing literally "$(echo YOUWIN)" back, meaning
that no execution has happened... except for one. In the configuration settings
I set the "Satellite Name" field. The name becomes `YOUWIN`. Holy crap holy crap
holy fuck. I'm in. I fucking win.

Okay okay, maybe I'm not in yet. I can't be sure that I'm root yet and I
probably need to be in order to _really_ do anything... I type a new value into
"Satellite Name": `$(whoami)`. The new Satelite Name becomes `root`. I nearly
jump out of my chair in surprise and happiness. I start crying. I dance on the
ground. I scream "woot woot woot!" in the air.

My name being "root" means that I have complete control of the satelite. I can
run almost anything I want, delete anything. No security settings on UNIX
_ever_ restricts what is called "root access." I just need to write and run the
correct software to somehow establish a network connection with the other
civboots.

I quickly rename the satellite: `Civboot Alpha has root -- PLEASE HOLD -- Wait
for further instructions here` just in case someone else is trying to hack into
the satellite as well. It would be bad if we were both trying to make changes at
the same time.

I sit back and revel in the feeling coursing in my veins. I think it's the
first time I've felt real joy since... well since the literal end of the world.
It's an almost forgotten feeling. The words I just typed, another human outside
my Civboot may actually _read_ those words. And soon I'll be able to read their
words. Another feeling starts to well up inside me, one that I wasn't sure could
exist any more. Hope. Hope for a future that might be good.  It's not all over,
humanity might actually have a chance.

I bend over and get straight to work. I proceed to work all day learning the
satelite's operating system, taking notes, building small scripts to help my
investigations go faster. Maye shows up with some food.

"Why weren't you at any meanls?" she asks, handing me what must be leftover
dinner.

"I've gotten into the satelite. I'm trying to make connection but I need to go
slow and understand everything. I don't want to fuck anything up because if I
do, there is probably no going back."

She nods, seeing my intensity. "If that's the case then you need to eat, take a
break. I understand that you're focused but you should try and make a plan to
avoid breaking anything."

I push back from the computer and take a deep breath. "You're right. Do you know
anything about linux or how to code?" I pick up the food and start chewing, not
even noticing what I'm eating.

"Not really, but if you need someone as a sounding board I can try to understand
and listen. You'll have to explain to me like I'm a moron, but maybe that will
actually help you to understand the problem."

TODO: finish chapter.

