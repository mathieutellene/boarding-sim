# LinkedIn draft — optional, only if you want it

Written in the register of the reference post: artifact first, motivation as a
question, one line of stack, explicitly provisional, ends with a real question.
No "thrilled to announce", no emoji bullets, no hours-spent brag.

Do not post the repo link in the first comment — LinkedIn's reach penalty for
outbound links is smaller than the cost of people not finding the thing.

---

I built a simulator for boarding an aircraft, and it told me I was wrong four times.

Boarding is a queueing problem with one aisle and no overtaking. Every passenger is
an agent with their own walking speed, bags and seat, and I raced fifteen boarding
methods against the identical passenger manifest — same people, same bags, same
seats — so any difference is the method and not the draw.

I wrote each method's description from what I expected to happen, then measured it.
Four had to be rewritten:

Rotating zones (tail, nose, tail) come out worse than plain back-to-front. Calling
a nose zone early puts those people stowing in front of half a cabin that still has
to walk past them.

Adding "window seats first" to zone boarding removes almost all the climbing-over,
and is still slower than sorting nobody at all.

Boarding the slowest passengers first is faster, not slower. The jams form while
the aisle is still half empty.

And the method most airlines actually announce — back to front — is 16% slower than
boarding at random.

The result I didn't expect isn't in the ranking at all. Steffen's optimal method
does 7.9 minutes with a perfect queue and 11.9 when people don't line up properly.
Window-middle-aisle moves 7% across that same range, because it only ever asks for
three lines. Robustness beats peak performance, which is why the second one is what
gets used.

It runs in a browser as a single HTML file with no dependencies, including the 3D
cabin view.

github.com/mathieutellene/boarding-sim

I'm curious what operations people would tell me I'm still missing: what stops a
real boarding that isn't bags and isn't seat interference?

---

## If you'd rather not post at all

That is a perfectly good answer. The repo works on its own — it is linkable from
your CV, from mathieutellene.github.io, and in any interview where someone asks
what you do when the data disagrees with you. Nothing about this project needs a
LinkedIn post to be useful.
