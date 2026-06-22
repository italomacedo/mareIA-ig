# ADR-0004 — Codificação e faixas do IVCF-20

- **Status:** PROPOSTO — aguarda confirmação da equipe clínica
- **Bloqueia:** componente L2 §6 (decisão) e Questionnaire L3

## Contexto
O Anexo 15.6.3 do protocolo transcreve o IVCF-20 (20 questões, pesos por item). O texto traz:
- Faixas de risco: **0–6 Robusto**, **7–14 Risco de fragilização**, **≥15 Frágil**.
- Um cabeçalho "Pontuação (FINAL 40)" sugerindo escore máximo 40, porém a soma dos pesos máximos
  por item transcritos parece exceder/divergir de 40 (itens AVD com teto, mobilidade, comorbidades).
- O IVCF-20 publicado (Moraes et al.) usa, na versão original, faixas comumente citadas como
  0–6 / 7–14 / ≥15 sobre um total de 40 pontos.

## Questões abertas (não decidir sozinho)
1. Confirmar **escore total = 40** e os pesos/tetos exatos por item (especialmente AVD instrumental
   teto 4, mobilidade aeróbica/muscular, comorbidades múltiplas teto 4).
2. Confirmar as **3 faixas** e os rótulos (Robusto / Risco de fragilização / Frágil).
3. Definir codificação: usar CodeSystem **local** `atento60-ivcf-risk` (proposto) por não haver
   código LOINC/SNOMED consagrado para as faixas; itens individuais sem código padrão → CodeSystem
   local `atento60-ivcf-item`.

## Decisão provisória (para destravar L2/L3, marcada como tentativa)
Codificar **como escrito no protocolo**: total 40, faixas 0–6 / 7–14 / ≥15, com `// REVISAR`
nos artefatos e este ADR referenciado. Reabrir como ADR-0004a se a equipe ajustar.
