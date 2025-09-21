## Exercise 1 (2 pts)
> What major changes have there been in software development in the last 3-5
> years, and how do they impact the work of a software engineer?

За 5 лет появились средства автоматической разработки на основе NLP моделей, которые научились переводить текстовые запросы по функционалу кода в сам исполняемый код. Использование LM в задачах меняет пайплайн разработки программы: если раньше разработчик должен был уметь из декларативной постановки, которую ему принес менеджер или заказчик перевести в императивно исполняемые код, то теперь все чаще разработчик должен уметь именно хорошо переформулировать декларативную постановку задачи, уточняя детали, которые для заказчика очевидны, но для LM нет. 

Несмотря на ограниченность их умений, знания в таких областях как frontend and web development а также backend development стали менее ценными: LM научились выполнять junior level задачи, что повлияло на рынок труда и требуемые скиллы. Также изменилась парадигма поиска информации: если раньше при возникновении бага приходилось идти на профильные сайты в поисках похожей проблемы или читать документацию, то теперь обратиться с проблемой можно к чат боту на базе LM (к примеру Grok) и получить точечное решение вашей проблемы в разы быстрее, что это ускоряет разработку в новой для програмииста области.
## Exercise 2 (2 pts)
> What further changes do you expect to see in the coming 3-5 years?

Я ожидаю переход большей части software разработки на декларативные языки (либо natural language или какой-то другой язык приемлемый для LLM), разработчиков станет сильно меньше и эффективность каждого сильно вырастет. AI агенты на базе языковых моделей заменят бОльшую часть разработчиков поддерживающих инфраструктуру. А новые системы будут делать senior SWE с большим участием AI агентов и ассистентов в их работе. Будет небольшое число R&D команд развивающих агентов и их средства взаимодействия, в остальном рынок именно Software разработки достаточно сильно схлопнется. Возможно (но маловероятно, что в течение 3-5 лет) благодаря RL и самоулучшающимся алгоритмам агентами будет разработан более эффективный для LM ЯП, который заменит текущие человеко-удобные ЯП.


For the coming two questions, one of the three points is for coming up with an idea that is feasible within the constraints of a course.
## Exercise 3 (3 pts)
> What can be improved about programming languages and their tooling to
> better fit these changes?

Разработать более простые для понимания для текущих архитектур LLM ЯП, но тут есть проблема с новыми или редкими ЯП: для них мало кода на котором LLM может учиться, поэтому более хорошим решением будет предложить AI agent фреймворк при котором AI агент сам сможет разработать удобный для себя ЯП попутно генерируя примеры (возможно нужно предоставить некоторые тулы для быстрой разработчки компилятора или интерпретатора для новых ЯП, чтобы агент мог быстро и без большого числа багов менять язык и смотреть насколько он удобен в использовании).

Подытожу:
1. Разработать и протестировать ЯП удобный для понимания LLM с текущей SOTA архитектурой (которая может вызвать сложности для понимания LLMкой некоторых конструкций языка) [но это подход с больим inductive bias]
2. Описать и запустить фреймворк для самообучения AI агента разрабатывающего удобный для LLM ЯП
3. Разработать и предоставить тулзы, чтобы AI агент в течение обучения могу легко менять ЯП при этом быстро проверяя новый язык в действии.

## Exercise 4 (3 pts)
> How can we measure whether a language is a good fit for the modern
> development flow?

Так как modern flow подразумевает тесную работу с LM, то одним из критериев качества ЯП является то, насколько хорошо ЯП подходит для них. Для этого можно:
1. Можно составить набор программистских задач на natural language и тестов к ним, далее подать в LM описание языка и попросить написать решение для каждой из задач и проверить его корректность. С данным подходом есть несколько проблем: сложно откалибровать сложность задач, чтобы с одной стороны они не были слишком простыми, но и слишком сложные тоже нельзя, также у всех подобных бенчмарков есть bias в то, что ЯП похожие на уже существующие будут получать скоры лучше, так как модели на них обучены, но это не означает, что если на одинаковом размере данных учить модель на новом ЯП и старом результат будет тот же.

2. Чтобы исправить 2ую проблему можно использовать фреймворк самосовершенствующихся AI агентов, которые бы могли обучаться данному языку в RL постановке. Тогда можно сравнить 2х агентов уже обучившихся каждый под свой язык, что убрало бы bias их претреина на существующих языках и показало то, насколько сложно LM обучиться под данный язык.

3. Также наверное стоит добавить, что язык должен сохранять human readable черты или быть транслируемым в язык понимаемым человеком, чтобы всегда можно было отдебажить AI generated код, что в особенности важно в критических инфраструктурных ПО (к примеру у военных или в NASA или в ПО управляющем инфраструктурой ДЦ Google (чтобы не было шатдаунов) или низкоуровневом ПО (по типу ядра ОС)). Это можно замерить с помощью тестов на людях: создать набор программ с различного сорта багами и потом замерить насколько быстро люди могут находить данные баги в программах (и могут ли)

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