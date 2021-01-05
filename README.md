# MVC

## M

> Model

## V

> View

## C

> Controller

## Explicação de Funcionamento

Se acessamos um site com a seguinte URL

> site.com.br/algumacoisa/seila/sobre.php

Entendemos que, na RAIZ desse servidor, há uma pasta chamada **algumacoisa** e, dentro dessa pasta há uma outra pasta chamada **seila**, que, dentro dela, há um arquivo chamado **sobre.php**

> No MVC, essa estrutura passa a ser relativa. Na estrutura MVC, tudo que vem após a / (barra), não necessariamente, a partir de agora, será uma pasta, um arquivo, etc... Podem ser apenas instruções para o site/sistema.

Normalmente, a estrutura MVC, tem um arquivo inicial, que é o arquivo onde começa o sistema. Todo o sistema que é feito em MVC, começa a partir de um único arquivo. Ex: site.com.br/
Vamos supor que na raiz deste servidor, tem um arquivo chamado **index.php**. Ao invés de acessarmos site.com.br/index.php, não é necessário digitar o nome do arquivo, porque ele será carregado automaticamente.

> Vamos supor que acessamos a seguinte URL site.com.br/sobre

Esse "sobre", não necessariamente é uma pasta, o MVC vai acessar o mesmo arquivo index, independente do que for colocado após a /, contudo, ele irá pegar o endereço que foi acessado e também vai mandar para o index.

Basicamente, ele vai receber o que foi digitado e realizar os procedimentos, para entregar corretamente ao usuário o que foi requisitado.
Então, a partir de agora, esse conceito de pastas e arquivos que observamos na URL do site, agora serão relativos, pois podemos construir o site colocando basicamente o que quisermos após a /. E não necessariamente o que foi digitado, será o endereço de algum arquivo, pasta, etc... O que for digitado, simplesmente será enviado à nossa estrutura MVC.

## Processos Internos

- Usuário requisita a URL site.com.br/sobre ;
- MVC verifica se essa rota está estabelecida;
- MVC manda a requisição para o **Controller** da rota

> Após o Controller receber a requisição, ele irá realizar o controle do que será feito. Ex: exibir uma página, exibir um JSON, não mostrar nada, etc... Ele será o **coração** do sistema.

No nosso exemplo, queremos acessar a página **sobre**, então o MVC realizou os passos listados acima e então o Controller terá duas principais ações a serem realizadas.

1. Carregar um View
2. Chamar um Model

Onde:

> *VIEW* é a parte gráfica e ou visual de um sistema, e um *MODEL*, é uma classe diretamente relacionada com alguma tabela do banco de dados. Ex: usuarios. Teríamos um Model chamado **Usuario**, onde nessa classe ele recuperaria informações de usuário e mandaria para o View.

Ficaríamos com esse flow:

1. Controller (Base de tudo)
2. Model (Informações do banco de dados)
3. View (Apresentação)
