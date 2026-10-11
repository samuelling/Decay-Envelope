# Decay Envelope

A Katamari-style rolling puzzle and small adventure set inside a eurorack synthesizer.

Otto Brandt, 84, repaired synthesizers in Lindenau for fifty-one years. Nobody has been born there for eleven. He falls asleep at the rack he built for his late wife in 1979 and wakes up small enough to roll through it. Each module he patches brings back one layer of the rack's voice, over a kick that starts as his heartbeat, while the scrollers around him never look up.

**Play:** https://samuelling.github.io/Decay-Envelope/

## How it plays

- **Move:** drag anywhere (touch or mouse), or WASD / arrow keys.
- **Grow:** roll over anything up to half your diameter. Bigger things get shoved.
- **Chaos:** every few seconds a gate pulse fires from a blinking jack and knocks pieces off you. Knobs are walls until you outgrow them.
- **Win a module:** reach the target diameter, then roll into the OUT jack.
- **Difficulty:** the growth-rate slider on the title and module cards scales how much each pickup grows you (0.6× to 2.5×, default 1.5×). It's remembered between sessions.

## The modules

Seven single-module levels, then a final level that spans the whole 128HP rack. Every module keeps its quirk in the final level.

| Level | Module | Twist | What patching it adds to the music |
|---|---|---|---|
| 1 | VCO · Origin | none | two detuned sawtooth oscillators |
| 2 | LFO · Tide | a slow current moves you and everything loose | pitch and filter drift |
| 3 | SEQ · Steps | eight floor pads light on the 8th notes and shove you to the next one | an eight-step melody |
| 4 | VCF · Resonance | glowing peaks fling you and shake things off | resonant filter sweep |
| 5 | ENV · Contour | Attack / Decay / Sustain / Release floor bands: fast, sticky, normal, slippery | plucky notes and a bass line on the kick |
| 6 | VCA · Attenuation | near darkness; only you, the parts and the phones give light | hi-hats, brighter lead |
| 7 | DLY · Echo | two delayed echoes follow your path and collect for you | dotted-8th delay on the lead |
| 8 | The whole rack | all of the above, side by side; bump scrollers so they look up | chord progression, pads, bells |

### The kick

An 808 kick runs under everything at 100 BPM. In level 1 it is Otto's slow lub-dub heartbeat; it gets louder and busier each level until it is four on the floor in the final rack. Gate pulses fire on the downbeat, and the parts on the floor jump with every kick.

Each level hides one keepsake. The ending changes with how many scrollers looked up, whether you found Jonas, and how many of the eight keepsakes you kept.

## Tech

One self-contained `index.html`: Canvas 2D for rendering, Web Audio for all sound (synthesized live, no samples), Google Fonts for type. World units are millimetres; panels use real eurorack dimensions (1 HP = 5.08 mm, 3U = 128.5 mm).
