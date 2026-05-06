# Большая Подборка Open Source AI Agent Репозиториев и Стеков для Русскоязычной Аудитории

Этот файл собран не как "все подряд", а как curated-карта рынка.

Задача подборки:
- быстро сориентировать русскоязычную аудиторию в сильных open-source решениях;
- показать не только framework-ы, но и реальные полезные репозитории;
- отдельно закрыть темы `agents`, `skills`, `MCP`, `browser automation`, `memory`, `evals`, `voice`;
- сохранить прагматичный фокус на self-hosted и production-friendly инструментах.

Все ключевые ссылки в этой версии ведут на официальные репозитории и официальную документацию.

---

## Быстрая Навигация

- `20 репозиториев, которые стоит знать` - если нужно быстро получить базовую карту рынка;
- `Готовые подборки по сценариям` - если хотите сразу выбрать стек под задачу;
- `Агентные framework-ы` - если сравниваете инженерные основы;
- `Coding agents` - если нужен practical layer для кода и IDE;
- `Skills, MCP, AGENTS.md` - если важны repo-local правила, tools и расширяемость;
- `Browser agents`, `memory`, `evals`, `voice` - если собираете более серьезный agent stack;
- `Инфраструктура и стек по умолчанию` - если нужен прагматичный путь до self-hosted продукта.

---

## Кому Полезен Этот Файл

- разработчикам, которые хотят быстро понять, что реально стоит изучать в AI-agent экосистеме;
- командам, которые выбирают стек для первого AI-продукта;
- фаундерам и продактам, которым нужен понятный landscape без лишнего шума;
- тем, кто делает Telegram-ботов, internal tools, AI-workspaces, coding agents или голосовых агентов;
- авторам, преподавателям и комьюнити-лидам, которым нужен один сильный публичный материал для аудитории.

---

## Как Читать Эту Подборку

Не идите сверху вниз как по энциклопедии.

1. Сначала выберите задачу.
2. Потом возьмите 3-5 репозиториев из нужного блока.
3. И только потом решайте, какой стек брать в работу.

Если вы:
- делаете Python-агента: смотрите `LangGraph`, `PydanticAI`, `LlamaIndex`, `Mem0`, `Langfuse`;
- делаете визуальную AI-платформу: смотрите `Dify`, `Langflow`, `Flowise`, `AnythingLLM`;
- делаете coding agent: смотрите `OpenHands`, `Aider`, `Cline`, `Continue`;
- делаете browser agent: смотрите `browser-use`, `Skyvern`, `Playwright`;
- делаете voice agent: смотрите `Pipecat`, `LiveKit Agents`;
- строите tool ecosystem и skills: смотрите `modelcontextprotocol/servers`, `awesome-mcp-servers`, а также раздел про `AGENTS.md` и `skills/`.

---

## Быстрый Ответ: 20 Репозиториев, Которые Правда Стоит Знать

Если времени мало, начните отсюда.

### Базовые agent framework-ы

**LangGraph**  
https://github.com/langchain-ai/langgraph  
Когда брать:
- если нужен stateful orchestration;
- если важны long-running workflows, память, durable execution, human-in-the-loop;
- если вы строите production-агента, а не просто демо.

**PydanticAI**  
https://github.com/pydantic/pydantic-ai  
Когда брать:
- если нужен Python-first agent framework с сильной типизацией и валидацией;
- если нравится "ощущение FastAPI", но для agent development;
- если вам нужна аккуратная разработка и структурированный output.

**Semantic Kernel / Microsoft Agent Framework**  
https://github.com/microsoft/semantic-kernel  
Когда брать:
- если вы строите enterprise-grade multi-agent систему;
- если нужна сильная Microsoft-экосистема и межъязыковой стек.  
Важно:
- на `2026-05-06` README репозитория прямо указывает, что Semantic Kernel уже идет как Microsoft Agent Framework и позиционируется как production-ready successor.

**LlamaIndex**  
https://github.com/run-llama/llama_index  
Когда брать:
- если ваша главная задача это документы, индексация, retrieval и RAG;
- если вам не нужен тяжелый multi-agent слой на старте.

**Agno**  
https://github.com/agno-agi/agno  
Когда брать:
- если вы хотите не просто собрать агента, а запускать его как production software;
- если важны runtime, sessions, tracing, scheduling, RBAC и единый control plane.

**AutoGen**  
https://github.com/microsoft/autogen  
Когда брать:
- если вы исследуете multi-agent patterns и старые AutoGen-подходы;
- если нужно понять исторически важный стек.  
Важно:
- на `2026-05-06` README помечает AutoGen как `maintenance mode` и советует новым пользователям смотреть в сторону Microsoft Agent Framework.

### Визуальные платформы и self-hosted AI workspaces

**Dify**  
https://github.com/langgenius/dify  
Когда брать:
- если нужен production-ready open-source LLM app platform;
- если хотите быстро собрать workflow, RAG, agents, model management и observability в одном продукте;
- если нужен self-hosted путь от MVP к боевому использованию.

**Langflow**  
https://github.com/langflow-ai/langflow  
Когда брать:
- если нужен visual builder, но без потери гибкости;
- если важны API и MCP export из workflow;
- если хочется быстро собирать и публиковать flows как инструменты.

**Flowise**  
https://github.com/FlowiseAI/Flowise  
Когда брать:
- если нужен визуальный конструктор агентов и LLM-пайплайнов на Node-стеке;
- если хотите быстрый self-hosted старт через `docker compose`.

**AnythingLLM**  
https://github.com/Mintplex-Labs/anything-llm  
Когда брать:
- если нужен приватный AI workspace для команды;
- если нужен "chat with docs + agents + multi-user" без тяжелой настройки;
- если нужен понятный продукт для внутреннего использования, а не только dev framework.

### Coding agents

**OpenHands**  
https://github.com/OpenHands/OpenHands  
Когда брать:
- если нужен большой open-source coding-agent проект с SDK, CLI, GUI и облачным сценарием;
- если хотите изучать архитектуру agentic development систем;
- если интересны `skills/`, `.agents/skills` и repo-local agent patterns.

**Aider**  
https://github.com/Aider-AI/aider  
Когда брать:
- если нужен практичный terminal coding assistant;
- если вы хотите pair programming в текущем git-репозитории;
- если нужен простой и быстрый путь в coding-agent workflow без отдельной платформы.

**Cline**  
https://github.com/cline/cline  
Когда брать:
- если нужен IDE agent с браузером, терминалом, diff workflow и MCP;
- если важен строгий human-in-the-loop на каждом действии;
- если вы хотите показать аудитории понятный "агент внутри IDE" сценарий.

**Continue**  
https://github.com/continuedev/continue  
Когда брать:
- если интересны source-controlled AI checks в CI;
- если вы хотите хранить AI checks и правила прямо в репозитории;
- если вам важны `skills/`, `.continue/checks/` и agent-based review workflows.

### Browser agents и automation

**browser-use**  
https://github.com/browser-use/browser-use  
Когда брать:
- если нужен open-source browser agent library;
- если вы строите агент, который реально ходит по сайту, кликает, читает и выполняет задачи;
- если нужен сильный стартовый репозиторий для web automation именно под LLM agents.

**Skyvern**  
https://github.com/Skyvern-AI/skyvern  
Когда брать:
- если нужны browser workflows на базе LLM + computer vision;
- если нужен не только SDK, но и no-code workflow builder;
- если вы автоматизируете ручные browser-процессы бизнеса.

**Playwright**  
https://github.com/microsoft/playwright  
Когда брать:
- если вам нужна фундаментальная база для web automation;
- если вы строите browser agents и не хотите зависеть только от "магии" поверх браузера;
- если важны CLI, MCP и тестовая инфраструктура вокруг браузера.

### Память, графы, evals и observability

**Mem0**  
https://github.com/mem0ai/mem0  
Когда брать:
- если нужен отдельный memory layer для агентов;
- если вы делаете персонализацию, повторное использование контекста и долговременную память.

**Graphiti**  
https://github.com/getzep/graphiti  
Когда брать:
- если вам нужен не просто векторный retrieval, а temporal context graph;
- если факты меняются во времени и история состояния реально важна.

**Langfuse**  
https://github.com/langfuse/langfuse  
Когда брать:
- если нужна production observability для LLM/agent приложения;
- если вы хотите traces, evals, prompt management и self-hosted LLMOps слой.

**Phoenix**  
https://github.com/Arize-ai/phoenix  
Когда брать:
- если нужна AI observability, evaluation и troubleshooting;
- если вы строите систему вокруг tracing и экспериментов.

**Promptfoo**  
https://github.com/promptfoo/promptfoo  
Когда брать:
- если нужны evals, red teaming, проверка агентов и RAG в CI;
- если вы хотите проверять надежность, безопасность и качество до релиза.

### Voice и realtime agents

**Pipecat**  
https://github.com/pipecat-ai/pipecat  
Когда брать:
- если вы строите realtime voice / multimodal conversational agents;
- если важны low-latency pipelines, transports, STT/TTS/LLM orchestration.

**LiveKit Agents**  
https://github.com/livekit/agents  
Когда брать:
- если вы строите voice agents поверх WebRTC;
- если нужны telephony, realtime voice, multimodal sessions и MCP support;
- если хотите production-friendly voice agent framework с open-source server stack.

### MCP и tool ecosystem

**Model Context Protocol Servers**  
https://github.com/modelcontextprotocol/servers  
Когда брать:
- если вы хотите понять MCP не по пересказам, а по reference implementations;
- если вы проектируете собственные tools / servers / client integrations.

**Awesome MCP Servers**  
https://github.com/punkpeye/awesome-mcp-servers  
Когда брать:
- если вам нужен discovery-каталог MCP серверов;
- если вы подбираете готовые tool connectors под задачи команды.

---

## Готовые Подборки По Сценариям

### 1. Хочу собрать первого Python-агента без лишней боли

Минимальный старт:
- `PydanticAI`
- `FastAPI`
- `PostgreSQL`
- `Redis`
- `Ollama`
- `Qdrant`
- `Langfuse`

Логика:
- `PydanticAI` дает хороший DX и строгую валидацию;
- `FastAPI` удобно использовать как API-слой и webhook backend;
- `Ollama` закрывает локальный старт;
- `Qdrant` закрывает retrieval;
- `Langfuse` нужен, чтобы не отлаживать вслепую.

### 2. Хочу собрать production-агента с долгой жизнью и состоянием

Берите:
- `LangGraph`
- `Mem0` или `Graphiti`
- `LiteLLM`
- `Langfuse`
- `Promptfoo`

Когда это нужно:
- агент живет долго;
- нужны retries, state, handoffs, memory и нормальная трассировка;
- нельзя позволить себе "оно иногда просто странно сработало".

### 3. Хочу визуально собирать AI workflows и быстро показать результат

Берите:
- `Dify`
- `Langflow`
- `Flowise`

Как выбирать:
- `Dify`: ближе к продуктовой платформе;
- `Langflow`: сильный visual builder с API/MCP-экспортом;
- `Flowise`: быстрый self-hosted визуальный конструктор.

### 4. Хочу запустить внутренний AI workspace для команды

Берите:
- `AnythingLLM`
- `Dify`
- `Ollama`
- `Qdrant`
- `MinIO`

Подходит для:
- внутренней базы знаний;
- приватного AI assistant для команды;
- self-hosted контуров без зависимости от внешнего SaaS.

### 5. Хочу coding-agent стек

Берите:
- `OpenHands`
- `Aider`
- `Cline`
- `Continue`

Как выбирать:
- `OpenHands`: если хотите большую платформу и изучение полноценной agent architecture;
- `Aider`: если нужен самый практичный terminal workflow;
- `Cline`: если нужен сильный IDE agent с browser + terminal + MCP;
- `Continue`: если нужен repository-native AI checks и CI-контур.

### 6. Хочу агент, который реально работает с браузером

Берите:
- `browser-use`
- `Skyvern`
- `Playwright`

Как выбирать:
- `browser-use`: библиотека для browser agent сценариев;
- `Skyvern`: browser workflows + vision + no-code слой;
- `Playwright`: надежная нижняя база для web automation и agent tooling.

### 7. Хочу голосового или realtime-агента

Берите:
- `Pipecat`
- `LiveKit Agents`

Как выбирать:
- `Pipecat`: если нужен Python-first real-time voice/multimodal pipeline framework;
- `LiveKit Agents`: если важны WebRTC, telephony, server-side sessions и production realtime stack.

---

## Агентные Framework-ы: Что Брать И Когда

### LangGraph
Сильнее всего в:
- stateful orchestration;
- long-running workflows;
- subgraphs, branching, human approval, memory.

Не лучший выбор:
- если вам нужен только простой RAG-бот;
- если команда еще не готова проектировать graph/state модель явно.

### PydanticAI
Сильнее всего в:
- Python DX;
- structured outputs;
- typed agents;
- аккуратной интеграции с существующим Python backend.

Лучший сценарий:
- вы и так живете в `FastAPI`/`Pydantic`/Python-мире;
- вам нужна не агентная "магия", а инженерно понятный код.

### Semantic Kernel / Microsoft Agent Framework
Сильнее всего в:
- enterprise orchestration;
- Microsoft-экосистеме;
- plugin/tool extensibility;
- multi-agent системах с долгим жизненным циклом.

Лучший сценарий:
- команда enterprise-oriented;
- нужен межъязыковой стек;
- критичны governance и production support.

### LlamaIndex
Сильнее всего в:
- ingestion;
- knowledge pipelines;
- RAG;
- документных системах.

Лучший сценарий:
- главная проблема это знания и retrieval, а не orchestration.

### Agno
Сильнее всего в:
- запуске агентов как сервисов;
- unified runtime;
- sessions, scheduling, tracing, RBAC.

Лучший сценарий:
- вы хотите рано перейти от "локальный агент" к "агент как продакшен-сервис".

### AutoGen
Почему все еще полезен:
- исторически один из самых влиятельных multi-agent framework-ов;
- много материалов и примеров в сети.

Но:
- новым проектам лучше смотреть на более живые production-oriented пути;
- сам README сейчас прямо предупреждает о `maintenance mode`.

---

## Визуальные Платформы И AI App Builders

### Dify
Брать, если нужен:
- self-hosted LLM app platform;
- продуктовый UI;
- workflows + RAG + agents + model management + observability.

Сильная сторона:
- быстрое движение от прототипа к реальному внутреннему продукту.

### Langflow
Брать, если нужен:
- visual authoring;
- API export;
- MCP server export;
- удобная публикация flow как инструмента.

Сильная сторона:
- хорошее сочетание визуальности и инженерной расширяемости.

### Flowise
Брать, если нужен:
- очень быстрый self-hosted visual builder;
- Node/JS-путь;
- понятный старт через `docker compose`.

Сильная сторона:
- очень низкий порог входа для агентных UI-сценариев.

### AnythingLLM
Брать, если нужен:
- приватный командный AI workspace;
- chat with docs;
- built-in agents без тяжелой сборки.

Сильная сторона:
- ощущается как готовый продукт, а не только dev framework.

---

## Coding Agents: Что Стоит Изучать В 2026

### OpenHands
Чем хорош:
- это уже не просто "очередной coding bot", а крупная открытая платформа;
- внутри есть `skills/`, `.agents/skills`, CLI, GUI, REST API, облачный сценарий.

Кому нужен:
- тем, кто хочет изучать архитектуру полноценных software agents;
- тем, кто строит что-то похожее сам.

### Aider
Чем хорош:
- терминальный workflow;
- понятный git-centric сценарий;
- очень хорош для реальной ежедневной работы по коду.

Кому нужен:
- тем, кто хочет быстро начать использовать LLM в существующих репах без большой платформы.

### Cline
Чем хорош:
- IDE agent;
- browser use;
- terminal use;
- MCP extensibility;
- строгий human approval loop.

Кому нужен:
- тем, кто хочет "агент прямо в IDE", а не отдельную CLI-утилиту.

### Continue
Чем хорош сейчас:
- source-controlled AI checks;
- CI-driven agent review;
- repo-local checks в `.continue/checks/`;
- сильный подход к policy / quality / review automation.

Кому нужен:
- тем, кто думает не только о написании кода агентом, но и о проверке качества в CI.

---

## Skills, MCP, AGENTS.md И Repo-Local Agent Patterns

Это один из самых важных блоков во всей agent-экосистеме.

Большинство людей смотрят только на "framework", но реальная сила агентных систем часто лежит в том, как описаны:
- правила работы агента;
- разрешенные действия;
- reusable skills;
- tool servers;
- human approval boundaries;
- контекст проекта.

### Что стоит понимать

**`AGENTS.md`**  
Файл с правилами и рабочим контекстом для coding/assistant agents внутри конкретного репозитория.

**`CLAUDE.md`, `.clinerules`, `.continue/*`, `.cursor/*`**  
Vendor-specific или tool-specific инструкции, которые формируют поведение агента.

**`skills/`**  
Переиспользуемые agent skills: узкие инструкции, сценарии, пайплайны, recipe-like workflows.

**MCP**  
Model Context Protocol превращает tools и data sources в стандартный интерфейс для агентных клиентов. Это сильно лучше, чем каждый раз городить ad hoc glue code.

### Репозитории, которые стоит изучать именно ради skills / repo patterns

**OpenHands**  
https://github.com/OpenHands/OpenHands  
Почему полезно изучить:
- есть `skills/` и `.agents/skills`;
- видно, как устроена большая coding-agent платформа.

**Cline**  
https://github.com/cline/cline  
Почему полезно изучить:
- видны `skills`, MCP-ориентированное расширение, IDE workflow, rule files.

**browser-use**  
https://github.com/browser-use/browser-use  
Почему полезно изучить:
- есть `skills/`;
- можно посмотреть, как оформляют агентные browser сценарии.

**Continue**  
https://github.com/continuedev/continue  
Почему полезно изучить:
- `skills/`;
- `.continue/checks/`;
- хорошая модель repository-native AI checks.

**Mem0**  
https://github.com/mem0ai/mem0  
Почему полезно изучить:
- есть `skills/`, plugins и tool-specific agent integrations;
- видно, как строят ecosystem вокруг memory layer.

**LiveKit Agents**  
https://github.com/livekit/agents  
Почему полезно изучить:
- сам README рекомендует ставить docs MCP server и agent skill для coding agents;
- это сильный пример того, как documentation + skill + MCP работают вместе.

### Какой практический вывод

Если вы строите свой агентный продукт, вам почти наверняка нужны не только:
- модель;
- framework;
- prompts.

Вам нужны еще:
- repo-local правила;
- reusable skills;
- tool boundary;
- observability;
- evals;
- и безопасный способ подключать внешние действия.

Именно поэтому блок `AGENTS.md + skills + MCP` сегодня настолько важен.

---

## MCP: Что Смотреть В Первую Очередь

### Model Context Protocol Servers
https://github.com/modelcontextprotocol/servers

Это не "список всего на свете", а reference implementations.

Что дает:
- официальный набор примеров;
- понимание, как устроены MCP servers;
- хорошие стартовые шаблоны для своих инструментов.

Особенно полезны идеи из reference servers:
- filesystem;
- fetch;
- git;
- memory;
- sequential thinking;
- time.

### Awesome MCP Servers
https://github.com/punkpeye/awesome-mcp-servers

Это уже discovery-слой.

Брать, если:
- хотите быстро найти готовый server;
- нужно понять, какие integrations уже существуют;
- не хотите писать все сами с нуля.

### Почему MCP важен

MCP удобен потому что:
- делает tool integrations переносимыми между клиентами;
- упрощает переиспользование инструментов;
- помогает перестать делать "каждый агент со своим уникальным glue code".

---

## Browser Agents И Browser Automation

### browser-use
https://github.com/browser-use/browser-use

Сильные стороны:
- agent-first browser automation;
- удобный старт для задач "агент сам ходит по вебу";
- examples и benchmark-подход вокруг браузерных задач.

Лучший сценарий:
- агенту нужно открыть сайт, прочитать, ввести данные, пройти сценарий.

### Skyvern
https://github.com/Skyvern-AI/skyvern

Сильные стороны:
- LLM + computer vision для browser workflows;
- no-code builder;
- сильный продуктовый сценарий автоматизации ручных процессов.

Лучший сценарий:
- автоматизация бизнес-операций на реальных сайтах;
- brittle DOM/XPath automation уже не справляется.

### Playwright
https://github.com/microsoft/playwright

Сильные стороны:
- это фундаментальная база для надежной browser automation;
- есть library, test runner, CLI и MCP;
- прямо позиционируется как инструмент не только для тестов, но и для AI agents.

Практический вывод:
- `browser-use` и `Skyvern` полезны;
- но если вы строите серьезный browser-agent слой, понимать `Playwright` обязательно.

---

## Память И Контекст Для Агентов

### Mem0
https://github.com/mem0ai/mem0

Что дает:
- отдельный memory layer;
- user / session / agent memory;
- personalization;
- удобную интеграцию в агентные приложения.

Брать, если:
- агент должен помнить предпочтения пользователя;
- нужны долгоживущие отношения с контекстом, а не только текущий диалог.

### Graphiti
https://github.com/getzep/graphiti

Что дает:
- temporal context graphs;
- знания, которые меняются во времени;
- provenance и запросы к историческому состоянию.

Брать, если:
- данные не статичны;
- важно не только "что известно", но и "когда и как это изменилось".

### Что выбрать

- `Mem0`: если нужен быстрый и практичный memory layer.
- `Graphiti`: если нужна более сложная graph/time-aware memory модель.

---

## Evals, Red Teaming И Observability

### Langfuse
https://github.com/langfuse/langfuse

Что дает:
- traces;
- prompt management;
- evals;
- self-hosting;
- LLMOps слой для production agent systems.

Брать, если:
- у вас уже есть приложение;
- вам надо понимать, почему агент сработал именно так;
- вы хотите наблюдаемость, а не веру в magic.

### Phoenix
https://github.com/Arize-ai/phoenix

Что дает:
- open-source AI observability;
- tracing;
- evaluation;
- troubleshooting для LLM/agent workloads.

Брать, если:
- ваша команда мыслит через эксперименты, дебаг и анализ execution traces.

### Promptfoo
https://github.com/promptfoo/promptfoo

Что дает:
- evals;
- red teaming;
- vulnerability scanning;
- checks в CI/CD.

Брать, если:
- нужно гонять агента через тесты до продакшена;
- вы хотите не "вроде работает", а измеряемую надежность.

### Практическое правило

Если у вас есть агент в проде и нет хотя бы одного из:
- `Langfuse`;
- `Phoenix`;
- `Promptfoo`;

то вы, скорее всего, еще не довели инфраструктуру качества до взрослого уровня.

---

## Голосовые И Realtime Агенты

### Pipecat
https://github.com/pipecat-ai/pipecat

Сильные стороны:
- real-time voice and multimodal agents;
- composable pipelines;
- низкая задержка;
- экосистема вокруг debugging, UI kit, flows и subagents.

Брать, если:
- вы строите conversational AI с голосом как основным интерфейсом.

### LiveKit Agents
https://github.com/livekit/agents

Сильные стороны:
- realtime programmable participants;
- voice / video / WebRTC;
- telephony integration;
- MCP support;
- открытый server stack.

Брать, если:
- вам нужен production-grade voice stack;
- важны WebRTC и интеграция с клиентскими приложениями.

---

## Полезные Учебные И Curated Репозитории

### AI Agents for Beginners
https://github.com/microsoft/ai-agents-for-beginners

Что это:
- большой бесплатный курс в формате репозитория.

Почему полезно:
- хорошо объясняет фундаментальные темы;
- покрывает tool use, RAG, memory, browser use, production topics, context engineering.

Лучший сценарий:
- отправить тем, кто только входит в тему и тонет в хаосе.

### Model Context Protocol Servers
https://github.com/modelcontextprotocol/servers

Почему в учебной подборке:
- это лучший официальный источник, чтобы реально понять MCP.

### Promptfoo
https://github.com/promptfoo/promptfoo

Почему в учебной подборке:
- очень быстро заставляет думать не только про capability, но и про reliability/security.

---

## Агентная Инфраструктура И Поддерживающий Стек

Ниже уже не "агенты как таковые", а то, без чего большинство agent-продуктов быстро упирается в потолок.

### Ollama
https://docs.ollama.com/

Когда брать:
- нужен локальный старт;
- нужен приватный контур;
- нужно быстро тестировать open models без тяжелой инфраструктуры.

### LiteLLM
https://github.com/BerriAI/litellm

Когда брать:
- нужен единый gateway к 100+ LLM APIs;
- хотите не привязывать код к одному провайдеру;
- нужны routing, logging, guardrails, self-hosted gateway слой.

### Qdrant
https://qdrant.tech/documentation/

Когда брать:
- нужен semantic search / hybrid search;
- нужен production-ready vector store под RAG.

### PostgreSQL
https://www.postgresql.org/docs/

Когда брать:
- почти всегда как основную транзакционную БД;
- особенно если кроме AI-слоя у вас еще есть реальное приложение.

### Redis
https://redis.io/

Когда брать:
- кэш;
- queues;
- rate limits;
- locks;
- ephemeral agent state.

### MinIO
https://docs.min.io/

Когда брать:
- нужен свой S3-совместимый storage для документов, датасетов, артефактов, uploads.

### Docker Compose
https://docs.docker.com/compose/

Когда брать:
- почти всегда на старте;
- локальная разработка;
- staging;
- первый production на одном или нескольких серверах.

### Caddy / Nginx
- https://caddyserver.com/docs/
- https://nginx.org/en/docs/

Когда брать:
- `Caddy`: если нужен максимально простой HTTPS и быстрый старт;
- `Nginx`: если у команды уже есть strong ops expertise.

---

## Рекомендуемые Стеки По Умолчанию

### 1. Telegram-бот + AI + база знаний

- `aiogram`
- `FastAPI`
- `PostgreSQL`
- `Redis`
- `Qdrant`
- `Ollama`
- `LangGraph` или `PydanticAI`
- `Langfuse`
- `Docker Compose`

### 2. Internal AI assistant для команды

- `AnythingLLM` или `Dify`
- `Ollama`
- `Qdrant`
- `MinIO`
- `PostgreSQL`
- `Langfuse`

### 3. Browser workflow automation

- `browser-use` или `Skyvern`
- `Playwright`
- `LiteLLM`
- `Promptfoo`

### 4. Coding agent / repo assistant

- `OpenHands` или `Cline` или `Aider`
- `Continue`
- `Langfuse`
- `Promptfoo`
- repo-local `AGENTS.md`
- `MCP` tools

### 5. Voice / realtime agent

- `Pipecat` или `LiveKit Agents`
- `LiteLLM`
- `Langfuse`
- `Promptfoo`

---

## Что Я Бы Не Советовал Делать На Старте

- Не тащить в проект 5 agent framework-ов одновременно.
- Не строить multi-agent архитектуру, пока один хороший агент еще не доказал свою полезность.
- Не игнорировать `evals` и `observability`.
- Не делать tool integrations ad hoc, если можно вынести их в MCP.
- Не полагаться только на "промпт улучшили и стало лучше" без тестового контура.
- Не запускать browser agent в бизнес-процесс без понимания fallback, retries и human approval.

---

## Как Оценивать Новый Agent Репозиторий

Смотрите не только на звезды.

Проверяйте:
- есть ли внятный README и примеры;
- есть ли `AGENTS.md`, `skills/`, `examples/`, `evals/`;
- есть ли self-hosted путь;
- есть ли traces / observability / testing story;
- есть ли tool / MCP strategy;
- есть ли понятный production narrative, а не только демо;
- не находится ли проект уже в `maintenance mode`.

Если всего этого нет, перед вами может быть не platform-grade репозиторий, а просто удачный хайповый демо-проект.

---

## Если Нужен Очень Короткий Совет

Если вы русскоязычный разработчик и хотите без лишнего шума собрать сильный AI stack в 2026, чаще всего разумный старт такой:

- framework: `LangGraph` или `PydanticAI`
- docs/RAG: `LlamaIndex` + `Qdrant`
- local models: `Ollama`
- gateway: `LiteLLM`
- app platform: `Dify` или `Langflow`
- coding agent: `Aider` или `Cline`, для более крупного стека `OpenHands`
- browser automation: `browser-use` + `Playwright`
- memory: `Mem0`
- observability: `Langfuse`
- evals/security: `Promptfoo`
- infra: `PostgreSQL`, `Redis`, `MinIO`, `Docker Compose`

Это не "единственно правильный" стек.

Но это один из самых практичных наборов для:
- быстрого старта;
- self-hosted сценариев;
- обучения;
- публикации кейсов;
- и реального доведения продукта до usable состояния.

---

## Источники И Обновление

Материал сверялся по официальным репозиториям и официальной документации.

Ключевые источники этой версии:
- `langchain-ai/langgraph`
- `pydantic/pydantic-ai`
- `microsoft/semantic-kernel`
- `microsoft/autogen`
- `agno-agi/agno`
- `OpenHands/OpenHands`
- `Aider-AI/aider`
- `cline/cline`
- `continuedev/continue`
- `FlowiseAI/Flowise`
- `langflow-ai/langflow`
- `langgenius/dify`
- `Mintplex-Labs/anything-llm`
- `modelcontextprotocol/servers`
- `punkpeye/awesome-mcp-servers`
- `browser-use/browser-use`
- `Skyvern-AI/skyvern`
- `microsoft/playwright`
- `mem0ai/mem0`
- `getzep/graphiti`
- `langfuse/langfuse`
- `Arize-ai/phoenix`
- `promptfoo/promptfoo`
- `pipecat-ai/pipecat`
- `livekit/agents`
- `microsoft/ai-agents-for-beginners`

Последнее обновление: `2026-05-06`
