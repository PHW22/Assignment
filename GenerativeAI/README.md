# 生成式人工智慧簡介
以下作業皆使用 Gemini API

## HW3 「Colab and Gradio Tutorial」 以API快速搭建自己的應用 
Part 1: Summarization 對文章進行總結  
Part 2: Role-Play 角色扮演遊戲(一問一答)    
Part 3: Customized Task 英翻中  

使用Gemini API key 或 OpenAI API key  

## HW4「Become_an_AI_Hypnosis_Master」
藉由提示詞提高精準度，更多參考:
1. [FB 林育聖](https://www.facebook.com/moinwawa/posts/pfbid0VBRrBKjvF2eP2ED3jWNTCpfK227uKC1uD3ZHMN5JpuY3bYdkeVMnM2hNh8ywagvWl)
2. In-Context Learning  

使用Gemini API key

## HW5 「LLM_fine_tuning」
調整模型超參數，以 Transformer 為例

## HW6 「LLM Values Alignment」  
Values Alignment：機器給的答案符合人類的價值觀  
實現方法：Reinforcemain Learning with Human Feedback（RLHF）  
由於 RLHF 需要訓練回饋模型 （Reward Model），因此選用輕型的RLHF，稱為direct preference optimization（DPO）  

| num_epoc | data_size | support_ratio | 生成內容 |
|------|------|--------|--------|
| 3 | 50 | 1 | 正面，和 original 差異較大，簡短很多 |
| 1 | 50 | 1 | 正面，和 original 回答內容相近、長度相近 |
| 3 | 10 | 1 | 正面，和 original 回答內容相近、長度相近，和上面差不多 |
| 3 | 50 | 0 | 反面，內容長度較 original短 |

模型：[Breeze-7b](https://www.mediatek.tw/blog/mediatek-research-breeze-7b)（聯發科）





