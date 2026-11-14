# Chapter 1: Spin

Book: *Quantum Computing for Everyone* (Chris Bernhardt). Notes written 13-14 November 2026.

## 5-line summary

1. A classical bit is one of two states. A qubit can be physically represented by the spin of an electron or the polarization of a photon.
2. Measuring spin always gives one of **two answers** (N or S), never a continuous range. You must choose a direction to measure along.
3. Repeating the same measurement gives the same result. Measuring along a different direction gives a **random 50/50** result.
4. **Measuring changes the system.** vertical, then horizontal, then vertical gives 50/50 on the last step, so the first answer is forgotten.
5. The randomness is believed to be real (not hidden information). Photons in polarized filters behave the same way.

## Key terms

| Term | Meaning |
|---|---|
| Spin | A two-valued property of a particle, measured along a chosen direction |
| Stern-Gerlach experiment | 1922 experiment: silver atoms hit a screen in only two spots, not a smear |
| Quantized | Only certain discrete results are possible |
| Hidden variables | The idea that secret information determines the "random" result (tested by Bell's inequality, ch. 5) |
| Polarization | The direction a photon's light wave oscillates; the photon analogue of spin |

## Part 1: The experiment

- Stern and Gerlach sent silver atoms through a magnetic field. Classical physics predicted a continuous line on the screen. They got **two dots**.
- Atoms (and electrons) act like tiny bar magnets, but only ever with their axis pointing along the measuring direction.
- There is nothing special about "vertical". You can rotate the magnets and measure along any direction. Angles are measured clockwise from the upward vertical (0°).
- Notation: "spin N in direction 0°" means the north pole is up. "Spin S in direction 180°" is the same thing.
- **Quantum clock analogy:** you can only ask "is the hand pointing at 12?" The answer is yes, or "it is pointing at 6" (the opposite).

## Part 2: Repeated measurements

**Same direction twice:** same result every time. N stays N, S stays S.

**Different directions:** vertical then horizontal gives a completely random N/S (50/50).

**Three measurements (vertical, horizontal, vertical):** the last result is 50/50 again.

Three conclusions from the book:
1. Repeating the same question gives the same answer (some answers are definite).
2. Randomness occurs.
3. Measurements affect outcomes (the middle question changed the answer to the third).

**Measurement:** in classical physics, measuring barely disturbs the system. In quantum mechanics, the act of measuring changes it, regardless of how gentle the measurement is.

**Randomness:** a coin toss only looks random (it is deterministic with perfect information). Quantum randomness is believed to be true randomness. Einstein suggested hidden variables; experiments (Bell's inequality) show simple hidden-variable theories fail.

**Polarized light (3-filter experiment):**
- Two filters at 90° block all light.
- Slide a third filter at 45° between them and light passes through.
- Same reason as spin: the middle measurement changes the photons.

**Connection to computing:** N can be read as bit 0 and S as bit 1. The last step of any quantum computation is a measurement, so the final answer is classical bits.

## Worked example

Start with 100 electrons already measured as N in the vertical direction.
- Measure horizontally: about 50 are N, about 50 are S.
- Keep the 50 N electrons and measure vertically again: about 25 are N, about 25 are S.

Classically you would expect all 50 to still be N vertically. They aren't.

## Self-test

1. Vertical N, then measure horizontally. Probabilities? (50/50)
2. Then measure vertically again. Result? (50/50, not definitely N)
3. Why can't an electron have a definite vertical and horizontal spin together? (Measuring one erases the other.)

## Interview questions

1. Why does a measurement in a different direction destroy the earlier result?
2. How is quantum randomness different from the randomness of a coin toss?
3. Explain the three-polarized-filter experiment and what it shows.

## To do

- [ ] Python notebook: simulate the vertical, horizontal, vertical experiment and check the 50/50 results
