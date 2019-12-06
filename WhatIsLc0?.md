# What is lc0? (in layman's terms)

Lc0 is often referred to as a chess engine, however, Lc0 is more like a chess engine *shell* than an actual chess engine.
Lc0 needs a *neural network* in order to play, just as a car requires a driver, or a mech requires a pilot.

The brains of Lc0, the true *player* of the engine, is the neural network that it uses.
With a weak net, Lc0 can play as poorly as a toddler, and with a strong net, Lc0 can beat even the strongest existing chess engines.

So what networks are available, and what are the differences between them?

## T Nets

T nets are the main Lc0 networks.

The T nets are created by playing against themselves for a fixed number of games (like 32,000).
After looking at those games, a new network is created by adjusting the previous network based on what worked and what didn't in the games.

There are different generations of T nets. 

The current (Dec 6,'19) generation that is being trained is called **T60**.

The previous generation, that is no longer being trained, is called **T40**.

You may ask, "Where is T50?"

**T50** is a set of small, lightweight nets that are used to test different training methods before applying those training methods to T60.

All of the main networks can be downloaded from [lczero.org](https://lczero.org/networks/)

## J Nets

[J nets](https://github.com/jhorthos/lczero-training/wiki/Leela-Training) are nets created by jhorthos.

J nets are not the main Lc0 networks, but are still important networks, and are often used in tournaments against other engines.

Because all of the T net games are saved, all of them can be used as training data for other networks as well.
J nets are trained on these games.

The J nets have different network sizes and different training parameters from the T nets, which can sometimes make them stronger than the T nets in some ways.

There are many J nets, each of different sizes and different parameters. Here is a summary, but for the full description of each, head to [this page](https://github.com/jhorthos/lczero-training/wiki/Leela-Training).

**J13** nets are trained on T40 games.

**J48** nets are trained on T60 games.

**LD2** (Little Demon 2) is a specific J net trained on T40 games.
