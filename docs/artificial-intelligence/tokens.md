# Tokens for LLMs

Tokens are pieces of words used for natural language processing. For English text, 1 token is approximately 4 characters or 0.75 words². Large Language Models (LLMs) use a consumption pricing model that charges based on the amount of text characters (tokens) exchanged between the application and the AI³.

## OpenAI Charges

OpenAI charges per token for their text APIs, including Text Completion, Embeddings, and Fine-tuning³. The prices per 1,000 tokens vary per model. For example, the GPT-4 model from OpenAI charges $0.03 per 1,000 tokens for 8k context¹, while the GPT-3.5-Turbo model charges $0.002 per 1,000 tokens⁴.

## OpenAI Tokenizer

OpenAI has an online tool to calculate the number of tokens in text.  https://platform.openai.com/tokenizer

The below is 64 tokens and 252 characters
```
Many words map to one token, but some don't: indivisible.

Unicode characters like emojis may be split into many tokens containing the underlying bytes: 🤚🏾

Sequences of characters commonly found next to each other may be grouped together: 1234567890
```