# Vehicle Image Classification using Fine-Tuning

This project demonstrates image classification using a pretrained deep learning model with fine-tuning.

---

## Dataset
- **CIFAR-10** dataset is used.
- Only vehicle-related classes are selected:
  - Airplane
  - Automobile
  - Ship
  - Truck
- The dataset is downloaded automatically inside the notebook using:
  ```python
  torchvision.datasets.CIFAR10

  Model
	•	A ResNet18 pretrained on ImageNet is used.
	•	The final fully connected layer is replaced to match 4 target classes.

## Training Strategies

## Freeze
	•	Pretrained layers are frozen.
	•	Only the final classification layer is trained.
	•	Faster training, lower accuracy.

## Unfreeze
	•	All layers are trained.
	•	Slower training, higher accuracy.

⸻

## Experiments

The model is trained and evaluated using:
	•	A small dataset (subset of the training data).
	•	The full dataset.

## Observations
	•	Unfreezing the model achieves higher accuracy on both small and large datasets.
	•	This comes at the cost of longer training time.

⸻

## Environment
	•	Python 3
	•	PyTorch
	•	Torchvision
	•	Google Colab (GPU recommended)

⸻

## How to Run
	1.	Open the notebook in Google Colab.
	2.	Set runtime to GPU (if available).
	3.	Run all cells in order.
