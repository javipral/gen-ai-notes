# Open Source Models

## What are Open Source Models?

For a model to be truly open source, the following should be publicly available:

- Datasets used for training.
- Full model weights as part of the training.
- The evaluation code.
- The fine-tuning code.
- Full model weights and training metrics.

Few models meet these criteria, but the [OLMo model by Allen Institute for AI](https://huggingface.co/allenai/OLMo-7B?WT.mc_id=academic-105485-koreyst) is one example. Models below

## Benefits of Open Models

- **Highly Customizable**: Open models come with detailed training information, allowing researchers and developers to modify the model's internals for specialized tasks like code generation, mathematical operations, and biology.
- **Cost**: Using and deploying these models is cheaper than proprietary models. Performance versus cost should be considered when building Generative AI applications.
- **Flexibility**: Open models offer flexibility in terms of usage and combination with other models. For instance, [HuggingChat Assistants](https://huggingface.co/chat?WT.mc_id=academic-105485-koreyst) allow users to select the model directly in the interface.

## Exploring Different Open Models

### Llama 2

[LLama2](https://huggingface.co/meta-llama?WT.mc_id=academic-105485-koreyst) by Meta is optimized for chat-based applications due to its fine-tuning with a large amount of dialogue and human feedback, improving user experience. Examples of fine-tuned versions include [Japanese Llama](https://huggingface.co/elyza/ELYZA-japanese-Llama-2-7b?WT.mc_id=academic-105485-koreyst) and [Llama Pro](https://huggingface.co/TencentARC/LLaMA-Pro-8B?WT.mc_id=academic-105485-koreyst).

### Mistral

[Mistral](https://huggingface.co/mistralai?WT.mc_id=academic-105485-koreyst) focuses on high performance and efficiency using the Mixture-of-Experts approach, where specialized expert models are selected based on the input. Fine-tuned versions include [BioMistral](https://huggingface.co/BioMistral/BioMistral-7B?text=Mon+nom+est+Thomas+et+mon+principal?WT.mc_id=academic-105485-koreyst) for the medical domain and [OpenMath Mistral](https://huggingface.co/nvidia/OpenMath-Mistral-7B-v0.1-hf?WT.mc_id=academic-105485-koreyst) for mathematical computation.

### Falcon

[Falcon](https://huggingface.co/tiiuae?WT.mc_id=academic-105485-koreyst) by the Technology Innovation Institute (TII) was trained on 40 billion parameters, outperforming GPT-3 with less compute budget due to its use of the FlashAttention algorithm and multiquery attention, making it suitable for chat applications. Fine-tuned versions include [OpenAssistant](https://huggingface.co/OpenAssistant/falcon-40b-sft-top1-560?WT.mc_id=academic-105485-koreyst) and [GPT4ALL](https://huggingface.co/nomic-ai/gpt4all-falcon?WT.mc_id=academic-105485-koreyst).

## How to Choose

Choosing an open model depends on specific use case. Tools like Azure AI Studio's filter by task feature and the Hugging Face LLM Leaderboard can help identify suitable models. For comparisons, [Artificial Analysis](https://artificialanalysis.ai/?WT.mc_id=academic-105485-koreyst) is a useful resource.

Experimenting with multiple open models to see how they perform according to expectations is recommended.
