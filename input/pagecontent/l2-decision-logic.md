Componente 6 do DAK — *Decision-support logic*. Fonte estruturada: `l2/6-decision-logic.csv`.
Implementada no L3 como `Library` (CQL) + `PlanDefinition`.

> A plataforma **apoia** a decisão; o profissional tem autonomia para **aceitar, modificar ou
> recusar** as recomendações (Protocolo §9).

### DT-1 · Escore IVCF-20
Soma dos 20 itens, respeitando os tetos de grupo (AVD Instrumental q3–q5 = máx 4; q14 = máx 2;
q20 = máx 4) → `ivcf-score` (0–40). **REVISAR ADR-0004.**

### DT-2 · Faixa de risco
| Escore | Faixa |
|---|---|
| 0–6 | **Robusto** (baixo risco) |
| 7–14 | **Risco de fragilização** (médio) |
| ≥ 15 | **Frágil** (alto risco) |

**REVISAR ADR-0004** (escore máximo e faixas a confirmar).

### DT-3 · Periodicidade de monitoramento
| Faixa de risco | Frequência de coleta |
|---|---|
| Alto (Frágil) | a cada **3 meses** |
| Médio | a cada **2 meses** |
| Baixo (Robusto) | a cada **1 mês** |

> ⚠️ **REVISAR ADR-0005** — o protocolo associa maior risco a menor frequência (contraintuitivo).
> Codificado literalmente até confirmação da equipe clínica.

### DT-4 · Gatilhos de alerta (independem da faixa)
Queda (qualquer) · internação recente (<6 meses) · IoT fora de referência crítica (PA, FC,
oximetria) · perda de peso não intencional · IMC < 22 · humor alterado · autopercepção piorando em
visitas consecutivas.

**Conduta:** alerta crítico → antecipar agendamento / aumentar a frequência de acompanhamento com a
equipe ou o ACS; notificação em tempo real às equipes.

*Fonte: Protocolo mareIA WP1, §8 (p.13), §9 (p.14), §10 (p.16), Anexo 15.6.3.*
