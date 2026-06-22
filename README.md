# mareIA — ATENTO 60+ · WHO SMART Guidelines IG

Implementation Guide (FHIR R4) da **linha de cuidado ATENTO 60+** da Plataforma mareIA —
telemonitoramento ativo da **pessoa idosa** na Atenção Primária à Saúde, com estratificação
de risco pelo **Índice de Vulnerabilidade Clínico-Funcional (IVCF-20)**.

Este repositório é a **adaptação digital** do *Protocolo Clínico Geral mareIA (WP1)* — a
camada **L1 (Narrativa)** do [WHO SMART Guidelines](https://www.who.int/teams/digital-health-and-innovation/smart-guidelines) —
para as camadas **L2 (DAK — Digital Adaptation Kit)** e **L3 (IG FHIR, máquina-legível)**.

> No SMART Guidelines, **cada linha de cuidado (pathway) é um IG separado**. Este repo cobre
> **somente o ATENTO 60+**. Os demais cenários da mareIA (CardioRemoto, FamilIAr_Ativa, AgroSUS)
> serão repositórios próprios, reaproveitando este como template.

## Camadas SMART Guidelines

| Camada | O que é | Onde está |
|---|---|---|
| **L1** | Narrativa (protocolo clínico) | `sources/` (PDF + texto extraído) |
| **L2** | DAK — 9 componentes estruturados | `l2/` (fonte) + `input/pagecontent/l2-*.md` (narrativa do IG) |
| **L3** | Artefatos FHIR (FSH) | `input/fsh/**` → compilado para `fsh-generated/` |

## Estrutura

```
sources/      → L1: protocolo (fonte-verdade clínica)
l2/           → L2: DAK estruturado (CSV/DMN/BPMN/MD)
input/fsh/    → L3: FHIR Shorthand (profiles, instances, valuesets, libraries)
input/pagecontent/ → narrativa do IG publicado
docs/         → disciplina agentic-dev: PRD, ADRs, cookbooks, Hard-Earned Lessons
.claude/      → camada executável: subagentes (agents/) e skills/
```

## Desenvolvimento agêntico (agentic-based development)

O conteúdo é produzido por um **pipeline de agentes** versionado, com disciplina de docs
padrão de mercado. Pipeline L1 → L2 → L3:

1. `/l1-extract` — extrai fatos normalizados do protocolo (L1).
2. `/dak-build` — gera os 9 componentes do DAK (L2).
3. `/fhir-generate` — converte L2 em FSH (L3).
4. `/ig-build` — compila com SUSHI + IG Publisher e valida.

Decisões não-triviais viram **ADRs** (`docs/adr/`); armadilhas viram **Hard-Earned Lessons**
(`docs/hard-earned-lessons.md`). Veja `CLAUDE.md` para as convenções.

## Build

```bash
# 1. Compilar FSH → recursos FHIR JSON
sushi .

# 2. Gerar o site do IG (requer Java 11+; baixa o IG Publisher na 1ª vez)
./_genonce.sh      # Linux/macOS
_genonce.bat       # Windows
```

Saída em `output/index.html`.

## Status

`draft` v0.1.0 — fase WP1. Itens pendentes de confirmação clínica em `docs/adr/`.

## Licença

CC-BY-SA-4.0 (conteúdo). Instrumento IVCF-20 © seus autores (Moraes et al.) — uso conforme fonte.
