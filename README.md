# SageMath reproducibility package for *Trees with exactly three main eigenvalues*

This repository is the companion reproducibility package for the paper *Trees with exactly three main eigenvalues*. It collects the SageMath notebooks used for the symbolic verifications in Lemmas 3.3 and 3.4, the linear-system verification for Theorem 3.6, and the exhaustive computational searches reported in the conclusion for trees with exactly three main eigenvalues and exactly three Q-main eigenvalues.

Repository: https://github.com/ditf015/trees-with-3-main-eigenvalues

## Repository structure

- `lemma3_3/grobner_basis.ipynb`  
  Gröbner basis elimination and verification of the explicit coefficients
  $H_1,H_2,H_3$ for the Diophantine system in Lemma 3.3.

- `lemma3_4/grobner_basis.ipynb`  
  Gröbner basis elimination and verification of the explicit coefficients
  $H_1,H_2,H_3$ for the Diophantine system in Lemma 3.4.

- `theorem3_6/verify_linear_system_coefficients.ipynb`  
  Verification of the walk-count coefficients appearing in the linear system of Theorem 3.6.

- `search_trees_with_3_main_eigenvalues/A_all_mg_fast.ipynb`  
  Exhaustive search over all trees of order `n <= 35` with exactly three main eigenvalues.

- `search_trees_with_3_q_main_eigenvalues/Q-all-fix-next.ipynb`  
  Exhaustive search over all trees of order `n <= 35` with exactly three Q-main eigenvalues.

## Requirements

- SageMath 10.7 or a compatible recent version
- Jupyter Notebook, launched from the SageMath environment
- `gentreeg` from nauty/gtools for the exhaustive-search notebooks
- A C compiler such as `gcc` or `clang` for the worker code used in the exhaustive searches

> Important: run the notebooks with the SageMath kernel, not a plain Python kernel.

## How to run

1. Clone or download this repository.
2. Open a terminal in the repository root.
3. Start Jupyter through SageMath:

```bash
sage -n jupyter
```

4. Open the notebook corresponding to the result you want to reproduce.

## Notes

- The Gröbner basis notebooks verify both the elimination arguments and the
  displayed ideal-membership certificates used in the proofs.
- The exhaustive-search notebooks are long-running computations and may create result folders next to the notebook files.
- For an exact software citation, please use the archived GitHub or Zenodo release corresponding to the version you used.

## Citation

If you use this repository, please cite the associated paper and the archived software release when available. Citation metadata are provided in `CITATION.cff`.
