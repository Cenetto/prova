# CLAUDE.md

Istruzioni guida per Claude Code in questo progetto. Aggiorna questo file man mano che il progetto evolve.

## Panoramica del progetto

_Descrivi qui brevemente cosa fa il progetto, lo stack tecnologico principale e l'obiettivo generale._

## Struttura della repository

- `CLAUDE.md` — questo file, il "cervello" del progetto per Claude.
- `.env` — chiavi API e segreti locali (mai committato, vedi `.gitignore`).
- `.claude/settings.json` — configurazione di permessi e impostazioni del progetto.
- `.claude/skills/` — skill custom richiamabili con `/nome-skill`.
- `.claude/agents/` — agenti dedicati per compiti isolati.
- `.claude/rules/` — regole di sviluppo dettagliate (es. sicurezza, stile del codice).

## Convenzioni di sviluppo

_Aggiungi qui le convenzioni di codice, naming, testing, ecc. specifiche del progetto._

### Creazione di nuove skill

- La cartella `.claude/skills/skill-creator/` contiene la skill ufficiale Anthropic **Skill Creator**.
- **Regola vincolante:** ogni volta che viene richiesto di creare, modificare o ottimizzare una skill custom, Claude DEVE invocare la skill `skill-creator` (tramite lo strumento Skill) invece di scrivere un `SKILL.md` a mano o improvvisare la struttura.
- Questo garantisce che ogni skill del progetto segua lo stesso formato, le stesse convenzioni e (dove utile) passi per la fase di valutazione/eval prevista da `skill-creator`.

## Integrazioni MCP

### Composio

- Composio è collegato come **connector di claude.ai** (Settings → Connectors), non tramite un file `.mcp.json` nel repository: l'autenticazione è OAuth, legata all'account claude.ai dell'utente, e non è portabile via Git.
- Ogni collaboratore che vuole usare gli strumenti Composio in una sessione Claude Code deve avere il connector "Composio" abilitato sul proprio account claude.ai — non c'è nulla da installare o configurare in questo repository per farlo funzionare.
- Toolkit applicativo attualmente collegato tramite Composio: **Excel** (Microsoft Graph), account `gcrispino@hotmail.it`.
- Non committare mai token, API key o credenziali Composio nel repository: eventuali chiavi vanno in `.env` (già escluso da Git, vedi `.gitignore`).

## Comandi utili

_Aggiungi qui i comandi principali per build, test, lint, ecc._

## Note

- Parti dal minimo, aggiungi il resto quando serve.
