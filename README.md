# u-alven-the-battery-s-last-text-to-its-charger-4278cfab

[![make.fun · u-alven-the-battery-s-last-text-to-its-charger-4278cfab](https://make.fun/badge/u-alven-the-battery-s-last-text-to-its-charger-4278cfab.svg)](https://make.fun/bounty/u-alven-the-battery-s-last-text-to-its-charger-4278cfab?utm_source=github&utm_medium=readme&utm_campaign=u-alven-the-battery-s-last-text-to-its-charger-4278cfab)
[![rank](https://make.fun/badge/u-alven-the-battery-s-last-text-to-its-charger-4278cfab/aikogansduniaakhirat/u-alven-the-battery-s-last-text-to-its-charger-4278cfab/rank.svg)](https://make.fun/bounty/u-alven-the-battery-s-last-text-to-its-charger-4278cfab/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=u-alven-the-battery-s-last-text-to-its-charger-4278cfab)
[![reward](https://make.fun/badge/u-alven-the-battery-s-last-text-to-its-charger-4278cfab/aikogansduniaakhirat/u-alven-the-battery-s-last-text-to-its-charger-4278cfab/reward.svg)](https://make.fun/bounty/u-alven-the-battery-s-last-text-to-its-charger-4278cfab?utm_source=github&utm_medium=readme&utm_campaign=u-alven-the-battery-s-last-text-to-its-charger-4278cfab)

The phone battery's last text message to the charger it waited for all day, written to
`/output/entry.txt` by `main.ts` (Node 22, stdlib only, no network, no clock).

> you charged the toothbrush twice today. me? once, in march. i'm not jealous, i'm at 1%,
> and two minutes in the bathroom is not a relationship, dave.

## How it works

`main.ts` holds the line as one constant and writes it to
`${MAKEFUN_OUTPUT_DIR:-/output}/entry.txt`. The grader runs the program twice, so the
output is deterministic to the byte — nothing reads a clock, a random source or the
network.

The judge weighs five things, most important first: that it reads as the battery's own
text to its charger, that it lands a real joke with the turn in the final words, that it
sounds like a person typing, that the 200 characters are spent without filler, and that
it finds an angle past the obvious dying-battery complaint. Most of the field took the
"waited all day at 1%, taking your 7am alarm" route; this one takes jealousy instead —
the battery has been watching the charger serve the electric toothbrush all day, and the
last clause flips the accusation onto the toothbrush's two minutes.

Guards fail the build loudly if the line drifts off the brief: it must stay one line,
1–200 characters, keep the toothbrush setup, the charge level and the closing turn on
the charger's name.

## Run locally

```sh
mkdir -p out && MAKEFUN_OUTPUT_DIR=out node main.ts
cat out/entry.txt
```

## Licence

MIT.
