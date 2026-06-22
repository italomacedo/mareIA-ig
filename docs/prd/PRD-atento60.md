# PRD — IG ATENTO 60+ (mareIA / WHO SMART Guidelines)

- **Produto:** Implementation Guide FHIR R4 da linha de cuidado ATENTO 60+.
- **Versão:** 0.1.0 (WP1) · **Status:** draft · **Data:** 2026-06
- **Fonte L1:** `sources/Protocolo_Clinico_Geral_mareIA_WP1.pdf`

## 1. Problema
O SUS precisa de cuidado contínuo e equitativo à **pessoa idosa** na APS, em territórios de
difícil acesso. A mareIA propõe telemonitoramento ativo com IA. Para ser interoperável
(RNDS/SUS Digital) e auditável, a diretriz clínica precisa ser convertida da narrativa (L1) para
artefatos estruturados (L2) e máquina-legíveis (L3) segundo o WHO SMART Guidelines.

## 2. Objetivo
Entregar um IG que represente fielmente o protocolo ATENTO 60+: cadastro → triagem com **IVCF-20**
→ monitoramento contínuo (*Sentinel loop*) → resposta clínica, com estratificação de risco,
geração de alertas e periodicidade de monitoramento, em FHIR R4.

## 3. Escopo
**Inclui:** pathway ATENTO 60+ (fluxo geral aplicado ao idoso), IVCF-20 completo, sinais vitais
por IoT, lógica de risco/alertas, periodicidade, indicadores, requisitos e interoperabilidade.
**Exclui:** demais pathways (repos próprios), L4/L5, integração executável real com e-SUS/RNDS,
módulos de Educação em Saúde e Telessaúde além do que toca o fluxo de monitoramento.

## 4. Personas (resumo — ver L2 §2)
Pessoa idosa monitorada · Agente Comunitário de Saúde (coleta) · Equipe de Gestão do Cuidado (ESF)
· Equipe de Gestão do Monitoramento · Gestor da unidade.

## 5. Requisitos-chave (ver L2 §8)
- **RF:** coleta offline-first com sincronização; cálculo de escore IVCF-20; estratificação em
  3 faixas; disparo de alertas; agenda de reavaliação por risco; dashboard longitudinal.
- **RNF:** FHIR R4; envio à RNDS (Portaria GM/MS 1.434/2020); LGPD (dados sensíveis, minimização,
  criptografia, auditoria); CID-10/LOINC; IoT via BLE com dispositivos ANVISA.

## 6. Critérios de aceite
1. `sushi .` compila com **0 erros**.
2. IG Publisher gera site com 0 erros de QA.
3. `Questionnaire` IVCF-20 com 20 itens e escore calculado renderiza corretamente.
4. Lógica de decisão estratifica: escore 0–6 → Robusto; 7–14 → Risco de fragilização; ≥15 → Frágil
   (faixas conforme L1; pendência de confirmação em ADR-0004).
5. Pelo menos 1 `Measure` por indicador de processo do protocolo.
6. Rastreabilidade L3→L1 presente em cada artefato.

## 7. Riscos / itens abertos
- Periodicidade x risco aparenta inversão no L1 (ADR-0005).
- Faixas/peso de itens do IVCF-20 a confirmar (ADR-0004).
- Disponibilidade de Java para o IG Publisher no ambiente de build.
