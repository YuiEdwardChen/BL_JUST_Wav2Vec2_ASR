## Introduction

<p align="center">
  <img src="https://github.com/YuiEdwardChen/Enhancing-ASR-for-Diverse-Languages-through-Joint-Pre-training-and-Fine-tuning-with-Wav2Vec2-Models/blob/main/BL-JUST.2.png" width="450" title="hover text">

</p>

<h3>For BL-JUST</h3>


<p align="center">
  <img src="https://github.com/YuiEdwardChen/Enhancing-ASR-for-Diverse-Languages-through-Joint-Pre-training-and-Fine-tuning-with-Wav2Vec2-Models/blob/main/Wav2vec2.3.png" width="450" title="hover text">

</p>

## Example Result

Three experiments were conducted to evaluate the model's performance in different learning rates, numbers of CNN and RNN layers, and low-resource datasets. The first example generated and compared WERs under different learning rate settings of BL-JUST using CNN-LSTM acoustic models on Librispeech. We used 3 CNN layers and 5 LSTM layers and kept them constant while changing the pre-training (α) and fine-tuning (β). The experiment result showed that when $\alpha = 10^{-3}$ and $\beta = 10^{-4}$, the WER was the lowest, and it was the optimal learning rates for the BL-JUST settings in this model. In the second experiment, we tested WERs under various number of CNN and LSTM layers settings of BL-JUST using CNN-LSTM acoustic models on Librispeech. As we increased the numbers oof CNN layers and LSTM layers, the WERs for Pre-training and Fine-tuning (PT+FT) and for BL-JUST both decreased while the number of parameters increased. For each numbers of CNN and LSTM layers, WER(PT+FT) was higher than WER(BL-JUST). As for the final experiment, we evaluated WERs of Wav2Vec2-JUST and Wav2Vec2 (FT) on Dutch, Mongolian, and Arabic languages using training datasets. For each low-resource language, the WER for Wav2Vec2 (FT) was higher than the one of Wav2Vec2-JUST. All the three methods demonstrate the effectiveness of our model on low-resource datasets using a combination of Wav2Vec2 architecture and BL-JUST on CNN-LSTM settings.

## Demonstration

I will complete it. 

## Installation

## Citation

We will write this after the arxiv submission.
