# Skills

Cartella per le custom skill del progetto.

Ogni skill è una sottocartella con un file `SKILL.md` che ne descrive nome, trigger e istruzioni. Una volta creata, una skill è richiamabile con `/nome-skill`.

Esempio di struttura:

```
skills/
  nome-skill/
    SKILL.md
  skill-creator/
    SKILL.md
```

## `skill-creator`

La skill `skill-creator/` (ufficiale Anthropic) è lo strumento standard per creare, modificare e ottimizzare qualsiasi skill di questo progetto.

**Regola vincolante:** ogni volta che viene richiesto di generare una nuova skill, Claude deve invocare `skill-creator` (non creare `SKILL.md` a mano). Vedi la sezione "Convenzioni di sviluppo" in `CLAUDE.md` per il dettaglio della regola.
