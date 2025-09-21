## Exercise 1 (2 pts): What major changes have there been in software development in the last 3–5 years, and how do they impact the work of a software engineer?  
In the last five years programming became mainstream, and in the last three years the paradigm shifted to massive use of LLMs. For most common tasks they can now generate working code, maybe not on the first try, but usable. Benchmarks also changed: in 2024 HumanEval with short abstract tasks was enough, but now the standard is SWE-bench and CommitZero, working at repository and application level. In 2025 GPT-5 even took first place in ICPC. For engineers this means less manual coding and more focus on design, validation, and integration of AI outputs.  

## Exercise 2 (2 pts): What further changes do you expect to see in the coming 3–5 years?  
I expect programmers to become operators of LLMs, just like workers once moved from manual labor to operating machines. Developers will plan architecture, set requirements, test generated solutions, report bugs for rework, and present results, while the LLM will handle the bulk of implementation.  

## Exercise 3 (3 pts): What can be improved about programming languages and their tooling to better fit these changes?  
We can look at large datasets of code, check where LLMs fail, and adapt. For example, take popular tasks and analyze at which tokens the model makes mistakes. If the problem comes from ambiguous syntax, adapt the rules of the language. If not, then at least create clearer standards for formulating tasks so models understand them better.  

## Exercise 4 (3 pts): How can we measure whether a language is a good fit for the modern development flow?  
The main measure is development time, including compilation and debugging. In the context of LLMs it is also how easily they can generate correct and efficient code in this language, which shows how well the language supports the new workflow.  

## Exercise 5 (2 pts): Sources  

- OpenAI. *GPT-5 Codex System Card* (2025). [PDF](https://cdn.openai.com/pdf/97cc5669-7a25-4e63-b15f-5fd5bdc4d149/gpt-5-codex-system-card.pdf)  
- Wikipedia. *List of programming languages for artificial intelligence.* [Link](https://en.wikipedia.org/wiki/List_of_programming_languages_for_artificial_intelligence)  
- OpenAI. *ICPC 2025 Competition Results Repository.* [GitHub](https://github.com/openai/openai-icpc-2025)

## Exercise 6 (2 pts): Narrative / Pitch  
Software development has changed: LLMs moved from solving small exercises to competing with the best in algorithmic contests and fixing real repository issues. The role of engineers is shifting too. In the future, developers will not type every function by hand but operate LLMs, guiding them with requirements, architecture, and tests. To support this shift, languages and tools must adapt: they should reduce ambiguity, make code easier for models to generate, and provide strong testing and validation. The success of such a language will be assessed based on how well an LLM can complete tasks in it, and how effectively the resulting solutions are.