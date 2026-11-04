# Basis-independent Kirkwood-Dirac nonclassicality: certification and a robust contextuality test

Companion code for the paper of the same title by **Sudip Chakrabarty** (S. N. Bose National Centre for Basic Sciences, Kolkata, India).

The notebook [`Basis_independent_KD_nonclassicality_reproduction_final.ipynb`](Basis_independent_KD_nonclassicality_reproduction_final.ipynb) reproduces every numerical result, table and figure of the paper, in the order in which they appear. Each section of the notebook names the section, equation, figure or table of the paper that it reproduces, so that any number in the paper can be traced to the line of code that produces it.

## About the paper

Negative and nonreal values of the Kirkwood-Dirac quasiprobability distribution underlie quantum advantages in metrology, thermodynamics and weak measurements, yet they are defined relative to reference bases that an experiment has to describe and calibrate. The paper defines this nonclassicality without any reference basis, as the failure of a set of states to have only nonnegative Bargmann invariants. The resulting resource lies strictly between basis-independent coherence and imaginarity, is the presence of a nontrivial geometric phase for pure states, and can be certified by cycle tests with one measured invariant per independent loop of the set. Its fourth-order part, invisible to ordinary Kirkwood-Dirac distributions, violates a noncontextuality inequality for sequential weak measurements that tolerates realistic imperfections, and a single-photon experiment with walk-off crystals and a quadrant detector would show the violation with about 10⁷ detected photons.

## What the notebook reproduces

| Paper | Content of the notebook |
|---|---|
| Sec. II C, Fig. 1, App. A | Exact simulation of the cycle test, confirming that the ancilla measures the Bargmann invariant. Fig. 1 |
| Sec. III B | Nonnegativity of all two-letter invariants up to order five for random mixed states |
| Sec. III D, Fig. 2 | Two pure states that are set coherent but KD classical, the trine invariant −1/8. Fig. 2 |
| Sec. III E, Fig. 3 | Cyclomatic number β(H) = 2 for the graph of Fig. 3, and a test of Theorem 2 in both directions on six states. Fig. 3 |
| Sec. III F | Signed-cycle states in KC<sub>k−1</sub> but not KC<sub>k</sub> for k = 3,…,6, and the invariant Tr(Π₀Π₊Π₁Π₋) = −1/4 |
| Secs. III G and III H | Mixed trine: third-order invariant, the order bound of Theorem 5, and the smallest Bloch length with a negative word for orders 3, 4, 5, 6 and 12 |
| Sec. III I | A pair of real qutrit states with a negative sixth-order invariant, of order −10⁻⁸ |
| Sec. IV A | Hoeffding run numbers (973 for the trine, 244 for the four qubit states) and invariance under a common drift |
| Sec. IV B | Depolarized KD witness: q₁₊ = −0.10, classicality at p = 0.29, and the cost of the multi-copy witness at p = 0.9 |
| Sec. V A | Single weak values, the joint weak value −1/2, and the contextuality criterion −1/4 |
| Sec. V B | Numerical confirmation of Lemma 3, p<sub>d</sub> = (1 − \|κ\|)/2 |
| Sec. VI A, Fig. 4 | Gaussian pointer with sign readout and its small-shift behaviour. Fig. 4 |
| Secs. VI B and VI C | Ideal performance: violation for u < 0.381, optimal margin 1.74 × 10⁻³ at u = 0.254, and 5.0 × 10⁶ detected photons |
| Sec. VI D, Table I, Fig. 5 | Full error budget, Table I, measurement times, and Fig. 5 |
| Sec. VI E | Detector rotation: P<sub>mis</sub> = 2ϑ/π, the 0.68 mrad alignment tolerance, and the effect of a tilted walk-off direction |
| App. B | Pure qubit states satisfy KC₄ = KC, checked on 400 random tuples |
| App. D | Direct numerical integration of the pointer, and 20 000 random commuting configurations that never violate the bound of Theorem 6 |

## Requirements

* Python 3.9 or later
* `numpy`, `scipy`, `matplotlib`
* Jupyter (Notebook or Lab)
* Optional: a LaTeX installation. If `latex` is found, figure text is typeset with LaTeX so that it matches the paper. Otherwise matplotlib's built-in Computer Modern rendering is used, and all numerical results are unaffected.

Install the Python packages with

```bash
pip install numpy scipy matplotlib jupyter
```

## Running the notebook

```bash
git clone https://github.com/sudipchakrabarty27042000/Basis-independent-Kirkwood-Dirac-nonclassicality-certification-and-a-robust-contextuality-test.git
cd Basis-independent-Kirkwood-Dirac-nonclassicality-certification-and-a-robust-contextuality-test
jupyter notebook Basis_independent_KD_nonclassicality_reproduction_final.ipynb
```

Then run all cells (Kernel → Restart & Run All). A full run takes one to a few minutes on a laptop. The figures are written to `fig1.pdf` … `fig5.pdf`, with PNG copies, in the working directory.

To run the notebook from the command line instead:

```bash
jupyter nbconvert --to notebook --execute --inplace Basis_independent_KD_nonclassicality_reproduction_final.ipynb
```

All random numbers are drawn from seeded generators, so every run gives the same results. Differences at the level of 10⁻¹⁶ between machines are floating-point rounding.

## Citation

If you use this code, please cite the paper:

```bibtex
@article{Chakrabarty_KD_basis_independent,
  author = {Chakrabarty, Sudip},
  title  = {Basis-independent {Kirkwood-Dirac} nonclassicality: certification and a robust contextuality test},
}
```

The entry will be updated with the journal reference once the paper is published.

## Contact

Sudip Chakrabarty, S. N. Bose National Centre for Basic Sciences, Kolkata, India
sudip27042000@gmail.com

## License

This code is released under the MIT License. See [`LICENSE`](LICENSE).
