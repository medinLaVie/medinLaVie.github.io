---
title:  "AI Agentic Workflows"
date:   2024-04-01 10:55:00 # 4/3 10:55-
layout: page
#
# toc: true
# categories:
---

*What is an agentic workflow?*
Instead of having an LLM generate its final output directly, an agentic workflow prompts the LLM multiple times, giving it opportunities to build step by step to higher-quality output.

# 1.Reflection

You may have had the experience of prompting ChatGPT/Claude/Gemini, receiving unsatisfactory output, delivering critical feedback to help the LLM improve its response, and then getting a better response. What if you automate the step of delivering critical feedback, so the model automatically criticizes its own output and improves its response?

Take the task of asking an LLM to write code. We can prompt it to generate the desired code directly to carry out some task X. After that, we can prompt it to reflect on its own output, perhaps as follows:

Here’s code intended for task X:
[previously generated code]
Check the code carefully for correctness, style, and efficiency, and give constructive criticism for how to improve it.

Sometimes this causes the LLM to spot problems and come up with constructive suggestions. Next, we can prompt the LLM with context including (i) the previously generated code and (ii) the constructive feedback, and ask it to use the feedback to rewrite the code. This can lead to a better response. Repeating the criticism/rewrite process might yield further improvements. This self-reflection process allows the LLM to spot gaps and improve its output on a variety of tasks including producing code, writing text, and answering questions.


# 2.Tool use

And we can go beyond self-reflection by giving the LLM tools that help evaluate its output; for example, running its code through a few unit tests to check whether it generates correct results on test cases or searching the web to double-check text output. Then it can reflect on any errors it found and come up with ideas for improvement.

- Analysis
    - code execution
    - wolframe alpha
    - bearly code interpreter
- Research
    - web browse
    - search
    - wiki
- Productivity
    - email
    - calendar
    - cloud storage
- Image
    - image generation
    - image captioning
    - object detection

# 3. Planning

# 4. Multi-agent collaboration

Further, we can implement Reflection using a multi-agent framework. I've found it convenient to create two different agents, one prompted to generate good outputs and the other prompted to give constructive criticism of the first agent's output. The resulting discussion between the two agents leads to improved responses.


*Reference*:
1. [What's next for AI agentic workflows ft. Andrew Ng of AI Fund](https://youtu.be/sal78ACtGTc?feature=shared&t=111)(3/26/24)
1. https://www.deeplearning.ai/the-batch/issue-242/
1. https://x.com/AndrewYNg/status/1773393357022298617?s=20


- Self-Refine: Iterative Refinement with Self-Feedback, by Madaan et al. (2023)
- Reflexion: Language Agents with Verbal Reinforcement Learning, by Shinn et al. (2023)
- CRITIC: Large Language Models Can Self-Correct with Tool-Interactive Critiquing, by Gou et al. (2024)
