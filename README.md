# Perturbed-Alexanders invariant via quantum cluster algebras

Mathematica program to derive a perturbative expansion of knot invariants

© 2026 Boudewijn Bosch

---

## Acknowledgements
Boudewijn Bosch acknowledges support by the Dutch Research Council (NWO) under grant number 613.009.152.

---
## Table of Contents
- [What is this program?](#what-is-this-program)
- [Getting Started](#getting-started)
  - [Installing NCAlgebra](#installing-ncalgebra)
- [Usage](#usage)
- [Example Execution](#example-execution)
- [Contributors](#contributors)

---

## What is this program?
Using this program, a perturbed R-matrix is derived using the theory of quantum cluster algebras. The perturbed R-matrix can then be used to derive perturbed-Alexander polynomials using the perturbed Gaussian formalism provided in the Mathematica code due to Roland van der Veen and Dror Bar-Natan, available at https://www.rolandvdv.nl/PG/. The input is a Gauss code for a knot diagram, and the output is a perturbed-Alexander invariant.

---

## Getting Started

This package requires [Mathematica](https://www.wolfram.com/mathematica/) along with the following dependencies:

- [**NCAlgebra**](https://github.com/NCAlgebra/NC) — a noncommutative algebra package for Mathematica
- **NCGBX** — the noncommutative Gröbner basis package (ships with NCAlgebra)

### Installing NCAlgebra

Starting with version 6, NCAlgebra is installed via its paclet distribution. In Mathematica, run:

```mathematica
PacletInstall["https://github.com/NCAlgebra/NC/blob/master/NCAlgebra-6.0.3.paclet?raw=true"]
```

Once installed, load NCAlgebra and NCGBX with:

```mathematica
<< NC`
<< NCAlgebra`
<< NCGBX`
```

---

## Usage
The function $\text{Pert}_{i,j}$ computes the perturbed R-matrix. This is automatically computed by evaluating all initialization cells.

---

## Example Execution
Perturbed-Alexander polynomials for the trefoil:

```mathematica
Z31 = hR15 hR62 hR37 C4 hv8 hv9 hv10;
Do[Z31 = Z31 //. hm[i, 1] -> 1, {i, 2, 10}]
```
---

## Contributors
Boudewijn Bosch

