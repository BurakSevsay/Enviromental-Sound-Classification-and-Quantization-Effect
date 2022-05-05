# Enviromental-Sound-Classification-and-Quantization-Effect
This is a lecture project (MMI-727, Deep Learning: Methods and Applications). 2021-2022 Fall.

The project aims to construct a CNN model for environmental sound classification problem. Then, investigate the quantization effect on the constructed model.
Link for the Dataset: [UrbanSound8k](https://urbansounddataset.weebly.com/)

128 MFCC coefficient is extracted from the each audio in the dataset. [LibRosa](https://librosa.org/doc/latest/index.html) library is used for MFCC extraction.

Convolutional Neural Network is defined. It is consistent with the paper [1]. The paper uses 2D convolution, and construct 1D MFCC features as 2D image. It is found unnecessary. Therefore, 1D convolution is used in this project. Layer types and numbers are consistent with the paper.

Three types of quantization are applied. They are static post training quantization, dynamic post training quantization, and quantization aware training. Pytorch library is used for quantization.
Inference time is calculated on CPU, so they dont show the correct results. Model size and accuracy become the main results of this project.

[1] K. J. Piczak, "Environmental sound classification with convolutional neural networks," 2015 IEEE 25th International Workshop on Machine Learning for Signal Processing (MLSP), 2015, pp. 1-6, doi: 10.1109/MLSP.2015.7324337.
