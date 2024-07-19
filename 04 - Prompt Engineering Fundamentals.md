# Prompt Engineering Fundamentals

- _Tokenization_ = how the model "sees" the prompt
- _Base LLMs_ = how the foundation model "processes" a prompt
- _Instruction-Tuned LLMs_ = how the model can now see "tasks"

### Tokenization

An LLM sees prompts as a _sequence of tokens_ where different models (or versions of a model) can tokenize the same prompt in different ways. Since LLMs are trained on tokens (and not on raw text), the way prompts get tokenized has a direct impact on the quality of the generated response. Example: [OpenAI Tokenizer](https://platform.openai.com/tokenizer?WT.mc_id=academic-105485-koreyst).

### Concept: Foundation Models

Once a prompt is tokenized, the primary function of the Base LLM is to predict the next token in that sequence. LLMs are trained on big text datasets, they have a good sense of the statistical relationships between tokens and can make that prediction with some confidence. They don't understand the _meaning_ of the words in the prompt, they just see a pattern. They can continue predicting the sequence till terminated by user intervention or some pre-established condition.

### Concept: Instruction Tuned LLMs

An Instruction Tuned LLM starts with the foundation model and fine-tunes it with examples or input/output pairs (e.g., multi-turn "messages") that can contain clear instructions - and the response from the AI attempt to follow that instruction.

## Why do we need Prompt Engineering?

### Key Challenges and Solutions

1. **Stochastic Responses**

   - _Issue_: The same prompt can produce different responses with different models or even the same model at different times.
   - _Solution_: Prompt engineering techniques can help minimize variations by providing better guardrails.

2. **Fabricated Responses**

   - _Issue_: Models can produce completions that are inaccurate, imaginary, or contradictory due to limitations in their training data.
   - _Solution_: Prompt engineering techniques help identify and mitigate fabrications, e.g., by asking AI for citations or reasoning.

3. **Varying Model Capabilities**
   - _Issue_: Different models and versions have unique quirks and trade-offs in cost and complexity.
   - _Solution_: Prompt engineering helps develop best practices and workflows to adapt to model-specific requirements seamlessly.
