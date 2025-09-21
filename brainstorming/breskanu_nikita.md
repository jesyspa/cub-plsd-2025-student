# Homework 1 — Breskanu Nikita  

---  

### 1: What major changes have there been in software development in the last 3–5 years, and how do they impact the work of a software engineer?  

The largest change is the appearance of **Large Language Models (LLMs)** and their growing usage for coding. Specifically, LLMs are used when they:  

- Generate code from a natural language requirement  
- Suggest autocompletion of code in Integrated Development Environments (IDEs)  
- Provide natural language descriptions of code and answer questions to help users understand it better  

At a high level, the change can be summarized as:  

- Shift from code writing to code reviewing  
- Increased productivity for routine tasks (handled by LLMs)  
- Easier exploration and learning with LLMs, resulting in a lower entry level for many jobs and higher competition among junior developers  

---  

### 2: What further changes do you expect to see in the coming 3–5 years?  

Currently, the biggest issues with AI-written code are the frequent absence of logic and the lack of handling corner cases. These issues make it hard to fully integrate LLMs into the software development workflow.  

I expect the AI community to combat these issues, specifically through **increased code validation**. LLMs will likely be used in conjunction with brute-force search (or perhaps AI-driven search) together with extensive validation.  

We might also see the emergence of **intermediate-level languages**, which strike a balance between ambiguous natural language and deterministic, verbose programming languages.  

---  

### 3: What can be improved about programming languages and their tooling to better fit these changes?  

- **Strict validation**: For a language to be AI-friendly, it needs to make writing “bad” code very difficult. The compiler should catch as many issues as possible, with a continuous cycle between LLM generation and compiler correction.  
- **Intermediate LLM-optimized language**: A language that is designed to be well-understood by LLMs and can almost always be deterministically compiled into a main programming language with the help of LLMs. This would require creating a very complex and sophisticated compiler.  
- **Handling edge cases**: Infrastructure-ready code must account for rare but possible scenarios that are easily overlooked. In the future, I believe there will be systems capable of performing brute-force searches (likely aided by LLMs) to detect edge cases. Such systems would help correct mistakes made by both AI-generated and human-written code, greatly improving productivity and application security.  

---  

### 4: How can we measure whether a language is a good fit for the modern development flow?  

There is a trade-off between **ease of writing** and **determinism**. A good language should strike a “golden middle”: it must be relatively easy to understand (both for humans and LLMs), while remaining as deterministic as possible.  

- **Measuring ease of understanding**: This can be estimated using perplexity (the probability of the text according to a language model) computed by an LLM trained only on natural text, comparing the same program written in multiple languages.  
- **Measuring determinism**: While most major languages today are fully deterministic, in cases of non-deterministic programming (e.g., involving natural language instructions), the probability of correct compilation can be empirically estimated using an LLM with non-zero temperature. Existing metrics such as **pass@k** (the probability of at least one of *k* generated code samples passing unit tests) can also be adapted for compilation success rates.  

---  

### 5: Provide at least two sources supporting your answers  

**Chen, Mark, et al.** *“Evaluating Large Language Models Trained on Code.”* arXiv preprint arXiv:2107.03374 (2021).  

This paper rigorously studies code generation by LLMs. The authors find that the “absence of logic” is still present, despite good scores. The primary evaluation metric used is **pass@k**. The paper also highlights the importance of test-driven development, supporting my argument for extensive validation.  

**Fei, Haoxiang, et al.** *“MoonBit: Explore the Design of an AI-Friendly Programming Language.”* Proceedings of the 1st International Workshop on Large Language Models for Code. 2024.  

This paper introduces the new AI-friendly language **MoonBit**, created for more efficient AI code generation. It demonstrates that “intermediate” languages are indeed being developed today.  


### 6: Formulate your answers into a compelling narrative that effectively makes your point. 

In the past few years, software engineering has been transformed by the rise of Large Language Models (LLMs), shifting the role of developers from primarily writing code to reviewing, validating, and refining it. While this change has boosted productivity for routine tasks and lowered the entry barrier for new programmers, it has also introduced challenges, such as logical inconsistencies and overlooked edge cases in AI-generated code. Looking ahead, I expect that improvements in validation and the integration of AI-driven search techniques will make LLMs far more reliable partners in software development. This evolution may also lead to the creation of intermediate, AI-friendly programming languages that act as a bridge between human communication and machine precision. To support this future, programming languages and tooling must emphasize strict validation, edge-case detection, and better compiler integration to ensure correctness. Ultimately, the languages best suited for modern development will strike a balance between ease of understanding and determinism, creating a workflow where both humans and AI collaborate effectively.