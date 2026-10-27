# Constrained Optimization

## Definition
You are asked to find the global (absolute) max or min of a function of two variables, subject to some kind of physical, geometrical or otherwise mathematical constraint.
> Source: Week of October 16.pdf

## Key Concepts
- **Procedure:**
  1. Write down the function you are trying to maximize or minimize.
  2. Write down the constraint as an equation.
  3. Use the constraint equation to **reduce** the number of variables in the optimized quantity down to one.
  4. Use either the closed or global interval method to optimize the desired quantity.
  5. If needed, use the constraint equation to determine the value of the other variable at the optimized points.
  > Source: Week of October 16.pdf
- **Role of the constraint:** the constraint gives a relation between the variables (e.g. between y and x), which is what lets the objective become a function of one variable.
  > Source: Week of October 16.pdf
- **Physical domain restrictions:** physical quantities give the domain, e.g. lengths satisfy x > 0 and y > 0. This typically makes the interval open, so the global interval method is used.
  > Source: Week of October 16.pdf
- **Simplifying assumptions:** real-world problems are modelled with stated assumptions before optimizing.
  > Source: Week of October 16.pdf

## Examples
- **Concrete-lined hole.** A rectangular hole with a square base (open top) is excavated. The walls and floor are lined with concrete; the concrete on the walls must be three times the thickness of the floor. If the hole has volume 48 m³, determine the dimensions that minimize the concrete used.
  - Let x = side of the square base, y = depth. Note x > 0 and y > 0.
  - Constraint: 48 = Vol = x²y, giving a relation between y and x.
  - Simplifying assumptions: (i) 1 unit/m² on the floor; (ii) 3 units/m² on the walls; (iii) the poured concrete has zero volume.
  - Objective: M = amount of concrete needed = M_base + M_walls = 1·x² + 3·4·xy (mass per m² × area of base, plus mass per m² × number of walls × area of each wall) = x² + 12xy.
  - Apply the constraint y = 48/x²: M(x) = x² + 12x·(48/x²) = x² + 576/x, for x > 0.
  - Critical points: 0 = M'(x) = 2x − 576/x² ⇔ x³ = 288 ⇔ x = ∛288 = 2∛36 ≈ 6.6 m.
  - Sign of M'(x): try x = 1, negative; try x = 1000, positive. Single critical point, so it must be the global min (the local min is the global min).
  - When x = ∛288: y = 48/x² = 48/288^(2/3) = 12/36^(2/3) ≈ 1.1 m.
  - The required dimensions are ≈ 6.6 m (base side) and 1.1 m (depth).
  > Source: Week of October 16.pdf

## Related Topics
- [Closed Interval Method](closed-interval-method.md)
- [Global Interval Method](global-interval-method.md)
- [Related Rates](related-rates.md)
