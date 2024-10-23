## Introduction

<p align="center">
  <img src="https://github.com/YuiEdwardChen/Enhancing-ASR-for-Diverse-Languages-through-Joint-Pre-training-and-Fine-tuning-with-Wav2Vec2-Models/blob/main/BL-JUST.2.png" width="450" title="hover text">

</p>

<h3>Problem Introduction:</h3>
<ul>
        <li>Robustness: One of the key challenges towards ASR models is the background noise. The stability of the ASR model have to be improved to deal with real-life speech.</li>
        <li>Applicability: Conventional ASR algorithms always have difficulties in handling various accents and dialects, recognizing limited data resources (minor languages), and adapting to new domains and speakers. Our new model hope to expand its application over those situations.</li>
</ul>

<h3>For Wav2Vec2:</h3>
As a Self-supervised learning (SSL) technique, the Wav2Vec2 model capture rich acoustic and linguistic features from speech data without requiring labeled inputs. Wav2Vec2 leverages vast amounts of unlabeled speech data to learn powerful representations, making it highly effective for ASR tasks involving low-resource languages, while conformer models mainly focus on major language.

<h3>For BL-JUST:</h3>
<ul>
        <li>Accuracy: The BL-JUST models displays lower Word Error Rate (WER) than conformer models which only contains one pre-training and fine-tuning loop (PT+FT). In this model, the latent feature representations of the Wav2Vec2 model are further optimized for down-stream tasks utilizing BL-JUST algorithm.</li>
        <li>Flexibility: The BL-JUST algorithm is able to help with the model to generalize and adapt across different linguistic settings, making it highly-flexible for multilingual ASR challenges. The cycle feedback mechanism, which allows Wav2Vec2 model to improve its representation performance, makes BL-JUST more stable towards dialect variations, background noise, and domain-specific requirements.</li>
        <li>Scope: BL-JUST's task-specific fine-tuning, which is combined with Wav2Vec2's strong pre-training, enables the model to better handle low-resource languages.</li>
</ul>

<h3>Contributions of the Method:</h3>
<ul>
        <li>We integrate BL-JUST with the Wav2Vec2 model to enhance the latent feature representations of Wav2Vec2. BL-JUST leverages recent advances in penalty-based optimization to address ASR challenges, while maintaining computational efficiency and ensuring convergence.</li>
        <li>We demonstrate the model’s ability to generalize across multiple languages using the Covost v2 dataset, highlighting its performance in diverse multilingual settings.</li>
</ul>

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
