# Creating Advanced prompts

## Prompt Engineering

Prompt engineering involves crafting prompts to achieve desired outcomes. It's not a formal engineering discipline but rather a set of techniques for effective interaction with language models (LLMs).

### Example of a Prompt

Basic Prompt Example:

> Generate 10 questions on geography.

Techniques applied in this prompt:

- **Context**: Specifies "geography".
- **Limiting the output**: Requests no more than 10 questions.

### Limitations of Simple Prompting

Simple prompts might not always yield the desired results due to:

- **Broad Topics**: Vague coverage (e.g., countries, capitals, rivers).
- **Formatting**: Lack of specific format requirements.

### Techniques for Prompting

Prompting is an emergent property of LLMs, discovered through usage. Key techniques include:

- **Zero-shot prompting**: A single prompt without additional context.
- **Few-shot prompting**: Providing examples to guide the model.
- **Chain-of-thought prompting**: Breaking down problems into steps.
- **Generated knowledge**: Adding facts or knowledge to improve responses.
- **Least to most prompting**: Sequentially solving steps of a problem.
- **Self-refine**: Critiquing and improving the model's output.
- **Maieutic prompting**: Ensuring accuracy by asking the model to explain parts of its answer.

### Zero-shot Prompting

A simple prompt without additional context or examples.

- Example:
  - Prompt: "What is Algebra?"
  - Answer: "Algebra is a branch of mathematics that studies mathematical symbols and the rules for manipulating these symbols."

### Few-shot Prompting

Provides examples to help the model understand the desired output.

- Example:
  - Prompt: "Write a poem in the style of Shakespeare. Here are a few examples of Shakespearean sonnets..."
  - Answer: "Upon the sky, the moon doth softly gleam, In silv'ry light that casts its gentle grace,..."

### Chain-of-thought Prompting

Guides the model through a series of steps to reach the correct answer.

- Example:
  - Prompt: "Lisa has 7 apples, throws 1 apple, gives 4 apples to Bart and Bart gives one back: 7 -1 = 6, 6 -4 = 2, 2 +1 = 3. Alice has 5 apples, throws 3 apples, gives 2 to Bob and Bob gives one back, how many apples does Alice have?"
  - Answer: 1

### Self-refine Technique

Involves critiquing the model’s output and requesting improvements.

- Steps:
  1. Initial prompt.
  2. Model answers.
  3. Critique the answer and ask for improvements.
  4. Model revises its response.

### Maieutic Prompting

Ensures the model’s output is accurate by asking for explanations of its parts.

- Steps:
  1. Ask a question.
  2. Request detailed explanations for each part of the answer.
  3. Identify and discard inconsistencies.
  4. Repeat until satisfied with the answer.

### Good Practices

- **Specify context**: More context improves relevance.
- **Limit the output**: Define the number of items or length.
- **Specify both what and how**: Clearly state what you want and how you want it.
- **Use templates**: Enrich prompts with data and variables.
- **Spell correctly**: Correct spelling enhances response quality.
