# rimfrost-service-workflow-openapi

OpenAPI-specifikation för Rimfrost workflow service.

## Endpoints

| Metod | Sökväg | Beskrivning |
|-------|--------|-------------|
| `POST` | `/yrkande` | Skapa ett nytt yrkande och starta en ny handläggningsprocess |
| `POST` | `/handlaggning/{handlaggningId}/process` | Starta en ny processinstans för en befintlig handläggning |

## Centrala begrepp

- **Yrkande** — ett yrkande för handläggning, med period, individer, roller och förväntade resultat
- **Handläggning** — ärendeinstansen som skapas när ett yrkande tas emot; innehåller referens till BPMN-processinstansen (`processinstansId`)
- **replyTo** — ett Kafka-topic som anroparen anger; tjänsten publicerar en notifiering dit när handläggningen är avslutad

## Relaterade repon

- [`rimfrost-service-handlaggning-openapi`](../rimfrost-service-handlaggning-openapi) — CRUD-API för handläggningsdata
