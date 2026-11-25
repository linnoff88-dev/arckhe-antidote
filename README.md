ï»¿<div align="center">

```
    _   _  _ _____ ___ ___  ___ _____ ___
   /_\ | \| |_   _|_ _|   \/ _ \_   _| __|
  / _ \| .` | | |  | || |) | (_) || | | _|
 /_/ \_\_|\_| |_| |___|___/ \___/ |_| |___|
```

**The antidote to bloated AI frameworks.**

[![Python](https://img.shields.io/badge/Python-3.11+-3776AB?style=flat-square&logo=python&logoColor=white)](https://www.python.org/)
[![Telegram](https://img.shields.io/badge/Telegram-Bot-26A5E4?style=flat-square&logo=telegram&logoColor=white)](https://core.telegram.org/bots)
[![OpenRouter](https://img.shields.io/badge/OpenRouter-100%2B%20Models-6c63ff?style=flat-square)](https://openrouter.ai/)
[![SQLite](https://img.shields.io/badge/Memory-SQLite%20FTS5-003B57?style=flat-square&logo=sqlite&logoColor=white)](https://www.sqlite.org/fts5.html)
[![Ollama](https://img.shields.io/badge/Local%20AI-Ollama-black?style=flat-square)](https://ollama.ai/)
[![Encrypted](https://img.shields.io/badge/Secrets-Fernet%20Encrypted-00D26A?style=flat-square)](https://cryptography.io/)
[![macOS](https://img.shields.io/badge/Platform-macOS-000000?style=flat-square&logo=apple&logoColor=white)](https://www.apple.com/macos/)

*~3,000 lines êÂ· 35 files êÂ· 7 dependencies êÂ· 0 Docker containers*

[Framework Comparison ê¢â â](https://linnoff88-dev.github.io/

</div>

---

## O que êÂ©

**Antidote** êÂ© um assistente de IA pessoal construêÂ­do do zero em Python ê¢â¬â sem frameworks de agente pesados, sem cloud obrigatêÂ³ria, sem Docker, sem dashboard web. Roda no seu Mac, fala via Telegram, lembra de tudo, e tem personalidade definida por vocêÂª.

êâ° exatamente o que o nome diz: o antêÂ­doto contra frameworks de IA inchados.

```
VocêÂª no Telegram
     ê¢â â
Antidote recebe via long-polling
     ê¢â â
Agent loop pensa, busca memêÂ³ria, usa ferramentas
     ê¢â â
OpenRouter (cloud) ou Ollama (local) gera a resposta
     ê¢â â
VocêÂª recebe a resposta no Telegram
```

---

## O que este projeto NêÆO êÂ©

| ê¢ÂÅ O que nêÂ£o êÂ© | ê¢Åâ¦ O que êÂ© |
|---------------|-----------|
| Multi-usuêÂ¡rio | Single-owner, para vocêÂª |
| Dependente de cloud | Roda 100% local com Ollama |
| Cheio de YAML | 7 dependêÂªncias pip, ponto |
| Precisa de Docker | `./start.sh` e acabou |
| Interface web | Telegram êÂ© a interface |
| Black-box | ~3.000 linhas legêÂ­veis |

---

## Quickstart

```bash
# Clone

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="48" />
  <p><strong>Arckhé AI</strong></p>
</div>

git clone https://github.com/linnoff88-dev/antidote.git
cd antidote

# Inicia tudo: cria venv, instala dependêÂªncias, roda o wizard
./start.sh
```

O wizard guia vocêÂª por tudo:

```
  ê¢âÅê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢âÂ
  ê¢ââ   Bem-vindo ao Antidote                              ê¢ââ
  ê¢ââ   The antidote to bloated AI frameworks.             ê¢ââ
  ê¢ââê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢ââ¬ê¢âË

  [1/6] Telegram Bot Token
        Abra o Telegram ê¢â â @BotFather ê¢â â /newbot ê¢â â cole o token
        ê¢Åâ Token vêÂ¡lido ê¢â¬â bot: @MeuAntidoteBot

  [2/6] OpenRouter API Key
        openrouter.ai/keys ê¢â â crie uma chave ê¢â â cole aqui
        ê¢Åâ Chave vêÂ¡lida ê¢â¬â 147 modelos disponêÂ­veis

  [3/6] Modelo padrêÂ£o
        ê¢ÂÂ¯ Claude Sonnet 4 (recomendado)
          Claude Haiku 4 (mais barato)
          GPT-4.1 Mini (mais econêÂ´mico)
          DeepSeek R1 (melhor custo-raciocêÂ­nio)

  [4/6] Nome do seu assistente
        > Antidote

  [5/6] Personalidade em uma frase
        > Direto, honesto, sem enrolaêÂ§êÂ£o.

  ê¢Åâ ConfiguraêÂ§êÂ£o salva
  ê¢Åâ Banco de memêÂ³ria criado
  ê¢Åâ Auto-start instalado (launchd)

  Pronto. Mande uma mensagem no Telegram.
```

---

## Arquitetura

```
antidote/
ê¢âÅê¢ââ¬ê¢ââ¬ wizard.py                    # Wizard de setup (rich + questionary)
ê¢âÅê¢ââ¬ê¢ââ¬ start.sh                     # Launcher: venv + install + run
ê¢âÅê¢ââ¬ê¢ââ¬ com.antidote.agent.plist     # macOS launchd ê¢â¬â auto-restart
ê¢âÅê¢ââ¬ê¢ââ¬ pyproject.toml               # Pacote Python, entry point `antidote`
ê¢âÅê¢ââ¬ê¢ââ¬ requirements.txt             # 7 dependêÂªncias
ê¢ââ
ê¢âÅê¢ââ¬ê¢ââ¬ antidote/
ê¢ââ   ê¢âÅê¢ââ¬ê¢ââ¬ main.py                  # Entry point + CLI router
ê¢ââ   ê¢âÅê¢ââ¬ê¢ââ¬ config.py                # Loader de config (singleton)
ê¢ââ   ê¢ââ
ê¢ââ   ê¢âÅê¢ââ¬ê¢ââ¬ agent/
ê¢ââ   ê¢ââ   ê¢âÅê¢ââ¬ê¢ââ¬ loop.py              # ê¢Ëâ¦ Core: recebe ê¢â â pensa ê¢â â responde (max 5 rounds)
ê¢ââ   ê¢ââ   ê¢ââê¢ââ¬ê¢ââ¬ context.py          # Monta system prompt + memêÂ³rias relevantes
ê¢ââ   ê¢ââ
ê¢ââ   ê¢âÅê¢ââ¬ê¢ââ¬ providers/
ê¢ââ   ê¢ââ   ê¢âÅê¢ââ¬ê¢ââ¬ base.py              # Interface abstrata
ê¢ââ   ê¢ââ   ê¢âÅê¢ââ¬ê¢ââ¬ openrouter.py        # OpenRouter via LiteLLM (100+ modelos)
ê¢ââ   ê¢ââ   ê¢ââê¢ââ¬ê¢ââ¬ ollama.py            # Ollama local (zero custo, zero privacidade comprometida)
ê¢ââ   ê¢ââ
ê¢ââ   ê¢âÅê¢ââ¬ê¢ââ¬ channels/
ê¢ââ   ê¢ââ   ê¢âÅê¢ââ¬ê¢ââ¬ base.py              # Interface abstrata
ê¢ââ   ê¢ââ   ê¢ââê¢ââ¬ê¢ââ¬ telegram.py         # Long-polling, split de msg, typing indicator
ê¢ââ   ê¢ââ
ê¢ââ   ê¢âÅê¢ââ¬ê¢ââ¬ memory/
ê¢ââ   ê¢ââ   ê¢ââê¢ââ¬ê¢ââ¬ store.py             # SQLite FTS5 + BM25 ranking + deduplicaêÂ§êÂ£o
ê¢ââ   ê¢ââ
ê¢ââ   ê¢âÅê¢ââ¬ê¢ââ¬ tools/
ê¢ââ   ê¢ââ   ê¢âÅê¢ââ¬ê¢ââ¬ base.py              # Interface abstrata
ê¢ââ   ê¢ââ   ê¢âÅê¢ââ¬ê¢ââ¬ registry.py          # Descoberta e dispatch de ferramentas
ê¢ââ   ê¢ââ   ê¢âÅê¢ââ¬ê¢ââ¬ filesystem.py        # read_file, write_file, list_directory
ê¢ââ   ê¢ââ   ê¢ââê¢ââ¬ê¢ââ¬ shell.py             # run_command (com safety check)
ê¢ââ   ê¢ââ
ê¢ââ   ê¢ââê¢ââ¬ê¢ââ¬ security/
ê¢ââ       ê¢âÅê¢ââ¬ê¢ââ¬ secrets.py           # Store Fernet (chave = UUID do hardware)
ê¢ââ       ê¢ââê¢ââ¬ê¢ââ¬ safety.py            # Blocklist de comandos + audit log
ê¢ââ
ê¢ââê¢ââ¬ê¢ââ¬ workspace/
    ê¢âÅê¢ââ¬ê¢ââ¬ SOUL.md                  # Personalidade da IA
    ê¢âÅê¢ââ¬ê¢ââ¬ AGENTS.md                # Regras de comportamento
    ê¢âÅê¢ââ¬ê¢ââ¬ USER.md                  # Perfil e preferêÂªncias do usuêÂ¡rio
    ê¢ââê¢ââ¬ê¢ââ¬ MEMORY.md                # Fatos de bootstrap (seed inicial)
```

### Fluxo de uma mensagem

```
Telegram long-polling
    ê¢â â  IncomingMessage
AgentLoop.process_message()
    ê¢âÅê¢ââ¬ê¢ââ¬ ContextBuilder
    ê¢ââ       ê¢âÅê¢ââ¬ê¢ââ¬ SOUL.md + AGENTS.md + USER.md
    ê¢ââ       ê¢ââê¢ââ¬ê¢ââ¬ memory.search(query) ê¢â â memêÂ³rias relevantes
    ê¢ââ
    ê¢âÅê¢ââ¬ê¢ââ¬ Provider.chat(messages, tools)
    ê¢ââ       ê¢â â  LLMResponse
    ê¢ââ       ê¢ââê¢ââ¬ê¢ââ¬ tool_calls? ê¢ââ¬ê¢ââ¬ê¢â â ToolRegistry.execute()
    ê¢ââ                               ê¢ââê¢ââ¬ê¢ââ¬ re-envia ao LLM (max 5 rounds)
    ê¢ââ
    ê¢âÅê¢ââ¬ê¢ââ¬ memory.save(resumo da conversa)
    ê¢ââ
    ê¢ââê¢ââ¬ê¢ââ¬ Channel.send(OutgoingMessage)
            ê¢â â
        Telegram (split automêÂ¡tico em >4096 chars)
```

---

## Stack de Identidade

A personalidade do Antidote vive em arquivos Markdown editêÂ¡veis ê¢â¬â sem banco de dados especial, sem interface separada. Edite no editor de texto.

| Arquivo | O que define |
|---------|-------------|
| `workspace/SOUL.md` | Personalidade: tom, valores, estilo de resposta |
| `workspace/AGENTS.md` | Regras: quando usar ferramentas, como usar memêÂ³ria |
| `workspace/USER.md` | Perfil do usuêÂ¡rio, preferêÂªncias, contexto de vida |
| `workspace/MEMORY.md` | Fatos de bootstrap carregados na primeira vez |

Esses arquivos sêÂ£o carregados por `agent/context.py` a cada mensagem e montam o system prompt enviado ao LLM.

---

## MemêÂ³ria

Usa **SQLite FTS5** com ranking **BM25** ê¢â¬â sem embeddings, sem chamadas de API para busca, sem custo extra.

```sql
-- Busca full-text com ranking de relevêÂ¢ncia
SELECT * FROM memories_fts
WHERE memories_fts MATCH 'projeto python semana passada'
ORDER BY bm25(memories_fts)
LIMIT 10;
```

| Categoria | O que armazena |
|-----------|---------------|
| `fact` | Fatos sobre vocêÂª, preferêÂªncias, contexto |
| `conversation` | Resumos de conversas importantes |
| `solution` | SoluêÂ§êÂµes para problemas recorrentes |
| `preference` | Como vocêÂª gosta das coisas |

- **DeduplicaêÂ§êÂ£o automêÂ¡tica**: se o conteêÂºdo novo tem >80% de sobreposiêÂ§êÂ£o com uma entrada existente, atualiza em vez de duplicar
- **PersistêÂªncia**: `~/.antidote/memory.db` ê¢â¬â sobrevive a reinicializaêÂ§êÂµes
- **Ferramentas do LLM**: `save_memory`, `search_memory`, `forget_memory` disponêÂ­veis diretamente na conversa

---

## SeguranêÂ§a

### Secrets encriptados (Fernet)
```
API Key ê¢â â AES-128-CBC + HMAC-SHA256 ê¢â â ~/.antidote/.secrets
                ê¢â â
    Chave derivada do UUID do hardware macOS via PBKDF2
    (arquivo .secrets êÂ© inêÂºtil em outra mêÂ¡quina)
```

### Blocklist de comandos
```python
BLOCKED = ["rm -rf /", "mkfs", "dd if=", "shutdown", "reboot", "> /dev/sd"]
# Bloqueio por substring ê¢â¬â qualquer variaêÂ§êÂ£o êÂ© pega
```

### Outros controles
- Path traversal: ferramentas de filesystem restritas ao `workspace/`
- Timeout: 60s mêÂ¡ximo por comando shell
- Truncamento: output de comandos limitado a 10KB, leitura de arquivo a 100KB
- Audit log: todo comando executado em `~/.antidote/audit.log`
- Gitignore: `config.json`, `.secrets`, `.env`, `*.db`, `*.log` nunca sobem

---

## Provedores de LLM

### OpenRouter (padrêÂ£o)
- Acesso a 100+ modelos com uma êÂºnica chave de API
- Claude, GPT, Gemini, DeepSeek, Llama, Mistral ê¢â¬â vocêÂª escolhe
- Retry automêÂ¡tico com backoff exponencial (rate limits e 5xx)
- Log de tokens consumidos para controle de custo

### Ollama (local/gratuito)
- Zero custo, zero dados enviados para fora
- Modelos: Llama 3.2, Mistral, Gemma, Phi-4, e outros
- Fallback automêÂ¡tico se OpenRouter falhar
- Requer Ollama instalado: `brew install ollama`

---

## Auto-restart (macOS launchd)

O Antidote nêÂ£o morre com sleep, crash ou reboot.

```bash
# O wizard instala automaticamente. Para instalar manualmente:
cp com.antidote.agent.plist ~/Library/LaunchAgents/
launchctl load ~/Library/LaunchAgents/com.antidote.agent.plist

# Para parar:
launchctl unload ~/Library/LaunchAgents/com.antidote.agent.plist
```

Logs ficam em `~/.antidote/logs/` para diagnêÂ³stico.

---

## Comandos

```bash
# InicializaêÂ§êÂ£o
./start.sh              # Tudo: venv + install + wizard (se necessêÂ¡rio) + bot
antidote                # Com venv ativo: auto-detecta config, inicia bot
antidote setup          # ForêÂ§a re-execuêÂ§êÂ£o do wizard

# Desenvolvimento
source .venv/bin/activate
pip install -e .
python -m pytest tests/ -v

# Logs
tail -f ~/.antidote/logs/antidote.log
tail -f ~/.antidote/audit.log

# launchd
launchctl list | grep antidote
launchctl stop com.antidote.agent
launchctl start com.antidote.agent
```

---

## ConfiguraêÂ§êÂ£o

O wizard gera `~/.antidote/config.json` (gitignored). Estrutura:

```json
{
  "name": "Antidote",
  "providers": {
    "default": "openrouter",
    "openrouter": { "model": "anthropic/claude-sonnet-4-20250514" },
    "ollama": { "model": "llama3.2", "base_url": "http://localhost:11434" }
  },
  "channels": {
    "telegram": { "enabled": true }
  },
  "memory": {
    "db_path": "~/.antidote/memory.db",
    "max_context_memories": 10
  },
  "safety": {
    "blocked_commands": ["rm -rf /", "mkfs", "dd if=", "shutdown"],
    "max_command_timeout": 60
  }
}
```

---

## DependêÂªncias

| Pacote | VersêÂ£o | Para que serve |
|--------|--------|---------------|
| `litellm` | ê¢â°Â¥1.40.0 | Interface unificada para OpenRouter e Ollama |
| `python-telegram-bot` | ê¢â°Â¥21.0 | Bot API async com long-polling |
| `cryptography` | ê¢â°Â¥42.0 | Fernet ê¢â¬â encriptaêÂ§êÂ£o dos secrets |
| `aiosqlite` | ê¢â°Â¥0.20.0 | SQLite async sem bloquear o event loop |
| `python-dotenv` | ê¢â°Â¥1.0 | Fallback de config via `.env` |
| `rich` | ê¢â°Â¥13.0 | Terminal: painêÂ©is, tabelas, cores |
| `questionary` | ê¢â°Â¥2.0 | Prompts interativos no wizard |

---

## Roadmap

### Phase 2
- [ ] Cron scheduling (`tools/cron.py`)
- [ ] Web search/fetch (`tools/web.py`)
- [ ] Skills loader (`skills/loader.py`)
- [ ] Agent profiles (`agent/profiles.py`)

### Phase 3
- [ ] Browser automation ê¢â¬â Playwright (`tools/browser.py`)
- [ ] Webhook triggers (`tools/webhook.py`)
- [ ] Screenshot + vision (`tools/screenshot.py`)
- [ ] Obsidian vault integration (`integrations/obsidian.py`)
- [ ] MCP protocol client (`integrations/mcp.py`)

---

## Interfaces (contratos)

Cada subsistema implementa uma classe abstrata. Adicionar um novo provedor, canal ou ferramenta = criar um arquivo novo, sem tocar no cêÂ³digo existente.

```python
# Novo provedor: implemente BaseProvider
class MyProvider(BaseProvider):
    async def chat(self, messages, tools, model, temperature) -> LLMResponse: ...

# Nova ferramenta: implemente BaseTool
class MyTool(BaseTool):
    name = "my_tool"
    description = "..."
    parameters = {...}  # JSON Schema
    async def execute(self, **kwargs) -> ToolResult: ...

# Novo canal: implemente BaseChannel
class MyChannel(BaseChannel):
    async def start(self, on_message): ...
    async def send(self, message: OutgoingMessage): ...
    async def stop(self): ...
```

---

<div align="center">

**~3,000 linhas êÂ· 35 arquivos êÂ· 7 dependêÂªncias êÂ· 0 containers Docker**

[Ver anêÂ¡lise completa de frameworks ê¢â â](https://linnoff88-dev.github.io/

</div>

---

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="32" />
  <p><strong>Arckhé AI</strong></p>
</div>