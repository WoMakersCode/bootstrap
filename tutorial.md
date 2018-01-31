# Estrutura de ToDo App com Bootstrap 4

Nesta oficina você aprenderá como é fácil criar um modelo de página responsiva para utilizar em sua ToDo App, utilizando Bootstrap 4. 

Antes de começar, certifique-se de ter um editor de código, como texto, Visual Studio Code, Sublime ou Notepad ++ e algum conhecimento de HTML e CSS.

Para este tutorial, você deverá criar uma pasta com o nome do seu projeto e nela, você deverá criar uma estrutura três pastas e dois arquivos HTML:

- index.html – este servirá como um arquivo principal, no qual iremos listar as tarefas do aplicativo
- pasta css - para folhas de estilo (CSS)
- pasta js - para JavaScript

### Fazendo o download do Bootstrap 4
Existem duas versões disponíveis para download: versão compilada do Bootstrap e arquivos de origem do Bootstrap.
No entanto, a versão compilada ainda não está disponível no momento da redação. Você pode baixar os arquivos de origem do Bootstrap aqui .

### Configurar Arquivos Necessários
Para este tutorial, nos concentraremos em escolher os arquivos necessários que precisamos para o nosso modelo responsivo de uma página.
Uma vez baixado, descompacte os arquivos de origem do Bootstrap e copie os seguintes arquivos dentro da pasta dist. Você pode obter esses arquivos dentro da pasta css e js ao abrir a pasta dist.

### Marcação Básica
Nosso documento HTML começará com o HTML5 ``<!DOCTYPE html>`` para informar ao navegador que trata-se de um documento HTML. Então, na nossa seção ``<head>``, podemos colocar todos os nossos links CSS e Webfonts (fontes de texto customizadas). Para fins de desempenho, você pode querer colocar os arquivos JavaScript na parte inferior do documento (antes da tag de fechamento ``</body>``). 
```html
<!DOCTYPE html>
<html lang="en">

<head>
    <title>Boostrap 4 - ToDo APP</title>
    <meta charset="utf-8">
    <meta name="author" content="Sam Norton">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <meta http-equiv="x-ua-compatible" content="ie=edge">
    <link rel="stylesheet" href="css/bootstrap.min.css">
    <link href='https://fonts.googleapis.com/css?family=Lato:400,700,900,300' rel='stylesheet' type='text/css'>
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/font-awesome/4.4.0/css/font-awesome.min.css">
</head>

<body>
    <!-- CONTENT HERE -->
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/2.1.4/jquery.min.js"></script>
    <script src="js/bootstrap.min.js"></script>
</body>

</html>
```

Note que estamos utilizando duas meta tags diferentes, a viewport e a http-equix, que servem para auxiliar o navegador a renderizar a página considerando o tamanho da tela, ou seja, aplicará um design diferenciado e ajustável a cada tamanho de tela, quando estivermos trabalhando com o Bootstrap ou fazendo a escrita de CSS com media-queries.

```html
<meta name="viewport" content="width=device-width, initial-scale=1">
<meta http-equiv="x-ua-compatible" content="ie=edge">
```

Para começar, usaremos o modelo abaixo como nosso HTML inicial para o nosso modelo responsivo de uma página. Observe que adicionei alguns links de bibliotecas hospedadas, como Font Awesome e Google Fonts. 

### Trabalhando com Grids
O sistema de grade Bootstrap 4 pode ter 12 colunas e você pode escolher a escala de coluna que deseja exibir em diferentes tamanhos de viewport. Confira a grade média Bootstrap 4 abaixo com as classes.

Não vamos falar muito sobre o sistema de grade em profundidade neste tutorial, no entanto, iremos direto na escala de coluna que vamos usar no nosso modelo de uma página.
Vamos primeiro criar um wrapper de conteúdo para adicionar uma espécie de welcome em nosso ToDo App e também o header da página, que terá link para ações de criar nova tarefa e visualizar a listagem. Para isso, adicione o seguinte trecho de código em seu arquivo index.html, substituindo o trecho escrito ``<!---CONTENT HERE-->``.

```html
    <header class="tdapp-header">
        <nav>
            <ul>
                <li>
                    <a class="p-2 text-dark" href="index.html">Lista de Tarefas</a>
                </li>
                <li>
                    <a class="p-2 text-dark" href="criar.html">Adicionar tarefa</a>
                </li>
            </ul>
        </nav>
    </header>
    <div class="container-fluid">
        <div class="jumbotron">
            <h1>Bootstrap Tutorial</h1>
            <p>Bootstrap is the most popular HTML, CSS, and JS framework for developing responsive, mobile-first projects on
                the web.</p>
        </div>

    </div>
```

### Listagem de tarefas
Feito o setup inicial da sua página, vamos adicionar uma tabela de listagem das nossas tarefas. Para isso, após o trecho de HTML que adicionamos no passo anterior, crie um novo container e adicione uma tabela. Você pode copiar e colar o código abaixo para facilitar a integração da tabela à sua página.

```html
<div class="container">
        <table class="table">
            <thead>
                <tr>
                    <th scope="col">#</th>
                    <th scope="col">Nome da tarefa</th>
                    <th scope="col">Status</th>
                    <th scope="col">Ações</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <th scope="row">1</th>
                    <td>Fazer tutorial</td>
                    <td>Incompleta</td>
                    <td>
                        <button type="button" class="btn btn-success">Finalizar</button>
                        <button type="button" class="btn btn-warning">Editar</button>
                        <button type="button" class="btn btn-danger">Deletar</button>
                    </td>
                </tr>
            </tbody>
        </table>
    </div>
```

### Adicionando um rodapé a página
Por questões de boas práticas em interface web, vamos adicionar um rodapé a nossa página, com ícones e links para nossas redes sociais e também um texto informando a autoria do projeto e o ano.

```html
<footer class="footer" id="footer">
        <div class="container">
            <div class="row">
                <div class="col-lg-12">
                    <ul>
                        <li>
                            <a href="#">
                                <i class="fa fa-facebook"></i>
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                <i class="fa fa-twitter"></i>
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                <i class="fa fa-linkedin"></i>
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                <i class="fa fa-pinterest"></i>
                            </a>
                        </li>

                    </ul>
                    <p>
                        © 2018 - Women Dev Summit na Campus Party
                        <br>
                    </p>
                </div>
            </div>
        </div>
    </footer>
```

![tela1](https://user-images.githubusercontent.com/2198735/35646892-e131ab30-06b7-11e8-8442-53f9a94b325b.PNG)


## PASSO 2: Template de Criação e Edição de Tarefa

### Formulário de Tarefas

Com a página inicial pronta, vamos criar o template da página de formulário para criação e edição da tarefa. Para isso, crie um novo arquivo chamado ``criar.html``. Nele, adicione a mesma estrutura do ``index.html`` e vamos substituir o conteúdo pelo formulário.

Copie este código e substitua o container de conteúdo:

```html
    <div class="container">
        <form action="#" method="post">
            <div class="form-group">
                <label for="tdapp-nome">Nome da tarefa</label>
                <input type="text" id="tdapp-nome" class="form-control" placeholder="Informe o nome da sua tarefa">
            </div>
            <div class="form-group">
                <label for="tdapp-status">Status da Tarefa</label>
                <select class="form-control" id="tdapp-status">
                    <option>Nova</option>
                    <option>Incompleta</option>
                    <option>Finalizada (apenas para registro)</option>
                </select>
            </div>

            <div class="form-group">
                <label for="tdapp-info">Descrição da atividade</label>
                <textarea class="form-control" id="tdapp-info" rows="3"></textarea>
            </div>
            <div class="form-group">
                <input type="submit" value="Salvar" class="btn btn-success">
            </div>
        </form>
    </div>
```
![tela2](https://user-images.githubusercontent.com/2198735/35646893-e151e8f0-06b7-11e8-9e62-42cf45efc21d.PNG)


## Adicionando um estilo à sua página

Se você seguiu os passos até aqui, irá notar que o visual das nossas páginas está bastante simples. Que tal adicionarmos um pouco de estilo?!

Crie um arquivo chamado ``custom.css`` e salve-o dentro da pasta ``css`` e adicione a chamada para este arquivo dentro do ``<head>``, que deverá ficar assim:

```html
<head>
    <title>Boostrap 4 - ToDo APP</title>
    <meta charset="utf-8">
    <meta name="author" content="Sam Norton">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <meta http-equiv="x-ua-compatible" content="ie=edge">
    <link rel="stylesheet" href="css/bootstrap.min.css">
    <link rel="stylesheet" href="css/custom.css">
    <link href='https://fonts.googleapis.com/css?family=Lato:400,700,900,300' rel='stylesheet' type='text/css'>
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/font-awesome/4.4.0/css/font-awesome.min.css">
</head>
```

Esta chamada fará com que os estilos que escrevermos neste documento será interpretado pelo browser, trazendo mais design para nossa página :smile:. No arquivo custom.css, adicione o seguinte código:

```css
.tdapp-header {
    box-shadow: 1px 2px 10px #ccc;
}

.tdapp-header ul {
    list-style: none;
}

.tdapp-header ul li {
    display: inline-block;
    padding: 15px;
}

.tdapp-header ul li a {
    color: #2A2575;
    font-weight: bold;
}

.footer {
    background:#563d7c;
    margin-top:120px;
    position:relative
}

.footer .container {
    padding:60px 0 20px;
}

.footer ul {
    margin:0 auto;
    margin-bottom:30px;
    margin-top:10px;
    text-align:center;
    list-style-type:none;
    padding-left:0;
}

.footer ul li {
	text-align:center;
    display:inline-block;
    background:rgba(0,0,0,0.2);
    color:#fff;
    line-height:45px;
    margin:0 4px;
    width:45px!important;
    height:45px!important;
    -webkit-border-radius:3px;
    border-radius:3px;
}

.footer ul li:hover {
    background:#2a2a2a;
}

.footer ul li:hover	a {
    color:#fff;
}

.footer ul li a {
    color:#fff;
    width:42px!important;
    height:42px!important;
}

.footer ul li a i {
    line-height:45px;
    color:#fff;
}

.footer p {
    color:#fff;
    font-size:.9em;
    line-height:24px;
    font-weight:300;
    text-align:center;
    text-transform:uppercase;
}

.footer a,.footer a:hover {
    color:#fff;
}

input.form-control,
select.form-control {
    background:#fff;
    border:solid 1px #ddd;
    color:#000;
    padding:15px 30px;
    margin-right:3%;
    margin-bottom:30px;
    outline:none;
    border-radius: 0;
}

textarea.form-control {
    background:#fff;
    color:#000;
    border:solid 1px #ddd;
    padding:15px 30px;
    margin-bottom:40px;
    outline:none;
    height:200px;
    border-radius: 0;
}

button.contact.submit {
    background:#333;
    font-family:'Lato',sans-serif;
    color:#fff;
    font-size:1em;
    font-weight:400;
    text-align:center;
    margin:0;
    border:none!important;
    border-radius:3px;
    padding:15px 45px;
}

button.contact.submit:hover {
    background:#563d7c;
}

.form-control:focus{
    border-color: #563d7c;
    outline: 0;
}


.done {
    display:none;
}
```

Salve e teste em seu navegador. O resultado será este:
![tela3](https://user-images.githubusercontent.com/2198735/35646894-e172a7b6-06b7-11e8-8d07-3e9b0745d4d6.PNG)

Gostou e quer fazer mais coisas? Coloque sua criatividade para funcionar e conte com a ajuda das mentoras para melhorar sua página!
