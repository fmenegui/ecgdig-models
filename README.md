# ecgdig models

Network weights used by [ecg-digitalization-classic](https://github.com/fmenegui/ecg-digitalization-classic)
(`ecgdig`): one GitHub release per trained model, with the ONNX file ecgdig loads and the PyTorch
checkpoint to continue training from.

Every release names the training run (a `gpu-train.yml` run of ecg-digitalization-classic), the
code commit, the training data and the validation numbers.

Training data: pages and photos rendered from PTB-XL signals (PhysioNet, CC BY 4.0) with
ecg-torch-renderer. PM-ECG-ID and LITFL are never used for training; the PM-ECG-ID source ECGs are
removed from the PTB-XL bank. Weights trained on pages of the Kaggle "PhysioNet - Digitization of ECG
Images" competition are not published here.

| Release | Network | Config field |
|---|---|---|
| `page-*` | page structure (rows, lead changes, lead names) | `page_model` |
| `dewarp-*` | photo flattening field | `dewarp_model` |
