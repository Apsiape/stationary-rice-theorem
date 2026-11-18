# A Rice theorem for stationary states under fixed noise

Seth Douglas and Nidhal Mghirbi. Preprint, version 2.0.0, November 2026. [Archive DOI](https://doi.org/10.5281/zenodo.24241163) (all versions)

## Abstract

Which macroscopic questions about a noisy lattice can an algorithm decide from its local rule? We show that already on the line, for deterministic finite-range rules followed by independent uniform replacement at one fixed positive rational rate, every nontrivial property determined by the number of extreme translation-invariant stationary laws, all-law ergodicity, and the existence of a translation-invariant stationary law with nondecaying local covariance is undecidable. A refined theorem retains the numbers of extreme translation-invariant stationary states with nondecaying covariance and with a Bragg atom at some nonzero wavevector. The same holds for circuits of local quantum channels on the line with independent single-qubit depolarization after every layer, and, with uniqueness among all Gibbs measures in place of ergodicity, for Gibbs measures on the square lattice given by positive rational Boltzmann weights. On the line, ergodicity excludes nondecaying covariance, and two or more translation-invariant stationary states force nondecaying covariance and exclude ergodicity, so only four kinds of coarse data can occur. In both line categories, for every r ≥ 1 the cut "at most r extremes" is Π⁰₂ and halting-hard, and for every k ≥ 2 the cut "at least k" is Σ⁰₂ and nonhalting-hard. In dimension seven the same Rice theorem holds for quantum circuits followed by whole-site depolarization, and under a stated published-source condition C_T, at another fixed rational rate, these cuts are Π⁰₂-complete and Σ⁰₂-complete in both categories. The scope has a decidable boundary: a classical translation-invariant stationary law attains the noise entropy floor exactly when the deterministic rule is constant.

## Results

Theorem numbers refer to `paper/main.pdf`. N counts the extreme translation-invariant stationary states, N_ord those with nondecaying covariance and N_Br those with a Bragg atom at some nonzero wavevector; E means that one stationary state attracts every initial state (all-law ergodicity), and L that some translation-invariant stationary state has nondecaying local covariance.

- **Theorem 3.1 (the line, classical).** For deterministic finite-range rules on Z followed by independent uniform replacement at one fixed positive rational rate, every predicate of (N, E, L) that is nonconstant on the realized data is undecidable.
- **Theorem 3.2 (the line, quantum).** The same holds for circuits of local quantum channels on Z with independent single-qubit depolarization after every layer.
- **Theorem 3.3 (refined).** In each category on the line, every predicate of (N, N_ord, N_Br, E, L) that is nonconstant on the realized values is undecidable; halting or nonhalting many-one reduces to it, according to its value at the realized continuum datum.
- **Theorem 7.1 (the square lattice).** For Gibbs measures on Z^2 given by positive rational Boltzmann weights, the same holds with E replaced by uniqueness among all Gibbs measures.
- **Theorem 8.1 (necessary data on the line).** Ergodicity excludes nondecaying covariance, and two or more translation-invariant stationary states force nondecaying covariance and exclude ergodicity, so only four kinds of coarse data (N, E, L) can occur; two of them are realized.
- **Theorem 8.3 (degrees on the line).** For every r ≥ 1 the cut N ≤ r is Π⁰₂ and halting-hard; for every k ≥ 2 the cut N ≥ k is Σ⁰₂ and nonhalting-hard.
- **Theorems A, B and C (dimension seven, unchanged from version 1.0.0).** The Rice theorem on Z^7 for classical rules and for quantum circuits followed by whole-site depolarization; under the stated published-source condition C_T, the cuts N ≤ r and N ≥ k are Π⁰₂-complete and Σ⁰₂-complete.
- **Theorems 13.1 and 13.2 (the decidable boundary).** A classical translation-invariant stationary law attains the noise entropy floor exactly when the deterministic rule is constant; the quantum one-site version is also proved.

## Archive contents

- `paper/` contains the manuscript PDF, the LaTeX sources, the plain-text abstract, a strict build driver and build instructions.
- The root contains citation metadata, licensing information and `SHA256SUMS`, the SHA-256 digest of every distributed file except the checksum list itself. Verify it from the archive root with `sha256sum -c SHA256SUMS`.

## Build the paper

From `paper/`, run `python -B build.py` with pdfLaTeX installed. The driver disables shell escape, runs pdfLaTeX three times, and rejects warnings, unresolved references and box defects. No bibliography program or external images are required. The tested engine is MiKTeX-pdfTeX 4.23 (MiKTeX 25.12). [Build instructions](paper/README.txt)

## Changes in version 2.0.0

The paper adds the theorems on the line: the classical, quantum and refined Rice theorems (Theorems 3.1 to 3.3), the square-lattice Gibbs version for positive rational weights (Theorem 7.1), the necessary data on the line (Theorem 8.1) and partial degree results (Theorem 8.3). Theorems A, B and C and the other seven-dimensional results are unchanged in statement from [version 1.0.0](https://doi.org/10.5281/zenodo.24241164).

## Citation and license

Douglas, Seth, and Nidhal Mghirbi (2026). *A Rice theorem for stationary states under fixed noise*. Version 2.0.0. [Archive DOI](https://doi.org/10.5281/zenodo.24241163) · [Citation metadata](CITATION.cff)

Paper and documentation are licensed under CC BY 4.0; the build script `paper/build.py` under MIT or Apache 2.0, at your option. [Licensing details](RIGHTS.md)
