Componente 3 do DAK — *User scenarios*. Narrativas curtas por persona, cobrindo as 4 macrofases.

### Cenário A — Entrada e cadastro (Pré-Intervenção)
**Como** Equipe de Gestão do Cuidado, **identifico** uma pessoa idosa já acompanhada na USF que
atende aos critérios de elegibilidade, **para** incluí-la no telemonitoramento. O **ACS** confirma a
elegibilidade, registra o **TCLE** e cadastra a pessoa no app (módulo de Coleta e Processamento).

### Cenário B — Triagem inicial (Intervenção 1ª etapa)
**Como** ACS, **aplico** o **IVCF-20** e **coleto** sinais vitais por dispositivos IoT (PA, FC, SpO2,
peso, estatura→IMC, temperatura), **para** gerar a *linha de base* da pessoa. A plataforma calcula o
escore, **classifica o risco** em três faixas e dispara **alertas críticos** se houver dados alterados.
Em área sem conectividade, opero **offline** e sincronizo ao reconectar.

### Cenário C — Monitoramento contínuo (Intervenção 2ª etapa / Sentinel loop)
**Como** pessoa idosa/cuidador, **registro** sintomas e **realizo** coletas periódicas conforme a
frequência definida pelo risco, **para** manter o acompanhamento. A IA **reanalisa** e **reclassifica**
o risco, gerando novos alertas quando necessário.

### Cenário D — Resposta clínica (Pós-Intervenção)
**Como** Equipe de Gestão do Cuidado, **recebo** notificações em tempo real, **consulto** o dashboard
longitudinal, a **lista de prioridades** e o **mapa de risco georreferenciado**, **para** priorizar
atendimentos, ajustar a agenda e construir o plano de cuidado. **Como** Equipe de Monitoramento,
**supervisiono** a aplicação do protocolo e **apoio** clinicamente a equipe via telessaúde.

*Fonte: Protocolo mareIA WP1, §6 (p.9–10).*
