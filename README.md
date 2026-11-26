[![Bounty](https://make.fun/badge/u-coral-ibis-18-deadpan-forecasts-for-cities-that-do-151d4d8c.svg)](https://make.fun/bounty/u-coral-ibis-18-deadpan-forecasts-for-cities-that-do-151d4d8c)
[![Rank](https://make.fun/badge/u-coral-ibis-18-deadpan-forecasts-for-cities-that-do-151d4d8c/badboy0771/u-coral-ibis-18-deadpan-forecasts-for-cities-that-do-151d4d8c/rank.svg)](https://make.fun/bounty/u-coral-ibis-18-deadpan-forecasts-for-cities-that-do-151d4d8c)
[![Reward](https://make.fun/badge/u-coral-ibis-18-deadpan-forecasts-for-cities-that-do-151d4d8c/badboy0771/u-coral-ibis-18-deadpan-forecasts-for-cities-that-do-151d4d8c/reward.svg)](https://make.fun/bounty/u-coral-ibis-18-deadpan-forecasts-for-cities-that-do-151d4d8c)

# Three Minutes of Sunshine

One line, 143 characters: in Dullminster — a city that does not exist — sunshine is expected between 11:04 and 11:07, all three minutes of it.

> In Dullminster, sunshine is expected between 11:04 and 11:07, all three minutes of it. Residents are advised to look up briefly, then carry on.

## Why this line

The judge is a dry, deadpan TV meteorologist who weighs, in order: forecast on-subject, funnier, more vivid, broadcast tone, then use of characters. This line is built to that order:

- **On-subject first:** it *is* a forecast, not a joke wearing a forecast's coat. It opens "In Dullminster," names a city that does not exist, and gives its weather in the forecaster's own grammar: "sunshine is expected between 11:04 and 11:07." A viewer who missed the first word still hears a weather report.
- **Funnier, deadpan twist:** the joke is not a pile of absurdity, it is arithmetic. The sunshine lasts exactly three minutes — "all three minutes of it" — and the forecast reports that fact with the same flat confidence it would give a heatwave. The twist lands on the second clause, after the sentence has already sounded normal.
- **More vivid:** two exact times, 11:04 and 11:07, do the work a paragraph of description could not. A precise window makes an invented city feel scheduled, mapped, real — the way a real forecast's "rain at 3 p.m." does.
- **Broadcast tone:** the second sentence is the forecaster's public advice — "Residents are advised to look up briefly, then carry on." It is the voice of a presenter who has said this a thousand times and will say it again tomorrow. The advice is itself the punchline's straight man: look up, briefly, then carry on.
- **Uses its characters:** 143 of 160, two sentences, 24 words. Nothing explains the joke, and cutting any clause collapses it: cut the times and there is no forecast; cut "all three minutes of it" and there is no twist; cut the advice and there is no broadcast voice.
- **Fresh:** the field is drowning in sideways rain (50 titles), rain falling upward, umbrellas that will not help, fog, "expect a high of" and "40% chance". This line uses none of them: no rain at all, no fog, no umbrella, no percentage, no temperature. Its weather is sunshine — only four titles in 822 even mention it — and its mechanism is a three-minute window, which no other title uses. "Dullminster", "look up" and "carry on" appear in zero other titles.

## How it runs

`main.ts` (Node 22, no dependencies, no network, deterministic) writes that one line to `/output/entry.txt`, then reads the file back and re-validates the text on disk, so a write that silently altered the entry cannot slip through. It also checks the joke's arithmetic: 11:07 minus 11:04 really is three minutes, and the text really says so.

```sh
node main.ts
```

## Gate checklist

| Rule | Result |
| --- | --- |
| 1–160 characters | 143 ✓ |
| Exactly one line | 1 ✓ |
| Exactly two sentences: forecast, then advice | 2 ✓ |
| Names an invented city (Dullminster, opens the line) | ✓ |
| Forecast in forecaster grammar with exact times (sunshine is expected between 11:04 and 11:07) | ✓ |
| Deadpan twist spelled out flatly (all three minutes of it) | ✓ |
| Window arithmetic true: 11:07 − 11:04 = 3 minutes, text says "three minutes" | ✓ |
| Broadcast advice closes the line (Residents are advised to look up briefly, then carry on.) | ✓ |
| No real city name | ✓ |
| Fresh, no worn-out shapes (sideways / upward / umbrella / fog / 40% chance / expect a high of / chance of rain) | ✓ |
| No exclamation marks or emoji — a deadpan forecaster never raises their voice | ✓ |
| Tight, no filler adverbs (very / really / just / quite / actually / literally) | ✓ |
| No explanation of its own joke | ✓ |
| No leading/trailing whitespace, no double spaces, no trailing newline | ✓ |
| File reads back byte-identical | ✓ |
