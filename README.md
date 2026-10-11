# Decay Envelope

A Katamari-style rolling puzzle and small adventure set inside a eurorack synthesizer.

Otto Brandt, 84, repaired synthesizers in Lindenau for fifty-one years. Nobody has been born there for eleven. He falls asleep at the rack he built for his late wife in 1979 and wakes up small enough to roll through it. Each module he patches brings back one layer of the rack's voice, over a kick that starts as his heartbeat, while the scrollers around him never look up.

**Play:** https://samuelling.github.io/Decay-Envelope/

## How it plays

- **Move:** drag anywhere (touch or mouse), or WASD / arrow keys.
- **Grow:** roll over anything up to half your diameter. Bigger things get shoved.
- **Chaos:** every few seconds a gate pulse fires from a blinking jack and knocks pieces off you. Knobs are walls until you outgrow them.
- **Win a module:** reach the target diameter, then roll into the OUT jack before the clock runs out.
- **Clock:** each module lasts a set number of bars of the kick. In the last 8 bars the HUD turns red and the music thins out. Run out and the patch fades; you retry the module.
- **Leak:** from level 2 on, parts slowly drift off you on their own, like a note in its release stage. You only grow if you collect faster than you drain.
- **Feed:** hearts, badges and phones grow you twice as fast, but they speed up your leak for a while (the HUD shows the multiplier). Real parts grow you slowly with no penalty.
- **Hunters:** red-ringed scrollers notice you when you move fast nearby and chase you to film you. If they catch you, pieces fly. Outrun them, or get big enough and hit them hard to knock their phone loose.
- **Difficulty:** the growth-rate slider on the title and module cards scales how much each pickup grows you (0.6× to 2.5×, default 1.5×). It's remembered between sessions.

## The modules

Seven single-module levels, then a final level that spans the whole 128HP rack. Every module keeps its quirk in the final level.

| Level | Module | Rule | What patching it adds to the music |
|---|---|---|---|
| 1 | VCO · Origin | chain pickups quickly: each one in a row is worth more, up to 2× | two detuned sawtooth oscillators |
| 2 | LFO · Tide | a slow current moves everything; rolling with it gives 1.5× growth, against it 0.6× | pitch and filter drift |
| 3 | SEQ · Steps | lit floor pads shove you round a ring and spray parts; accent steps 4 and 8 kick hard | an eight-step melody |
| 4 | VCF · Resonance | only parts inside the sweeping passband color stick; resonant peaks fling you | resonant filter sweep |
| 5 | ENV · Contour | Attack fast, Decay sticky but 1.5×, Sustain normal, Release slippery with 3× leak | plucky notes and a bass line on the kick |
| 6 | VCA · Attenuation | near darkness; your light fades and glowing parts recharge it | hi-hats, brighter lead |
| 7 | DLY · Echo | two echoes follow you and collect, but only the kind of part you picked up last | dotted-8th delay on the lead |
| 8 | The whole rack | every rule in its own section; bump scrollers so they look up | chord progression, pads, bells |

Once you are much bigger than the scrollers, they scatter out of your way and you sweep through them without slowing down. Hunters stop chasing you.

### The kick

An 808 kick runs under everything at 100 BPM. In level 1 it is Otto's slow lub-dub heartbeat; it gets louder and busier each level until it is four on the floor in the final rack. Gate pulses fire on the downbeat, and the parts on the floor jump with every kick.

Each level hides one keepsake. The ending changes with how many scrollers looked up, whether you found Jonas, and how many of the eight keepsakes you kept.

## Ending

Patching the final rack plays a short animated ending: the rack lights up, a release wave dissolves the scrolling feeds, and Lindenau becomes a trance forest while the music opens into four-on-the-floor arps and pads. Captions change with how many scrollers looked up, whether you found Jonas, and how many keepsakes you kept. Then the credits roll. Tap to skip.

## Credits

A game by Sam Ling and Claude, with thanks to everyone who has ever made a game or made music.

## Tech

One self-contained `index.html`: Canvas 2D for rendering, Web Audio for all sound (synthesized live, no samples), Google Fonts for type. World units are millimetres; panels use real eurorack dimensions (1 HP = 5.08 mm, 3U = 128.5 mm).
