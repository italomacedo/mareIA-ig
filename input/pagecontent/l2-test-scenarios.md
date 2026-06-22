Componente 9 do DAK — *Test scenarios*. Casos para validar a lógica de decisão (comp. 6) no L3.

### Casos de escore/faixa (IVCF-20)
| Caso | Respostas (resumo) | Escore esperado | Faixa esperada |
|---|---|---|---|
| TC-01 | Idoso saudável: idade 60–74, sem itens positivos | 0 | Robusto |
| TC-02 | Idade 75–84 + autopercepção regular + 1 queda no ano | 1+1+2 = 4 | Robusto |
| TC-03 | ≥85 + esquecimento + duas quedas + visão | 3+1+2+2 ≈ 8–10 | Risco de fragilização |
| TC-04 | Frágil: banho dependente (6) + AVDI (4) + comorbidades (4) + marcha (2) | ≥ 16 | Frágil |

> Escores **REVISAR ADR-0004** (tetos/escore total a confirmar).

### Casos de alerta (independem da faixa)
| Caso | Gatilho | Resultado esperado |
|---|---|---|
| TC-05 | 2+ quedas no último ano | ALERTA + notificação às equipes |
| TC-06 | IMC < 22 | ALERTA |
| TC-07 | SpO₂ fora da referência crítica (IoT) | ALERTA crítico → antecipar agendamento |
| TC-08 | Internação recente (<6 meses) | ALERTA |

### Casos de periodicidade
| Caso | Faixa | Próxima coleta esperada |
|---|---|---|
| TC-09 | Frágil (alto) | +3 meses (**REVISAR ADR-0005**) |
| TC-10 | Robusto (baixo) | +1 mês (**REVISAR ADR-0005**) |

*Casos derivados do Protocolo mareIA WP1, §8, §10 e Anexo 15.6.3.*
