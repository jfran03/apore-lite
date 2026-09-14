# Power in Resistors

## Definition
For a resistor with current labelled in the direction of voltage drop, combining P = Vi with Ohm's Law V = iR gives P = i²R, or equivalently P = V²/R.
> Source: Week 3 - Full.pdf

## Key Concepts
- **Derivation:** Power P = Vi and Ohm's Law V = iR, therefore **P = i²·R** or **P = V²/R**.
  > Source: Week 3 - Full.pdf
- **Resistors always absorb:** P is always positive for resistors. They will always absorb power.
  > Source: Week 3 - Full.pdf
- **Source supplies what the resistor absorbs (worked example):** In the 100 V / 10 Ω circuit, the resistor absorbs 1000 W and the source supplies 1000 W.
  > Source: Week 3 - Full.pdf
- **Arbitrary current direction does not change the physical answer:** Choosing the reference direction for i_R the opposite way changes the sign of the computed current but yields the same actual current and the same power results.
  > Source: Week 3 - Full.pdf

## Examples
- **100 V source with 10 Ω resistor — find power for both elements.** The source notes that we "need to find unknown voltages & currents. For now, let's logic our way through this. Later, we will develop systematic ways of finding voltage & current."
  - *Step 1:* Find the voltage across the resistor. It is connected to the same 2 points as the 100 V source, so V_R = 100 V (point B is higher in potential than point A by 100 V).
  - *Step 2:* Choose an arbitrary direction for i_R.
  - *Step 3:* From Ohm's Law, i_R = V_R / 10 Ω = 100 V / 10 Ω = 10 A. For the resistor, P = V_R·i_R = (100 V)(10 A) = 1000 W — it absorbs 1000 W. This can also be computed as P = (i_R)²·R = (V_R)²/R.
  - *Step 4:* The current i_R will continue to flow through the source. Because the current sees the (−) terminal first, P_source = −V·i_R = −(100 V)(10 A) = −1000 W — the source supplies 1000 W.
  > Source: Week 3 - Full.pdf
- **Same circuit with the opposite reference direction for i_R:** Ohm's Law becomes V_R = −i_R·R, so i_R = −V_R/R = −100 V / 10 Ω = −10 A (the same actual current as before). For the resistor, P = −V_R·i_R = −(100 V)(−10 A) = 1000 W. For the source, P_source = (100 V)·i_R = (100 V)(−10 A) = −1000 W. Both results match the original choice of direction.
  > Source: Week 3 - Full.pdf

## Common Misconceptions
- _(none explicitly stated in source)_

## Related Topics
- [Resistors and Ohm's Law](resistors-and-ohms-law.md)
- [Power and Energy](power-and-energy.md)
