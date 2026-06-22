Componente 4 do DAK — *Business processes and workflows*. As 4 macrofases do fluxo ATENTO 60+.
O diagrama BPMN 2.0 fonte está em `l2/4-business-process.bpmn` (importável no bpmn.io).

### Fase 1 — Pré-Intervenção (Entrada e Cadastro)
1. Identificação de pessoa idosa elegível pela Equipe de Gestão do Cuidado.
2. Verificação dos critérios de inclusão/exclusão.
3. Registro do **TCLE**.
4. Cadastro na plataforma (integração com e-SUS APS/Território).
5. Definição de protocolo, área de abrangência e parâmetros de monitoramento.

### Fase 2 — Intervenção 1ª etapa (Triagem inicial / Baseline)
1. Aplicação do **IVCF-20** (instrumento validado).
2. Coleta de sinais vitais por **IoT** + formulário digital.
3. Transmissão/sincronização (suporta **offline**).
4. Processamento por IA → escore, **classificação de risco** e *baseline*.
5. **Gateway de risco**: Robusto / Risco de fragilização / Frágil.
6. Geração de alertas (crítico/prioritário/cuidado/informativo) se dados alterados.

### Fase 3 — Intervenção 2ª etapa (Sentinel loop)
1. Coletas periódicas conforme a frequência por risco (ver Decisão).
2. Reanálise por IA → **reclassificação** de risco.
3. Atualização do monitoramento; geração de novos alertas.

### Fase 4 — Pós-Intervenção (Resposta e Gestão do Cuidado)
1. Integração e classificação por risco/prioridade.
2. Saídas: mapa de risco georreferenciado; lista de prioridades; dashboard longitudinal; suporte à decisão.
3. Notificação em tempo real às equipes.
4. Sugestão de agendamento por risco/alerta; **plano de cuidado** baseado em dados.
5. Supervisão contínua pela Equipe de Monitoramento (telessaúde).

### Tarefas × dados × decisões
| Tarefa | Dados (comp.5) | Decisão (comp.6) |
|---|---|---|
| Triagem IVCF-20 | itens q01–q20 | escore + faixa de risco |
| Coleta IoT | PA, FC, SpO2, peso, IMC, temperatura | gatilhos de alerta |
| Reavaliação periódica | escore IVCF-20, sinais vitais | periodicidade por risco |

*Fonte: Protocolo mareIA WP1, §6 (p.9–10), Anexo 15.1/15.2 (fluxogramas).*
