# AIML 425 T2/2022 - PROJECT
## Wavelet decomposition

The first step in my pipeline is a decomposition of the training data set into 4 wavelet components (LL, LH, HL, HH). This is performed in the following notebook.
[Jupyter Notebook for Wavelet decomposition](https://github.com/econdatatech/AIML425/blob/main/Project/Wavelet_decomposition.ipynb)
[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/econdatatech/AIML425/blob/main/Project/Wavelet_decomposition.ipynb)
LL Result: https://drive.google.com/file/d/19jblBdeuVY7wO0s_LTb036t6p3BIHxWx/view?usp=share_link
LH Result: https://drive.google.com/file/d/15KFbRlG18QAMyzQ9__fblp0iRhz0ItGq/view?usp=share_link
HL Result: https://drive.google.com/file/d/18eACoQobUFMhI15banoUCBNEq1jdcCOr/view?usp=share_link
HH Result: https://drive.google.com/file/d/1wcuvhFWQ7HefHnhr90mPPsB8PTb-CJx8/view?usp=share_link

## Training of diffusion models
Next we train 4 separate diffusion models on each of the wavelet decompositions (LL, LH, HL, HH). All models were trained for 100k. The original paper trained their model for 700k epochs, but that wasn't in my time or monetary budget (cloud GPU)
[LL Diffusion](https://github.com/econdatatech/AIML425/blob/main/Project/Gauss%20CelebA%2064LL.ipynb)
[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/econdatatech/AIML425/blob/main/Project/Gauss%20CelebA%2064LL.ipynb)
LL Result: https://drive.google.com/file/d/1g7fO-dHYNUDuNdjV3IIqWrQ7MHYlylN9/view?usp=share_link
[LH Diffusion](https://github.com/econdatatech/AIML425/blob/main/Project/Gauss%20CelebA%2064LH.ipynb)
[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/econdatatech/AIML425/blob/main/Project/Gauss%20CelebA%2064LH.ipynb)
LH Result: https://drive.google.com/file/d/1YWtUG0-S8BcWVOFowfEkd05-WPhX60ze/view?usp=share_link
[HL Diffusion](https://github.com/econdatatech/AIML425/blob/main/Project/Gauss%20CelebA%2064HL.ipynb)
[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/econdatatech/AIML425/blob/main/Project/Gauss%20CelebA%2064HL.ipynb)
HL Result: https://drive.google.com/file/d/1k0aVtu0lE9APo-4H_PuRZ0X-BRZti_wv/view?usp=share_link
[HH Diffusion](https://github.com/econdatatech/AIML425/blob/main/Project/Gauss%20CelebA%2064HH.ipynb)
[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/econdatatech/AIML425/blob/main/Project/Gauss%20CelebA%2064HH.ipynb)
HH Result: https://drive.google.com/file/d/13nkO4OOCd62fBv949VCeyVZ-RePhHhPd/view?usp=share_link

## Generating new images with trained model
I use the 4 model to denoise 4 wavelet components (LL, LH, HL, HH)
[Denoise test](https://github.com/econdatatech/AIML425/blob/main/Project/Test_on_training_data.ipynb)
[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/econdatatech/AIML425/blob/main/Project/Test_on_training_data.ipynb)

## Recompose from denoised wavelet components
Last but not least we try to puzzle the denoised wavelet components back together to one single picture
[Recompose](https://github.com/econdatatech/AIML425/blob/main/Project/Recomposition.ipynb)
[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/econdatatech/AIML425/blob/main/Project/Recomposition.ipynb)
