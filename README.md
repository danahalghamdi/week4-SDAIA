Vehicle Image Classification using Fine-Tuning

This project demonstrates image classification using a pretrained deep learning model with fine-tuning.

Dataset

The CIFAR-10 dataset is used, with a subset of vehicle-related classes:
	•	Airplane
	•	Automobile
	•	Ship
	•	Truck

The dataset is downloaded directly inside the notebook using torchvision.datasets.CIFAR10, so no manual data upload is required.

Model

A pretrained ResNet18 model trained on ImageNet is used.
	•	The final fully connected layer is replaced to match the 4 target classes.
	•	Two training strategies are applied:
	•	Freeze: pretrained layers are frozen and only the final layer is trained.
	•	Unfreeze: all layers are trained to fully adapt to the new dataset.

Experiments

The model is trained and evaluated using:
	•	A small dataset (subset of the training data).
	•	The full dataset.

Results show that unfreezing the model achieves higher accuracy on both small and large datasets, at the cost of longer training time.

Environment
	•	Python 3
	•	PyTorch
	•	Torchvision
	•	Google Colab (GPU recommended)

How to Run
	1.	Open the notebook in Google Colab.
	2.	Make sure the runtime is set to GPU (if available).
	3.	Run all cells in order.
