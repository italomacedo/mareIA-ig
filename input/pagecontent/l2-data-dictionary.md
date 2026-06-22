Componente 5 do DAK — *Core data elements*. Fonte estruturada: `l2/5-data-dictionary.csv`.

### IVCF-20 — itens e pesos

> **REVISAR (ADR-0004):** escore total e faixas a confirmar com a equipe clínica.

| Item | Seção | Peso (Sim) |
|---|---|---|
| 1. Idade | Idade | 60–74=0 · 75–84=1 · ≥85=3 |
| 2. Autopercepção da saúde | Autopercepção | regular/ruim=1 |
| 3. Deixou de fazer compras | AVD Instrumental | 4 (grupo 3–5 teto 4) |
| 4. Deixou de controlar dinheiro | AVD Instrumental | 4 (teto 4) |
| 5. Deixou trabalhos domésticos | AVD Instrumental | 4 (teto 4) |
| 6. Deixou de tomar banho sozinho | AVD Básica | 6 |
| 7. Está ficando esquecido | Cognição | 1 |
| 8. Esquecimento piorando | Cognição | 1 |
| 9. Esquecimento impede cotidiano | Cognição | 2 |
| 10. Desânimo/tristeza | Humor | 2 |
| 11. Perda de interesse/prazer | Humor | 2 |
| 12. Incapaz de elevar braços | Mobilidade (preensão) | 1 |
| 13. Incapaz de segurar objetos | Mobilidade (preensão) | 1 |
| 14. Perda peso/IMC<22/panturrilha<31/marcha>5s | Mobilidade (aeróbica) | 2 (teto 2) |
| 15. Dificuldade para caminhar | Mobilidade (marcha) | 2 |
| 16. Duas ou mais quedas no ano | Mobilidade (marcha) | 2 |
| 17. Perde urina/fezes | Continência | 2 |
| 18. Problemas de visão | Comunicação | 2 |
| 19. Problemas de audição | Comunicação | 2 |
| 20. Polipatologia/polifarmácia/internação <6m | Comorbidades múltiplas | 4 (teto 4) |

**Escore total** → faixa: 0–6 *Robusto* · 7–14 *Risco de fragilização* · ≥15 *Frágil*.

### Sinais vitais (IoT) — codificação LOINC

| Dado | Unidade | LOINC | Dispositivo |
|---|---|---|---|
| PA sistólica | mmHg | 8480-6 | Esfigmomanômetro digital |
| PA diastólica | mmHg | 8462-4 | Esfigmomanômetro digital |
| Glicemia capilar | mg/dL | 2339-0 | Glicosímetro |
| SpO₂ | % | 59408-5 | Oxímetro de pulso |
| Frequência cardíaca | /min | 8867-4 | Oxímetro de pulso |
| Peso | kg | 29463-7 | Balança digital |
| Estatura | cm | 8302-2 | Estadiômetro |
| IMC (derivado) | kg/m² | 39156-5 | — |
| Temperatura | °C | 8310-5 | Termômetro |

*Fonte: Protocolo mareIA WP1, §7.2–7.3 (p.11–12), Anexo 15.6.3.*
