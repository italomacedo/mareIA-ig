Componente 5 do DAK — *Core data elements*. Fonte estruturada: `l2/5-data-dictionary.csv`.

> **Codificação.** Sinais vitais usam **LOINC** (código oficial). Os itens do IVCF-20 são itens de
> questionário **sem LOINC consagrado** → usam o CodeSystem local `atento60-ivcf-item` (coluna
> *Código local*). Mapeamento LOINC por item do IVCF-20 é item aberto (ver ADR-0004 no repositório).

### IVCF-20 — itens, pesos e código

> **REVISAR (ADR-0004):** escore total e faixas a confirmar com a equipe clínica.

| Item | Seção | Peso (Sim) | Código local (`atento60-ivcf-item`) | LOINC |
|---|---|---|---|---|
| 1. Idade | Idade | 60–74=0 · 75–84=1 · ≥85=3 | `q01` | — |
| 2. Autopercepção da saúde | Autopercepção | regular/ruim=1 | `q02` | — |
| 3. Deixou de fazer compras | AVD Instrumental | 4 (grupo 3–5 teto 4) | `q03` | — |
| 4. Deixou de controlar dinheiro | AVD Instrumental | 4 (teto 4) | `q04` | — |
| 5. Deixou trabalhos domésticos | AVD Instrumental | 4 (teto 4) | `q05` | — |
| 6. Deixou de tomar banho sozinho | AVD Básica | 6 | `q06` | — |
| 7. Está ficando esquecido | Cognição | 1 | `q07` | — |
| 8. Esquecimento piorando | Cognição | 1 | `q08` | — |
| 9. Esquecimento impede cotidiano | Cognição | 2 | `q09` | — |
| 10. Desânimo/tristeza | Humor | 2 | `q10` | — |
| 11. Perda de interesse/prazer | Humor | 2 | `q11` | — |
| 12. Incapaz de elevar braços | Mobilidade (preensão) | 1 | `q12` | — |
| 13. Incapaz de segurar objetos | Mobilidade (preensão) | 1 | `q13` | — |
| 14. Perda peso/IMC<22/panturrilha<31/marcha>5s | Mobilidade (aeróbica) | 2 (teto 2) | `q14` | — |
| 15. Dificuldade para caminhar | Mobilidade (marcha) | 2 | `q15` | — |
| 16. Duas ou mais quedas no ano | Mobilidade (marcha) | 2 | `q16` | — |
| 17. Perde urina/fezes | Continência | 2 | `q17` | — |
| 18. Problemas de visão | Comunicação | 2 | `q18` | — |
| 19. Problemas de audição | Comunicação | 2 | `q19` | — |
| 20. Polipatologia/polifarmácia/internação <6m | Comorbidades múltiplas | 4 (teto 4) | `q20` | — |

**Escore e faixa** (códigos locais): escore total → `atento60-obs-code#ivcf-20-score`;
faixa de risco → `atento60-obs-code#ivcf-20-faixa` com valor em `atento60-ivcf-risk`
(`robusto` 0–6 · `risco-fragilizacao` 7–14 · `fragil` ≥15).

### Sinais vitais (IoT) — codificação LOINC

| Dado | Unidade | Sistema | Código (LOINC) | Dispositivo |
|---|---|---|---|---|
| PA sistólica | mmHg | LOINC | 8480-6 | Esfigmomanômetro digital |
| PA diastólica | mmHg | LOINC | 8462-4 | Esfigmomanômetro digital |
| Glicemia capilar | mg/dL | LOINC | 2339-0 | Glicosímetro |
| SpO₂ | % | LOINC | 59408-5 | Oxímetro de pulso |
| Frequência cardíaca | /min | LOINC | 8867-4 | Oxímetro de pulso |
| Peso | kg | LOINC | 29463-7 | Balança digital |
| Estatura | cm | LOINC | 8302-2 | Estadiômetro |
| IMC (derivado) | kg/m² | LOINC | 39156-5 | — |
| Temperatura | °C | LOINC | 8310-5 | Termômetro |

*Fonte: Protocolo mareIA WP1, §7.2–7.3 (p.11–12), Anexo 15.6.3.*
