# Original dataset mapping

The supplied 139 MB `archive (7).zip` is stored as two GitHub-compatible binary parts: `archive.zip.part01` and `archive.zip.part02`. Each part is below GitHub's 100 MB per-file limit. Notebook data-loading cells automatically concatenate them into `data/archive.zip` before extraction.

The archive root maps directly to the notebook loader:

| Archive path | Notebook use |
|---|---|
| `Train/Glioma/images/*.jpg` | Folder-derived label `Glioma`; original training partition |
| `Train/Meningioma/images/*.jpg` | Folder-derived label `Meningioma`; original training partition |
| `Train/No Tumor/images/*.jpg` | Folder-derived label `No Tumor`; original training partition |
| `Train/Pituitary/images/*.jpg` | Folder-derived label `Pituitary`; original training partition |
| `Val/<class>/images/*.jpg` | Same folder-derived label; original validation partition, audited only |

YOLO annotation text files are not used for image-level classification. The notebooks keep exact 512x512 images, use folder names as labels, remove byte-identical duplicates, and form new stratified folds. The archive has 5,249 images; only 16 No Tumor images are 512x512, so that class is excluded from five-fold model training by the minimum-count rule.

The listing names the Nickparvar brain-tumor MRI collection and the Sartaj Bhuvaji collection as inspiration. Review source terms before redistribution or publication.
