<p align="center">
  <a href="https://normahub.cc">
    <img src="https://raw.githubusercontent.com/normahubcc/normahubcc/main/docs/images/logo.png" alt="NormaHub" width="130" />
  </a>
</p>

<h1 align="center">NormaHub</h1>

<p align="center">
  <b>Единый AI API в России: доступ к текстовым моделям, генерации изображений и видео без VPN.</b><br>
  Один ключ для всех моделей, оплата картами РФ и через СБП, посекундный биллинг и единый баланс.
</p>

<p align="center">
  <a href="https://normahub.cc"><img src="https://img.shields.io/badge/Сайт-normahub.cc-6366f1?style=flat-square" alt="NormaHub" /></a>
  <a href="https://api.normahub.cc/docs"><img src="https://img.shields.io/badge/API-Документация-4f46e5?style=flat-square" alt="Docs" /></a>
  <a href="https://www.npmjs.com/package/@normahub/mcp-server"><img src="https://img.shields.io/npm/v/@normahub/mcp-server?style=flat-square&color=CB3837&logo=npm" alt="npm" /></a>
  <a href="https://github.com/marketplace/actions/normahub-ai-code-review"><img src="https://img.shields.io/badge/Marketplace-Code_Review-purple?style=flat-square&logo=github" alt="Marketplace" /></a>
</p>

---

### Open Source экосистема

| Проект | Описание | Быстрый запуск |
|---|---|---|
| [**`mcp-server-normahub`**](https://github.com/normahubcc/mcp-server-normahub) | Официальный MCP-сервер для Cursor, Claude Desktop и AI-агентов (Whisper, генерация видео, баланс) | `npx -y @normahub/mcp-server` |
| [**`normahub-cli`**](https://github.com/normahubcc/normahub-cli) | Терминальный ассистент, бенчмарк задержек (TTFT/tok/s) и локальный шлюз с SQLite-кэшем | `normahub benchmark` |
| [**`seedance-video-api-python`**](https://github.com/normahubcc/seedance-video-api-python) | Python SDK и CLI для видеогенерации SeeDance 2.5 / 2.0 и Grok Video (`generate`, `status`, `models`) | `pip install seedance-video-api` |
| [**`code-review-action`**](https://github.com/normahubcc/code-review-action) | GitHub Action для AI код-ревью в Pull Request с поддержкой `.normahub-review.yml` | `uses: normahubcc/code-review-action@v1` |
| [**`fastapi-ai-enterprise-starter`**](https://github.com/normahubcc/fastapi-ai-enterprise-starter) | High-Load AI Gateway на FastAPI с персистентным SQLite RAG, гибридным поиском и семантическим кэшем | `docker compose up` |
| [**`multi-agent-starter`**](https://github.com/normahubcc/multi-agent-starter) | Автономная мульти-агентная система на LangGraph 0.2+ с изолированной песочницей pytest | `python -m agent.cli` |
| [**`telegram-multimodal-studio`**](https://github.com/normahubcc/telegram-multimodal-studio) | Мультимодальная студия (Whisper транскрипция, SeeDance 2.5 видео и пресеты стилей) | `python -m bot.main` |
| [**`nextjs-ai-starter`**](https://github.com/normahubcc/nextjs-ai-starter) | Фуллстек Next.js 15 AI-чат с Live Canvas для интерактивных артефактов и Model Arena (Duel) | `pnpm dev` |
| [**`aiogram-ai-starter`**](https://github.com/normahubcc/aiogram-ai-starter) | Продакшен-стартер Telegram-бота (aiogram 3, транскрипция голосовых и кружочков, Stars) | `python -m bot.main` |
| [**`install_scripts`**](https://github.com/normahubcc/install_scripts) | Скрипты быстрой настройки Claude Code, Codex, OpenCode и экспресс-диагностики `check_normahub` | `bash check_normahub.sh` |

---

### Подключение

Эндпоинт полностью совместим с протоколом OpenAI. Подходит для Cursor, Continue, Roo-Code, Open WebUI и любых OpenAI-клиентов:

- **Base URL:** `https://api.normahub.cc/v1`
- **API Key:** `nr_hub_...` (выпускается в [личном кабинете](https://normahub.cc))

```python
from openai import OpenAI

client = OpenAI(
    base_url="https://api.normahub.cc/v1",
    api_key="nr_hub_..."
)

response = client.chat.completions.create(
    model="deepseek-v4.1-flash",
    messages=[{"role": "user", "content": "Привет!"}]
)
print(response.choices[0].message.content)
```

---

<p align="center">
  <a href="https://normahub.cc">normahub.cc</a> &nbsp;·&nbsp;
  <a href="https://api.normahub.cc/docs">Документация API</a> &nbsp;·&nbsp;
  <a href="https://normahub.cc/models">Каталог моделей</a> &nbsp;·&nbsp;
  <a href="mailto:manager@normahub.cc">Поддержка</a>
</p>
