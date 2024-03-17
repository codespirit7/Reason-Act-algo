# ReAct: Synergizing Reasoning and Acting in Language Models

## Abstract

Integrating LLMs (Large Language Models) with external tools is a frequently used technique in the real business applications.
For instance, ChatGPT plugins can interact with external tools in its conversations. Microsoft has also integrated LLMs (OpenAI GPT) and external tools (such as, Office applications) in Copilot framework.
Another example is the search integration. LLMs doesn’t always give correct answers, and the method to interact with external search engine (for both internet and intranet) is then often applied in real QA systems.
Several flexible architectures with combination between LLM’s reasoning and additional tools (experts) are then proposed in several papers – such as, in ReAct (Reasoning + Acting) or MRKL (Modular Reasoning, Knowledge and Language).

ReAct is a fundamental of agent framework which has been introduced in this paper (Shunyu et al., 2022).
As you can see in this post, you can apply this method in various types of automation (orchestration) between LLMs and external tools.
For instance, now we define the action “search [entity]” which returns the sentences from the corresponding Wikipedia entity. By applying ReAct prompting, the multi-hop questions (which cannot be answered from a single Wikipedia entity, 
but can be answered by referencing the multiple entities) can then be disassembled into multiple search’s actions and all actions will then be processed by external tools.
Finally, the answer is obtained using all these threads as a context in LLM’s question-answering. 

## Run your First ReAct

```
git clone git@github.com:codespirit7/Reason-Act-algo.git

cd <Your-cloned-app-directory>

npm install

# set your OPENAI_API_KEY in .env file

npm run build

npm run start

```

After executing the cmd you will get the desired ouptut as below.


![Screenshot from 2024-03-17 09-56-20](https://github.com/codespirit7/Reason-Act-algo/assets/88592710/dc2da34b-c603-41df-88d6-c134942226e2)

List of References:
 
  https://arxiv.org/abs/2210.03629
  
  https://tsmatz.wordpress.com/2023/03/07/react-with-openai-gpt-and-langchain/
  
  https://react-lm.github.io/



