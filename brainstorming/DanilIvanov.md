#### Disclaimer
I wrote this as little bit of an essay, due to last exercise asking us to create a narrative, so necessarily, I repeat myself multiple times, I add some embellishments, figures of speech, etc. I hope it's not a big issue, I simply enjoy writing, although it carries me away sometimes. I tried to highlight the ponts, relevant for the exercies, however, so it should be clearer than I usually write

#### Essay

The software development landscape is undergoing a fundamental identity shift in the recent years. Without a doubt, the emergence and development of AI can and shall change the way the developers write code in the days to come. The arrival of powerful, ubiquitous AI like ChatGPT has moved artificial intelligence from a distant promise to a daily partner in the coding trenches. Instead of crawling through Stack Overflow, papers, articles, or simply writing Google queries, developers can open any powerful enough LLM, generate a function, debug a cryptic error, or draft a project plan, all in span of seconds, instead of days. This new partnership is accelerating everything around the core act of creation — research, boilerplate generation, and documentation. But as any seasoned engineer knows, a powerful new partner requires a new way of working. This essay argues that to truly harness this shift, we must look beyond the tools themselves and reimagine the very foundation of our craft: our programming languages. We need languages and ecosystems designed not just for human intuition, but for human-AI collaboration, and we need a concrete way to measure their effectiveness in this new paradigm.

#### Exercise 1 (2 pts): What major changes have there been in software development in the last 3-5 years, and how do they impact the work of a software engineer?

The most prominent change in software development over the past couple of years is undoubtedly the transition from AI as a theoretical concept to a practical, ubiquitous co-pilot. I started my career about 2.5 years ago, and initially, tools like ChatGPT were novelties, a fun little you, and nothing more. However, their rapid evolution has fundamentally altered the software development lifecycle. The impact is less about automating the act of writing code and more about accelerating the surrounding processes, in my opinion: generating templates, creating baselines, writing documentation, and, most significantly, democratizing access to information.

  

I’ve been working mostly as an ML developer and a little bit as a teacher. I must admit, I still have the initial skepticisim towards AI, due to how raw and unpolished it was it the time, but I’ve seen various teammates using it somewhat successfully. For analysts and product managers, this has been of great help, enabling rapid hypothesis generation and data exploration that bypasses traditional search engine limitations. In educational contexts, it has become an inescapable research assistant, for better or worse. However, for complex, creative engineering tasks—like architecting a novel ML system—the current generation of AI still falls short. It lacks fundamental comprehension, often leading to a situation where the time saved in initial code generation is lost to meticulous debugging and validation.

  

Therefore, the major change is a paradigm shift: the software engineer's role is evolving from a pure coder to a synthesiser and auditor of AI-generated output. Our core value is shifting towards asking the right questions, critically evaluating answers, and integrating components into a coherent, reliable whole, which is still a rather large and complex task, perhaps even more difficult than writing code.

  

#### Exercise 2 (2 pts): What further changes do you expect to see in the coming 3-5 years?

  

In any case, despite my attitude, I believe the next 3-5 years will bring substantial, albeit evolutionary, shifts. The change will be less about replacement and more about profound integration. The most significant development will be the move from generic copilots to context-aware, customized AI agents deeply embedded into the developer ecosystem.

  

The proof against full replacement lies in the current inability of LLMs to grasp true product intent, navigate complex business logic, or make architecturally significant trade-off decisions requiring human intuition, simply because it’s different for any company and for any project, there is no universal tool, and there will never be. However, the counterpoint is the rapid advancement in agentic AI — systems that can chain together tasks, use tools, and perform limited autonomous problem-solving within a well-defined scope.

  

Perhaps, the key enabler will be customization through RAG, or something similar, and fine-tuning on private codebases, documentation, and team knowledge. This will transform clunky internal tools into seamless quality-of-life accelerators, automating everything from writing project-specific boilerplate to generating accurate documentation and onboarding new hires. Consequently, the software engineer's role will increasingly focus on high-level design, prompt-driven direction of these AI agents, and complex integration, fundamentally elevating the work rather than merely speeding it up. Although, from I’ve seen in my professional experience at certain non-mentionable bigtech companies, there is still a long way ahead until we reach that point, but at least it is something tangible, unlike dreams of a real AI that will take our work and life.

  

#### Exercise 3 (3 pts): What can be improved about programming languages and their tooling to better fit these changes?

  

I must say, I’m not an expert in programming languages, by any means. I do believe that any language can be suited for any task, and it’s ultimately a matter of preference and materials availability.

  

I suppose that, in order to better fit the paradigm of AI-assisted development, programming languages and their ecosystems might need to evolve as well. The core improvement needed is a shift towards explicit richness over implicit cleverness. This means languages should facilitate AI tools in understanding not just the what (the code itself) but the why (the intent and context).

  

First, we need stronger, more formalized mechanisms for documenting intent. This goes beyond comments. Languages could natively support annotations for preconditions, postconditions, invariants, etc. This gives an AI assistant a much richer context to generate and verify code against. It is a small thing to add, but every bit helps, especially for dynamic languages, duck-typing and whatnot.

  

Second, tooling must become deeply integrated and context-aware. The IDE of the future shouldn't just offer completions; it should act as an AI proxy that understands the entire project. Imagine a tool that can answer a prompt like, "Find me all functions that interact with the payment API and show me where they're called, then refactor them to use the new authentication model." This requires tooling to move from syntax-aware to semantics-aware, perhaps making it closer to a meta-language.

  

Finally, languages themselves could become more declarative and probabilistic. Instead of meticulously writing how to do something step-by-step, we might declare what we want and let the AI tooling figure out the optimal implementation. For instance, stating "ensure this data is sorted before processing" and allowing the tool to choose and implement the best sorting algorithm based on the inferred data size and type, instead of memorizing all the algorithms in the world, and still failing to pick the right one. This would fundamentally change the developer's role from a coder to a specifier and validator, and the language must be designed to support that.

  

#### Exercise 4 (3 pts): How can we measure whether a language is a good fit for the modern development flow?

  

As someone who has experience working in the industry, I’d like to come up with something measurable, in numbers, preferably something that we can AB-test, but know no metric of the sorts, so I will have to make one up.

  

I would say that measuring a language's fitness for the modern, AI-augmented flow requires moving beyond traditional metrics like raw performance. It is important, of course, and it needs to be accounted for, but then we would end up with C++ or Rust. They are good, surely, but not without limitations. Instead, we should develop a cross-language benchmark that would be tested through controlled experiments (A/B tests) where developers of varying skill levels complete a standardized set of tasks using different languages, each equipped with a powerful AI assistant, for example, pretty much like CSAT or DSAT.

  

This benchmark would measure three core dimensions:

  

1.  Productivity Acceleration: This measures the reduction in "time-to-correct-solution" when using an AI assistant versus coding alone. We can count concrete metrics: the number of AI prompts required, the percentage of AI-generated code that compiles and passes tests on the first try, and the time saved on boilerplate, debugging, and research. A high-fit language requires fewer, more effective interactions and, of course less time overall.
    

  

2.  Learning Curve Attenuation: How quickly can a developer new to the language (but not to programming) become productive with AI assistance? We can measure the time it takes for them to complete tasks or the number of errors stemming from language-specific quirks that the AI fails to capture. A good modern language makes its hidden facts discoverable by the AI, and makes itself easy to learn for complete beginners.
    

  

3.  Robustness to Change: This is more of a specific metric. If we were to evaluate a language for QA tasks, for instance. Modern development requires constant iteration. We can measure how effectively an AI assistant can perform common refactoring tasks (e.g., "rename this method across the entire codebase and update all call sites") or implement a new feature request based on a natural language description. The metric is the success rate and the number of bugs introduced during the change. A language with good tooling and clear syntax enables more reliable AI-driven refactoring. The same can be expanded for other areas, such as frontend, backend, analytics, and so on. The task is largely the same - code generation, but the metrics will obviously differ.
    

  

In short, a language is a good fit not just if it's powerful, but if it amplifies human (and AI) potential by being predictable, explicit, and easy for both a human and a machine to reason about. We measure this by testing the efficiency of the human-AI partnership it enables.

  

#### Exercise 5 (2 pts): Provide at least two sources supporting your answers.

  

As for materials that support the answers, I believe, there are two key points: the paradigm shift in favor of AI, and programming languages evaluation, I’ll try to look for both.

  
There are several articles that support the notion of AI revolution. First is [Sushant Gaurav's The Impact of LLMs on AI, ML, and Industries (Medium, 2024)](https://sushantgaurav57.medium.com/the-impact-of-llms-on-ai-ml-and-industries-0f978b3d48f5). It describes how LLMs like ChatGPT have shifted software development from manual coding to AI-assisted workflows, emphasizing their role in automating documentation, debugging, and code generation. It aligns with the argument that AI tools have accelerated ancillary processes like boilerplate generation and research, though they struggle with complex, creative tasks.

  

**NB.** I bear no love for Medium articles, but it does cover the point I want to make, so I might as well include it. After all, the essay I write is not that dissimilar of an average Medium article.

  

As for programming languages evaluation there is also an article from another notorious source - [GeeksforGeeks' Language Evaluation Criteria (2023)](https://www.geeksforgeeks.org/software-engineering/language-evaluation-criteria) . This outlines criteria like readability, writability, and reliability, which directly inform the need for languages to support explicit intent documentation (e.g., annotations for preconditions) and better tooling integration. It validates the argument that languages must evolve to be more "AI-friendly”. Of course, it does not propose any meaningful way to measure said criteria, or even describe the tasks required to measure them, but that’s where my essay comes for help. In any case, things like readability can be measured via UX-experiments, reliability is a similar thing to what has been proposed above, so it can serve as proof of concept, vague as it is.

  

To summarize the narrative, the trajectory is clear. AI will not replace software engineers, at least I would love to think so, but engineers who effectively leverage AI will undoubtedly replace those who do not. The transition we are witnessing is from being pure coders to becoming architects and orchestrators of intelligence. This future demands programming languages that prioritize explicit intent over implicit cleverness, and tooling that provides deep, semantic awareness of a project's context. It demands a new benchmark to cut through the hype and objectively measure what truly makes a language fit for this modern flow. The goal is no longer just to write code that a machine can execute, but to design systems and articulate specifications that both an AI and a human can understand and evolve collaboratively. The languages and tools that embrace this collaborative, augmented future will not only define the next era of development but will ultimately empower us to tackle challenges of complexity and creativity that remain beyond our reach today.