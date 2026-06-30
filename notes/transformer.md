## Why do RNNs struggle with very long sequences?
```
RNNs process sequences one element at a time, passing information through a hidden state. For long sequences, information from earlier tokens must travel through many intermediate hidden states before reaching later tokens. This makes it difficult to preserve long-range dependencies, and during training, gradients propagated through many time steps can vanish or explode. Although LSTMs improve memory, they still process tokens sequentially. Transformers overcome these limitations by allowing every token to directly attend to every other token through the attention mechanism."
```

## Self attention
```
Which other words in this sentence should I pay attention to in order to understand the current word?
```

## Query, Key, Value.
```
Query = What information am I looking for?
Key = What information do I contain?
Value = What information do I provide if I'm selected?
```

## Self-attention and multi-head attention
```
A single attention mechanism can capture only one type of relationship at a time. Multi-Head Attention allows the model to learn multiple relationships in parallel. Different attention heads can focus on different aspects of the input, such as syntactic dependencies, semantic meaning, or long-range relationships. Combining these perspectives produces richer contextual representations.
```

## Encoder vs Decoder

```
Encoder - Helps understand the input and used for problems like classification, sentiment analysis, NER

Decoder - Required for next token generation

Transformers
        │
        ├──► BERT (Encoder)
        │       - Classification
        │       - Sentiment Analysis
        │       - NER
        │
        ├──► GPT (Decoder)
        │       - Chatbots
        │       - Code Generation
        │       - LLMs
        │
        └──► Encoder-Decoder
                - Translation
                - Summarization
```