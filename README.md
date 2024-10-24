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

<ul>
        <li>The Relationship Between WERs and the Learning Rates: We conduct the search using 3 convolutional layers and 5 LSTM layers to identify the optimal learning rates. We utilize different configurations for α (self-supervised learning rate) and β (supervised learning rate). The best configuration, $\alpha = 10^{-3}$ and $\beta = 10^{-4}$, yields the lowest WER of 10.0%.
        <li>The Relationship Between WERs and the Number of CNN and LSTM layers: We demonstrate the effect of varying the number of LSTM and CNN layers on ASR performance that increasing the number of layers generally improves the Word Error Rate (WER). For example, models with 6 LSTM layers achieve the best WER across both PT+FT and BL-JUST methods, with BL-JUST reaching a WER as low as 9.5%. However, with this improvement comes the cost of increased computational complexity and longer running time. We limited our experiments to a maximum of 6 LSTM layers and 4 CNN layers, for further increases in layer numbers spends more computational resources.

## Demonstration

A demonstration of the Dutch speech recognition task.

<p align="center">
  <img src="https://github.com/YuiEdwardChen/Enhancing-ASR-for-Diverse-Languages-through-Joint-Pre-training-and-Fine-tuning-with-Wav2Vec2-Models/blob/main/dutch%20gif.gif" width="550" title="hover text">

</p>

## Installation

## Citation

We will write this after the arxiv submission.
