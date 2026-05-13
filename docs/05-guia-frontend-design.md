# Guia Completo de Frontend e Design (Hugo)

Este documento estabelece o modelo mental, o fluxo de trabalho e as restrições arquiteturais para a criação e modificação da interface visual da plataforma Conecta Saber Digital. O site utiliza o gerador estático Hugo com o tema Hugo Book.

## 1. O Modelo Mental: O que é o Hugo?
Para trabalhar no frontend deste projeto, você deve abandonar a mentalidade de "editar páginas HTML estáticas". O Hugo é um **compilador** (Static Site Generator - SSG). 

Ele pega arquivos de texto (Markdown), injeta-os em esqueletos de interface (Layouts) e compila tudo em um site ultrarrápido.
* **Go Templates:** Você escreverá código HTML padrão, mas injetará lógica e variáveis usando chaves duplas: `{{ }}`. 
* *Exemplo:* Para exibir o título de uma página dentro de uma tag `<h1>`, você não escreve o texto diretamente. Você escreve: `<h1>{{ .Title }}</h1>`. O Hugo preencherá esse espaço durante a compilação.

## 2. A Regra de Ouro da Infraestrutura (Proibição)
O tema do nosso site (`Hugo Book`) está instalado como um *Git Submodule*. Isso significa que ele é um componente de terceiros bloqueado (somente leitura).

**NUNCA edite nenhum arquivo dentro do diretório `site/themes/book/`.**
Qualquer alteração feita diretamente neste diretório será destruída na próxima atualização da infraestrutura e o Git rejeitará seus commits.

## 3. Como Alterar o Visual (A Técnica de "File Shadowing")
O Hugo opera com uma hierarquia estrita de arquivos chamada *File Shadowing* (Sombreamento de Arquivos). Se você criar um arquivo na raiz do seu projeto com o mesmo nome e caminho de um arquivo do tema, o Hugo ignorará o arquivo do tema e usará o seu.

Todo o seu trabalho ocorrerá em apenas duas pastas específicas:

### A. Estilos e CSS (`site/assets/`)
O Hugo possui um sistema chamado *Hugo Pipes* que minifica e compila arquivos de estilo automaticamente. Para mudar cores, fontes ou espaçamentos:
1. Navegue até o diretório `site/assets/` (crie se não existir).
2. Crie um arquivo chamado `_custom.scss`.
3. Escreva seu código CSS ou SCSS neste arquivo. Ele será aplicado por cima do estilo padrão do tema.

*Exemplo de uso no `_custom.scss`:*
```scss
// Mudando a cor de fundo do menu lateral
.book-menu {
    background-color: #1a1a1a;
}
```

### B. Estrutura e HTML (`site/layouts/`)
Se você precisa mudar a estrutura de uma página (ex: alterar o cabeçalho, rodapé ou criar um banner):
1. Abra a pasta proibida do tema (`site/themes/book/layouts/`) **apenas para estudar** como o desenvolvedor original escreveu o código.
2. Encontre o arquivo que deseja alterar (ex: `partials/header.html`).
3. Recrie a **mesma estrutura de pastas** na sua área de trabalho: `site/layouts/partials/`.
4. Copie o arquivo original para a sua pasta e edite a sua cópia local. O Hugo passará a renderizar o seu HTML modificado.

## 4. Fluxo de Trabalho e Testes Locais
Você não precisa instalar Go, Node.js ou o Hugo no seu computador. Nossa infraestrutura é conteinerizada.

Para visualizar suas alterações em tempo real (Hot-Reload):
1. Instale o **Docker Desktop** na sua máquina.
2. Clone o repositório do projeto.
3. Abra o terminal na pasta `infra/hugoserver/` e execute: `docker compose up -d`
4. Abra o navegador em `http://localhost:1313`.
5. Salve qualquer arquivo `.scss` ou `.html`. O navegador será atualizado instantaneamente refletindo seu novo design.

## 5. Fontes Oficiais de Estudo

1. **Introdução aos Go Templates:** Aprenda a usar `if`, loops e variáveis dentro do HTML.
    * [Hugo Docs: Introduction to Go Templates](https://gohugo.io/templates/introduction/)
2. **Templates Base:** Entenda como criar um layout mestre sem duplicar código.
    * [Hugo Docs: Base Templates](https://gohugo.io/templates/base/)
3. **Hugo Asset Pipeline:** Entenda como o processamento de SCSS funciona.
    * [Hugo Docs: Hugo Pipes](https://gohugo.io/hugo-pipes/introduction/)
