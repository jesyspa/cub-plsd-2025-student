## PLSD: Brainstorming Homework

With the rise of AI, software development is undergoing a seismic shift. Agentic coding and intent-driven workflows are redefining what it means to be a developer. I believe, that in the next 3-5 years, we will witness the emergence of programming languages and tools that are not just instruments for code writing speedup, but intelligent collaborators. This pitch outlines the key transformations, evaluates current gaps, and proposes a vision for the future of programming and software development.

## The Evolution: AI, Cloud and Security

**During the last 3 years we have witnessed significant changes in software engineering. The most important trends, that, in my opinion, will continue to shape the field and form new approaches, are:**

-   **The rise of AI-powered IDEs and Agentic Coding.** In my view, this is the **main** shift in software developing/engineering process over the past 5 years. Tools like GitHub Copilot and Claude Code automate code generation, testing, and debugging. Overall code development process is now shifting from writing strictly structured code to declaring intent and experimenting. In 2025, Generative AI can already be used as a virtual team member, managing workflows and writing meaningful code, based on the developer's ideas formulated in natural language (while the code may not always be perfectly optimized, it is often highly functional). A clear example of this trend is the rapid rise of the IDE Cursor, which is now called 'the fastest growing startup ever' and has gained \$9.9B valuation **\[1\]\[2\]**.

-   **DevOps Maturity and the Spread of Cloud-Native Architectures.** Serverless, containerized systems dominate modern infrastructure Cloud platforms like AWS, Azure, Google Cloud and Vercel have made serverless computing, containerization and container orchestration technologies (e.g., Docker and Kubernetes) the industry standard. Continuous integration and continuous delivery (CI/CD) have shifted from being a "nice to have" to a baseline expectation for modern software pipelines.

-   **Security & Ethics.** Security-by-design and privacy-by-design, along with ethical AI coding assistants, are becoming mandatory requirements. The languages, which provide the memory safety and do not have some of the vulnerabilities by design, are growing in popularity (Rust, Go, Kotlin), while the languages, which do not satisfy these requirements, are being used more cautiously (C, C++). In fact, in 2023, CISA explicitly recommended moving away from 'unsafe' languages like C and C++ towards memory-safe languages such as Rust, Go, and Swift for building critical systems **\[3\]**. As AI-generated code introduces new vulnerabilities and cybersecurity threats become increasingly AI-driven, software developers and engineers are already starting to factor in ethical boundaries, data privacy, and adversarial testing (and almost surely this trend will only intensify). According to Netacea research (2024) **\[4\]**, 93% of their respondents believe they will face daily AI attacks in 2025.

## The Next Wave: 2025-2030

**Based on the trends, stated above, we may expect following changes in Software Development field in the next 5 years:**

-   **AI as the main developer.** Within the next 5 years, AI will become integrated even deeper into developer tools, driving the automation of coding, refactoring, and testing. The development process will follow a simple pattern:

    **Developer defines the goal → AI builds the solution.**

    With RL and advanced tuning techniques, AI assistants will gain a deeper understanding of complex codebases and generate higher-quality code in less time. This shift will lower the barrier to entry, allowing even non-developers to create software.

    AI-generated code will still have flaws and inefficiencies. Human expertise will remain essential for reviewing, refining, and scaling solutions. The future software development cycle will likely evolve into **three key phases:**

    -   **Concept & Specification** - The developer collaborates with AI in a low-code or no-code environment to brainstorm, define requirements, set rules and constraints, and design system architecture through a visual interface. This phase is quite similar to spec-driven development **\[5\]**.

    -   **Automated Prototyping** - The AI assistant generates a functional prototype along with documentation.

    -   **Human-Led Optimization** - The developer reviews problematic code, fixes errors, and scales the solution, potentially with further AI assistance.

    This shift will help the developers to focus more on their strategy and ideas instead of the programming language formalism, at least at the start of the development cycle.

-   **Higher Interpretability of the AI-generated code.** Over the next 5 years, as context windows will continue to grow and the reasoning modes of LLMs will improve, AI coding assistants will become able not just to simply write code, but to explain the meaning behind it, making them more valuable to developers by improving transparency.

-   **Cloud Integration and Multi-Cloud Solutions.** Further advances in edge computing, cloud platforms and micro-service architectures will create new paradigms for performance and scalability. In my opinion, the main shift in this area will be the dramatic rise of multi-cloud solutions, often combined with edge computing. This trend will be driven by the increasing popularity of the Kubernetes and the growing risks of relying on a single cloud provider.

-   **Privacy and Ethics-First Development.** In the coming years, compliance will be deeply integrated into every layer and stage of the software development process. For AI-powered development, a new layer of security must also be considered: the risk of unintended code leakage to third-party LLM assistants.

## The language and tools of the future:

**As a future of programming, we can imagine a new kind of programming language where developers simply express what they want to achieve, and AI agents determine how to build it. This programming language should be:**

-   **Human-readable and intent-driven:** It should focus on expressing goals and intentions, rather than low-level syntax. Ideally, it should be very close to natural language.

-   **AI-native:** Designed to support agentic workflows.

-   **Quasi-deterministic:** While it is very difficult to make LLM
    responses fully deterministic, this language should aim to minimize stochastic behavior to ensure predictability and stability in generated code.

-   **Three stages of the future development cycle (stated above) should be presented:**
    
    **Specification → Automated Prototyping → Human-Led Optimization**

\
**The example of the proposed code at the stage of planning:**

`Goal: Build a gym training booking website`
\
`UX: Mobile-first, voice input, filter by sport/day/coach/level`
\
`Data: Google Calendar API, Firebase Auth, MongoDB`
\
`AI_Assistants: UXAgent, CodeAgent, TestAgent`
\
`Constraints: GDPR, < 200ms response, no tracking cookies`
\
`Deploy: Vercel`

\
While the idea of such a language is strategic and forward-looking, several **near-term** programming enhancements to programming languages may be proposed to reduce the gap between today's tools and the future vision of software development:

-   **Code-level Agentic Coding:** a special feature of the language, e.g., `@agent` decorator placed before the function signature, - could autocomplete the function for the developer before the code interpreter executes.

-   **Code-level Agentic Documentation:** another special feature of the language, e.g., `@explain` decorator, - could analyze the existing code and generate the docstring for the developer.

-   **Privacy:** a special decorator, e.g., `@erase`, - could restrict the LLM coding assistant from reading certain code blocks.

## 4. Evaluating if a language is a good fit for modern development

**To make sure that programming languages of the future support the new software development paradigms and that they are still suitable for regular code writing, I consider the following set of key metrics:**

| **Metric**                | **Why It Matters**                                                                 | **Indicators**                                                                                          | **How to Measure It**                                                                                                      |
|---------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| **Human Readability**      | Improves collaboration and maintainability                                         | Concise syntax, meaningful naming conventions, intuitive structure                                      | Human experts’ majority vote                                                                                               |
| **AI Readability**         | Ensures AI assistants understand the language and generate code aligned with users’ goals and intentions | Accurate compliance with users’ goals and requirements, no unnecessary or extra code is generated       | The CodeBLEU metric                                                                                                    |
| **Performance**            | Efficiently handles compute-heavy tasks                                           | Compilation speed, runtime efficiency, memory usage                                                     | Straightforward benchmarking of relevant performance metrics                                                               |
| **Speedup when using AI tools** | AI-powered development should be faster and more efficient than manual coding     | It is faster to complete the task using the AI-powered language compared to a certain standard PL (e.g., Python) | Relative time speedup (%) compared to manual coding in a standard PL (averaged over $N$ benchmark tasks and $M$ people)   |
| **Security**               | Prevents vulnerabilities by design                                                | Type safety, memory safety, built-in error handling, privacy compliance                                 | The metric is applied to the resulting (low-level) code and combines several other sub-metrics, e.g., Cyclomatic Complexity (when code is less complex, it probably contains less risks), Vulnerability Density (number of issues found using software analysis tools per 100 lines of code) |
| **Tooling Ecosystem**      | A language is only as strong as its ecosystem                                      | Rich libraries, active community, cloud platform support, integration with CI/CD and AI tools           | Human experts’ majority vote                                                                                               |



## Final Thought

The future of software will be less about manually writing code and more about expressing intent, orchestrating intelligent AI assistants, and building adaptive systems. I believe that software engineering will evolve from creating static code to a highly dynamic, continuous process. Tooling will empower developers to lead hybrid teams of humans and AI agents, allowing them to focus more on strategy and architecture rather than the code itself.

**References:**

**\[1\]** [Bloomberg (2025). Anysphere, Hailed as Fastest Growing Startup Ever, Raises \$900 Million](https://www.bloomberg.com/news/articles/2025-06-05/anysphere-hailed-as-fastest-growing-startup-ever-raises-900-million)

**\[2\]** [TechCrunch (2025). Cursor\'s Anysphere nabs \$9.9B valuation, soars past \$500M ARR](https://techcrunch.com/2025/06/05/cursors-anysphere-nabs-9-9b-valuation-soars-past-500m-arr/)

**\[3\]** [CISA (2023). The Urgent Need for Memory Safety in Software Products](https://www.cisa.gov/news-events/news/urgent-need-memory-safety-software-products)

**\[4\]** [Netacea (2024). Cyber Security in the Age of Offensive AI](https://netacea.com/reports/cyber-security-in-the-age-of-offensive-ai/)

**\[5\]** [The GitHub Blog (2025). Spec-driven development with AI: Get started with a new open source toolkit](https://github.blog/ai-and-ml/generative-ai/spec-driven-development-with-ai-get-started-with-a-new-open-source-toolkit/)
