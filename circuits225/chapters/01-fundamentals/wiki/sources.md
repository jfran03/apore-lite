# Sources (Independent and Dependent)

## Definition
All circuit elements are characterized by their voltage-current relationships. Sources are circuit elements categorized as independent voltage sources, dependent voltage sources, independent current sources, and dependent current sources.
> Source: Week 2 - Full.pdf

## Key Concepts
- **Independent Voltage Source:** Voltage (potential difference) is specified exactly and is not affected by any other circuit element. Current through the source depends on the circuit it is connected to and must be found by solving the circuit. Can be DC (e.g. a constant 30 V source, with terminal a higher in potential than terminal b by 30 V) or AC (e.g. 100 sin(120πt)).
  > Source: Week 2 - Full.pdf
- **Dependent Voltage Source:** Has the same properties as an independent voltage source, except the value of voltage depends on either a voltage or current elsewhere in the circuit. A voltage-controlled voltage source (VCVS) has value μV_x, where V_x is the controlling voltage and μ is a constant (no unit). A current-controlled voltage source (CCVS) has value μi_x, where i_x is the controlling current and μ is a constant (unit: V/A). These can be AC or DC.
  > Source: Week 2 - Full.pdf
- **Independent Current Source:** Current is specified explicitly and is not affected by other circuit elements. Voltage across the source depends on the circuit it is connected to and must be found by solving the circuit. Can be DC (e.g. 10 A) or AC (e.g. 100 cos(120πt)).
  > Source: Week 2 - Full.pdf
- **Dependent Current Source:** Same properties as an independent current source, except the current depends on a voltage or current elsewhere in the circuit. A voltage-controlled current source (VCCS) has value μV_x (unit: A/V). A current-controlled current source (CCCS) has value μi_x (no units).
  > Source: Week 2 - Full.pdf
- **Controlling variable labeling:** For all dependent sources, i_x or V_x are always labeled on the circuit — their direction/polarity does not need to be assumed. The given reference polarity or direction for V_x and i_x is not necessarily the actual polarity or direction of voltage or current for the controlling element.
  > Source: Week 2 - Full.pdf

## Examples
- A circuit with a VCVS (3V_x) and a CCVS (2i_x): if V_x is calculated to be 2 V, the VCVS becomes a 6 V source (point 'a' higher in potential than point 'b' by 6 V; the current through the VCVS must still be found by solving the circuit). If i_x is calculated to be -2 A, the CCVS is -4 V, which is equivalent to a 4V source with reversed polarity.
  > Source: Week 2 - Full.pdf

## Common Misconceptions
- _(none explicitly stated in source)_

## Related Topics
- [Electric Circuits and Circuit Elements](electric-circuits-and-elements.md)
- [Voltage](voltage.md)
- [Current](current.md)
