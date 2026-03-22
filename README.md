# Series Fade Sequence

A self-running 3-LED light effect built in Falstad Circuit Simulator. All 3 LEDs light up together when the switch closes, then fade out one by one at different speeds — creating a waterfall sequence using RC timing.

---

## Demo

 gallary![assets/gif-of-faslad.gif]


**Live demo:** [https://is.gd/gSgEcT]


---

## How it works

When the switch closes, the 5V source charges all three capacitors. All 3 LEDs glow bright.

When the switch opens, each capacitor slowly discharges through its LED — creating the fade. Each branch has a different R and C value so they fade at different speeds:

| LED | Timing R | Capacitor | Fade time |
|-----|----------|-----------|-----------|
| LED 1 | 1kΩ | 100mF | Fast (~0.1s) |
| LED 2 | 1kΩ | 1mF | Medium (~1s) |
| LED 3 | 1kΩ | 10mF | Slowest (~5s) |

The fade time is controlled by the RC time constant: `time ≈ R × C`. Bigger R or C = longer glow. Each LED also has a 470Ω series resistor to protect it from too much current.

---

## Components

- 5V DC voltage source
- 1x switch
- 3x LEDs
- 3x 470Ω resistors (current limiters)
- 1kΩ, 1kΩ, 1kΩ resistors (timing)
- 100mF, 1mF, 10mF capacitors (timing)

---
