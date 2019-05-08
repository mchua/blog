---
layout: post
title: "Getting set up for circuitpython development"
date: 2019-05-07 21:43:00.000000000 -05:00
type: post
published: true
password: ''
status: publish
categories: null
author:
  login: mchua
  display_name: Mel
  first_name: Mel
  last_name: Chua
---

I went to [PyCon US](https://us.pycon.org/2019/about/) this year for the first time in... many years. Although I was formally there to talk with PyPI developers about being part of our [research on FOSS digital infrastructure sustainability](https://www.fordfoundation.org/ideas/equals-change-blog/posts/announcing-13m-in-funding-for-digital-infrastructure-research/), I also encountered a new-to-me open software/hardware project for learning electronics, [CircuitPython](https://learn.adafruit.com/welcome-to-circuitpython/what-is-circuitpython).

The first few minutes with the starter kit were enough to impress me - having taught introductory undergraduate electronics courses, I've seen pretty much every way a smart, motivated, and new-to-electronics student can, uh... go awry. Plug in a board, and it shows up as a drive (as if you'd plugged in a thumbdrive). Open the drive, and you'll find a Python file. Edit the file, and boom; the board is running it. It felt like going from PIC18F assembly to seeing an Arduino for the first time; this feels like just as huge a step toward usability (and honestly, humaneness-towards-students). Kattni (one of the developers) patiently fielded my questions as my smile grew broader and broader.

These are notes for getting started with development both with and on CircuitPython, for my own future reference (though others might find them helpful as well). For reference, we got a [Circuit Playground Express](https://learn.adafruit.com/adafruit-circuit-playground-express) in our PyCon swag bags, so that's what I'm working with.

0. First is the guide on [setting up a CircuitPython git/github workflow](https://learn.adafruit.com/contribute-to-circuitpython-with-git-and-github).
1. For using CircuitPython, [the Welcome page](https://learn.adafruit.com/welcome-to-circuitpython/what-is-circuitpython) is well-organized to guide you through the process.
2. For developing CircuitPython in Python, look at this [template for a CircuitPython library](https://github.com/adafruit/cookiecutter-adafruit-circuitpython). Note that I haven't done this yet, since I want to look at the C first.
2. For developing CircuitPython in C, you'll have to [build it](https://learn.adafruit.com/building-circuitpython/introduction), so that page has instructions on how to do so. There was some debate at the Monday sprint as to which version of gcc should be used, but as of this writing, the version listed on that tutorial is the same one that one of the lead developers uses (thanks, Scott!)
3. For community and help while developing, there is a #circuitpython channel on the [Adafruit Discord](adafru.it/discord). Note that this is distinct from #help-with-circuitpython, which is for help _using_ circutpython. The #circuitpython channel is for developing circuitpython itself.
4. There is a weekly meeting, currently on Mondays at 11am PST over Discord (it's audio, so I'll see what works best for access if I end up trying this, since I'm a Deaf developer). They do have [meeting notes on github](https://github.com/adafruit/adafruit-circuitpython-weekly-meeting/), though!
5. Code and issues are in the [CircuitPython github](https://github.com/adafruit/circuitpython). 

I usually start out in a project by watching and learning how things go before jumping in a ton myself. I'm currently watching [a feature request related to tab completion](https://github.com/adafruit/circuitpython/issues/1636) and [another on PWM](https://github.com/adafruit/circuitpython/issues/1838) and [another on r/w calibration offsets](https://github.com/adafruit/Adafruit_CircuitPython_BNO055/issues/21). I'm also peeking in on a [clang-format issue](https://github.com/adafruit/circuitpython/issues/1012) (I've never seen clang-format before!) and one on [pnm support](https://github.com/adafruit/Adafruit_CircuitPython_ImageLoad/issues/1) because I have no idea how image formats work, and eavesdropping is usually a helpful way to pick up incidental learning.

In the meantime, I stumbled across [issue #1833](https://github.com/adafruit/circuitpython/issues/1833) which was - as far as I can tell - a one-line fix, which I've just sent in as my first PR (pull request, or "I think this fixes the thing, can y'all check?").

Thanks to all the maintaners (especially Scott and Kattni) who've helped me start learning so far!
