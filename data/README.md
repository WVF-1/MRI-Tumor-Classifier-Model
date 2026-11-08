# Original dataset mapping

The supplied `archive (7).zip` is the source archive for this project. Place it here as `data/archive.zip` (or set `ZIP_PATH` in each notebook to its location). It is intentionally not committed: the archive is about 139 MB, and the dataset is redistributed under its own source terms.

The archive root maps directly to the notebook loader:

| Archive path | Notebook use |
|---|---|
| `Train/Glioma/images/*.jpg` | Class label `Glioma`, original training partition |
| `Train/Meningioma/images/*.jpg` | Class label `Meningioma`, original training partition |
| `Train/No Tumor/images/*.jpg` | Class label `No Tumor`, original training partition |
| `Train/Pituitary/images/*.jpg` | Class label `Pituitary`, original training partition |
| `Val/<class>/images/*.jpg` | Same folder-derived class; original validation partition, used for audit only |

YOLO annotation text files are not used for image-level classification. The notebooks keep only exact 512×512 images, use folder names as labels, remove byte-identical duplicates, and form new stratified folds. The archive has 5,249 images total. Only 16 No Tumor images are 512×512, so that class is excluded from five-fold model training by the documented minimum-count rule.

The data source page lists the Nickparvar brain-tumor MRI collection and the Sartaj Bhuvaji collection as inspiration. See the root README for attribution and licensing caveats.
