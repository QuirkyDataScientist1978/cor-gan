# COR-GAN: Correlation-Capturing Convolutional Neural Networks for Generating Synthetic Healthcare Records

This repository contains an implementation of "COR-GAN:
Correlation-Capturing Convolutional Neural Networks for Generating
Synthetic Healthcare Records". This is not an officially supported
Google product.


For the following reason, this implementation *does not contain* the ``full implementation`` of the code:
* Ongoing research
* The restrictions regarding this work.

For a detailed description of the architecture please read [our paper](https://arxiv.org/abs/2001.09346). Using the code of this reposity is allowed with **proper attribution**: Please cite the paper if you use the code from this repository in your work.

## Bibtex

    @article{torfi2020cor,
    title={COR-GAN: Correlation-Capturing Convolutional Neural Networks for Generating Synthetic Healthcare Records},
    author={Torfi, Amirsina and Fox, Edward A},
    journal={arXiv preprint arXiv:2001.09346},
    year={2020}
    }

## Contributions

**Abstract:** *Deep learning models have demonstrated high-quality performance in areas such as image classification and speech processing.
However, creating a deep learning model using electronic health record (EHR) data, requires addressing particular privacy challenges that are unique to researchers in this domain. This matter focuses attention on generating realistic synthetic data while ensuring privacy.
In this paper, we propose a novel framework called correlation-capturing Generative Adversarial Network (corGAN), to generate synthetic healthcare records. In corGAN we utilize Convolutional Neural Networks to capture the correlations between adjacent medical features in the data representation space by combining Convolutional Generative Adversarial Networks and Convolutional Autoencoders.
To demonstrate the model fidelity, we show that corGAN generates synthetic data with performance similar to that of real data in various Machine Learning settings such as classification and prediction. We also give a privacy assessment and report on statistical analysis regarding realistic characteristics of the synthetic data.*

## Running the Code

### Prerequisites

* Pytorch ``1.4``
* CUDA [strongly recommended]

**NOTE:** PyTorch does a pretty good job in installing required packages but you should have installed CUDA according to PyTorch requirements.
Please refer to [our paper](https://pytorch.org/) for further information.

### Datasets

You need to download and process the following datasets as due to privacy restrictions we cannot provide the data here.

* MIMIC-III dataset: https://mimic.physionet.org/ [implementation with this dataset is included]
* UCI Epileptic Seizure Recognition dataset: https://archive.ics.uci.edu/ml/datasets/Epileptic+Seizure+Recognition [implementation with this dataset is NOT included]

One good source code for processing MIMIC-III can be found [here](https://github.com/mp2893/medgan).


### Training

To check the implementation refer to the folder ``Generative`` and you will see the following implementations:

* corGAN: The implementation of the paper with concolutional autoencoders and regular multi-layer perceptions for discriminator and generator.
* corGAN: The implementation of the [medGAN paper](https://arxiv.org/abs/1703.06490) as one of the baselines. This is a reimplemetation of this medGAN in ``PyTorch`` as we could not reproduce the results with [their code](https://github.com/mp2893/medgan). Furthermore, **PyTorch is more flexible compare to TensorFlow for research!**
* VAE: One of the the baselines.
