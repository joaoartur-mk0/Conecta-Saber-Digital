---
target: site/themes/ConectaSaberDigital/layouts (homepage, aula, sobre)
total_score: 21
max_score: 32
na_heuristics: 7,9
p0_count: 2
p1_count: 1
timestamp: 2026-08-25T13-00-03Z
slug: es-conectasaberdigital-layouts-homepage-aula-sobre
---
## Design Health Score

| # | Heuristic | Score | Key Issue |
|---|-----------|-------|-----------|
| 1 | Visibility of System Status | 3 | active/aria-current na sidebar funcionando |
| 2 | Match System / Real World | 2 | details/summary é idioma de computador pro novato |
| 3 | User Control and Freedom | 2 | Sem "onde estou" fora da sidebar; CTA externo sem volta clara |
| 4 | Consistency and Standards | 3 | Vocabulário consistente nas 3 páginas |
| 5 | Error Prevention | 3 | Ícone de link externo existe, não anunciado a leitor de tela |
| 6 | Recognition Rather Than Recall | 3 | Sidebar visível, nav anterior/próximo evita decorar URL |
| 7 | Flexibility and Efficiency | n/a | Não aplicável |
| 8 | Aesthetic and Minimalist Design | 4 | Densidade baixa mantida |
| 9 | Error Recovery | n/a | Sem formulários no escopo |
| 10 | Help and Documentation | 1 | Zero onboarding/ajuda |
| **Total** | | **21/32** | **Acceptable (66%)** |

## Design Specificity Verdict
Copy e wayfinding autorais (cartão de módulo destacado deliberado). Interação ainda usa details/summary genérico. Detector DEGRADED, 0 findings, valor evidencial fraco (sem parsers instalados).

## Priority Issues
- [P0] Conteúdo de aula placeholder (topico-01.md só "Windows")
- [P0] "Começar agora" e "Comece por aqui" apontam pra destinos diferentes
- [P1] Nenhuma orientação/ajuda em lugar nenhum
- [P2] Prazo de inscrição ainda gera pressão no hero
- [P3] Links externos sem aviso pra leitor de tela (ícone aria-hidden)

## Persona Red Flags
Jordan: incerto entre 3 CTAs no hero, sidebar colapsada sem indicar mais módulos.
Dona Marta (baixa visão/tremor): ícone externo 12px dificil de acertar; toggle com posição absoluta fixa não testada em zoom alto.

## Minor Observations
- Texto justificado pode criar rios de espaçamento
- Links da sidebar sem font-size explícito, possivelmente menor que corpo da aula
- Sem link "pular para o conteúdo"

## Questions to Consider
- Dois CTAs de "comece aqui" — qual é o de verdade?
- Espaço generoso basta como defesa de acessibilidade, ou falta contraste/tamanho mínimo garantidos?
