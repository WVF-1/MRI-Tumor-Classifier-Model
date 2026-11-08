# Figures

The audit preview PNGs and a CNN architecture diagram are included now. Run notebooks 1-3 in order to generate the complete numbered figure series. Each notebook writes publication-resolution PNGs here.

## Included previews

- `01_class_counts_512.png` - counts of exact 512×512 images by folder label.
- `02_sample_scans.png` - one representative scan from each label that has retained images.
- `03_validation_exact_duplicates.png` - exact byte overlap in the shipped validation split after the 512×512 filter.
- `04_fold_class_balance.png` - expected held-out class counts across five stratified folds.
- `cnn_architecture.png` - an explanatory CNN diagram used in Notebook 2.

## Full notebook figure series

| Figure | Notebook | Visual |
|---|---|---|
| 01 | 1 | Class counts through each cleaning step |
| 02 | 1 | Representative scans by retained class |
| 03 | 1 | Shipped train/validation duplicate leakage |
| 04 | 1 | Stratified fold class balance |
| 05 | 2 | Training and validation learning curves |
| 06 | 2 | CNN feature maps |
| 07 | 3 | Accuracy and macro-F1 by fold |
| 08 | 3 | Out-of-fold confusion matrix |
| 09 | 3 | Per-class precision and recall |
| 10 | 3 | Class activation maps for held-out predictions |

The notebook creates model-result figures only after the corresponding training run completes. CAMs are qualitative checks, not evidence of clinical reasoning.
