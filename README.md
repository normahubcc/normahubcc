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

### Open Source инструменты

| Проект | Описание | Быстрый запуск |
|---|---|---|
| [**`mcp-server-normahub`**](https://github.com/normahubcc/mcp-server-normahub) | Официальный MCP-сервер для Cursor, Claude Desktop и AI-агентов | `npx -y @normahub/mcp-server` |
| [**`normahub-cli`**](https://github.com/normahubcc/normahub-cli) | Локальный шлюз с SQLite-кэшем и эмуляцией протоколов OpenAI/Ollama | `normahub start` |
| [**`seedance-video-api-python`**](https://github.com/normahubcc/seedance-video-api-python) | Python SDK и CLI для видеомоделей SeeDance 2.5 и Grok Video | `pip install seedance-video-api` |
| [**`code-review-action`**](https://github.com/normahubcc/code-review-action) | GitHub Action для автоматического код-ревью в Pull Request | `uses: normahubcc/code-review-action@v1` |
| [**`install_scripts`**](https://github.com/normahubcc/install_scripts) | Скрипты быстрой настройки Claude Code, Codex и OpenCode под NormaHub | `bash install_claude.sh` |

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
