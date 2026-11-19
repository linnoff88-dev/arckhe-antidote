<div align="center">

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

*~3,000 lines Â· 35 files Â· 7 dependencies Â· 0 Docker containers*

[Framework Comparison â†’](https://inematds.github.io/antidote/)

</div>

---

## O que Ã©

**Antidote** Ã© um assistente de IA pessoal construÃ­do do zero em Python â€” sem frameworks de agente pesados, sem cloud obrigatÃ³ria, sem Docker, sem dashboard web. Roda no seu Mac, fala via Telegram, lembra de tudo, e tem personalidade definida por vocÃª.

Ã‰ exatamente o que o nome diz: o antÃ­doto contra frameworks de IA inchados.

```
VocÃª no Telegram
     â†“
Antidote recebe via long-polling
     â†“
Agent loop pensa, busca memÃ³ria, usa ferramentas
     â†“
OpenRouter (cloud) ou Ollama (local) gera a resposta
     â†“
VocÃª recebe a resposta no Telegram
```

---

## O que este projeto NÃƒO Ã©

| âŒ O que nÃ£o Ã© | âœ… O que Ã© |
|---------------|-----------|
| Multi-usuÃ¡rio | Single-owner, para vocÃª |
| Dependente de cloud | Roda 100% local com Ollama |
| Cheio de YAML | 7 dependÃªncias pip, ponto |
| Precisa de Docker | `./start.sh` e acabou |
| Interface web | Telegram Ã© a interface |
| Black-box | ~3.000 linhas legÃ­veis |

---

## Quickstart

```bash
# Clone

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="48" />
  <p><strong>Arckhé AI</strong></p>
</div>

git clone https://github.com/inematds/antidote.git
cd antidote

# Inicia tudo: cria venv, instala dependÃªncias, roda o wizard
./start.sh
```

O wizard guia vocÃª por tudo:

```
  â”Œâ”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”
  â”‚   Bem-vindo ao Antidote                              â”‚
  â”‚   The antidote to bloated AI frameworks.             â”‚
  â””â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”˜

  [1/6] Telegram Bot Token
        Abra o Telegram â†’ @BotFather â†’ /newbot â†’ cole o token
        âœ“ Token vÃ¡lido â€” bot: @MeuAntidoteBot

  [2/6] OpenRouter API Key
        openrouter.ai/keys â†’ crie uma chave â†’ cole aqui
        âœ“ Chave vÃ¡lida â€” 147 modelos disponÃ­veis

  [3/6] Modelo padrÃ£o
        â¯ Claude Sonnet 4 (recomendado)
          Claude Haiku 4 (mais barato)
          GPT-4.1 Mini (mais econÃ´mico)
          DeepSeek R1 (melhor custo-raciocÃ­nio)

  [4/6] Nome do seu assistente
        > Antidote

  [5/6] Personalidade em uma frase
        > Direto, honesto, sem enrolaÃ§Ã£o.

  âœ“ ConfiguraÃ§Ã£o salva
  âœ“ Banco de memÃ³ria criado
  âœ“ Auto-start instalado (launchd)

  Pronto. Mande uma mensagem no Telegram.
```

---

## Arquitetura

```
antidote/
â”œâ”€â”€ wizard.py                    # Wizard de setup (rich + questionary)
â”œâ”€â”€ start.sh                     # Launcher: venv + install + run
â”œâ”€â”€ com.antidote.agent.plist     # macOS launchd â€” auto-restart
â”œâ”€â”€ pyproject.toml               # Pacote Python, entry point `antidote`
â”œâ”€â”€ requirements.txt             # 7 dependÃªncias
â”‚
â”œâ”€â”€ antidote/
â”‚   â”œâ”€â”€ main.py                  # Entry point + CLI router
â”‚   â”œâ”€â”€ config.py                # Loader de config (singleton)
â”‚   â”‚
â”‚   â”œâ”€â”€ agent/
â”‚   â”‚   â”œâ”€â”€ loop.py              # â˜… Core: recebe â†’ pensa â†’ responde (max 5 rounds)
â”‚   â”‚   â””â”€â”€ context.py          # Monta system prompt + memÃ³rias relevantes
â”‚   â”‚
â”‚   â”œâ”€â”€ providers/
â”‚   â”‚   â”œâ”€â”€ base.py              # Interface abstrata
â”‚   â”‚   â”œâ”€â”€ openrouter.py        # OpenRouter via LiteLLM (100+ modelos)
â”‚   â”‚   â””â”€â”€ ollama.py            # Ollama local (zero custo, zero privacidade comprometida)
â”‚   â”‚
â”‚   â”œâ”€â”€ channels/
â”‚   â”‚   â”œâ”€â”€ base.py              # Interface abstrata
â”‚   â”‚   â””â”€â”€ telegram.py         # Long-polling, split de msg, typing indicator
â”‚   â”‚
â”‚   â”œâ”€â”€ memory/
â”‚   â”‚   â””â”€â”€ store.py             # SQLite FTS5 + BM25 ranking + deduplicaÃ§Ã£o
â”‚   â”‚
â”‚   â”œâ”€â”€ tools/
â”‚   â”‚   â”œâ”€â”€ base.py              # Interface abstrata
â”‚   â”‚   â”œâ”€â”€ registry.py          # Descoberta e dispatch de ferramentas
â”‚   â”‚   â”œâ”€â”€ filesystem.py        # read_file, write_file, list_directory
â”‚   â”‚   â””â”€â”€ shell.py             # run_command (com safety check)
â”‚   â”‚
â”‚   â””â”€â”€ security/
â”‚       â”œâ”€â”€ secrets.py           # Store Fernet (chave = UUID do hardware)
â”‚       â””â”€â”€ safety.py            # Blocklist de comandos + audit log
â”‚
â””â”€â”€ workspace/
    â”œâ”€â”€ SOUL.md                  # Personalidade da IA
    â”œâ”€â”€ AGENTS.md                # Regras de comportamento
    â”œâ”€â”€ USER.md                  # Perfil e preferÃªncias do usuÃ¡rio
    â””â”€â”€ MEMORY.md                # Fatos de bootstrap (seed inicial)
```

### Fluxo de uma mensagem

```
Telegram long-polling
    â†“  IncomingMessage
AgentLoop.process_message()
    â”œâ”€â”€ ContextBuilder
    â”‚       â”œâ”€â”€ SOUL.md + AGENTS.md + USER.md
    â”‚       â””â”€â”€ memory.search(query) â†’ memÃ³rias relevantes
    â”‚
    â”œâ”€â”€ Provider.chat(messages, tools)
    â”‚       â†“  LLMResponse
    â”‚       â””â”€â”€ tool_calls? â”€â”€â†’ ToolRegistry.execute()
    â”‚                               â””â”€â”€ re-envia ao LLM (max 5 rounds)
    â”‚
    â”œâ”€â”€ memory.save(resumo da conversa)
    â”‚
    â””â”€â”€ Channel.send(OutgoingMessage)
            â†“
        Telegram (split automÃ¡tico em >4096 chars)
```

---

## Stack de Identidade

A personalidade do Antidote vive em arquivos Markdown editÃ¡veis â€” sem banco de dados especial, sem interface separada. Edite no editor de texto.

| Arquivo | O que define |
|---------|-------------|
| `workspace/SOUL.md` | Personalidade: tom, valores, estilo de resposta |
| `workspace/AGENTS.md` | Regras: quando usar ferramentas, como usar memÃ³ria |
| `workspace/USER.md` | Perfil do usuÃ¡rio, preferÃªncias, contexto de vida |
| `workspace/MEMORY.md` | Fatos de bootstrap carregados na primeira vez |

Esses arquivos sÃ£o carregados por `agent/context.py` a cada mensagem e montam o system prompt enviado ao LLM.

---

## MemÃ³ria

Usa **SQLite FTS5** com ranking **BM25** â€” sem embeddings, sem chamadas de API para busca, sem custo extra.

```sql
-- Busca full-text com ranking de relevÃ¢ncia
SELECT * FROM memories_fts
WHERE memories_fts MATCH 'projeto python semana passada'
ORDER BY bm25(memories_fts)
LIMIT 10;
```

| Categoria | O que armazena |
|-----------|---------------|
| `fact` | Fatos sobre vocÃª, preferÃªncias, contexto |
| `conversation` | Resumos de conversas importantes |
| `solution` | SoluÃ§Ãµes para problemas recorrentes |
| `preference` | Como vocÃª gosta das coisas |

- **DeduplicaÃ§Ã£o automÃ¡tica**: se o conteÃºdo novo tem >80% de sobreposiÃ§Ã£o com uma entrada existente, atualiza em vez de duplicar
- **PersistÃªncia**: `~/.antidote/memory.db` â€” sobrevive a reinicializaÃ§Ãµes
- **Ferramentas do LLM**: `save_memory`, `search_memory`, `forget_memory` disponÃ­veis diretamente na conversa

---

## SeguranÃ§a

### Secrets encriptados (Fernet)
```
API Key â†’ AES-128-CBC + HMAC-SHA256 â†’ ~/.antidote/.secrets
                â†‘
    Chave derivada do UUID do hardware macOS via PBKDF2
    (arquivo .secrets Ã© inÃºtil em outra mÃ¡quina)
```

### Blocklist de comandos
```python
BLOCKED = ["rm -rf /", "mkfs", "dd if=", "shutdown", "reboot", "> /dev/sd"]
# Bloqueio por substring â€” qualquer variaÃ§Ã£o Ã© pega
```

### Outros controles
- Path traversal: ferramentas de filesystem restritas ao `workspace/`
- Timeout: 60s mÃ¡ximo por comando shell
- Truncamento: output de comandos limitado a 10KB, leitura de arquivo a 100KB
- Audit log: todo comando executado em `~/.antidote/audit.log`
- Gitignore: `config.json`, `.secrets`, `.env`, `*.db`, `*.log` nunca sobem

---

## Provedores de LLM

### OpenRouter (padrÃ£o)
- Acesso a 100+ modelos com uma Ãºnica chave de API
- Claude, GPT, Gemini, DeepSeek, Llama, Mistral â€” vocÃª escolhe
- Retry automÃ¡tico com backoff exponencial (rate limits e 5xx)
- Log de tokens consumidos para controle de custo

### Ollama (local/gratuito)
- Zero custo, zero dados enviados para fora
- Modelos: Llama 3.2, Mistral, Gemma, Phi-4, e outros
- Fallback automÃ¡tico se OpenRouter falhar
- Requer Ollama instalado: `brew install ollama`

---

## Auto-restart (macOS launchd)

O Antidote nÃ£o morre com sleep, crash ou reboot.

```bash
# O wizard instala automaticamente. Para instalar manualmente:
cp com.antidote.agent.plist ~/Library/LaunchAgents/
launchctl load ~/Library/LaunchAgents/com.antidote.agent.plist

# Para parar:
launchctl unload ~/Library/LaunchAgents/com.antidote.agent.plist
```

Logs ficam em `~/.antidote/logs/` para diagnÃ³stico.

---

## Comandos

```bash
# InicializaÃ§Ã£o
./start.sh              # Tudo: venv + install + wizard (se necessÃ¡rio) + bot
antidote                # Com venv ativo: auto-detecta config, inicia bot
antidote setup          # ForÃ§a re-execuÃ§Ã£o do wizard

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

## ConfiguraÃ§Ã£o

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

## DependÃªncias

| Pacote | VersÃ£o | Para que serve |
|--------|--------|---------------|
| `litellm` | â‰¥1.40.0 | Interface unificada para OpenRouter e Ollama |
| `python-telegram-bot` | â‰¥21.0 | Bot API async com long-polling |
| `cryptography` | â‰¥42.0 | Fernet â€” encriptaÃ§Ã£o dos secrets |
| `aiosqlite` | â‰¥0.20.0 | SQLite async sem bloquear o event loop |
| `python-dotenv` | â‰¥1.0 | Fallback de config via `.env` |
| `rich` | â‰¥13.0 | Terminal: painÃ©is, tabelas, cores |
| `questionary` | â‰¥2.0 | Prompts interativos no wizard |

---

## Roadmap

### Phase 2
- [ ] Cron scheduling (`tools/cron.py`)
- [ ] Web search/fetch (`tools/web.py`)
- [ ] Skills loader (`skills/loader.py`)
- [ ] Agent profiles (`agent/profiles.py`)

### Phase 3
- [ ] Browser automation â€” Playwright (`tools/browser.py`)
- [ ] Webhook triggers (`tools/webhook.py`)
- [ ] Screenshot + vision (`tools/screenshot.py`)
- [ ] Obsidian vault integration (`integrations/obsidian.py`)
- [ ] MCP protocol client (`integrations/mcp.py`)

---

## Interfaces (contratos)

Cada subsistema implementa uma classe abstrata. Adicionar um novo provedor, canal ou ferramenta = criar um arquivo novo, sem tocar no cÃ³digo existente.

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

**~3,000 linhas Â· 35 arquivos Â· 7 dependÃªncias Â· 0 containers Docker**

[Ver anÃ¡lise completa de frameworks â†’](https://inematds.github.io/antidote/)

</div>

---

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="32" />
  <p><strong>Arckhé AI</strong></p>
</div>