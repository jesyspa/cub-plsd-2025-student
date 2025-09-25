## Exercise 1 (2 pts)
> What major changes have there been in software development in the last 3-5
> years, and how do they impact the work of a software engineer?

Over the past five years, automatic development tools based on NLP models have emerged that have learned to translate text queries into executable code based on code functionality. The use of LM in tasks changes the program development pipeline: if previously a developer had to be able to translate a declarative statement brought to them by a manager or customer into imperative executable code, now more and more often a developer must be able to reformulate the declarative statement of the task, clarifying details that are obvious to the customer but not to LM. 

Despite their limited skills, knowledge in areas such as frontend and web development, as well as backend development, has become less valuable: LMs have learned to perform junior-level tasks, which has affected the labor market and the skills required. The paradigm of information search has also changed: if earlier, when a bug occurred, you had to go to specialized websites in search of a similar problem or read the documentation, now you can turn to an LM-based chatbot (for example, Grok) with your problem and get a specific solution to your problem many times faster, which speeds up development in an area that is new to the programmer.
## Exercise 2 (2 pts)
> What further changes do you expect to see in the coming 3-5 years?

I expect most software development to transition to declarative languages (either natural language or some other language acceptable to LLM), the number of developers will decrease significantly, and the efficiency of each will increase greatly. AI agents based on language models will replace most of the developers supporting the infrastructure. New systems will be developed by senior SWEs with significant involvement of AI agents and assistants in their work. There will be a small number of R&D teams developing agents and their interaction tools, but otherwise the software development market will shrink significantly. It is possible (but unlikely within 3-5 years) that thanks to RL and self-improving algorithms, agents will develop a more efficient programming language for LM, which will replace the current human-friendly programming languages.


For the coming two questions, one of the three points is for coming up with an idea that is feasible within the constraints of a course.
## Exercise 3 (3 pts)
> What can be improved about programming languages and their tooling to
> better fit these changes?

Develop simpler-to-understand LLM programming languages for current architectures, but there is a problem with new or rare programming languages: there is little code for LLM to learn from, so a better solution would be to offer an AI agent framework in which the AI agent itself can develop a programming language that is convenient for it, while generating examples (it may be necessary to provide some tools for quickly developing a compiler or interpreter for new programming languages, so that the agent can quickly and without a large number of bugs change the language and see how convenient it is to use).

To summarize:
1. Develop and test a programming language that is easy for LLM to understand with the current SOTA architecture (which may cause difficulties for LLM to understand some language constructs) [but this is an approach with a large inductive bias].
2. Describe and launch a framework for self-training an AI agent that develops a programming language convenient for LLM.
3. Develop and provide tools so that the AI agent can easily change the programming language during training while quickly testing the new language in action.

## Exercise 4 (3 pts)
> How can we measure whether a language is a good fit for the modern
> development flow?

Since modern flow involves close collaboration with LM, one of the criteria for language model quality is how well the language model suits them. To do this, you can:
1. Compile a set of programming tasks in natural language and tests for them, then submit a description of the language to LM and ask it to write a solution for each task and check its correctness. There are several problems with this approach: it is difficult to calibrate the complexity of the tasks so that, on the one hand, they are not too simple, but on the other hand, they are not too complex either. Also, all such benchmarks have a bias in that programming languages similar to existing ones will perform better, since the models are trained on them, but this does not mean that if you train a model on a new programming language and an old one with the same amount of data, the result will be the same.

2. To fix the second problem, you can use a framework of self-improving AI agents that could learn the language in an RL setting. Then you can compare two agents that have already been trained in their respective languages, which would remove the bias of their pre-training in existing languages and show how difficult it is for LM to learn a given language.

3. It is also worth adding that the language should retain human-readable features or be translatable into a language that humans can understand, so that AI-generated code can always be debugged, which is especially important in critical infrastructure software (for example, in the military or at NASA, or in software that manages Google's data center infrastructure (to prevent shutdowns) or low-level software (such as the OS kernel)). This can be measured using human testing: create a set of programs with various types of bugs and then measure how quickly people can find these bugs in the programs (and whether they can).

## Exercise 5 (2 pts)
> Provide at least two sources supporting your answers.

1. [Evaluating AI-generated code for C++, Fortran, Go, Java, Julia, Matlab, Python, R, and Rust](https://arxiv.org/html/2405.13101v2)
2. [Mutation-based Consistency Testing for Evaluating the Code
Understanding Capability of LLMs](https://arxiv.org/pdf/2401.05940)
3. Example of LM as interpreter for pl: [AIOS Compiler: LLM as Interpreter for Natural Language Programming and Flow Programming of AI Agents](https://arxiv.org/pdf/2405.06907)
4. [Example of LM friendlly language](https://www.moonbitlang.com/blog/ai-coding)
## Exercise 6 (2 pts)
> Formulate your answers into a compelling narrative that effectively makes your
> point. 

Over the last five years, software development has been transformed by the arrival of large language models (LLMs) capable of turning natural language descriptions into executable code. This shift alters the very role of the software engineer. Traditionally, engineers were translators: they took a declarative statement of requirements from a manager or client and painstakingly expressed it in imperative code. Now, the engineer’s value often lies in refining and reformulating those requirements into prompts that a model can understand, resolving ambiguities invisible to the client but critical for correct execution.

As a result, the skills landscape has changed. Routine knowledge of front-end or back-end development has become less scarce, as LLMs can increasingly handle junior-level implementation tasks. The job market has felt this pressure: engineers who once built boilerplate components now compete with models that can generate them instantly. Even the way developers debug has shifted: instead of combing through documentation or trawling forums for similar issues, engineers can ask a chatbot such as Grok for targeted fixes, dramatically speeding up the learning curve in unfamiliar domains.

Looking forward, the next three to five years are likely to bring an even deeper change in the development pipeline. Much of programming may move to declarative modes—whether in natural language itself or in hybrid languages optimized for machine comprehension. AI agents will take over much of the infrastructure and maintenance work, shrinking the overall workforce but amplifying the productivity of those who remain. Senior engineers will focus on designing systems in close collaboration with AI assistants, while a smaller number of R&D teams push forward the capabilities of the agents themselves. It is even conceivable that reinforcement learning and self-improving AI could create new programming languages better suited for machines than the human-centric ones we use today, though this may take longer than five years.

To adapt to this landscape, programming languages and their tooling must evolve. One promising direction is to design languages with constructs that map cleanly onto the inductive biases of current LLM architectures. The risk here is that new languages lack the training data needed for models to use them effectively. A stronger approach may be to create frameworks that allow AI agents to iteratively design, test, and refine their own languages, supported by tooling that makes it easy to generate interpreters or compilers for these new syntaxes. In such a setup, the agent learns not just to code but to shape its coding environment. This would let the language co-evolve with the model that uses it.

But how do we measure whether a language is a good fit for this modern development flow? One approach is to benchmark LLMs directly: provide a set of natural-language tasks, define test cases, and see whether the model can solve them correctly in the target language. Yet this carries bias: models will naturally do better in languages resembling those seen in pretraining, regardless of intrinsic quality. To counter this, we could use reinforcement-learning agents trained from scratch on different languages, then compare how quickly and effectively each learns. Finally, human readability must remain part of the equation. Even if a language is machine-friendly, engineers must be able to debug AI-generated code in critical settings—whether in aerospace, defense, or datacenter infrastructure. This can be measured experimentally by giving humans buggy programs and tracking how quickly and accurately they can identify errors.

In sum, software engineering is in the middle of a paradigmatic shift: from writing code directly to orchestrating AI systems that write code with us. To thrive, we need languages and tools designed not just for humans, but for the collaboration between humans and machines. The best languages of the future will be those that both LLMs can learn efficiently and humans can still read, reason about, and trust.