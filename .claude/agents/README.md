# Agents

Cartella per gli agenti AI dedicati del progetto.

Ogni agente è definito in un file Markdown con frontmatter (nome, descrizione, tool consentiti) e viene usato da Claude per delegare compiti isolati e specifici.

Esempio di struttura:

```
agents/
  nome-agente.md
```

## Agenti installati

| File | Nome | Ruolo |
|---|---|---|
| `code-reviewer.md` | `code-reviewer` | Revisiona codice/diff/PR per correttezza, sicurezza, qualità e performance. Sola lettura, non modifica file. |
| `qa-tester.md` | `qa-tester` | Verifica funzionalmente il codice: scrive ed esegue test, individua edge case, segnala bug con causa radice. |
| `researcher.md` | `researcher` | Esplora codebase o web su domande aperte e restituisce sintesi concise, tenendo il dettaglio fuori dal contesto principale. |

Claude li invoca automaticamente in base alla `description` di ciascuno (delega proattiva), oppure possono essere richiamati esplicitamente tramite lo strumento Agent.
