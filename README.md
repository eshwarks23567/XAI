# XAI

This repository contains a Python-based visualization notebook focused on model evaluation and explainable AI (XAI)-style reporting through publication-quality performance plots.

The primary artifact in this repo is the notebook `visualisation_and_XAI.ipynb`, which generates a comprehensive set of figures to compare multiple deep learning models on a multi-class classification task (example class labels: Glioma, Meningioma, No Tumor, Pituitary). The notebook currently uses predefined metric values and synthetic data generation to demonstrate evaluation visualizations.

## Contents

- `visualisation_and_XAI.ipynb`: End-to-end notebook that:
  - Defines a performance-metrics table for multiple models
  - Produces multiple comparison figures (bar charts, radar chart, ROC curves, confusion matrices, heatmap)
  - Prints a concise summary of the best-performing model based on the provided metrics

## Visualizations Generated

The notebook generates the following evaluation visuals:

1. Metrics comparison across models (subplot bar charts)
2. Radar chart for multi-metric comparison
3. Grouped bar chart with simulated cross-validation error bars
4. ROC curves (synthetic scores used to approximate target AUCs)
5. Confusion matrices for multi-class classification (synthetic predictions)
6. Performance summary heatmap
7. Statistical significance-style visualization using simulated p-values

## Metrics Included

The comparison uses the following metrics:

- Accuracy
- Precision
- Recall
- Specificity
- F1-Score
- AUC

Models included in the comparison (as defined in the notebook):

- MLP
- AlexNet
- InceptionV3
- R-CNN
- VGG16-Ensemble

## Requirements

Typical dependencies used in the notebook:

- Python 3.x
- numpy
- pandas
- matplotlib
- seaborn
- scikit-learn

## How to Run

### Option A: Run locally

1. Clone the repository:
   ```bash
   git clone https://github.com/eshwarks23567/XAI.git
   cd XAI
   ```

2. Install dependencies:
   ```bash
   pip install numpy pandas matplotlib seaborn scikit-learn
   ```

3. Launch Jupyter and open the notebook:
   ```bash
   jupyter notebook
   ```

4. Run all cells in `visualisation_and_XAI.ipynb`.

### Option B: Run in Google Colab

Open `visualisation_and_XAI.ipynb` in Colab and run the cells in order.

## Notes and Limitations

- Several plots (ROC curves, confusion matrices, error bars, and p-values) are generated using synthetic data to match the provided metric targets. Replace these sections with real predictions and probabilities if you want results tied to an actual dataset and trained models.
- The metrics table is currently hard-coded. For real experiments, compute metrics directly from `y_true` and `y_pred` (and probabilities where applicable).

## Suggested Next Steps (Optional Enhancements)

- Load real experiment outputs (predictions, probabilities, fold metrics) instead of using synthetic generation.
- Add a `requirements.txt` (or `environment.yml`) for reproducible environments.
- Add SHAP/LIME/Grad-CAM examples if the goal is model interpretability beyond evaluation reporting.

## License

Add a license file if you intend to make usage permissions explicit.
