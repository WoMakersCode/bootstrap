Nesta oficina você aprenderá como é fácil criar um modelo de página responsiva para utilizar em sua ToDo App, utilizando Bootstrap 4. 

Antes de começar, certifique-se de ter um editor de código, como texto, Visual Studio Code, Sublime ou Notepad ++ e algum conhecimento de HTML e CSS.

Para este tutorial, você deverá criar uma pasta com o nome do seu projeto e nela, você deverá criar uma estrutura três pastas e dois arquivos HTML:

- index.html – este servirá como um arquivo principal, no qual iremos listar as tarefas do aplicativo
- pasta img - para imagens
- pasta css - para folhas de estilo (CSS)
- pasta js - para JavaScript

### Fazendo o download do Bootstrap 4
Existem duas versões disponíveis para download: versão compilada do Bootstrap e arquivos de origem do Bootstrap.
No entanto, a versão compilada ainda não está disponível no momento da redação. Você pode baixar os arquivos de origem do Bootstrap aqui .

### Configurar Arquivos Necessários
Para este tutorial, nos concentraremos em escolher os arquivos necessários que precisamos para o nosso modelo responsivo de uma página.
Uma vez baixado, descompacte os arquivos de origem do Bootstrap e copie os seguintes arquivos dentro da pasta dist. Você pode obter esses arquivos dentro da pasta css e js ao abrir a pasta dist.

### Marcação Básica
Nosso documento HTML começará com o HTML5 <! DOCTYPE> para especificar qual idioma e versão o nosso documento está usando. Então, na nossa seção <head>, podemos colocar todos os nossos links CSS, JavaScripts e fontes / imagens. Para fins de desempenho, você pode querer colocar os arquivos JavaScript na parte inferior do documento (antes da tag de fechamento </ body>). 
```html
<!-- DOCTYPE -->
<!DOCTYPE html>
<html lang="en">
<head>
<title>Boostrap 4 - Tutorial</title>
<!-- Required meta tags always come first -->
<meta charset="utf-8">
<meta name="author" content="Sam Norton">
<!-- Bootstrap CSS -->
<link rel="stylesheet" href="css/bootstrap.min.css">
<link rel="stylesheet" href="css/custom.css">
<!-- Fonts -->
<link href='https://fonts.googleapis.com/css?family=Lato:400,700,900,300' rel='stylesheet' type='text/css'>
<link href='http://fonts.googleapis.com/css?family=Open+Sans:400,300,300italic,400italic,600,600italic,700,700italic,800,800italic' rel='stylesheet' type='text/css'>
<link href='https://fonts.googleapis.com/css?family=Raleway:400,300,600,700,900' rel='stylesheet' type='text/css'>
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/font-awesome/4.4.0/css/font-awesome.min.css">
</head>
```

Podemos também adicionar o seguinte código para forçar o Internet Explorer a renderizar para o modo de renderização e a propriedade meta viewport para visualização sensível.

```html
<meta name="viewport" content="width=device-width, initial-scale=1">
<meta http-equiv="x-ua-compatible" content="ie=edge">
```

Para começar, usaremos o modelo abaixo como nosso HTML inicial para o nosso modelo responsivo de uma página. Observe que adicionei alguns links de bibliotecas hospedadas, como Font Awesome e Google Fonts. 

```html
<!-- DOCTYPE -->
<!DOCTYPE html>
<html lang="en">
<head>
<title>Boostrap 4 - Tutorial</title>
<!-- Required meta tags always come first -->
<meta charset="utf-8">
<meta name="author" content="Sam Norton">
<meta name="viewport" content="width=device-width, initial-scale=1">
<meta http-equiv="x-ua-compatible" content="ie=edge">
<!-- Bootstrap CSS -->
<link rel="stylesheet" href="css/bootstrap.min.css">
<link rel="stylesheet" href="css/custom.css">
<!-- Fonts -->
<link href='https://fonts.googleapis.com/css?family=Lato:400,700,900,300' rel='stylesheet' type='text/css'>
<link href='http://fonts.googleapis.com/css?family=Open+Sans:400,300,300italic,400italic,600,600italic,700,700italic,800,800italic' rel='stylesheet' type='text/css'>
<link href='https://fonts.googleapis.com/css?family=Raleway:400,300,600,700,900' rel='stylesheet' type='text/css'>
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/font-awesome/4.4.0/css/font-awesome.min.css">
</head>
<body>
<!---CONTENT HERE-->
<!-- JavaScripts -->
<script src="https://ajax.googleapis.com/ajax/libs/jquery/2.1.4/jquery.min.js"></script>
<script src="js/bootstrap.min.js"></script>
<script src="js/tether.min.js"></script>
</body>
</html>
```

### Trabalhando com Grids
O sistema de grade Bootstrap 4 pode ter 12 colunas e você pode escolher a escala de coluna que deseja exibir em diferentes tamanhos de viewport. Confira a grade média Bootstrap 4 abaixo com as classes.

Não vamos falar muito sobre o sistema de grade em profundidade neste tutorial, no entanto, iremos direto na escala de coluna que vamos usar no nosso modelo de uma página.
Vamos primeiro criar um wrapper de conteúdo para adicionar uma espécie de welcome em nosso ToDo App. Para isso, adicione o seguinte trecho de código em seu arquivo index.html, dentro do bloco ``<body></body``.

```html
<div class="container">
  <div class="jumbotron">
    <h1>Bootstrap Tutorial</h1>      
    <p>Bootstrap is the most popular HTML, CSS, and JS framework for developing responsive, mobile-first projects on the web.</p>
  </div>
  <p>This is some text.</p>      
  <p>This is another text.</p>      
</div>
```
