# AI Agents

AI Agents enable LLMs to evolve from assistants into agents capable of taking actions. AI Agent frameworks allow developers to create applications that give LLMs access to tools and state management. These frameworks also enhance visibility, allowing users and developers to monitor the actions planned by LLMs..

### What Are AI Agents?

AI Agents allow Large Language Models (LLMs) to perform tasks by giving them access to a **state** and **tools**.

- **Large Language Models**: These are the models such as GPT-3.5, GPT-4, Llama-2, etc.
- **State**: Refers to the context that the LLM is working in, including past actions and current context, guiding its decision-making.
- **Tools**: Resources like databases, APIs, external applications, or even other LLMs that the LLM can use to complete tasks.

### LangChain Agents

[LangChain Agents](https://python.langchain.com/docs/modules/agents/?WT.mc_id=academic-105485-koreyst) manage the state using a built-in function called the `AgentExecutor`, which accepts the defined `agent` and available `tools`. The `AgentExecutor` stores the chat history to provide context.

LangChain offers a [catalog of tools](https://integrations.langchain.com/tools?WT.mc_id=academic-105485-koreyst) that can be imported into your application. The team at LangChain has also developed LangSmith to enhance visibility into which tools the LLM is using and why.

### AutoGen

[AutoGen](https://microsoft.github.io/autogen/?WT.mc_id=academic-105485-koreyst) focuses on conversations and enables LLMs to be **conversable** and **customizable**.

- **Conversable**: LLMs can start and continue conversations with other LLMs to complete tasks.
- **Customizable**: Agents can be LLMs, users, or tools. For instance, a `UserProxyAgent` can interact with the user for feedback.

AutoGen uses Python code to manage state and execute tasks, with system messages guiding the LLM on relevant functions.

### Taskweaver

[Taskweaver](https://microsoft.github.io/TaskWeaver/?WT.mc_id=academic-105485-koreyst) is a "code-first" agent framework, useful for data analysis and generation tasks, and works with DataFrames in Python.

- **State and Tools**: Managed by a `Planner`, an LLM that maps out tasks based on user requests. Plugins, such as Python classes or code interpreters, are used to complete tasks.

Taskweaver verifies the code before execution and uses `experience` to store conversation context over the long term, improving LLM performance on repetitive tasks.

### JARVIS

[JARVIS](https://github.com/microsoft/JARVIS?tab=readme-ov-file?WT.mc_id=academic-105485-koreyst) uses an LLM to manage the state of the conversation, with tools being other specialized AI models.

- The LLM receives user requests, identifies tasks, and formats requests for specialized AI models.
- The LLM interprets responses from multiple models and integrates them to generate the final user response.
