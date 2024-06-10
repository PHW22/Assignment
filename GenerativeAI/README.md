# 生成式人工智慧簡介

## HW3 「Colab and Gradio Tutorial」 以API快速搭建自己的應用 
Part 1: Summarization 對文章進行總結  
Part 2: Role-Play 角色扮演遊戲(一問一答)    
Part 3: Customized Task 英翻中  

使用Gemini API key 或 OpenAI API key  

## HW4「Become_an_AI_Hypnosis_Master」
藉由提示詞提高精準度，更多參考:
1. [FB 林育聖](https://www.facebook.com/moinwawa/posts/pfbid0VBRrBKjvF2eP2ED3jWNTCpfK227uKC1uD3ZHMN5JpuY3bYdkeVMnM2hNh8ywagvWl)
2. In-Context Learning  

使用 Gemini API key

## HW5 「LLM fine tuning」
調整模型超參數，以 Transformer 為例

## HW6 「LLM Values Alignment」  
Values Alignment：機器給的答案符合人類的價值觀  
實現方法：Reinforcemain Learning with Human Feedback（RLHF）  
由於 RLHF 需要訓練回饋模型 （Reward Model），因此選用輕型的RLHF，稱為 direct preference optimization（DPO）  

| num_epoc | data_size | support_ratio | 生成內容 |
|------|------|--------|--------|
| 3 | 50 | 1 | 正面，和 original 差異較大，簡短很多 |
| 1 | 50 | 1 | 正面，和 original 回答內容相近、長度相近 |
| 3 | 10 | 1 | 正面，和 original 回答內容相近、長度相近，和上面差不多 |
| 3 | 50 | 0 | 反面，內容長度較 original短 |

模型：[Breeze-7b](https://www.mediatek.tw/blog/mediatek-research-breeze-7b)（聯發科）

## HW7 「LLM explanation」  
方法一：[inseq](https://github.com/inseq-team/inseq/)  
套件內有多種方法，作業內使用 'saliency' 和 'attention'。生成表格查看 input tokens 和 output tokens 的相關性。  
saliency：從 output tokens 回推，每一個 output tokens 對每一個 input tokens 的重要性（數值）。  
attention：常用於 transfotmer-based models，數值代表 output tokens 對應 input tokens 的權重（猜測：attention 由第一個 token 往後生成，因此第一個權重最高）。  
方法二：[問LLM](https://arxiv.org/pdf/2310.11207)  
給LLM一句話，依照正反面，給每一個單字評分（正面1，反面-1）  

## HW8 「Safety Issues of Generative AI」  
LLaMA-2-7B：未經過 fine-tuning，可以生成歧視性言論的句子  
TULU-2-DPO-7B：經過 fine-tuning，無法生成歧視性言論的句子  

## HW9 「Quick Summary of Lecture Video」  
透過 Whisper 將語音轉文字，藉由 API 連接 ChatGPT 整理重點  
整理重點方法一：Multi-Stage Summarization，拆成 n 段落，每個段落分別重點整理  
整理重點方法二：Refinement，拆成 n 段落，第 1 段落做總結，(總結 + 第2段落) 做總結，(總結 + 第3段落) 做總結，以此類推  

## HW10 「Stable Diffusion Fine-tuning」









