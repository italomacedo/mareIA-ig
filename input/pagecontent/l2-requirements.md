Componente 8 do DAK — *Functional and non-functional requirements*. Fonte: `l2/_l1-facts.yaml`.
No L3: `CapabilityStatement` (capacidades FHIR) e `Requirements`.

### Requisitos Funcionais

| Id | Requisito | Fonte |
|---|---|---|
| RF-01 | Cadastro de paciente apenas com TCLE registrado | p.9, p.19 |
| RF-02 | Coleta por formulário digital e dispositivos IoT via app | p.7,10,12 |
| RF-03 | Operação **offline** com sincronização automática ao reconectar | p.10,11 |
| RF-04 | Cálculo automático do escore IVCF-20 e do IMC | p.11, Anexo 15.6.3 |
| RF-05 | Estratificação de risco em 3 faixas e geração/classificação de alertas | p.10,13 |
| RF-06 | Cálculo da próxima coleta conforme risco/alertas | p.16 |
| RF-07 | Dashboard longitudinal; mapa de risco georreferenciado; lista de prioridades | p.7,10 |
| RF-08 | Notificação em tempo real às equipes de cuidado e monitoramento | p.10,14 |
| RF-09 | Telessaúde (chat assíncrono) e conteúdo educativo | p.7 |

### Requisitos Não-Funcionais

| Id | Requisito | Fonte |
|---|---|---|
| RNF-01 | Interoperabilidade **HL7 FHIR R4**; vocabulários **CID-10** e **LOINC** | p.17 |
| RNF-02 | Envio à **RNDS** (Portaria GM/MS nº 1.434/2020); integração e-SUS APS/Território | p.17 |
| RNF-03 | **LGPD**: consentimento específico, minimização, criptografia, log de auditoria, TLS | p.17,19 |
| RNF-04 | Dashboard gestor com **dados desidentificados** (Art. 12 LGPD) | p.17,19 |
| RNF-05 | IoT via **BLE**; dispositivos certificados **ANVISA** | p.17 |
| RNF-06 | Desempenho em territórios com conectividade precária | p.10,11 |

*Fonte: Protocolo mareIA WP1, §5, §12, §13.*
