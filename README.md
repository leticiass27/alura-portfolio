# HTML e CSS

## Ambientes de desenvolvimento, estrutura de arquivos e tags

- É uma boa prática termos pastas e subpastas que explicitem e organizem os arquivos de código de forma lógica.
- Nem sempre os projetos terão apenas dois ou três arquivos, a depender do nível de complexidade, podem chegar na casa das centenas de arquivos. Portanto, é uma boa prática separar arquivos por categorias claras e objetivas fazendo uso de pastas e subpastas.
- Por padrão o arquivo principal html é chamado "index.html". O termo “index” significa “índice”, pois esse arquivo será a página principal, onde irá conter os links que redirecionam para as outras páginas do seu projeto. Sendo assim, esse nome facilita para que este arquivo seja reconhecido como “padrão” dentro de sua pasta e será a primeira página carregada sempre que seu projeto for aberto.
- Geralmente um projeto de Front-end possui vários arquivos sendo eles HTML, CSS, Javascript, etc. Quando iniciamos, precisamos criar uma pasta para organizar os nossos arquivos.

## O que é HTML?

- Significa linguagem de marcação de hipertexto. Mostra o que vai ser cada texto.
- É a linguagem de marcação padrão para criação de páginas da Web
- É a estrutura de uma página da Web
- Consiste em uma série de elementos
  - Um elemento HTML é definido por uma tag inicial, algum conteúdo e uma tag final
    - Os elementos HTML informam ao navegador como exibir o conteúdo
    - Os elementos HTML rotulam partes do conteúdo como “este é um título”, “este é um parágrafo”, “este é um link”, etc.
- Exemplo:

  ```html
    <!DOCTYPE html>
    <html>
    <head>
        <title>Página HTML</title>
    </head>
    <body>
        <h1>Olá Mundo!</h1>
        <p>Olá mundo com HTML.</p>
    </body>
    </html>
  ```

  - `<!DOCTYPE html>`: Define que este documento é um documento HTML
  - `<html>`: É o elemento raiz de uma página HTML
  - `<head>`: Elemento que contém meta informações sobre a página HTML
  - `<title>`: Elemento que especifica um título para a página HTML (que é mostrado na barra de título do navegador ou na guia da página)
  - `<body>`: Elemento que define o corpo do documento e é um contêiner para todos os conteúdos visíveis, como títulos, parágrafos, imagens, hiperlinks, tabelas, listas, etc.
  - `<h1>`: Elemento que define um título grande
  - `<p>`: Elemento que define um parágrafo
- Existem os atributos que fazem parte de um elemento.
  - No elemento img (imagem), podemos usar atributos.
    - "src": Que é a origem da imagem, ou seja, qual é o caminho que se encontra a imagem que será usada.
    - "alt": Que é um texto alternativo. É importante para descrever o que é aquela imagem.
- O metadado http-equiv="X-UA-Compatible" content="IE=edge" é utilizado para configurar a página web no Internet Explorer, para que ela esteja sempre em sua versão mais recente.
- O metadado charset="UTF-8" é empregado para repassar aos navegadores qual é o formato de codificação de caracteres utilizado naquele documento.
- Para criarmos um título em destaque abrimos a tag com `<h1>` e fechamos com `</h1>`. E para adicionar parágrafos usamos as tags `<p>` e também fechamos com `</p>`.
- A tag `<button>` é diferente da tag `<a>`, pois, além da semântica, a finalidade também é outra. Usamos `<button>` para criar um botão de ação e `<a>` para indicar um link.
  - As tags são diferentes em ambos os aspectos e é necessário saber utilizar cada uma na sua função correta. Enquanto `<button>` pode ser utilizada para ações como envios de formulários, a tag `<a>` não possui essa funcionalidade, já que seu papel é apenas redirecionar o usuário para diferentes urls.

## Modo Quirks
>
> Nos velhos dias da web, páginas eram tipicamente escritas em duas versões: Uma para o Netscape Navigator, e outra para o Microsoft Internet Explorer.
> Quando os padrões web foram criados pelo W3C, navegadores não puderam começar a usá-los imediatamente, pois isto iria quebrar a maior parte dos sites existentes na web. Portanto os navegadores introduziram dois modos para tratar os novos padrões em sites condescendentes diferentemente dos antigos sites legados.
> Existem agora três modos usados pelos mecanismos de layout nos navegadores web: "quirks mode" ("modo equivocado"), "almost standards mode" ("modo quase padrão"), e "full standards mode" ("modo de padrões completos").
> Em quirks mode, o layout emula o comportamento não-padrão do Netscape Navigator 4 e do Internet Explorer 5 para Windows que é requerido para não quebrar o conteúdo existente na Web.
> No full standards mode, o comportamento é (espera-se) o descrito pelas especificações do HTML e CSS.
> No almost standards mode, há apenas um número muito pequeno de peculiaridades não-padrão implementadas.
> Para documentos HTML, os navegadores usam um DOCTYPE no início do documento para decidir se os tratarão em quirks mode ou standards mode. Para garantir que sua página use o full standards mode, certifique-se que sua página tenha um DOCTYPE.

## Figma

- É uma ferramenta de prototipagem de interfaces, onde vamos construir layouts.
- É uma plataforma online de criação de interfaces, wireframes e protótipos. Seu papel é oferecer recursos de design de telas para aplicações variadas, permitindo que times de Design trabalhem em conjunto no mesmo projeto remotamente e simultaneamente.

## CSS

- CSS significa Cascading Style Sheets. Descreve como os elementos HTML devem ser exibidos na tela.
- É uma linguagem de estilização, portanto não é uma linguagem de programação.
- Economiza muito trabalho. Ele pode controlar o layout de várias páginas da web de uma só vez
- O CSS externo é o mais indicado e recomendado, pois além dos seus arquivos HTML ficarem com uma estrutura mais limpa e tamanho menor, os mesmos estilos do arquivo .css podem ser usados em várias páginas.
- O HTML não reconhece a página de estilo automaticamente, portanto é necessário adicionar a tag `<link rel="stylesheet" href="nomedoarquivo.css">` dentro do `<head>` para que a estilização seja aplicada.
- O atributo "id" só podem ser usados uma vez dentro de uma página HTML, no sentido de que eles só devem aparecer SOMENTE UMA VEZ numa tag (que é chamada de elemento). Além disso, cada elemento só deve ter um ID. Por exemplo, se eu quiser inserir um ID nomeado de "meu-nome" numa `<div>`, não poderei mencionar este ID com este nome em nenhum outro elemento.
  - Cada elemento pode ter apenas um ID;
  - Cada página pode ter apenas um elemento com aquele ID.
- Cada elemento (tag) pode receber mais de uma "class" e estas mesmas classes podem ser usadas várias vezes dentro da mesma página HTML. Pegando o mesmo exemplo citado acima, eu poderia criar uma "class='meu-nome'" dentro de uma `<div>` e usar este mesmo elemento em outros locais da página ou usar o mesmo nome "meu-nome" em outra tag ou ainda acrescentar outra classe dentro do mesmo elemento logo após "meu-nome".
  - Você pode usar a mesma classe para vários elementos;
  - Você pode usar várias classes para um mesmo elemento;
  - Para estilizar uma class é necessário utilizar o ponto final antes de chamar o nome atribuído à classe.
- Box Model: É usado quando se fala em design e layout. É essencialmente uma caixa que envolve cada elemento HTML. Consiste em: content(conteúdo), padding(preenchimento), border(bordas) e margin(margens).
  - Conteúdo: O conteúdo da caixa, onde aparecem textos e imagens
  - Preenchimento: Limpa uma área ao redor do conteúdo. O preenchimento é transparente
  - Borda: Uma borda que circunda o preenchimento e o conteúdo
  - Margem: Limpa uma área fora da fronteira. A margem é transparente
- Reset CSS: Limpa todos os padrões dos navegadores.
- Viewport é a porção de área visível de um plano e é utilizada como unidade de medida no CSS para criar páginas Web 100% responsivas. Em outras palavras, a viewport varia de dispositivo para dispositivo, por exemplo em computadores, tablets e celulares, cada tela possui dimensões diferentes e enquanto uma página não responsiva apresentaria os elementos desproporcionais, uma página responsiva utilizando viewport teria seus elementos adequados a cada proporção.
- box-sizing é responsável por como a largura e a altura totais de um elemento são calculadas.
- Flexbox é uma ferramenta do CSS que visa organizar os elementos de uma página HTML de forma dinâmica e mantendo um layout flexível.

### Propriedades CSS

- "background-color" é o atributo de cor de fundo.
- "color" é a cor do texto
- "background" serve para configurar todas as propriedades do plano de fundo em uma declaração mais implícita.
- "border" é responsável pelas bordas dos elementos HTML. Ao inserir um elemento em um documento HTML, há várias possibilidades de estilizar sua borda. Você pode utilizar estilos que a propriedade já possui, além de poder também alterar sua cor, espessura e até mesmo seu formato!
- "gap" não é exclusiva do Flexbox, porém é utilizada quase sempre em conjunto com ele. Ela especifica no CSS o tamanho dos espaços entre linhas e colunas em layouts de grid, flex e multi-column. Sua sintaxe é bem simples e ela aceita um ou dois valores.

## Ajuda

### VSCode

- Comandos:
- CTRL + N: Abre um novo arquivo
- CTRL + S: Salva o arquivo
- ALT + Z: Quebra a linha da area de código

### Links

- Introdução com [W3Schools](https://www.w3schools.com/html/html_intro.asp)

### Extensões (VSCode)

- Live Server: Para atualizar a página html sem ter que ficar clicando o tmepo todo no "refresh"
- ESLint: Encontra erros de sintaxe rapidamente em seu código JavaScript e soluciona automaticamente esses problemas.
- IntelliCode: Ela faz com que conforme digitamos, recomendações de autocomplete são criadas, colocando como prioridade no topo da lista aquilo que você tem mais probabilidade de usar.
- GitLens: Essa extensão é um combo recheado de recursos que te ajudam a compreender melhor o código. É possível visualizarmos todas alterações que foram feitas, quando e por quem, contribuindo para o trabalho em equipe. Além disso, traz diversas f informações sobre o histórico do Git, ou seja, histórico de arquivos, comparações com versões anteriores e muito mais.
- Vscode icons: Traz ícones referentes a cada tecnologia que você está utilizando e aplica nas pastas e arquivos
- IntelliSense for CSS class names in HTML: Fornece o preenchimento de nome de classe CSS para o atributo class com base nas definições encontradas em seu espaço de trabalho ou em arquivos externos referenciados por meio do elemento link.

### Outros

- Abrir o console no navegador Chrome:
  - botão F12
  - clicar com o botão direito do mouse e ir em "inspecionar"

### Exemplos basicos

- HTML

  ```html
    <!DOCTYPE html>
    <html>
        <head>
            <title>Portfolio</title> <!-- Será o nome da aba do navegador -->
        </head>

        <body>
            <h1>Meu título: Olá Mundo!</h1>

            <h2>Oi eu sou seu subtítulo.</h2>

            <p>E eu sou um parágrafo interessante.</p>

            <img src="./html5.jpg" alt="Logo do HTML5"> <!-- O "src" pode ser apenas o nome do arquivo,   já  que a imagem está na mesma pasta que o arquivo "index". Exemplo: scr="html5.png" -->
        </body>
    </html>
  ```

- CSS

  ```css
    body {
      background-color: lightblue;
    }

    h1 {
      color: white;
      text-align: center;
    }

    p {
      font-family: verdana;
      font-size: 20px;
    }
  ```
