# ADR-0005 — Periodicidade de monitoramento x risco (IVCF-20)

- **Status:** PROPOSTO — aguarda confirmação da equipe clínica
- **Bloqueia:** lógica de decisão L2 §6 / PlanDefinition L3

## Contexto
O protocolo (§10, ATENTO 60+) define:
- IVCF-20 **alto** risco → coleta a cada **3 meses**
- IVCF-20 **médio** risco → cada **2 meses**
- IVCF-20 **baixo** risco → cada **1 mês**

Isso é **contraintuitivo**: normalmente maior risco implica monitoramento **mais frequente**, não
menos. O texto também diz que "alertas críticos antecipam agendamento / aumentam a frequência",
o que sugere que a tabela pode estar com as faixas invertidas ou refletir intervalo de reavaliação
formal (não de contato).

## Questão aberta (não decidir sozinho)
Confirmar com a equipe clínica se a intenção é:
- (A) literal como no protocolo (alto=3m, médio=2m, baixo=1m); **ou**
- (B) inversão (alto=1m, médio=2m, baixo=3m); **ou**
- (C) outra semântica (ex.: reavaliação do IVCF-20 vs. contato/coleta de sinais).

## Decisão provisória
Codificar **literal (A)** conforme o protocolo, com `// REVISAR ADR-0005` no PlanDefinition/CQL e
destaque na narrativa, até confirmação. Não inferir a inversão por conta própria.
