# Power and Energy

## Definition
In electric circuits, power is the product of voltage and current: P = Vi. Equivalently, power is the rate of energy transfer: P = (dw/dq)·(dq/dt) = dw/dt, in units of J/s.
> Source: Week 3 - Full.pdf

## Key Concepts
- **Power as rate of energy transfer:** P = (dw/dq)·(dq/dt) = dw/dt [J/s], where dw/dq is the voltage V and dq/dt is the current i.
  > Source: Week 3 - Full.pdf
- **Unit of power:** P is power in Watts [W].
  > Source: Week 3 - Full.pdf
- **Passive reference direction:** If the current is labelled in the direction of voltage drop (`i →  + V −`), this is called the passive reference direction, which implies the element is absorbing power. In this case we must use **P = Vi**.
  > Source: Week 3 - Full.pdf
- **Current in direction of voltage rise:** If the current is labelled in the direction of voltage rise (`i →  − V +`), then we must use **P = −Vi**.
  > Source: Week 3 - Full.pdf
- **Sign interpretation:** In both cases (whether using P = Vi or P = −Vi): if P > 0, the element is absorbing power; if P < 0, the element is supplying power.
  > Source: Week 3 - Full.pdf
- **Energy from power:** Since P = dw/dt, energy is W = ∫[t₁ to t₂] P(t) dt.
  > Source: Week 3 - Full.pdf
- **Why energy matters:** Power companies measure energy to determine the monthly bill — i.e. usage of power over time.
  > Source: Week 3 - Full.pdf
- **kWh conversion:** 1 W = 1 J/s, therefore 1 J = 1 W·s = (1/1000) kW · (1/3600) h, and so 1 kWh = 3600 × 1000 J.
  > Source: Week 3 - Full.pdf

## Examples
- **Sign convention example (a):** For an element with V₁ = 12 V and i₁ = 10 A, where the current is in the direction of voltage rise: P = −V₁i₁ = −(12 V)(10 A) = −120 W. The element supplies 120 W.
  > Source: Week 3 - Full.pdf
- **Sign convention example (b):** For an element with V₁ = 60 V and i₁ = −10 A: P = −V₁i₁ = −(60 V)(−10 A) = 600 W. The element absorbs 600 W. Alternatively, the direction of the current can be changed to match the actual direction, giving P = Vi = (60 V)(10 A) = 600 W — the same result.
  > Source: Week 3 - Full.pdf
- **Energy example:** For an element with v(t) = 10 V and i(t) = 2e^(−t) A, with current in the direction of voltage drop: p(t) = v(t)·i(t) = 10 × 2e^(−t) = 20e^(−t) W. The power starts at 20 W and decays; the energy from t = 0 → ∞ is the area under the p(t) curve. w = ∫₀^∞ 20e^(−t) dt = −20e^(−t)|₀^∞ = 0 − (−20) = 20 J. Since w > 0, the element absorbs energy.
  > Source: Week 3 - Full.pdf
- **Electricity bill example:** Energy cost is $0.12 per kWh and the 30-day electrical bill is $60.00, with power constant over the period. (a) Total energy consumed in 30 days is W = $60.00 / ($0.12/kWh) = 500 kWh, so P = W/t = 500 kWh / (30 × 24) h = 694.4 W. The accumulated energy is w(t) = ∫₀^t p(t) dt = ∫₀^t 694.4 dt = 694.4t, rising linearly to 500 kWh at 30 days. (b) With voltage = 120 V, P = Vi gives i = P/V = 694.4 W / 120 V = 5.8 A.
  > Source: Week 3 - Full.pdf

## Common Misconceptions
- The source raises and answers the question "but isn't power the rate of energy transfer?" — showing that P = Vi and P = dw/dt are the same thing, since P = (dw/dq)·(dq/dt) with dw/dq = V and dq/dt = i.
  > Source: Week 3 - Full.pdf

## Related Topics
- [Resistors and Ohm's Law](resistors-and-ohms-law.md)
- [Power in Resistors](power-in-resistors.md)
