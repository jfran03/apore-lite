# Tangent-Line Problems

## Definition
For y = f(x), a tangent parallel to a line y = mx + b must have slope m; solve f'(a) = m. A tangent perpendicular to that line has slope -1/m when m ≠ 0; solve f'(a) = -1/m. If m = 0, a perpendicular tangent would be vertical, so a finite-derivative equation cannot find it.
> Source: MATH275-Week02-Lecture-Notes.pdf

## Key Concepts
- **Procedure:** after solving for the input a, compute f(a) to obtain the point (a, f(a)); then use y - f(a) = f'(a)(x - a) for the tangent-line equation.
  > Source: MATH275-Week02-Lecture-Notes.pdf
- **Normal line:** the line through (a, f(a)) perpendicular to the tangent. If f'(a) exists and is nonzero, its equation is y - f(a) = -1/f'(a) · (x - a). If f'(a) = 0, the normal is the vertical line x = a. If the curve instead has a vertical tangent, the normal is horizontal.
  > Source: MATH275-Week02-Lecture-Notes.pdf

## Examples
- Tangents parallel to a given line: find all points on g(x) = x³ - 3x whose tangent is parallel to y = 9x - 4. We need g'(x) = 9: 3x² - 3 = 9 ⟹ x = ±2. Since g(2) = 2 and g(-2) = -2, the points are (2,2) and (-2,-2), with tangent lines y - 2 = 9(x-2) and y + 2 = 9(x+2).
  > Source: MATH275-Week02-Lecture-Notes.pdf
- Perpendicular tangents: find every point on f(x) = 2x³ - 4x where the tangent is perpendicular to y = -½x + 3. The required tangent slope is 2 (negative reciprocal of -½). Since f'(x) = 6x² - 4 = 2, x = ±1. The points are (1,-2) and (-1,2).
  > Source: MATH275-Week02-Lecture-Notes.pdf

## Related Topics
- [The Derivative from First Principles](first-principle-derivative.md)
- [Basic Derivative Rules](derivative-rules.md)
