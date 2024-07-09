---
title:  "Build the Ramp"
date:   2024-07-08 11:09:00
layout: page
#
# toc: true
# categories:
---
tl;dr
1. build the thing
1. build the ramp

# on technical accessibility

One interesting observation I think back to often:
- when I first published the micrograd repo, it got some traction on GitHub but then somewhat stagnated and it didn't seem that people cared much.
- then I made the video building it from scratch, and the repo immediately went through hockey stick growth and became a verty often cited reference for people learning backpropagation.

This was interesting because the micrograd code itself didn't change at all and it was up on GitHub for many months before, stagnating. The code made sense to me (because I wrote it), it was only ~200 lines of code, it was extensively commented in the .py files and in the Readme, so I thought surely it was clear and/or self-explanatory. I was very happy with myself about how minimal the code was for explaining backprop - it strips away a ton of complexity and just gets to the very heart of an autograd engine on one page of code. But others didn't seem to think so, so I just kind of brushed it off and moved on.

Except it turned out that what stood in its way was "just" a matter of accessibility. When I made the video that built it and walked through it, it suddenly almost 100X'd the overall interest and engagement with that exact same piece of code. Not only from beginners in the field who needed the full intro and explanation, but even from more technical/expert friends, who I think could have understood it if they looked at it long enough, but were deterred by a barrier to entry.

I think as technical people we have a strong bias to put up code or papers or the final thing and feel like things are mostly self-explanatory. It's there, and also it's commented, there is a Readme, so all is well, and if people don't engage then it's just because the thing is not good enough. But the reality is that there is still a large barrier to engage with your thing (even for other experts who might not feel like spending time/effort!), and you might be leaving somewhere 10-100X of the potential of that exact same piece of work on the table just because you haven't made it sufficiently accessible. 

TLDR: Step 1 build the thing. Step 2 build the ramp. 📈
Some voice in your head will tell you that this is not necessary, but it is wrong.

source: https://x.com/karpathy/status/1760388761349927356 (2/21/24, kaparthy)