---
target: site/themes/ConectaSaberDigital/layouts (homepage, aula, sobre)
total_score: 15
max_score: 28
na_heuristics: 7,9,10
p0_count: 2
p1_count: 2
timestamp: 2026-08-25T12-00-24Z
slug: es-conectasaberdigital-layouts-homepage-aula-sobre
---
## Design Health Score

| # | Heuristic | Score | Key Issue |
|---|-----------|-------|-----------|
| 1 | Visibility of System Status | 1 | Nenhum indicador de "onde estou" na sidebar/header |
| 2 | Match System / Real World | 3 | Português claro; glifos `☰`/`‹` sem texto |
| 3 | User Control and Freedom | 2 | Sem breadcrumb, só botão voltar do navegador |
| 4 | Consistency and Standards | 2 | `.btn`/`.module-card` sem `:hover`/`:focus`, `.footer-nav-btn` tem |
| 5 | Error Prevention | 2 | Link externo de inscrição sem aviso visual |
| 6 | Recognition Rather Than Recall | 1 | Nenhuma marcação de posição atual |
| 7 | Flexibility and Efficiency | n/a | Não aplicável a site estático de ensino |
| 8 | Aesthetic and Minimalist Design | 4 | Disciplinado, um só acento de cor |
| 9 | Error Recovery | n/a | Sem estados de erro nos templates revisados |
| 10 | Help and Documentation | n/a | O site é o próprio material didático |
| **Total** | | **15/28** | **Acceptable (54%)** |

## Design Specificity Verdict
Visual system é autoral (regra de fonte única, um só acento, sem mascotes). Camada de interação usa padrões genéricos (details/summary, hover-only affordance) não adaptados ao público. Detector rodou DEGRADED (regex fallback, sem css-select/contraste) — 0 findings em 4 execuções, não deve ser lido como "limpo".

## Priority Issues
- [P0] Nenhum :hover/:focus em .btn/.module-card — sem confirmação visual de clique
- [P0] Nenhum indicador "você está aqui" na sidebar/header
- [P1] Toggle da sidebar só com ícone, sem rótulo de texto
- [P1] Corpo de texto de aula em 1.04rem, pequeno pro público
- [P2] Grid de 6 módulos indiferenciados como primeira decisão pós-hero

## Persona Red Flags
Jordan (iniciante): 3 CTAs competindo no hero, sem indicação de ordem no grid de módulos, sidebar details sem estado ativo.
Elena (baixa visão/tremor, 74): toggle 36px abaixo do alvo de toque de 44px; hover-only affordance invisível em touch/motor.

## Minor Observations
- topico-01.md com conteúdo placeholder ("Windows" só)
- Links externos (rodapé, inscrição) sem aviso de "abre em nova aba"
- Prazo de inscrição no hero contradiz tom "sem pressão" do PRODUCT.md

## Questions to Consider
- Details/summary exige familiaridade que o público, por definição, não tem — é o padrão certo?
- Prazo de inscrição na primeira tela serve ao aprendiz ou às métricas do programa?
