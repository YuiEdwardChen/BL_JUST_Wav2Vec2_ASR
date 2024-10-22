## Introduction

1. Copy the introduction from the main report.

With the rapid advancement of artificial intelligence (AI) and the growing complexity of input requirements in deep learning systems, Automatic Speech Recognition (ASR) has emerged as a widely used tool in numerous applications. ASR, a high-efficiency input method, can save an average of 20 minutes in our daily life compared to conventional methods such as typing~\cite{james2024advocating}. Despite the notable successes of AI, especially, deep learning, in ASR tasks, these systems continue to face several challenges. Key challenges include robustness to noise, handling various accents and dialects, limited data resources, and difficulties adapting to new domains and speakers~\cite{hinton2012deep}.

A promising approach to overcoming these challenges is through pre-training models on large, unlabeled datasets, which enables them to learn the underlying structure of languages. Self-supervised learning (SSL) has gained significant traction as a pre-training technique for ASR tasks, allowing models to capture rich acoustic and linguistic features from speech data without requiring labeled inputs. Wav2Vec2, an SSL technique, has shown notable improvement in ASR performance, especially in low-resource and multilingual settings~\cite{baevski2020wav2vec}. Wav2Vec2 leverages vast amounts of unlabeled speech data to learn powerful representations, making it highly effective for ASR tasks involving low-resource languages. While conventional ASR models often rely on large labeled datasets from major languages like English~\cite{james2024advocating}, low-resource languages, such as Ika~\cite{nzenwata2024automatic}, Chinese, or Turkish (from the Covost v2 dataset), present greater challenges. In these cases, supervised training often produces erroneous or misleading results, particularly in sensitive domains or conversational speech scenarios~\cite{cornell2024generating}. Wav2Vec2, however, effectively mitigates these issues due to its robust architecture and ability to learn powerful representations from unlabeled speech audio.

The Wav2Vec2 model has demonstrated impressive performance in many ASR tasks by leveraging self-supervised learning (SSL) on large amounts of unlabeled data. However, its latent feature representations can be further optimized for specific downstream tasks, especially in low-resource settings. The BL-JUST method~\cite{saif2024joint}, which integrates joint self-supervised training and supervised fine-tuning, addresses this need. BL-JUST refines the Wav2Vec2 model by combining SSL with task-specific supervised learning (SL) in an iterative, two-step process. This approach enables Wav2Vec2 not only to learn general acoustic features but also to adapt these features for more effective performance on downstream ASR tasks.

In low-resource ASR tasks, where labeled data is often limited, the BL-JUST method becomes particularly valuable. By cycling between SSL and SL, BL-JUST enhances the model’s ability to generalize and adapt across different linguistic settings, making it well-suited for multilingual ASR challenges. This cyclic feedback mechanism allows Wav2Vec2 to incrementally improve its representations, making it more robust to dialectal variations, noise, and domain-specific requirements. BL-JUST's impact is especially significant for underrepresented languages, where traditional models often struggle. The combination of Wav2Vec2’s strong pre-training and BL-JUST’s task-specific fine-tuning enables the model to better handle low-resource languages like Dutch, Mongolian, and Arabic, as found in the Covost v2 dataset~\cite{shi2024joyhallo}. This integration demonstrates Wav2Vec2’s adaptability and performance improvements in low-resource, multilingual ASR tasks, addressing key challenges in the field~\cite{kaloga2024multiview, jain2023wav2vec2}.

The contributions of our method are twofold:

\begin{itemize} \item We integrate BL-JUST with the Wav2Vec2 model to enhance the latent feature representations of Wav2Vec2. BL-JUST leverages recent advances in penalty-based optimization to address ASR challenges, while maintaining computational efficiency and ensuring convergence~\cite{saif2024joint}.

\item We demonstrate the model’s ability to generalize across multiple languages using the Covost v2 dataset, highlighting its performance in diverse multilingual settings~\cite{cheng2024task}.
\end{itemize}

By incorporating joint SSL and SL training steps, BL-JUST refines the learned feature representations of the Wav2Vec2 model beyond traditional fine-tuning, leading to superior performance in ASR tasks, particularly across a range of low-resource languages, compared to conventional approaches~\cite{tsiamas2024pushing}.

## Example Result


## Demonstration

## Installation

## Citation
