# ReAct: Synergizing Reasoning and Acting in Language Models

## Abstract

  While large language models (LLMs) have demonstrated impressive capabilities across tasks in language understanding and interactive decision 
  making, their abilities for reasoning (e.g. chain-of-thought prompting) and acting (e.g. action plan generation) have primarily been studied as 
  separate topics. In this paper, we explore the use of LLMs to generate both reasoning traces and task-specific actions in an interleaved manner, 
  allowing for greater synergy between the two: reasoning traces help the model induce, track, and update action plans as well as handle 
  exceptions, while actions allow it to interface with external sources, such as knowledge bases or environments, to gather additional information. 
  We apply our approach, named ReAct, to a diverse set of language and decision making tasks and demonstrate its effectiveness over state-of-the-
  art baselines, as well as improved human interpretability and trustworthiness over methods without reasoning or acting components. Concretely, 
  on question answering (HotpotQA) and fact verification (Fever), ReAct overcomes issues of hallucination and error propagation prevalent in chain-
  of-thought reasoning by interacting with a simple Wikipedia API, and generates human-like task-solving trajectories that are more interpretable
  than baselines without reasoning traces. On two interactive decision making benchmarks (ALFWorld and WebShop), ReAct outperforms imitation 
  and reinforcement learning methods by an absolute success rate of 34% and 10% respectively, while being prompted with only one or two in-
  context examples.


Integrating LLMs (Large Language Models) with external tools is a frequently used technique in the real business applications.
For instance, ChatGPT plugins can interact with external tools in its conversations. Microsoft has also integrated LLMs (OpenAI GPT) and external tools (such as, Office applications) in Copilot framework.
Another example is the search integration. LLMs doesn’t always give correct answers, and the method to interact with external search engine (for both internet and intranet) is then often applied in real QA systems.
Several flexible architectures with combination between LLM’s reasoning and additional tools (experts) are then proposed in several papers – such as, in ReAct (Reasoning + Acting) or MRKL (Modular Reasoning, Knowledge and Language).

ReAct is a fundamental of agent framework which has been introduced in this paper (Shunyu et al., 2022).
As you can see in this post, you can apply this method in various types of automation (orchestration) between LLMs and external tools.
For instance, now we define the action “search [entity]” which returns the sentences from the corresponding Wikipedia entity. By applying ReAct prompting, the multi-hop questions (which cannot be answered from a single Wikipedia entity, 
but can be answered by referencing the multiple entities) can then be disassembled into multiple search’s actions and all actions will then be processed by external tools.
Finally, the answer is obtained using all these threads as a context in LLM’s question-answering. 
