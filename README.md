## Abstractive Text Summarization using Pegasus Model

This project focuses on implementing an abstractive text summarization system using the Pegasus model. We first evaluate various Transformer models including T5, BART, GPT2 and Pegasus on the CNN/Daily Mail dataset, and based on the evaluation metrics (ROUGE and BLEU scores), we found that Pegasus outperformed the others.
This Repository contains two files:
1. EvaluatingModelsForSummarisation:
   - For different models we have evaluated the Rogue scores on the CNN Dailymail Dataset
3. TextSummarisation:
   - We have finetuned our Pegasus Model on the SAMsum Dataset and also deployed on Gradio App
     
**Evaluation on CNN/Daily Mail Dataset**

We evaluated the performance of three Transformer models, T5, BERT, and Pegasus, on the CNN/Daily Mail dataset for abstractive text summarization. Here are the evaluation results:

| Model   | rouge1    | rouge2    | rougeL    | rougeLsum |
|---------|-----------|-----------|-----------|-----------|
| baseline| 0.365079  | 0.145161  | 0.206349  | 0.285714  |
| gpt2    | 0.166667  | 0.043796  | 0.115942  | 0.152174  |
| t5      | 0.175824  | 0.000000  | 0.131868  | 0.153846  |
| bart    | 0.365591  | 0.131868  | 0.215054  | 0.322581  |
| pegasus | 0.500000  | 0.244898  | 0.360000  | 0.460000  |

NOTE: This Rogue score is calculated only for one Sample and not the whole dataset.

Based on the evaluation metrics, we selected the Pegasus model for further experimentation and deployment.


**SAMSum Dataset and Fine-Tuning**

We first evaluated the SacreBLEU score and Rogue Score, and found that Pegasus outperformed other models. Then for fine-tuning, we used the SAMSum (Short Ad-hoc Message Summarization), a  dataset designed for the task of summarizing short conversational messages, particularly from social media platforms like WhatsApp. It consists of dialogue data with messages exchanged between speakers, along with manually annotated summaries for each conversation. We fine-tuned the Pegasus model on this dataset to adapt it to our specific domain.

**Deployment on Gradio App**

We deployed the fine-tuned Pegasus model on a Gradio app for easy access and usage. Users can input lengthy text documents such as app reviews, and the model will generate abstractive summaries in real-time.

**Summarisation of Text on Gradio:**

![summarise1](https://github.com/Arpit-Avasarmol/Text-Summarization/assets/88440241/1eadec4d-5c1f-495d-b745-1b930e9ca681)
![Summarise2](https://github.com/Arpit-Avasarmol/Text-Summarization/assets/88440241/b029be7f-45a7-457c-8d48-a14f9a57b6be)
