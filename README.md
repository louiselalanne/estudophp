<h1 align="center">Estudos PHP</h1>
Programação de páginas dinêmicas com PHP
<p align="center">
<img src="http://img.shields.io/static/v1?label=STATUS&message=EM%20DESENVOLVIMENTO&color=GREEN&style=for-the-badge"/>
</p>

![php-cover](https://user-images.githubusercontent.com/100588945/160294625-24baedc3-b370-48ac-b1d4-160b3cfba47e.png)

- Iniciado pela tag “<?php” e fechado com a tag “?>”.
Isso é necessário para que o servidor Web entenda qual código deve ser interpretado e qual deve ser apenas renderizado.
- As instruções PHP devem ser, obrigatoriamente, terminadas com a utilização de ponto e vírgula.
- Comentários podem ser feitos com // ou /* e */.
- Declaração e inicialização de variável: usa-se o símbolo “$” seguido do nome da mesma.
- Para atribuição de strings pode usar aspas duplas ou simples.
- Existem variáveis predefinidas – também chamadas de superglobais. Entre elas, estão as de requisição HTTP: $_REQUEST, $_POST e $_GET. Em linhas gerais,
essas três variáveis têm a mesma função, ou seja, receber dados provenientes de formulários HTML ou de outras requisições HTTP que façam uso dos métodos POST e GET.

<h2 align="center">Métodos de requisição PHP:</h1>

🐘 GET - Utilizado na requisição e na recuperação de recursos de um servidor, como uma página ou um arquivo, entre outros.
exemplo: /endereco_servidor/script.php?var1=value1&var2=value2&var3=value3

**Em linhas gerais, não deve ser utilizado quando estamos lidando com informações sensíveis, uma vez que a query string fica visível na barra de endereços do navegador. Outra característica importante desse método é que ele pode ser usado a partir de formulários HTML.**

🐘 HEAD

🐘 POST - Usado no envio de dados para o servidor a fim de criar ou atualizar um recurso.
exemplo:  POST /endereco_servidor/script.php
          Host: dominio.com.br
          var1=value1&var2=value2&var3=value3
**Assim como o GET, esse método pode ser utilizado em formulários HTML, com a vantagem de não deixar os dados transmitidos visíveis na barra de endereços do navegador – embora seja possível acessá-los analisando a requisição em si.**

🐘 PUT

🐘 DELETE

🐘 CONNECT

🐘 OPTIONS

🐘 TRACE

🐘 PATCH

<h2>Variável $_GET</h2>
  Array associativo que contém as variáveis recebidas de métodos HTTP GET.
  
