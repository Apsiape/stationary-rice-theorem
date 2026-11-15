# A Rice theorem for stationary states under fixed noise

Seth Douglas and Nidhal Mghirbi. Version 1.0.0, November 2026. DOI for all versions: [10.5281/zenodo.24241163](https://doi.org/10.5281/zenodo.24241163); version 1.0.0: [10.5281/zenodo.24241164](https://doi.org/10.5281/zenodo.24241164).

**This is a preprint. It has not been peer reviewed. The authors have not independently verified the mathematical arguments; see "How it was checked" below.**

## Abstract

Which macroscopic questions about a noisy lattice can an algorithm decide from its local rule? Fix dimension seven and one positive rational replacement rate. Every nontrivial property determined by the number of extreme translation-invariant stationary laws, all-law ergodicity, and the existence of a translation-invariant stationary law with nondecaying local covariance is undecidable. A stronger theorem retains the numbers of extreme translation-invariant stationary states with nondecaying covariance and with a Bragg atom at some nonzero wavevector. The same statements hold for finite-depth circuits of local quantum channels with fresh product ancillas, followed by whole-site depolarization. Under a stated published-source condition C_T, at another fixed rational rate the total-count cuts "at most r" and "at least k" are respectively Π⁰₂-complete for every r ≥ 1 and Σ⁰₂-complete for every k ≥ 2, in both categories. The scope has a decidable boundary: a classical translation-invariant stationary law attains the noise entropy floor exactly when the deterministic rule is constant.

## What the paper proves

Theorem letters refer to `paper/main.pdf`. The statements below are quoted from the paper, with its notation written out in plain text.

- **Theorem A.** "For deterministic finite-range rules on Z^7 followed by uniform replacement at one fixed positive rational rate, every nontrivial property determined by the number of extreme translation-invariant stationary laws, all-law ergodicity, and existence of a translation-invariant stationary law with nondecaying local covariance is undecidable."
- **Theorem B (stationary-state Rice theorem).** For the datum σ = (N, N_ord, N_Br, E, L), where N counts the extreme translation-invariant stationary states, N_ord those with nondecaying cross-covariance, N_Br those with a Bragg atom at some nonzero wavevector, E means that a unique stationary state among all states attracts every initial state locally, and L means that some translation-invariant stationary state has nondecaying covariance: at D = 7 and the rate ε₀ = B^(-200) (B = 2Δ², Δ = 18·5K, K = 16^4), "in each input category separately, every nontrivial predicate of σ is undecidable." The two input categories are the classical rules of Theorem A and finite-depth circuits of local quantum channels with exact algebraic entries and fresh product ancillas, followed by whole-site depolarization.
- **Theorem C (phase-count completeness under C_T).** "Assume C_T. At D = 7 and the single rate ε₁ = 160000^(-101), in each input category separately, {M : N(M) ≤ r} is Π⁰₂-complete for every finite r ≥ 1, and {M : N(M) ≥ k} is Σ⁰₂-complete for every finite k ≥ 2, under computable many-one reductions." Condition C_T, stated in full in Section 6, is the validity of a totality source built on Törmä's 2015 construction (his Lemma 25, Corollary 26 and Lemmas 27–29, as published). The total-count cuts are the only predicates of the datum shown complete; for the others the paper gives one-sided second-level hardness and excludes nontrivial Δ⁰₂ members.
- **The decidable boundary (Section 7).** A classical translation-invariant stationary law attains the noise entropy floor exactly when the deterministic rule is constant, a finite exact test; the quantum one-site version is also proved.

The classical uniqueness, ergodicity and total-count instances of Theorem A already follow from our earlier forgetting preprint (Douglas and Mghirbi, version 2.2.0, Corollary 3.11), whose controller theorem this paper imports. The new content is the host-preserving construction and its Rice closure, the ordered and Bragg-ordered counts, the long-range-order flag, the quantum category and the conditional completeness theorem. Section 1 of the paper gives the full credits, including Kari's Rice theorem for limit sets, the undecidability of ergodicity for probabilistic cellular automata, and Sandhu's undecidable Gibbs uniqueness at fixed temperature. Open: realizability of exactly k ≥ 2 extreme translation-invariant stationary states, smaller fixed alphabets, lower dimensions, arithmetic upper bounds for the ordered and Bragg counts and for L, and matching degrees for all-law ergodicity.

## Contents and reproduction

- `paper/main.pdf`: the manuscript (23 pages).
- `paper/`: the LaTeX source (`main.tex`, `sections/`, `references.tex`), the plain-text abstract and a strict build driver. Run `python -B build.py` there with pdflatex installed. The build disables shell escape, runs pdflatex three times, and rejects warnings, unresolved references and box defects.
- `SHA256SUMS`: SHA-256 hashes of every shipped file except this manifest. Check with `sha256sum -c SHA256SUMS` from the repository root.

## How it was checked

The paper's section "How this work was done" gives the account. The authors directed the work. GPT-6.1 Sol agents in Codesk sessions found the constructions and proofs, with in-session audits, and drafted the text. Claude Opus 5.5, a model from a different family, checked the main theorem, its extension and the completeness theorem refutation-first, ran a literature check and reviewed the text. A final readback checked every revision against the proofs and reviews, rebuilt the paper and spot-checked nine citations against their sources. The authors have not independently verified the mathematical arguments. The results are written proofs; they are not formalized in Lean.

## Citation and rights

See `CITATION.cff` for citation metadata. Paper and documentation: CC BY 4.0. Script (`paper/build.py`): MIT or Apache 2.0, at your option. See `RIGHTS.md`, the license files and `NOTICE`.
