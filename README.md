# VS Code --- Guia Prático: Primeiro Projeto Web

------------------------------------------------------------------------

## Sumário

-   [1. Visão geral](#1-visão-geral)
-   [2. Estrutura do projeto](#2-estrutura-do-projeto)
-   [3. Criando o `index.html`](#3-criando-o-indexhtml)
-   [4. Estrutura semântica do HTML](#4-estrutura-semântica-do-html)
-   [5. Criando o `style.css`](#5-criando-o-stylecss)
-   [6. Resultado visual](#6-resultado-visual)
-   [7. Extensões do VS Code](#7-extensões-do-vs-code)
-   [8. Prettier e formatação
    automática](#8-prettier-e-formatação-automática)
-   [9. Salvamento automático](#9-salvamento-automático)
-   [10. Live Server](#10-live-server)
-   [11. Terminal integrado](#11-terminal-integrado)
-   [12. JavaScript e Run and Debug](#12-javascript-e-run-and-debug)
-   [13. Controle de versão e GitHub](#13-controle-de-versão-e-github)
-   [14. Conceitos técnicos
    essenciais](#14-conceitos-técnicos-essenciais)
-   [15. Fluxo de trabalho
    recomendado](#15-fluxo-de-trabalho-recomendado)
-   [16. Checklist](#16-checklist)
-   [17. Glossário](#17-glossário)

------------------------------------------------------------------------

# 1. Visão geral

O vídeo apresenta um fluxo introdutório para começar um projeto web no
**Visual Studio Code (VS Code)**.

O projeto demonstrado é chamado de `my-first-project` e contém três
arquivos principais:

``` text
my-first-project/
├── index.html
├── style.css
└── app.js
```

A ideia central é separar responsabilidades:

  Arquivo        Responsabilidade
  -------------- -----------------------------------
  `index.html`   Estrutura e conteúdo da página
  `style.css`    Aparência e apresentação
  `app.js`       Comportamento e lógica JavaScript

Essa separação é uma prática fundamental no desenvolvimento front-end.

------------------------------------------------------------------------

# 2. Estrutura do projeto

O terminal mostrado no vídeo apresenta comandos equivalentes a:

``` bash
pwd
ls
```

### `pwd`

Mostra o diretório atual:

``` bash
pwd
```

Exemplo exibido:

``` text
/Users/sahand/Desktop/my-first-project
```

### `ls`

Lista os arquivos e diretórios do local atual:

``` bash
ls
```

No projeto aparecem:

``` text
app.js
index.html
style.css
```

> Em Windows, os comandos e a apresentação do caminho podem variar
> conforme o shell utilizado, como PowerShell, Prompt de Comando ou Git
> Bash.

------------------------------------------------------------------------

# 3. Criando o `index.html`

O arquivo HTML demonstrado contém a estrutura básica de um documento
HTML5.

Uma versão organizada do código apresentado é:

``` html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>My First Project</title>

    <link rel="stylesheet" href="style.css">
</head>

<body>
    <h1>My First Project</h1>

    <p>I am learning VS Code</p>

    <button>Click Me</button>
</body>
</html>
```

### Tradução do conteúdo textual

  Original                  Português Brasileiro
  ------------------------- --------------------------
  `My First Project`        Meu Primeiro Projeto
  `I am learning VS Code`   Estou aprendendo VS Code
  `Click Me`                Clique em Mim

Se o objetivo for criar uma versão em português da página:

``` html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Meu Primeiro Projeto</title>

    <link rel="stylesheet" href="style.css">
</head>

<body>
    <h1>Meu Primeiro Projeto</h1>

    <p>Estou aprendendo VS Code</p>

    <button>Clique em Mim</button>
</body>
</html>
```

------------------------------------------------------------------------

# 4. Estrutura semântica do HTML

## `<!DOCTYPE html>`

Declara que o documento utiliza HTML5.

``` html
<!DOCTYPE html>
```

## `<html>`

É o elemento raiz do documento.

``` html
<html lang="pt-BR">
```

O atributo `lang` informa o idioma principal da página.

Para português brasileiro:

``` html
lang="pt-BR"
```

## `<head>`

Contém informações de configuração e metadados da página.

``` html
<head>
    ...
</head>
```

## `<meta charset="UTF-8">`

Define a codificação de caracteres.

``` html
<meta charset="UTF-8">
```

UTF-8 permite representar corretamente grande parte dos caracteres
utilizados em português, incluindo:

``` text
á ã ç ê õ ú
```

## Viewport

``` html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

É importante para a apresentação responsiva em dispositivos móveis.

-   `width=device-width`: utiliza a largura do dispositivo.
-   `initial-scale=1.0`: define a escala inicial.

## `<title>`

Define o título do documento, normalmente exibido na aba do navegador.

``` html
<title>Meu Primeiro Projeto</title>
```

## `<link>`

O vídeo demonstra a associação do HTML com uma folha de estilos externa:

``` html
<link rel="stylesheet" href="style.css">
```

Isso significa que o navegador deve carregar `style.css` como uma folha
de estilos.

## `<body>`

Contém o conteúdo que será renderizado na página.

``` html
<body>
    ...
</body>
```

## `<h1>`

Representa o título principal:

``` html
<h1>Meu Primeiro Projeto</h1>
```

## `<p>`

Representa um parágrafo:

``` html
<p>Estou aprendendo VS Code</p>
```

## `<button>`

Cria um botão:

``` html
<button>Clique em Mim</button>
```

------------------------------------------------------------------------

# 5. Criando o `style.css`

O vídeo demonstra uma folha de estilos semelhante a esta:

``` css
body {
    font-family: Arial, Helvetica, sans-serif;
    padding: 40px;
    background-color: lightgray;
}

button {
    padding: 12px 20px;
    background-color: black;
    color: white;
    border: none;
    border-radius: 10px;
}
```

## Regra `body`

``` css
body {
    font-family: Arial, Helvetica, sans-serif;
    padding: 40px;
    background-color: lightgray;
}
```

### `font-family`

Define a família tipográfica:

``` css
font-family: Arial, Helvetica, sans-serif;
```

O navegador tenta utilizar as fontes na ordem apresentada.

### `padding`

``` css
padding: 40px;
```

Cria espaçamento interno de 40 pixels.

### `background-color`

``` css
background-color: lightgray;
```

Define uma cor de fundo cinza-clara.

------------------------------------------------------------------------

## Regra `button`

``` css
button {
    padding: 12px 20px;
    background-color: black;
    color: white;
    border: none;
    border-radius: 10px;
}
```

### `padding: 12px 20px`

Com dois valores:

``` css
padding: 12px 20px;
```

o primeiro valor corresponde ao espaçamento vertical e o segundo ao
horizontal:

``` text
vertical:   12px
horizontal: 20px
```

### `background-color`

``` css
background-color: black;
```

Define o fundo preto do botão.

### `color`

``` css
color: white;
```

Define a cor do texto como branca.

### `border: none`

``` css
border: none;
```

Remove a borda padrão.

### `border-radius`

``` css
border-radius: 10px;
```

Arredonda os cantos.

------------------------------------------------------------------------

# 6. Resultado visual

A combinação de HTML e CSS produz uma página simples contendo:

1.  Um título principal.
2.  Um parágrafo.
3.  Um botão estilizado.
4.  Fundo em cinza-claro.
5.  Tipografia baseada em Arial.
6.  Espaçamento interno da página.
7.  Botão com fundo preto, texto branco e cantos arredondados.

O botão demonstrado é principalmente um elemento visual. **Não há, no
código exibido, uma ação JavaScript associada a ele.**

Para adicionar comportamento posteriormente, seria necessário
implementar um manipulador de evento em JavaScript.

Exemplo:

``` javascript
const button = document.querySelector("button");

button.addEventListener("click", () => {
    console.log("Botão clicado!");
});
```

------------------------------------------------------------------------

# 7. Extensões do VS Code

O vídeo mostra o Marketplace de extensões do VS Code e apresenta
extensões relacionadas ao desenvolvimento.

Entre as extensões visíveis estão:

-   **Auto Rename Tag**
-   **Prettier - Code formatter**
-   ferramentas relacionadas a React/Redux
-   ferramentas relacionadas a Docker/Dev Containers
-   ferramentas de formatação de JSON, XML e SQL

## Auto Rename Tag

A extensão auxilia na edição de elementos HTML/XML relacionados.

Por exemplo, ao alterar:

``` html
<div>
```

para:

``` html
<section>
```

uma ferramenta desse tipo pode auxiliar na atualização correspondente da
tag de fechamento.

## Prettier

O vídeo utiliza o **Prettier - Code formatter**.

Sua finalidade é aplicar uma formatação consistente ao código.

Exemplo antes da formatação:

``` html
<body><h1>Meu Projeto</h1><p>Texto</p><button>Clique</button></body>
```

Depois da formatação:

``` html
<body>
    <h1>Meu Projeto</h1>
    <p>Texto</p>
    <button>Clique</button>
</body>
```

A formatação melhora a legibilidade, mas não deve ser confundida com
alteração da lógica do programa.

------------------------------------------------------------------------

# 8. Prettier e formatação automática

O vídeo mostra comandos relacionados a:

**Format Document**

Tradução:

> Formatar Documento

Também aparecem opções como:

-   Format Document
-   Format Document (Forced)
-   Format Modified Lines
-   Format Selection

### Formatar documento

Pode ser utilizado para formatar o arquivo inteiro.

### Formatar seleção

Aplica a formatação apenas ao trecho selecionado.

### Format On Save

Nas configurações do VS Code aparece:

> Editor: Format On Save

Tradução:

> Editor: Formatar ao Salvar

Quando configurado, o editor pode executar o formatador ao salvar o
arquivo.

O vídeo também mostra:

> Editor: Default Formatter

Tradução:

> Editor: Formatador Padrão

Essa configuração determina qual formatador será utilizado como padrão.

------------------------------------------------------------------------

# 9. Salvamento automático

Nas configurações aparece:

> Files: Auto Save

Tradução:

> Arquivos: Salvamento Automático

Também é mostrada a opção:

> Files: Auto Save Delay

Tradução:

> Arquivos: Atraso do Salvamento Automático

O VS Code oferece diferentes comportamentos para o salvamento
automático.

Um exemplo é:

``` text
afterDelay
```

Nesse modo, o arquivo é salvo depois de um determinado intervalo.

O salvamento automático pode ser útil durante desenvolvimento, mas deve
ser configurado de acordo com o fluxo de trabalho do projeto.

------------------------------------------------------------------------

# 10. Live Server

O vídeo demonstra o projeto sendo executado localmente e mostra a porta:

``` text
Port: 5500
```

Esse comportamento é característico de uma ferramenta de servidor de
desenvolvimento, como o **Live Server**.

O objetivo é abrir o projeto HTML em um servidor local, por exemplo:

``` text
http://127.0.0.1:5500/
```

ou:

``` text
http://localhost:5500/
```

## Por que usar um servidor local?

Abrir simplesmente:

``` text
file:///...
```

é diferente de executar a aplicação por HTTP.

Um servidor local facilita o desenvolvimento de páginas e aplicações que
dependem de recursos carregados via HTTP.

## Fluxo típico

``` text
VS Code
   │
   ├── index.html
   ├── style.css
   └── app.js
          │
          ▼
   Servidor local
          │
          ▼
     Navegador
```

Ao salvar alterações, ferramentas de desenvolvimento podem atualizar ou
permitir atualizar a página rapidamente.

------------------------------------------------------------------------

# 11. Terminal integrado

O terminal integrado do VS Code é mostrado durante o projeto.

Exemplos:

``` bash
pwd
```

e:

``` bash
ls
```

O terminal permite executar ferramentas diretamente dentro do ambiente
de desenvolvimento.

Exemplos de tarefas comuns:

``` bash
git status
git add .
git commit -m "Primeiro commit"
```

ou, dependendo do ambiente:

``` bash
npm install
npm run dev
```

Esses últimos comandos são exemplos gerais e não significam que tenham
sido executados no vídeo.

------------------------------------------------------------------------

# 12. JavaScript e Run and Debug

O projeto também contém:

``` text
app.js
```

O conteúdo mostrado inclui:

``` javascript
console.log("Hello From VS Code!");
```

Tradução:

``` text
Olá do VS Code!
```

Esse comando envia uma mensagem para o console.

## `console.log()`

``` javascript
console.log("Hello From VS Code!");
```

é uma das formas mais simples de observar valores e mensagens durante o
desenvolvimento.

No navegador, a mensagem normalmente pode ser encontrada no **Console**
das ferramentas de desenvolvedor.

------------------------------------------------------------------------

## Run and Debug

O painel do VS Code apresenta:

> Run and Debug

Tradução:

> Executar e Depurar

O VS Code informa que, para personalizar o processo de execução e
depuração, pode ser criado um arquivo:

``` text
launch.json
```

Esse arquivo é utilizado para configurações de depuração.

O vídeo também mostra a referência ao **JavaScript Debug Terminal**,
destinado à execução e depuração de processos JavaScript/Node.js
iniciados no terminal.

------------------------------------------------------------------------

# 13. Controle de versão e GitHub

O painel **Source Control** aparece no projeto.

Tradução:

> Controle de Código-Fonte

O VS Code informa que a pasta aberta ainda não possui um repositório
Git.

A interface oferece a possibilidade de inicializar um repositório.

## Git

Git é um sistema distribuído de controle de versão.

Depois de inicializar o repositório, o projeto passa a ter um histórico
de alterações.

Fluxo básico:

``` bash
git init
git status
git add .
git commit -m "Primeiro commit"
```

## GitHub

A interface do VS Code também mostra a possibilidade de publicar a pasta
diretamente em um repositório do GitHub.

Um fluxo conceitual é:

``` text
Projeto local
     │
     ▼
Repositório Git
     │
     ▼
Commit
     │
     ▼
GitHub
```

> O vídeo mostra a opção de publicação, mas a existência dessa opção na
> interface não significa que um repositório remoto tenha
> necessariamente sido criado durante toda a demonstração.

------------------------------------------------------------------------

# 14. Conceitos técnicos essenciais

## HTML

HTML define a estrutura do documento.

Exemplo:

``` html
<h1>Título</h1>
<p>Parágrafo</p>
<button>Botão</button>
```

## CSS

CSS define a apresentação.

Exemplo:

``` css
button {
    background-color: black;
    color: white;
}
```

## JavaScript

JavaScript adiciona lógica e comportamento.

Exemplo:

``` javascript
document.querySelector("button").addEventListener("click", () => {
    console.log("Clique!");
});
```

## VS Code

O VS Code funciona como ambiente de desenvolvimento, reunindo:

-   editor de código;
-   terminal;
-   extensões;
-   controle de versão;
-   depuração;
-   gerenciamento de arquivos;
-   integração com ferramentas de desenvolvimento.

------------------------------------------------------------------------

# 15. Fluxo de trabalho recomendado

Um fluxo equivalente ao apresentado pode ser organizado assim:

## Etapa 1 --- Criar a pasta

``` text
my-first-project/
```

## Etapa 2 --- Abrir a pasta no VS Code

Abra a pasta como um workspace.

## Etapa 3 --- Criar os arquivos

``` text
index.html
style.css
app.js
```

## Etapa 4 --- Escrever o HTML

``` html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Meu Primeiro Projeto</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <h1>Meu Primeiro Projeto</h1>
    <p>Estou aprendendo VS Code</p>
    <button>Clique em Mim</button>
</body>
</html>
```

## Etapa 5 --- Adicionar CSS

``` css
body {
    font-family: Arial, Helvetica, sans-serif;
    padding: 40px;
    background-color: lightgray;
}

button {
    padding: 12px 20px;
    background-color: black;
    color: white;
    border: none;
    border-radius: 10px;
}
```

## Etapa 6 --- Adicionar JavaScript

``` javascript
console.log("Olá do VS Code!");
```

## Etapa 7 --- Instalar/configurar ferramentas

Por exemplo:

-   Prettier;
-   Live Server;
-   Auto Rename Tag.

## Etapa 8 --- Formatar o código

Utilize:

``` text
Format Document
```

ou configure:

``` text
Format On Save
```

## Etapa 9 --- Executar localmente

Utilize um servidor local, como o Live Server, e abra a página no
navegador.

## Etapa 10 --- Inspecionar e depurar

Verifique:

-   Console;
-   erros de HTML;
-   erros de JavaScript;
-   estilos CSS;
-   carregamento dos arquivos.

## Etapa 11 --- Versionar

Inicialize o Git e crie commits.

------------------------------------------------------------------------

# 16. Checklist

## Projeto

-   [x] Criar uma pasta de projeto.
-   [x] Abrir a pasta no VS Code.
-   [x] Criar `index.html`.
-   [x] Criar `style.css`.
-   [x] Criar `app.js`.

## HTML

-   [x] Usar `<!DOCTYPE html>`.
-   [x] Definir `lang`.
-   [x] Definir `charset`.
-   [x] Configurar viewport.
-   [x] Definir `<title>`.
-   [x] Vincular o CSS.
-   [x] Criar título.
-   [x] Criar parágrafo.
-   [x] Criar botão.

## CSS

-   [x] Definir fonte.
-   [x] Definir espaçamento.
-   [x] Definir fundo.
-   [x] Estilizar botão.
-   [x] Remover borda.
-   [x] Arredondar os cantos.

## VS Code

-   [x] Explorar extensões.
-   [x] Utilizar Prettier.
-   [x] Conhecer o Format Document.
-   [x] Conhecer Format On Save.
-   [x] Conhecer Auto Save.
-   [x] Utilizar o terminal.
-   [x] Conhecer Source Control.
-   [x] Conhecer Run and Debug.

------------------------------------------------------------------------

# 17. Glossário

  -----------------------------------------------------------------------
  Termo                               Significado
  ----------------------------------- -----------------------------------
  **VS Code**                         Editor de código da Microsoft

  **HTML**                            Linguagem de marcação utilizada
                                      para estruturar documentos web

  **CSS**                             Linguagem de estilos utilizada para
                                      definir a apresentação

  **JavaScript**                      Linguagem de programação utilizada
                                      para comportamento e lógica

  **Workspace**                       Pasta/projeto aberto no VS Code

  **Extension**                       Extensão que adiciona recursos ao
                                      VS Code

  **Prettier**                        Formatador automático de código

  **Live Server**                     Ferramenta para servir arquivos web
                                      localmente durante o
                                      desenvolvimento

  **Terminal**                        Interface de linha de comando

  **Git**                             Sistema de controle de versão

  **GitHub**                          Plataforma para hospedagem e
                                      colaboração em projetos, incluindo
                                      repositórios Git

  **Debug**                           Processo de investigar e corrigir
                                      problemas

  **`launch.json`**                   Arquivo de configuração de
                                      determinadas sessões de
                                      execução/depuração

  **`console.log()`**                 Comando JavaScript utilizado para
                                      registrar informações no console

  **`index.html`**                    Nome convencional para a página
                                      HTML inicial

  **`style.css`**                     Arquivo CSS utilizado no projeto
                                      demonstrado

  **`app.js`**                        Arquivo JavaScript utilizado no
                                      projeto demonstrado
  -----------------------------------------------------------------------

------------------------------------------------------------------------

## Resumo final

O vídeo apresenta um projeto web inicial construído no VS Code,
mostrando a relação entre **HTML, CSS e JavaScript** e, ao mesmo tempo,
introduzindo recursos do próprio editor.

O projeto pode ser entendido como:

``` text
                 PROJETO WEB
                     │
        ┌────────────┼────────────┐
        ▼            ▼            ▼
    index.html   style.css     app.js
        │            │            │
        ▼            ▼            ▼
    Estrutura     Aparência     Lógica
        │            │            │
        └────────────┼────────────┘
                     ▼
                 Navegador
```

A sequência pedagógica apresentada é adequada para compreender o ciclo
inicial de desenvolvimento:

``` text
Criar projeto
     ↓
Escrever HTML
     ↓
Aplicar CSS
     ↓
Adicionar JavaScript
     ↓
Formatar código
     ↓
Executar localmente
     ↓
Testar / depurar
     ↓
Versionar com Git
     ↓
Publicar no GitHub
```

---

**`Informática para Internet`**

O suporte fornecido por corporações permite-nos o desenvolvimento e implementação de programas, projetos e recursos para Eduardo.Inf.Br. Através dessas parcerias é possível que empreendedores e proprietários de pequenas empresas, recebam ampla variedade de conteúdos e ferramentas por meio de sistemas e suporte. "[Eduardo.Inf.Br](https://informatizar.netlify.app/)".

---

<img 
    align="left" 
    alt="HTML"
    title="HTML" 
    width="30px" 
    style="padding-right: 10px;" 
    src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/html5/html5-original.svg" 
/>
<img 
    align="left" 
    alt="CSS" 
    title="CSS"
    width="30px" 
    style="padding-right: 10px;" 
    src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/css3/css3-original.svg" 
/>
<img 
    align="left" 
    alt="JavaScript" 
    title="JavaScript"
    width="30px" 
    style="padding-right: 10px;" 
    src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/javascript/javascript-original.svg" 
/>
<img 
    align="left" 
    alt="Bootstrap"
    title="Bootstrap" 
    width="30px" 
    style="padding-right: 10px;" 
    src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/bootstrap/bootstrap-original.svg" 
/>
<img 
    align="left" 
    alt="Git" 
    title="Git"
    width="30px" 
    style="padding-right: 10px;" 
    src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/git/git-original.svg" 
/>

