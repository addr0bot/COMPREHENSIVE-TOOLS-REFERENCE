# Подборка AI-Агентных Инструментов И Репозиториев

Это не каталог "всего подряд". Здесь только те инструменты и репозитории, которые реально стоит открыть, понять и оставить в закладках.

Подборка собрана для двух задач:
- быстро понять, что вообще есть на рынке;
- быстро выбрать нормальный стартовый стек под свою задачу.

<a id="nav"></a>
## Навигация

- [С чего начать](#start-here)
- [20 репозиториев, которые стоит знать](#must-know)
- [Подборки по задачам](#by-task)
- [Фреймворки и агентная логика](#frameworks)
- [Кодовые агенты](#coding-agents)
- [AGENTS.md, skills и MCP](#agents-md-mcp)
- [Браузерные агенты](#browser-agents)
- [Память, evals и observability](#quality-stack)
- [Voice и realtime](#voice)
- [Инфраструктура](#infra)
- [Как фильтровать новые репозитории](#how-to-evaluate)

<a id="start-here"></a>
## С Чего Начать

Если времени мало, откройте сначала это:
- [LangGraph](https://github.com/langchain-ai/langgraph)
- [PydanticAI](https://github.com/pydantic/pydantic-ai)
- [Dify](https://github.com/langgenius/dify)
- [OpenHands](https://github.com/OpenHands/OpenHands)
- [Aider](https://github.com/Aider-AI/aider)
- [Cline](https://github.com/cline/cline)
- [modelcontextprotocol/servers](https://github.com/modelcontextprotocol/servers)
- [Langfuse](https://github.com/langfuse/langfuse)
- [Promptfoo](https://github.com/promptfoo/promptfoo)

Это уже дает базовую карту: orchestration, coding agents, MCP, observability и evals.

<a id="must-know"></a>
## 20 Репозиториев, Которые Стоит Знать

### Базовые фреймворки

- [LangGraph](https://github.com/langchain-ai/langgraph) - stateful workflows, long-running задачи, human-in-the-loop, нормальная orchestration-модель.
- [PydanticAI](https://github.com/pydantic/pydantic-ai) - аккуратный Python-first стек с типами, validation и хорошим DX.
- [Semantic Kernel](https://github.com/microsoft/semantic-kernel) - сильный вариант для enterprise и Microsoft-стека.
- [LlamaIndex](https://github.com/run-llama/llama_index) - когда основной фокус на docs, retrieval и knowledge pipelines.
- [Agno](https://github.com/agno-agi/agno) - про запуск агентных сервисов, runtime, sessions, tracing и control plane.
- [AutoGen](https://github.com/microsoft/autogen) - важный исторический проект для multi-agent подходов; полезен для обзора экосистемы, но не как дефолтный выбор для нового продукта.

### Визуальные платформы

- [Dify](https://github.com/langgenius/dify) - одна из самых цельных open-source платформ для LLM apps, workflows, RAG и agents.
- [Langflow](https://github.com/langflow-ai/langflow) - визуальный builder, который не мешает инженерной работе и умеет экспортировать flows.
- [Flowise](https://github.com/FlowiseAI/Flowise) - быстрый визуальный старт, особенно если команда ближе к Node/JS.
- [AnythingLLM](https://github.com/Mintplex-Labs/anything-llm) - удобное self-hosted рабочее пространство для chat with docs, внутренних ассистентов и командного использования.

### Кодовые агенты

- [OpenHands](https://github.com/OpenHands/OpenHands) - большая open-source платформа вокруг coding agents, полезна для изучения архитектуры и практики.
- [Aider](https://github.com/Aider-AI/aider) - лучший быстрый вход в terminal-first coding workflow.
- [Cline](https://github.com/cline/cline) - сильный IDE agent с браузером, терминалом, diff review и MCP.
- [Continue](https://github.com/continuedev/continue) - полезен не только как ассистент, но и как слой AI checks и CI automation рядом с репозиторием.

### Браузер и automation

- [browser-use](https://github.com/browser-use/browser-use) - библиотека для browser agents поверх реального браузера.
- [Playwright](https://github.com/microsoft/playwright) - фундамент для нормальной browser automation, без него browser-agent слой понимать тяжело.
- [Skyvern](https://github.com/Skyvern-AI/skyvern) - browser automation с уклоном в workflows и computer-vision сценарии.

### Память, observability и MCP

- [Mem0](https://github.com/mem0ai/mem0) - отдельный memory layer для агентных приложений.
- [Langfuse](https://github.com/langfuse/langfuse) - traces, prompt management, evals и production observability.
- [Promptfoo](https://github.com/promptfoo/promptfoo) - evals, red teaming и проверки в CI.
- [modelcontextprotocol/servers](https://github.com/modelcontextprotocol/servers) - reference implementations для MCP и лучший официальный старт в тему.

<a id="by-task"></a>
## Подборки По Задачам

### Нужен Python backend с агентной логикой

Берите:
- [PydanticAI](https://github.com/pydantic/pydantic-ai) или [LangGraph](https://github.com/langchain-ai/langgraph)
- [FastAPI](https://fastapi.tiangolo.com/)
- [PostgreSQL](https://www.postgresql.org/docs/)
- [Redis](https://redis.io/)
- [Langfuse](https://github.com/langfuse/langfuse)

Если есть docs/RAG:
- [LlamaIndex](https://github.com/run-llama/llama_index)
- [Qdrant](https://qdrant.tech/documentation/)

### Нужен внутренний ассистент по базе знаний

Берите:
- [Dify](https://github.com/langgenius/dify) или [AnythingLLM](https://github.com/Mintplex-Labs/anything-llm)
- [Qdrant](https://qdrant.tech/documentation/)
- [MinIO](https://docs.min.io/)
- [Ollama](https://docs.ollama.com/)

Это хороший вариант для внутреннего поиска, FAQ, chat with docs и закрытого контура.

### Нужен coding assistant для своей репы

Берите:
- [Aider](https://github.com/Aider-AI/aider), если нужен терминал и быстрый результат
- [Cline](https://github.com/cline/cline), если нужен IDE workflow
- [Continue](https://github.com/continuedev/continue), если хотите еще и policy/checks внутри репозитория
- [OpenHands](https://github.com/OpenHands/OpenHands), если интересен более тяжелый agent stack

### Нужен browser automation слой

Берите:
- [Playwright](https://github.com/microsoft/playwright) как базу
- [browser-use](https://github.com/browser-use/browser-use), если нужен именно browser agent
- [Skyvern](https://github.com/Skyvern-AI/skyvern), если нужен workflow-first подход
- [Promptfoo](https://github.com/promptfoo/promptfoo), если это идет в прод

### Нужен voice / realtime стек

Берите:
- [Pipecat](https://github.com/pipecat-ai/pipecat)
- [LiveKit Agents](https://github.com/livekit/agents)

### Нужен self-hosted старт без SaaS-зоопарка

Берите:
- [Ollama](https://docs.ollama.com/)
- [PostgreSQL](https://www.postgresql.org/docs/)
- [Redis](https://redis.io/)
- [Qdrant](https://qdrant.tech/documentation/)
- [MinIO](https://docs.min.io/)
- [Docker Compose](https://docs.docker.com/compose/)

<a id="frameworks"></a>
## Фреймворки И Агентная Логика

### [LangGraph](https://github.com/langchain-ai/langgraph)

Подходит, когда:
- нужен state и ветвление;
- агент живет дольше одного запроса;
- нужны retries, checkpoints, approvals, handoffs.

Не лучший старт, если вам нужен просто один чат с документами.

### [PydanticAI](https://github.com/pydantic/pydantic-ai)

Подходит, когда:
- команда на Python;
- важны typed outputs;
- не хочется тащить тяжелую orchestration-модель слишком рано.

Очень хороший дефолтный выбор для аккуратного backend-first проекта.

### [Semantic Kernel](https://github.com/microsoft/semantic-kernel)

Подходит, когда:
- нужен enterprise-friendly стек;
- команда уже сидит в Microsoft-экосистеме;
- важны plugins, integrations и более официальный enterprise narrative.

### [LlamaIndex](https://github.com/run-llama/llama_index)

Подходит, когда:
- главная проблема в знаниях, а не в orchestration;
- нужен ingestion, indexing, retrieval и пайплайн по документам.

### [Agno](https://github.com/agno-agi/agno)

Подходит, когда:
- вы смотрите не только на код агента, но и на то, как его запускать как сервис;
- вам нужны sessions, tracing, scheduling и runtime story.

### [AutoGen](https://github.com/microsoft/autogen)

Подходит, когда:
- хочется понять старые multi-agent паттерны;
- нужно читать экосистему шире, а не только текущий популярный стек.

Для новых продуктов обычно есть более прямые варианты.

<a id="coding-agents"></a>
## Кодовые Агенты

### [OpenHands](https://github.com/OpenHands/OpenHands)

Смотреть, если:
- хотите изучать архитектуру полноценных coding agents;
- нужны примеры большого проекта с skills, runtime и UI;
- интересен agent platform подход, а не только CLI-утилита.

### [Aider](https://github.com/Aider-AI/aider)

Смотреть, если:
- нужен рабочий инструмент на каждый день;
- вы живете в git-репах и терминале;
- не хотите лишний слой поверх привычного dev workflow.

### [Cline](https://github.com/cline/cline)

Смотреть, если:
- нужен IDE-first опыт;
- важны browser + terminal + MCP в одной связке;
- нужен строгий loop с подтверждением действий.

### [Continue](https://github.com/continuedev/continue)

Смотреть, если:
- вам нужен не только copilot, но и правила на уровне репозитория;
- интересно держать AI checks и review automation рядом с кодом.

<a id="agents-md-mcp"></a>
## AGENTS.md, Skills И MCP

Это один из самых полезных слоев во всей agent-теме. Не framework решает все. Очень много зависит от того, как вы описали правила, действия и инструменты.

### Что есть что

- `AGENTS.md` - локальная инструкция для агента внутри репозитория: правила работы, границы, стиль, контекст проекта.
- `skills/` - переиспользуемые мини-сценарии под отдельные задачи: исследование кода, релиз, triage, docs, review.
- `MCP` - стандартный способ подключать tools и data sources без кастомной каши в каждом агенте.

### Что смотреть

- [OpenHands](https://github.com/OpenHands/OpenHands) - большой практический пример repo-local skills.
- [Cline](https://github.com/cline/cline) - хороший пример связки IDE agent + MCP + rules.
- [Continue](https://github.com/continuedev/continue) - полезен именно как слой repo-based checks и правил.
- [modelcontextprotocol/servers](https://github.com/modelcontextprotocol/servers) - официальный reference по MCP.
- [awesome-mcp-servers](https://github.com/punkpeye/awesome-mcp-servers) - каталог готовых MCP servers.

### Практический вывод

Если агент должен стабильно работать в команде, вам нужны:
- локальные правила;
- переиспользуемые skills;
- понятный список инструментов;
- evals и traces;
- ограничения на действия, а не только "умный промпт".

<a id="browser-agents"></a>
## Браузерные Агенты

### [Playwright](https://github.com/microsoft/playwright)

Это база. Даже если сверху вы ставите agent layer, нормальная browser automation все равно держится на Playwright-подходе.

### [browser-use](https://github.com/browser-use/browser-use)

Полезен, когда:
- нужен агент, который сам читает страницу, кликает и проходит пользовательский сценарий;
- не хочется собирать все руками поверх Playwright.

### [Skyvern](https://github.com/Skyvern-AI/skyvern)

Полезен, когда:
- нужен browser workflow под реальные бизнес-задачи;
- интересен более продуктовый, а не только библиотечный путь.

<a id="quality-stack"></a>
## Память, Evals И Observability

### Память

- [Mem0](https://github.com/mem0ai/mem0) - быстрый и практичный memory layer.
- [Graphiti](https://github.com/getzep/graphiti) - полезен, когда важен temporal graph и история изменений.

### Observability

- [Langfuse](https://github.com/langfuse/langfuse) - один из самых понятных open-source вариантов для traces, prompts и evals.
- [Phoenix](https://github.com/Arize-ai/phoenix) - сильный стек под debugging и AI observability.

### Evals

- [Promptfoo](https://github.com/promptfoo/promptfoo) - хороший старт для regression checks, red teaming и CI.

Если агент идет в прод, без этого слоя жить неприятно.

<a id="voice"></a>
## Voice И Realtime

- [Pipecat](https://github.com/pipecat-ai/pipecat) - полезен для голосовых и multimodal пайплайнов.
- [LiveKit Agents](https://github.com/livekit/agents) - полезен для WebRTC, voice, sessions и production realtime-интеграций.

<a id="infra"></a>
## Инфраструктура

### База, которую чаще всего имеет смысл держать под рукой

- [Ollama](https://docs.ollama.com/) - локальные модели и быстрый self-hosted старт.
- [LiteLLM](https://github.com/BerriAI/litellm) - gateway между приложением и несколькими LLM providers.
- [Qdrant](https://qdrant.tech/documentation/) - vector DB под retrieval и hybrid search.
- [PostgreSQL](https://www.postgresql.org/docs/) - основная БД почти для любого нормального продукта.
- [Redis](https://redis.io/) - cache, locks, queues, rate limits.
- [MinIO](https://docs.min.io/) - S3-совместимое хранилище.
- [Docker Compose](https://docs.docker.com/compose/) - нормальный старт для локалки и первых серверов.
- [Caddy](https://caddyserver.com/docs/) или [Nginx](https://nginx.org/en/docs/) - reverse proxy и HTTPS.

### Нормальный базовый self-hosted набор

- [PydanticAI](https://github.com/pydantic/pydantic-ai) или [LangGraph](https://github.com/langchain-ai/langgraph)
- [FastAPI](https://fastapi.tiangolo.com/)
- [PostgreSQL](https://www.postgresql.org/docs/)
- [Redis](https://redis.io/)
- [Qdrant](https://qdrant.tech/documentation/)
- [Ollama](https://docs.ollama.com/)
- [Langfuse](https://github.com/langfuse/langfuse)
- [Docker Compose](https://docs.docker.com/compose/)

<a id="how-to-evaluate"></a>
## Как Фильтровать Новые Репозитории

Смотрите не только на звезды.

Проверяйте:
- есть ли внятный README;
- есть ли живые examples;
- есть ли self-hosted путь;
- есть ли история про evals, traces, testing;
- есть ли repo-local rules, `AGENTS.md`, `skills/` или хотя бы понятный workflow;
- есть ли понятная tool strategy или MCP story;
- выглядит ли это как продуктовый инструмент, а не как демо на хайпе.

## Что Я Бы Не Тащил В Проект Сразу

- пять framework-ов одновременно;
- multi-agent схему без внятной причины;
- browser automation без fallback и human review;
- "магическую" систему без traces и evals;
- кастомный tool layer, если можно сделать это через MCP.

## Источники

Все ссылки в документе ведут на официальные репозитории или официальную документацию. Основу этой версии составляют:
- [langchain-ai/langgraph](https://github.com/langchain-ai/langgraph)
- [pydantic/pydantic-ai](https://github.com/pydantic/pydantic-ai)
- [microsoft/semantic-kernel](https://github.com/microsoft/semantic-kernel)
- [microsoft/autogen](https://github.com/microsoft/autogen)
- [langgenius/dify](https://github.com/langgenius/dify)
- [OpenHands/OpenHands](https://github.com/OpenHands/OpenHands)
- [Aider-AI/aider](https://github.com/Aider-AI/aider)
- [cline/cline](https://github.com/cline/cline)
- [continuedev/continue](https://github.com/continuedev/continue)
- [modelcontextprotocol/servers](https://github.com/modelcontextprotocol/servers)
- [langfuse/langfuse](https://github.com/langfuse/langfuse)
- [promptfoo/promptfoo](https://github.com/promptfoo/promptfoo)

Проверено: `2026-05-06`
