# Conecta Saber Digital

Projeto de extensão universitária que leva letramento digital a quem mais precisa dele.

## Sobre o Projeto

O **Conecta Saber Digital** é um projeto de extensão do **IFNMG (Instituto Federal do Norte de Minas Gerais)** que enfrenta o analfabetismo digital, com foco prioritário na população idosa — o público que mais sofre com a exclusão em um mundo cada vez mais dependente de tecnologia.

A solução é uma trilha de aprendizagem estruturada em módulos (Windows, Google Workspace, Open Source, Inteligência Artificial, Cibersegurança e Cidadania Digital), construída por uma equipe multidisciplinar que combina desenvolvimento técnico e produção de conteúdo pedagógico. O objetivo não é apenas ensinar a operar um computador, mas formar cidadania digital.

O projeto é **open source** por escolha: o material é público e replicável, para que outras iniciativas de extensão e comunidades possam reaproveitá-lo. Toda a infraestrutura e documentação técnica são geridas pela equipe executora seguindo a cultura **Docs-as-Code**, com metodologias ágeis e automação DevOps.

## Site Publicado

O material está disponível em: **[conectasaberdigital.duckdns.org](https://conectasaberdigital.duckdns.org/)**

## Estrutura do Repositório

    /
    ├── .github/workflows/       # Esteiras de automação CI/CD (GitHub Actions)
    ├── infra/                   # Arquivos Docker, configuração do Traefik e scripts de deploy
    ├── docs/                    # Documentação interna da equipe (Não é o material do público)
    └── site/                    # Código-fonte do Hugo e Playbooks (Markdown)

## Stack Tecnológica

*   **Site:** Hugo (gerador de site estático) + Markdown
*   **Automação (CI/CD):** GitHub Actions
*   **Hospedagem:** VPS Oracle Cloud (Always Free Tier) + Docker + Traefik
*   **Gestão Ágil:** OpenProject (self-hosted)

## Processo e Metodologia

O projeto adota a cultura **Docs-as-Code**: playbooks e conteúdo pedagógico são versionados como código, em Markdown, passando pelo mesmo fluxo de revisão e histórico do restante do repositório. A gestão do trabalho segue metodologia ágil, com backlog e acompanhamento em um board OpenProject self-hosted.

A automação do site é feita via **GitHub Actions**:

*   **Integração contínua:** a cada pull request, um workflow valida se o `hugo build` do conteúdo em `site/` completa sem erros, evitando que quebras cheguem à `main`.
*   **Entrega contínua:** a cada push/merge na `main`, um runner self-hosted instalado no próprio VPS atualiza o código-fonte (`git pull`) na pasta servida pelo container Hugo. O Traefik, atuando como proxy reverso, mantém o roteamento e o TLS do domínio publicado sem necessidade de intervenção manual.

## Equipe Executora

*   **João Artur Ferreira Passos** — Playbook do módulo de Cibersegurança; infraestrutura do site e backend
*   **Maria Rita Ferreira Coelho** — Frontend e estilização geral do projeto; Playbook do módulo de Inteligência Artificial
*   **Ana Clara Ferreira** — Apoio na formação do chat no frontend; Playbook do módulo de Google Workspace
*   **Bismark** — Playbook do módulo de Windows
*   **Júnior** — Playbook do módulo de Open Source
*   **Marcelo** — Playbook do módulo de Cidadania Digital

## Licença

Este projeto é distribuído sob a licença **[Creative Commons Atribuição-NãoComercial (CC BY-NC)](https://creativecommons.org/licenses/by-nc/4.0/deed.pt_BR)**. Veja o texto completo em [LICENSE.md](LICENSE.md).
