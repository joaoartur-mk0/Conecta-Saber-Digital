# Padrões de Formatação Markdown (Playbooks)

Este documento estabelece as regras de formatação para a criação do material didático (Playbooks) que será disponibilizado para a comunidade. A padronização é fundamental para garantir uma leitura clara e acessível na plataforma final.

## Cabeçalho do Arquivo (Front Matter)

Como utilizamos o framework Hugo, todo arquivo Markdown deve iniciar obrigatoriamente com o bloco de configuração abaixo. Ele define o título da página e o status de publicação.

```yaml
---
title: "Nome do Módulo ou Aula"
date: 2026-05-11
draft: true
---
```

Nota: Mantenha `draft: true` enquanto estiver trabalhando no arquivo. Altere para `false` apenas quando o conteúdo estiver revisado e pronto para publicação.

## Estrutura de Títulos

Utilize a hierarquia correta para organizar o conteúdo. Evite pular níveis de título.

- `# Título Principal` (Evite usar no corpo do texto, pois o Hugo já gera o título automaticamente a partir do Front Matter).
- `## Subtítulo de Seção` (Use para separar os tópicos principais da aula).
- `### Tópico Secundário` (Use para subdivisões ou passos específicos dentro de uma seção).

## Formatação de Texto e Ênfase

A escrita deve ser simples, didática e livre de jargões não explicados. Para destacar elementos na tela ou termos importantes:

- **Negrito**: Utilize para dar ênfase em termos essenciais, nomes de menus ou botões que o usuário deve clicar. Exemplo: Clique em **Painel de Controle**. (Sintaxe: `**texto**`)
- *Itálico*: Utilize para palavras em idiomas estrangeiros. Exemplo: O termo *phishing*. (Sintaxe: `*texto*`)

## Listas de Instruções

Para enumerar passos de um tutorial ou laboratório prático, utilize listas numeradas. Para itens sem ordem cronológica obrigatória, utilize listas com marcadores.

**Lista numerada (Passo a passo):**
1. Abra o navegador de internet.
2. Acesse o site do serviço selecionado.
3. Preencha os dados solicitados.

**Lista com marcadores:**
- Documento de identificação.
- Endereço de e-mail válido.
- Número de telefone celular.

## Inserção de Imagens e Links

O uso de imagens é obrigatório para facilitar o entendimento da comunidade. Toda imagem inserida deve conter um texto alternativo estruturado para garantir a acessibilidade (leitores de tela).

**Sintaxe para Imagens:**
`![Descrição clara da imagem para o leitor de tela](/caminho/interno/da/imagem.png)`

**Sintaxe para Links:**
`[Texto descritivo do destino](https://www.site-destino.gov.br)`
Nunca insira o link cru diretamente no texto (exemplo: evite deixar apenas "https://..."). Sempre utilize um texto descritivo.
