# Related Rates

## Definition
Related rates problems are the second type of word problem encountered (after optimization). These problems involve changing quantities that have a fixed relationship. Given sufficient starting information, you are tasked with determining unknown rates.
> Source: Week of October 16.pdf

## Key Concepts
- **Process:**
  1. Write down and label all quantities.
  2. Determine the relationship between these quantities.
  3. Differentiate the equation determining this relationship with respect to time.
  4. Substitute in the known values (this can be the hard part and may require referencing the original equation) and compute the unknown rate.
  > Source: Week of October 16.pdf
- **All quantities depend on t:** every labelled quantity is a function of time, so differentiating with respect to t uses implicit differentiation and the chain rule (e.g. d/dt[A^(3/2)] = (3/2)A^(1/2) · dA/dt).
  > Source: Week of October 16.pdf
- **Relating the right quantities:** if the known rate and the wanted rate involve different quantities, relate them in a single equation first (e.g. eliminate a shared variable).
  > Source: Week of October 16.pdf
- **Sign of a rate:** a decreasing quantity has a negative rate (a rope reeled in at 5 m/s has dz/dt = −5 m/s).
  > Source: Week of October 16.pdf
- **Substitute after differentiating:** some values needed in the differentiated equation are not given directly and must be found from the original relationship (e.g. finding z from x).
  > Source: Week of October 16.pdf

## Examples
- **Expanding sphere.** The surface area of a sphere is expanding at 10π m²/s. How quickly is the volume changing when the surface area is 400π m²?
  - Let r = radius in m. V = (4/3)πr³, A = 4πr²; all depend on t.
  - Want dV/dt when A = 400π m². Know dA/dt = 10π m²/s.
  - Relate V and A in a single equation by solving for r in A: r = √(A/(4π)). Then V = (4π/3)(A/(4π))^(3/2) = 4A^(3/2) / (3√π · 4^(3/2)) = (1/(6√π)) A^(3/2), using 4^(3/2) = 2³ = 8.
  - Implicitly differentiate w.r.t. t: dV/dt = (1/(6√π)) · (3/2) · A^(1/2) · dA/dt (chain rule) = (A^(1/2) / (4√π)) · dA/dt.
  - Substitute: dV/dt = ((400π)^(1/2) / (4√π)) · 10π = (20√π / (4√π)) · 10π = 50π m³/s.
  > Source: Week of October 16.pdf
- **Boat pulled to a pier.** A boat is pulled into a pier with a rope. The attachment point of the rope on the pier is 5 m higher than on the boat. What is the water speed of the boat when the boat is 13 m from the pier if the rope is reeled in at 5 m/s?
  - Let z = length of the rope, x = horizontal distance from the pier.
  - Know dz/dt = −5 m/s. Want dx/dt when x = 13 m.
  - Right triangle with legs 5 and x, hypotenuse z: z² = 25 + x².
  - Differentiate w.r.t. t: 2z · dz/dt = 0 + 2x · dx/dt, so dx/dt = (z/x) · dz/dt.
  - Need z when x = 13 (from the original equation): z = √(25 + 13²) = √194.
  - So dx/dt = (√194 / 13)(−5) m/s.
  > Source: Week of October 16.pdf

## Related Topics
- [Constrained Optimization](constrained-optimization.md)
