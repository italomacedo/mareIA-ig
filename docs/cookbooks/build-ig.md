# Cookbook — Build & validação do IG

## Gate rápido (sem Java) — SUSHI
```bash
sushi .
```
- Lê `sushi-config.yaml` + `input/fsh/**`.
- Gera `fsh-generated/resources/*.json`.
- **Aceite:** 0 Errors. Warnings revisados.

## Build completo — IG Publisher (requer Java 11+)
```bash
./_updatePublisher.sh   # 1ª vez: baixa input-cache/publisher.jar
./_genonce.sh           # roda SUSHI + IG Publisher
```
- Saída: `output/index.html` e `output/qa.html` (relatório de QA).
- **Aceite:** 0 erros de QA; links e referências resolvidos.

## Diagnóstico
| Sintoma | Causa provável | Ação |
|---|---|---|
| `sushi` acusa código inválido | code com espaço/acentuação | usar code ASCII; display PT-BR |
| Page não encontrada no QA | página listada em `sushi-config` sem arquivo | criar `input/pagecontent/<page>.md` |
| Dependência não baixa | sem rede / versão errada do pacote | revisar `dependencies:` e cache `~/.fhir` |
| `java` ausente | IG Publisher não roda | instalar Temurin/OpenJDK 11+ (ver Hard-Earned Lessons) |

## CI
Pode-se rodar apenas `sushi .` em CI como gate barato; o IG Publisher completo em job separado.
