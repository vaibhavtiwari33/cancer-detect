# Histopathological Cancer Detection
Among the many steps in cancer identification, one conclusive
test involves sampling tissue from suspicious lumps and
observing it under a microscope to ascertain if it is malign.
Manual analysis of slides under a microscope is a painstaking
and time-consuming task, often prone to human error. This
project aims to explore machine learning and neural networks
as a tool for accurate detection of metastatic cancer. We use the
PatchCamelyon dataset which contains histopathologic scans
of lymph node sections of size (96 x 96 px) which are labelled
either 0/1 for absence/presence of cancer which we are trying
to predict.
We conducted experiments with three different deep learning
models and performed data augmentation on the input dataset
to add regularization, making it more robust to unseen data.
We also performed test-time augmentation to further improve
model efficiency. The CNN model from scratch and models
built from ResNet50 and MobileNetV2 were trained with 3
different methods of setting learning rates across epochs:
* Constant learning rate: Fixed learning rate across all
epochs.
* One Cycle Policy: Learning rate is initially gradually
increased on a slope upto a maximum value, and then
reduced. Extremely low learning rate applied in the final
epochs.
* Reduce Learning Rate on Plateau: Learning rate reduced
by a fixed factor when model’s validation accuracy
does not improve over some epochs.


We have used TensorFlow and Keras API to implement
all the models.

[Logistic Regression and CNN](https://nbviewer.jupyter.org/github/vaibhavtiwari33/cancer-detect/blob/main/LogisticRegression_CNN.ipynb):
1. Execute the following command in the execution directory:
   ln -s /datasets/home/91/391/sakundu/Project . 
2. The provided notebook can be run step by step. 

[MobileNetV2](https://nbviewer.jupyter.org/github/vaibhavtiwari33/cancer-detect/blob/main/MobileNetV2.ipynb):
1. Open the notebook on Google Colab. 
2. The provided notebook can be run step by step.

[ResNet50](https://nbviewer.jupyter.org/github/vaibhavtiwari33/cancer-detect/blob/main/ResNet50.ipynb):
1. Update the variable data_base_dir to '/datasets/home/91/391/sakundu/Project'
2. Prepend the following lines before importing modules:
   import sys
   sys.path.append('/opt/conda/lib/python3.7/site-packages')
3. The provided notebook can be run step by step. 


Peruse through our report for a detailed explaination on the dataset used, our approaches in tackling the challenge and analysis of each of our approaches.
