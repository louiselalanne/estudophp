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
  
exemplo: <?php

          //Requisição GET: /endereco_servidor/script.php?var1=value1&var2=value2&var3=value3

          echo $_GET['var1']; //imprimiria value1
          echo $_GET['var2']; //imprimiria value2
          echo $_GET['var3']; //imprimiria value3

<H2>Variável $_POST</H2>
A exemplo de $_GET, a variável predefinida $_POST também é um array associativo. Entretanto, ela contém as variáveis recebidas através de métodos POST.

<h2>Variável $_REQUEST</h2>
É considerada "coringa", uma vez que exerce múltiplos papéis. Com ela, é possível receber tanto variáveis provenientes de métodos GET 
quanto POST – e também do método cookies ($_COOKIE).

Sua utilização é semelhante ao que foi visto em $_GET e $_POST.

<h2>Operadores</h2>
“+”, “-“, “*”, “/”,"%" e "**"(exponenciação).

<?php

$var1 = 4; //a variável foi inicializada com o valor de 4
$var1 += 2; //com a utilização da combinação de operadores a variável $var1 passou a ter o valor de 6 (4 + 2)
$var1 *= 2; //com a utilização da combinação de operadores a variável $var1 passou a ter o valor de 12 (4 + 2) * 2

$var2 = "Programação";
$var2 .= " com PHP"; //com a utilização da combinação de operadores a variável $var2 passou a ter o conteúdo "Programação com PHP"

$var = ($var4 = "Copie esses códigos") . " e pratique seus conhecimentos!" ;
/*
No exemplo acima o conteúdo da variável $var3 é igual a "Copie esses códigos e pratique seus conhecimentos!"
Já a variável $var4 possui o conteúdo "Copie esses códigos"
*/

<h3>Operadores de comparação</h3></br></br>
<table><thead><tr><th>==</th><th>$var1 == $var2</th><th></th></tr></thead><tbody><tr><td>===</td><td>$var1 === $var2</td><td>Verifica se $var1 é idêntica a $var2. Nesse caso, além do valor, verifica se ambas são do mesmo tipo</td></tr><tr><td>!=</td><td>$var1 != $var2</td><td>Verifica se $var1 é diferente de $var2</td></tr><tr><td>&lt;&gt;</td><td>$var1 &lt;&gt; $var2</td><td></td></tr><tr><td>!==</td><td>$var1 !== $var2</td><td>Verifica se não são idênticas/iguais ou se não são do mesmo tipo</td></tr><tr><td>&lt;</td><td>$var1 &lt; $var2</td><td></td></tr><tr><td>&gt;</td><td>$var1 &gt; $var2</td><td></td></tr><tr><td>&lt;=</td><td>$var1 &lt;= $var2</td><td></td></tr><tr><td>&gt;=</td><td>$var1 &gt;= $var2</td><td></td></tr></tbody></table>

<h3>Operadores lógicos</h3></br></br>
<table><thead><tr><th>and</th><th>$var1 and $var2</th><th>Retorna true se $var1 E $var2 forem verdadeiras</th></tr></thead><tbody><tr><td>or</td><td>$var1 or $var2</td><td>Retorna true se $var1 OU $var2 forem verdadeiras</td></tr><tr><td>xor</td><td>$var1 xor $var2</td><td>Retorna true se $var1 OU $var2 forem verdadeiras, mas não ambas</td></tr><tr><td>!</td><td>!$var2</td><td>Retorna true se $var1 não for verdadeira</td></tr><tr><td>&amp;&amp;</td><td>$var1 &amp;&amp; $var2</td><td>Retorna true se $var1 E $var2 forem verdadeiras</td></tr><tr><td>||</td><td>$var1 || $var2</td><td>Retorna true se $var1 OU $var2 forem verdadeiras</td></tr></tbody></table>

