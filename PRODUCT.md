# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Users

Idosos em situação de exclusão digital, acessando o site sozinhos (uso individual, sem apoio presencial estruturado ou mediação familiar assumida como padrão). É o público que mais sofre com a exigência crescente de tecnologia para acessar serviços essenciais (bancos, saúde, benefícios sociais, comunicação com a família).

## Product Purpose

O Conecta Saber Digital é uma plataforma de ensino de letramento digital: uma trilha de aulas em módulos (Windows, Google Workspace, Open Source, Inteligência Artificial, Cibersegurança, Cidadania Digital) que ensina, do zero, a usar computador e internet com confiança. Sucesso é o visitante idoso conseguir acompanhar uma aula sozinho, do início ao fim, sem travar na navegação do próprio site.

## Positioning

Projeto de extensão universitária (IFNMG — Instituto Federal do Norte de Minas Gerais) com conteúdo gratuito e aberto (licença CC BY-NC), pensado especificamente para quem está começando do zero — não é um curso de TI genérico adaptado, é desenhado para o público idoso desde a concepção.

## Operating Context

Site estático gerado com Hugo, hospedado em VPS próprio (Oracle Cloud) atrás de Traefik. Conteúdo em Markdown, organizado por módulo/tópico com navegação lateral (sidebar) nas páginas de aula. Inscrições para turmas abertas periodicamente via formulário externo (Google Forms), divulgadas na home.

## Capabilities and Constraints

- Site 100% estático: sem contas de usuário, login ou acompanhamento de progresso persistente.
- Conteúdo versionado como código (Docs-as-Code); qualquer alteração de aula passa por commit no repositório.
- Deploy automatizado via GitHub Actions + runner self-hosted no próprio VPS.
- Sem processo de pagamento ou comércio (uso não-comercial, CC BY-NC).

## Brand Commitments

- Nome: **Conecta Saber Digital**.
- Identidade visual já estabelecida: paleta verde-floresta (`--forest`, `--forest-deep`, `--leaf`, `--mint`) sobre fundo creme/paper, tipografia sans-serif (Trebuchet MS/Segoe UI). Logo e ícone existentes em `site/static/img/`.
- Tom institucional e acolhedor, evitando jargão técnico nas páginas voltadas ao público final (diferente do README, que fala com avaliadores/recrutadores).

## Evidence on Hand

- Conteúdo real de aulas já publicado para os 6 módulos (`site/content/`).
- Página "Sobre o Projeto" (`site/content/sobre.md`) com propósito, motivação e equipe.
- Equipe executora nomeada com responsabilidades por módulo (ver `site/content/sobre.md` e `README.md`).
- Site publicado em produção: https://conectasaberdigital.duckdns.org/

## Product Principles

1. O site precisa ser navegável por alguém com pouquíssima familiaridade digital — essa é a barreira que o próprio produto existe para superar, então a interface não pode reproduzi-la.
2. Conteúdo aberto e replicável por design: nenhuma decisão de produto deve depender de conta, login ou infraestrutura paga do lado do visitante.
3. É extensão universitária, não produto comercial: linguagem acolhedora, sem pressão de venda, mesmo na seção de inscrições.
4. Identidade visual (verde-floresta, tipografia atual) é herdada e deve ser preservada em extensões, não redesenhada por padrão.

## Accessibility & Inclusion

Sem requisito formal definido ainda (ex: tamanho mínimo de fonte, padrão de contraste). Dado o público idoso com baixa familiaridade digital, isso é uma lacuna conhecida e deliberadamente em aberto — decisão de acessibilidade específica fica para trabalho de design futuro, não deve ser assumida ou inventada.
