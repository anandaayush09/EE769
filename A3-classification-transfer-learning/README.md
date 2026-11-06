# A3 — Classification, feature engineering & transfer learning

Notebook: `classification_transfer_learning.ipynb`

## Objective 1 — Bank marketing campaign prediction
Predict campaign success from the UCI/Kaggle *Bank Marketing* data (`data/bank.csv`; Moro, Cortez & Rita, 2014 is cited in the notebook as a reference).
1. EDA: usable variables, correlations, class balance of `poutcome`.
2. Outlier removal, one-hot encoding, train/test split.
3. Five-fold cross-validation with grid search for Random Forest, SVM and MLP.
4. Feature importance per model (impurity-based and permutation importance).
5. Test-set evaluation with the chosen metrics, plus sanity checks that the models "work".

## Objective 2 — Transfer learning
- **Ants vs bees:** fine-tune a pretrained ResNet-18 (PyTorch) on the hymenoptera set (`data/hymenoptera_data/{train,val}`).
- **CIFAR-10** (PyTorch/torchvision) and **Fashion-MNIST** with MobileNetV2 (TensorFlow/Keras) — datasets download automatically.

## Data (`data/`)
| Item | In repo? |
|------|----------|
| `bank.csv` | yes |
| `hymenoptera_data/` | no — download the standard ants/bees set and place `train/` and `val/` here |
| `cifar-10-batches-py/` | no — torchvision downloads it when missing |

## Run
```bash
jupyter notebook classification_transfer_learning.ipynb
```
Launch from this folder. The grid searches and deep-learning cells are slow on CPU; a GPU (or Colab) is recommended.
