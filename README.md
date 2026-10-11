# Decay Envelope

A Katamari-style rolling puzzle and small adventure set inside a eurorack synthesizer.

Otto Brandt, 84, repaired synthesizers in Lindenau for fifty-one years. Nobody has been born there for eleven. He falls asleep at the rack he built for his late wife in 1979 and wakes up small enough to roll through it. Each module he patches brings back one layer of the rack's voice, while the scrollers around him never look up.

**Play:** https://samuelling.github.io/Decay-Envelope/

## How it plays

- **Move:** drag anywhere (touch or mouse), or WASD / arrow keys.
- **Grow:** roll over anything up to half your diameter. Bigger things get shoved.
- **Chaos:** every few seconds a gate pulse fires from a blinking jack and knocks pieces off you. Knobs are walls until you outgrow them.
- **Win a module:** reach the target diameter, then roll into the OUT jack.

## The five modules

| Module | Name | Twist | What you hear after patching |
|---|---|---|---|
| VCO | Origin | none | two detuned sawtooth oscillators |
| LFO | Tide | a slow current moves you and everything loose | pitch and filter drift |
| VCF | Resonance | glowing peaks fling you and shake things off | resonant filter sweep |
| VCA | Attenuation | near darkness; only you and the phones give light | a gated melody |
| OUT | Release | bump scrollers to knock their phones loose; some look up | reverb bloom, bell chord |

Each module hides one keepsake (ring, glasses, photograph, letter, key). The ending changes with how many scrollers looked up, whether you found Jonas, and how many keepsakes you kept.

## Tech

One self-contained `index.html`: Canvas 2D for rendering, Web Audio for all sound (synthesized live, no samples), Google Fonts for type. World units are millimetres; panels use real eurorack dimensions (1 HP = 5.08 mm, 3U = 128.5 mm).
