Componente 2 do DAK — *Generic personas*. Os ids reservados abaixo mapeiam para `ActorDefinition`
quando o IG migrar para FHIR R5 (ver ADR-0006; nesta fase R4 as personas ficam no L2).

#### Diagrama de atores (PlantUML)

{% include actors-atento60.svg %}
<br clear="all"/>

| Id (ActorDefinition) | Persona | Acesso | Função no fluxo |
|---|---|---|---|
| `patient-elderly` | **Pessoa idosa** (pessoa cuidada) | App móvel (online/offline) | Autorrelato de sintomas; recebe orientações e conteúdo educativo. |
| `chw` | **Agente Comunitário de Saúde** (Agente de Coleta) | App móvel (online/offline) | Verifica elegibilidade; garante TCLE; cadastra; aplica IVCF-20 e opera dispositivos IoT; registra dados; comunica intercorrências. |
| `care-team` | **Equipe de Gestão do Cuidado** (ESF/USF) | Web (dashboard) / app profissional | Revisa classificação e alertas; prioriza ações; decide conduta; constrói o plano de cuidado. |
| `monitoring-team` | **Equipe de Gestão do Monitoramento** | Web (dashboard de gestão clínica) | Supervisiona a aplicação do protocolo; apoia clinicamente a equipe de cuidado via telessaúde. |
| `facility-manager` | **Gestor da unidade de saúde** | Web (dashboard gestor) | Monitoramento do território; priorização; relatórios gerenciais — **dados desidentificados**. |

### Notas
- No ATENTO 60+, o **Agente de Coleta é o ACS** vinculado à USF, com apoio da equipe
  multiprofissional da ESF (p.11).
- O gestor acessa apenas dados desidentificados, conforme Art. 12 da LGPD (p.17).

*Fonte: Protocolo mareIA WP1, §5 (p.7–8), §7.1 (p.11).*
