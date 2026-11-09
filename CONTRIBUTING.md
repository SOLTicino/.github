# Contribuire ai progetti SOLTI

Regole di lavoro valide per tutti i repository dell'organizzazione SOLTicino.

## Pianificazione

Il lavoro di NOTI è pianificato nel Project [NOTI](https://github.com/orgs/SOLTicino/projects/4).

- Ogni lavoro parte da una issue, con **Area**, **Priority** e **Size** compilati.
- Il campo **Release** indica in quale major update la issue arriverà su `main`.
- Le modifiche alle API del backend hanno la label `api-change`.

### Status

| Status | Significato |
|---|---|
| Backlog | Da valutare |
| Todo | Pronto, assegnato a uno sprint |
| In progress | In lavorazione |
| In staging | Su staging, in attesa del rilascio in prod |
| Done | Rilasciato in prod |
| Released (main) | Incluso in un major update su main |

## Branch

```
feature/X · bug/X → dev → staging → prod → main
```

- **dev**: integrazione del lavoro quotidiano
- **staging**: collaudo prima del rilascio
- **prod**: produzione, i deploy normali partono da qui
- **main**: solo i major update (v1.0, v2.0…), promossi da prod
- **Hotfix**: branch da `prod`, poi riportato in `staging` e `dev`

Nome dei branch di lavoro: `feature/<n-issue>-descrizione` oppure `bug/<n-issue>-descrizione`.

## Commit

Il messaggio inizia con un codice che indica il tipo di modifica:

| Codice | Uso |
|---|---|
| `ADD:` | Nuova funzionalità o nuovo file |
| `UPDATE:` | Modifica a qualcosa di esistente |
| `FIX:` | Correzione di un bug |
| `REMOVE:` | Rimozione di codice o file |

Esempio: `FIX: login fallisce con email maiuscole (#12)`
