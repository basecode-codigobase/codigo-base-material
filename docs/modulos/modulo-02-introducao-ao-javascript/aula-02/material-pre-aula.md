# Material Pré-aula — Aula 02: Primeiros Passos em JavaScript

Este material apresenta o conteúdo completo da Aula 02.

Nesta aula, você vai começar a escrever código JavaScript de verdade.

Na aula anterior, o foco foi aprender a pensar antes de programar: entender o problema, separar entrada, processamento e saída, organizar os passos e perceber quando existe uma decisão.

Agora vamos começar a transformar esse raciocínio em código.

## O que você vai estudar nesta aula

Nesta aula, você vai estudar:

- o que é JavaScript e para que ele é utilizado;
- pontos fortes e fracos do JavaScript;
- `console.log`;
- variáveis;
- `let`, `const` e `var`;
- tipos disponíveis em JavaScript;
- tipos primitivos;
- `typeof`;
- tipagem dinâmica;
- boas práticas na nomeação de variáveis;
- operadores de atribuição;
- operadores aritméticos;
- operadores condicionais;
- estruturas condicionais;
- `if`;
- `if else`;
- operador ternário;
- operadores lógicos.

O objetivo não é decorar tudo de uma vez.

O objetivo é entender o papel de cada peça e começar a usar essas peças em códigos pequenos.

---

## 1. O que é JavaScript?

JavaScript é uma linguagem de programação.

Uma linguagem de programação serve para escrever instruções que o computador consegue executar.

Com JavaScript, podemos criar códigos para:

- fazer cálculos;
- tomar decisões;
- manipular textos;
- validar informações;
- criar regras de sistemas;
- controlar interações em páginas web;
- criar aplicações no navegador;
- criar programas que rodam fora do navegador usando Node.js.

Neste começo do curso, vamos usar JavaScript principalmente para aprender fundamentos de programação.

Ou seja: JavaScript será a ferramenta que vamos usar para praticar lógica, variáveis, operadores, decisões, repetições, funções e resolução de problemas.

## 1.1 JavaScript é uma ferramenta, não uma solução mágica

JavaScript é muito importante no desenvolvimento web, mas ele não resolve todos os problemas do mundo.

Toda linguagem tem pontos fortes e pontos fracos.

Aprender isso desde o começo ajuda você a não enxergar uma linguagem como se ela fosse uma bala de prata.

Uma linguagem de programação é uma ferramenta.

E ferramentas são boas ou ruins dependendo do problema, do contexto e da forma como são usadas.

## 1.2 Pontos fortes do JavaScript

JavaScript tem vários pontos fortes:

- é muito usado na web;
- roda diretamente nos navegadores;
- permite criar páginas interativas;
- também pode rodar fora do navegador com Node.js;
- possui uma comunidade enorme;
- tem muitas bibliotecas e ferramentas;
- permite praticar fundamentos de programação sem depender de um ambiente muito complexo;
- é uma boa linguagem para começar a enxergar resultados rapidamente.

Exemplo de código JavaScript:

```js
console.log("Olá, JavaScript!");
```

Esse código mostra uma mensagem no console.

Ele é simples, mas já mostra uma ideia importante: escrevemos uma instrução e o computador executa.

## 1.3 Pontos fracos e cuidados com JavaScript

JavaScript também tem pontos que exigem cuidado:

- permite algumas conversões automáticas que podem confundir iniciantes;
- possui comportamentos antigos por causa da sua história;
- aceita formas diferentes de resolver o mesmo problema;
- pode esconder alguns erros se o programador não prestar atenção;
- em projetos grandes, código desorganizado pode virar bagunça rapidamente;
- alguns conceitos parecem simples no começo, mas têm detalhes importantes depois.

Veja este exemplo:

```js
console.log("5" + 2);
console.log("5" - 2);
```

O primeiro resultado será:

```text
52
```

O segundo resultado será:

```text
3
```

Isso acontece porque o JavaScript tenta interpretar os valores dependendo da operação.

Com `+`, ele pode juntar textos.

Com `-`, ele tenta fazer conta.

Por isso, no começo, vamos escrever códigos simples e observar os resultados com calma.

---

## 2. Como vamos testar código nesta aula

Nesta aula, vamos usar arquivos `.js` no VS Code e observar resultados no terminal.

Você pode criar um arquivo chamado:

```text
aula-02.js
```

Dentro dele, você pode escrever:

```js
console.log("Minha primeira aula de JavaScript");
```

Para executar, o instrutor vai orientar o comando adequado no ambiente da turma.

Em muitos ambientes com Node.js instalado, o comando será:

```bash
node aula-02.js
```

Se tudo estiver funcionando, o terminal vai mostrar:

```text
Minha primeira aula de JavaScript
```

---

## 3. O que é console.log?

`console.log` é uma instrução usada para mostrar informações no console.

Neste começo, vamos usar `console.log` para enxergar o que o nosso código está fazendo.

Ele será nossa principal forma de saída.

Lembre da Aula 01:

- entrada: dados que o programa usa;
- processamento: o que o programa faz com os dados;
- saída: resultado mostrado no final.

Por enquanto, nossa saída será feita com `console.log`.

Exemplo:

```js
console.log("Olá!");
console.log(10);
console.log(true);
```

Resultado esperado:

```text
Olá!
10
true
```

Também podemos mostrar resultados de contas:

```js
console.log(5 + 3);
console.log(10 - 4);
```

Resultado:

```text
8
6
```

E podemos mostrar valores guardados em variáveis:

```js
const nome = "Ana";
console.log(nome);
```

Resultado:

```text
Ana
```

---

## 4. Variáveis

Variável é um nome que usamos para guardar um valor.

Pense em uma variável como uma caixinha com etiqueta.

A etiqueta é o nome da variável.

O conteúdo é o valor guardado.

Exemplo:

```js
const nome = "Maria";
const idade = 20;

console.log(nome);
console.log(idade);
```

Nesse código:

- `nome` guarda o valor `"Maria"`;
- `idade` guarda o valor `20`;
- `console.log` mostra esses valores no console.

Resultado:

```text
Maria
20
```

## 4.1 Por que variáveis são importantes?

Variáveis são importantes porque programas precisam guardar informações para usar depois.

Exemplo:

```js
const preco = 100;
const desconto = 10;
const precoFinal = preco - desconto;

console.log(precoFinal);
```

Resultado:

```text
90
```

Aqui o programa guarda:

- o preço original;
- o desconto;
- o preço final calculado.

Sem variáveis, seria mais difícil organizar o raciocínio.

---

## 5. let, const e var

Em JavaScript, existem algumas formas de criar variáveis.

As principais são:

- `let`;
- `const`;
- `var`.

Hoje, no código moderno, usamos principalmente `let` e `const`.

## 5.1 const

Use `const` quando o valor não deve ser reatribuído.

Exemplo:

```js
const nome = "João";
console.log(nome);
```

Esse código funciona normalmente.

Mas este código gera erro:

```js
const nome = "João";
nome = "Maria";

console.log(nome);
```

Isso acontece porque uma variável criada com `const` não pode receber outro valor depois.

Use `const` por padrão quando você não pretende trocar o valor.

## 5.2 let

Use `let` quando o valor pode mudar.

Exemplo:

```js
let saldo = 100;
console.log(saldo);

saldo = 80;
console.log(saldo);
```

Resultado:

```text
100
80
```

Aqui faz sentido usar `let`, porque o saldo mudou.

## 5.3 var

`var` é uma forma antiga de criar variáveis em JavaScript.

Exemplo:

```js
var cidade = "São Paulo";
console.log(cidade);
```

Esse código funciona, mas no JavaScript moderno evitamos `var` na maior parte dos casos.

Por quê?

Porque `var` tem comportamentos que podem gerar confusão, principalmente em códigos maiores.

Neste curso, a regra inicial será:

- use `const` quando o valor não muda;
- use `let` quando o valor precisa mudar;
- evite `var` por enquanto.

## 5.4 Comparação rápida

```js
const cpf = "123.456.789-00";
let pontos = 0;
var apelido = "dev";

pontos = pontos + 10;

console.log(cpf);
console.log(pontos);
console.log(apelido);
```

Neste exemplo:

- `cpf` não deve mudar, então usamos `const`;
- `pontos` pode mudar, então usamos `let`;
- `apelido` foi criado com `var`, mas essa forma não será nosso padrão.

---

## 6. Tipos disponíveis em JavaScript

Valores em JavaScript possuem tipos.

O tipo indica que espécie de valor estamos usando.

Nesta aula, vamos conhecer estes tipos:

- `number`;
- `string`;
- `boolean`;
- `function`;
- `object`;
- `undefined`;
- `null`.

Não precisamos aprofundar todos agora.

O mais importante neste começo é reconhecer o que eles representam.

## 6.1 number

`number` representa números.

Pode ser número inteiro ou decimal.

```js
const idade = 25;
const altura = 1.75;
const saldo = -50;

console.log(idade);
console.log(altura);
console.log(saldo);
```

## 6.2 string

`string` representa texto.

Textos ficam entre aspas.

Podemos usar aspas duplas, aspas simples ou crase.

```js
const nome = "Ana";
const cidade = 'Recife';
const mensagem = `Olá, Ana`;

console.log(nome);
console.log(cidade);
console.log(mensagem);
```

Para começar, escolha uma forma e seja consistente.

## 6.3 boolean

`boolean` representa verdadeiro ou falso.

Só existem dois valores booleanos:

- `true`;
- `false`.

Exemplo:

```js
const alunoMatriculado = true;
const pagamentoAtrasado = false;

console.log(alunoMatriculado);
console.log(pagamentoAtrasado);
```

Booleanos são muito usados em condições.

## 6.4 function

`function` representa uma função.

Função é um bloco de código que pode ser executado quando chamado.

Não vamos aprofundar funções nesta aula, porque elas terão uma aula própria.

Por enquanto, veja apenas um exemplo:

```js
function mostrarMensagem() {
  console.log("Olá!");
}

console.log(typeof mostrarMensagem);
```

Resultado:

```text
function
```

## 6.5 object

`object` representa um objeto.

Objeto é uma forma de agrupar informações relacionadas.

Não vamos aprofundar objetos nesta aula, porque eles terão uma aula própria.

Exemplo:

```js
const aluno = {
  nome: "Ana",
  idade: 20
};

console.log(aluno);
console.log(typeof aluno);
```

Resultado do `typeof`:

```text
object
```

## 6.6 undefined

`undefined` significa que uma variável foi criada, mas ainda não recebeu valor.

Exemplo:

```js
let telefone;

console.log(telefone);
console.log(typeof telefone);
```

Resultado:

```text
undefined
undefined
```

## 6.7 null

`null` representa ausência intencional de valor.

É como dizer:

> Neste momento, esta variável não tem valor.

Exemplo:

```js
const endereco = null;

console.log(endereco);
```

Resultado:

```text
null
```

Um cuidado: em JavaScript, `typeof null` retorna `"object"`.

```js
const endereco = null;

console.log(typeof endereco);
```

Resultado:

```text
object
```

Esse é um comportamento antigo da linguagem.

Por enquanto, lembre apenas:

- `undefined`: valor ainda não definido;
- `null`: ausência de valor colocada de propósito.

---

## 7. Tipos primitivos

Tipos primitivos são tipos básicos da linguagem.

Nesta aula, vamos trabalhar principalmente com:

- `number`;
- `string`;
- `boolean`;
- `undefined`;
- `null`.

Exemplo com vários tipos:

```js
const nome = "Carlos";
const idade = 30;
const aprovado = true;
let telefone;
const endereco = null;

console.log(nome);
console.log(idade);
console.log(aprovado);
console.log(telefone);
console.log(endereco);
```

Esses tipos serão suficientes para muitos exercícios iniciais.

---

## 8. typeof

`typeof` é um operador usado para descobrir o tipo de um valor.

Exemplo:

```js
console.log(typeof "Ana");
console.log(typeof 25);
console.log(typeof true);
console.log(typeof undefined);
console.log(typeof null);
```

Resultado:

```text
string
number
boolean
undefined
object
```

Também podemos usar `typeof` com variáveis:

```js
const produto = "Teclado";
const preco = 150;
const disponivel = true;

console.log(typeof produto);
console.log(typeof preco);
console.log(typeof disponivel);
```

Resultado:

```text
string
number
boolean
```

Use `typeof` quando quiser investigar o tipo de um valor.

---

## 9. Tipagem dinâmica

JavaScript possui tipagem dinâmica.

Isso significa que o tipo está no valor, não preso de forma fixa na variável.

Exemplo:

```js
let dado = 10;
console.log(dado);
console.log(typeof dado);

dado = "dez";
console.log(dado);
console.log(typeof dado);
```

Resultado:

```text
10
number
dez
string
```

A mesma variável começou guardando um número e depois passou a guardar um texto.

Isso é possível em JavaScript.

## 9.1 Isso é bom ou ruim?

Depende.

Pode ser útil porque dá flexibilidade.

Mas pode causar erros se você não prestar atenção.

Exemplo:

```js
let valor = 10;
valor = "10";

console.log(valor + 5);
```

Resultado:

```text
105
```

O JavaScript juntou `"10"` com `5`, formando o texto `"105"`.

Por isso, precisamos prestar atenção nos tipos.

---

## 10. Boas práticas para nomear variáveis

Nome de variável é muito importante.

Um bom nome ajuda você a entender o código depois.

Também ajuda outras pessoas a entenderem o seu código.

## 10.1 Use nomes descritivos

Prefira:

```js
const idadeDoAluno = 18;
const valorDaCompra = 250;
const alunoAprovado = true;
```

Evite:

```js
const x = 18;
const v = 250;
const a = true;
```

Nomes como `x`, `v` e `a` não explicam quase nada.

## 10.2 Use camelCase

Em JavaScript, é comum usar `camelCase` para nomes de variáveis e funções.

No `camelCase`, a primeira palavra começa com letra minúscula e as próximas palavras começam com letra maiúscula.

Exemplos:

```js
const nomeDoAluno = "Beatriz";
const valorTotalDaCompra = 300;
const quantidadeDeProdutos = 4;
```

Evite misturar padrões sem necessidade:

```js
const nome_do_aluno = "Beatriz";
const ValorTotalDaCompra = 300;
```

Esses formatos existem em outros contextos, mas no JavaScript do dia a dia vamos priorizar `camelCase`.

## 10.3 Evite abreviações confusas

Evite:

```js
const qtdProd = 4;
const vlrCmp = 300;
```

Prefira:

```js
const quantidadeDeProdutos = 4;
const valorDaCompra = 300;
```

Abreviações podem parecer rápidas na hora de escrever, mas atrapalham a leitura depois.

## 10.4 Cuidado com nomes longos demais

Nomes descritivos são bons.

Mas nomes enormes também atrapalham.

Evite:

```js
const quantidadeTotalDeProdutosCompradosPeloClienteNaLojaDuranteAPromocao = 4;
```

Prefira algo claro e equilibrado:

```js
const quantidadeDeProdutos = 4;
```

## 10.5 Siga convenções já estabelecidas

Em JavaScript e Node.js, é comum encontrar nomes em `camelCase`.

Exemplos:

```js
const fileName = "dados.txt";
const userName = "ana";
const totalPrice = 150;
```

Você não precisa escrever tudo em inglês agora, mas deve entender que muitos códigos, bibliotecas e funções do ecossistema JavaScript usam esse padrão.

## 10.6 Evite nomes reservados

Algumas palavras têm significado especial em JavaScript.

Essas palavras são reservadas e não devem ser usadas como nomes de variáveis.

Exemplos de palavras reservadas:

- `const`;
- `let`;
- `var`;
- `if`;
- `else`;
- `function`;
- `return`;
- `true`;
- `false`;
- `null`.

Este código está errado:

```js
const if = "teste";
```

Use outro nome:

```js
const condicao = "teste";
```

---

## 11. Operadores de atribuição

Operadores de atribuição servem para atribuir valores a variáveis.

O principal operador de atribuição é `=`.

Exemplo:

```js
const nome = "Ana";
let idade = 20;
```

O sinal `=` não significa "igual" no sentido matemático.

Em programação, neste contexto, ele significa:

> guarde este valor nesta variável.

Também existem operadores de atribuição combinados.

## 11.1 +=

Soma e atribui.

```js
let pontos = 10;
pontos += 5;

console.log(pontos);
```

Resultado:

```text
15
```

É o mesmo que:

```js
pontos = pontos + 5;
```

## 11.2 -=

Subtrai e atribui.

```js
let saldo = 100;
saldo -= 30;

console.log(saldo);
```

Resultado:

```text
70
```

## 11.3 *=

Multiplica e atribui.

```js
let numero = 4;
numero *= 3;

console.log(numero);
```

Resultado:

```text
12
```

## 11.4 /=

Divide e atribui.

```js
let valor = 20;
valor /= 2;

console.log(valor);
```

Resultado:

```text
10
```

---

## 12. Operadores aritméticos

Operadores aritméticos servem para fazer contas.

Vamos estudar:

- adição;
- subtração;
- multiplicação;
- divisão;
- módulo;
- incremento;
- decremento.

## 12.1 Adição

```js
const soma = 10 + 5;
console.log(soma);
```

Resultado:

```text
15
```

## 12.2 Subtração

```js
const subtracao = 10 - 5;
console.log(subtracao);
```

Resultado:

```text
5
```

## 12.3 Multiplicação

```js
const multiplicacao = 10 * 5;
console.log(multiplicacao);
```

Resultado:

```text
50
```

## 12.4 Divisão

```js
const divisao = 10 / 5;
console.log(divisao);
```

Resultado:

```text
2
```

## 12.5 Módulo

O operador módulo `%` retorna o resto da divisão.

Exemplo:

```js
const resto = 10 % 3;
console.log(resto);
```

Resultado:

```text
1
```

Isso acontece porque 10 dividido por 3 dá 3 e sobra 1.

O módulo é muito usado para descobrir se um número é par ou ímpar.

```js
const numero = 8;
const restoDaDivisao = numero % 2;

console.log(restoDaDivisao);
```

Resultado:

```text
0
```

Se o resto da divisão por 2 for `0`, o número é par.

## 12.6 Incremento

Incremento aumenta uma variável em 1.

```js
let contador = 0;
contador++;

console.log(contador);
```

Resultado:

```text
1
```

É o mesmo que:

```js
contador = contador + 1;
```

## 12.7 Decremento

Decremento diminui uma variável em 1.

```js
let vidas = 3;
vidas--;

console.log(vidas);
```

Resultado:

```text
2
```

É o mesmo que:

```js
vidas = vidas - 1;
```

---

## 13. Operadores condicionais

Operadores condicionais comparam valores.

O resultado de uma comparação é sempre um booleano:

- `true`;
- `false`.

## 13.1 Igual a valor: ==

O operador `==` compara o valor, mas pode ignorar diferença de tipo.

```js
console.log(5 == "5");
```

Resultado:

```text
true
```

Isso pode confundir.

Por isso, no curso, vamos preferir `===`.

## 13.2 Estritamente igual: ===

O operador `===` compara valor e tipo.

```js
console.log(5 === "5");
console.log(5 === 5);
```

Resultado:

```text
false
true
```

No primeiro caso:

- `5` é number;
- `"5"` é string.

Mesmo parecendo parecidos, eles não são estritamente iguais.

## 13.3 Diferente de valor: !=

O operador `!=` verifica se os valores são diferentes, mas também pode ignorar diferença de tipo.

```js
console.log(5 != "5");
```

Resultado:

```text
false
```

Isso acontece porque o JavaScript considera que os valores são equivalentes.

## 13.4 Estritamente diferente: !==

O operador `!==` verifica se valor ou tipo são diferentes.

```js
console.log(5 !== "5");
console.log(5 !== 5);
```

Resultado:

```text
true
false
```

No curso, vamos preferir `!==` em vez de `!=`.

## 13.5 Maior que

```js
console.log(10 > 5);
console.log(3 > 8);
```

Resultado:

```text
true
false
```

## 13.6 Maior ou igual que

```js
console.log(10 >= 10);
console.log(9 >= 10);
```

Resultado:

```text
true
false
```

## 13.7 Menor que

```js
console.log(4 < 7);
console.log(9 < 2);
```

Resultado:

```text
true
false
```

## 13.8 Menor ou igual que

```js
console.log(5 <= 5);
console.log(8 <= 5);
```

Resultado:

```text
true
false
```

---

## 14. Estruturas condicionais

Estruturas condicionais permitem que o programa tome decisões.

Na Aula 01, você viu decisões em linguagem natural.

Exemplo:

> Se a média for maior ou igual a 7, o aluno está aprovado. Caso contrário, está reprovado.

Agora vamos escrever isso em JavaScript.

## 14.1 if

`if` significa "se".

Use `if` quando quiser executar um bloco de código apenas se uma condição for verdadeira.

```js
const idade = 20;

if (idade >= 18) {
  console.log("Pessoa maior de idade");
}
```

Resultado:

```text
Pessoa maior de idade
```

Se a idade fosse 15, nada seria mostrado.

```js
const idade = 15;

if (idade >= 18) {
  console.log("Pessoa maior de idade");
}
```

## 14.2 if else

Use `if else` quando existem dois caminhos:

- um caminho se a condição for verdadeira;
- outro caminho se a condição for falsa.

```js
const idade = 15;

if (idade >= 18) {
  console.log("Pode entrar");
} else {
  console.log("Não pode entrar");
}
```

Resultado:

```text
Não pode entrar
```

## 14.3 else if

Use `else if` quando existem mais de duas possibilidades.

Exemplo:

```js
const nota = 6;

if (nota >= 7) {
  console.log("Aprovado");
} else if (nota >= 5) {
  console.log("Recuperação");
} else {
  console.log("Reprovado");
}
```

Resultado:

```text
Recuperação
```

O programa testa na ordem:

1. A nota é maior ou igual a 7?
2. Se não for, a nota é maior ou igual a 5?
3. Se também não for, cai no `else`.

## 14.4 Exemplo completo: média do aluno

```js
const nota1 = 8;
const nota2 = 6;
const media = (nota1 + nota2) / 2;

console.log("Média:", media);

if (media >= 7) {
  console.log("Aluno aprovado");
} else {
  console.log("Aluno reprovado");
}
```

Resultado:

```text
Média: 7
Aluno aprovado
```

---

## 15. Operador ternário

O operador ternário é uma forma curta de escrever uma condição simples.

Formato:

```js
condicao ? valorSeVerdadeiro : valorSeFalso
```

Exemplo:

```js
const idade = 20;
const mensagem = idade >= 18 ? "Maior de idade" : "Menor de idade";

console.log(mensagem);
```

Resultado:

```text
Maior de idade
```

O código acima significa:

> Se idade for maior ou igual a 18, guarde "Maior de idade". Caso contrário, guarde "Menor de idade".

## 15.1 Quando usar ternário?

Use ternário quando a condição for simples e o resultado couber em uma linha clara.

Bom uso:

```js
const nota = 8;
const situacao = nota >= 7 ? "Aprovado" : "Reprovado";

console.log(situacao);
```

Evite ternário quando a lógica ficar difícil de ler.

Neste caso, prefira `if else`:

```js
const nota = 6;

if (nota >= 7) {
  console.log("Aprovado");
} else if (nota >= 5) {
  console.log("Recuperação");
} else {
  console.log("Reprovado");
}
```

Regra inicial:

- condição simples: ternário pode ser bom;
- condição com muitos caminhos: prefira `if`, `else if` e `else`.

---

## 16. Operadores lógicos

Operadores lógicos servem para combinar ou inverter condições.

Vamos estudar:

- AND: `&&`;
- OR: `||`;
- NOT: `!`.

## 16.1 AND: &&

O operador `&&` significa "E".

Ele só retorna `true` quando todas as condições são verdadeiras.

Exemplo:

```js
const idade = 20;
const temIngresso = true;

if (idade >= 18 && temIngresso === true) {
  console.log("Pode entrar no evento");
} else {
  console.log("Não pode entrar no evento");
}
```

Resultado:

```text
Pode entrar no evento
```

A pessoa só pode entrar se:

- tiver 18 anos ou mais;
- e tiver ingresso.

## 16.2 OR: ||

O operador `||` significa "OU".

Ele retorna `true` se pelo menos uma condição for verdadeira.

Exemplo:

```js
const temCartao = false;
const temPix = true;

if (temCartao === true || temPix === true) {
  console.log("Pagamento disponível");
} else {
  console.log("Nenhuma forma de pagamento disponível");
}
```

Resultado:

```text
Pagamento disponível
```

Aqui basta uma forma de pagamento estar disponível.

## 16.3 NOT: !

O operador `!` inverte um valor booleano.

Exemplo:

```js
const usuarioBloqueado = false;

if (!usuarioBloqueado) {
  console.log("Usuário pode acessar");
} else {
  console.log("Usuário bloqueado");
}
```

Resultado:

```text
Usuário pode acessar
```

`!usuarioBloqueado` significa:

> se o usuário não estiver bloqueado.

## 16.4 Exemplo completo com operadores lógicos

```js
const usuario = "admin";
const senha = "1234";
const contaBloqueada = false;

if (usuario === "admin" && senha === "1234" && !contaBloqueada) {
  console.log("Login realizado com sucesso");
} else {
  console.log("Não foi possível realizar o login");
}
```

Resultado:

```text
Login realizado com sucesso
```

---

## 17. Código completo para testar

Copie este código para um arquivo chamado `aula-02.js` e execute no ambiente indicado pelo instrutor.

```js
const nome = "Marina";
const idade = 19;
const nota1 = 8;
const nota2 = 6;
const temPresencaMinima = true;

const media = (nota1 + nota2) / 2;
const maiorDeIdade = idade >= 18;
const aprovadoPorNota = media >= 7;
const aprovado = aprovadoPorNota && temPresencaMinima;

console.log("Nome:", nome);
console.log("Idade:", idade);
console.log("Tipo da idade:", typeof idade);
console.log("Média:", media);
console.log("Maior de idade:", maiorDeIdade);

if (aprovado) {
  console.log("Situação: aluno aprovado");
} else {
  console.log("Situação: aluno não aprovado");
}

const mensagemIdade = maiorDeIdade ? "Pode se inscrever" : "Precisa de responsável";
console.log(mensagemIdade);
```

Depois de executar, tente alterar:

- o valor de `idade`;
- o valor de `nota1`;
- o valor de `nota2`;
- o valor de `temPresencaMinima`.

Observe como a saída muda.

---

## 18. Exercícios de fixação

Faça estes exercícios em um arquivo `.js`.

Use `console.log` para mostrar os resultados.

## Exercício 1 — Dados pessoais

Crie variáveis para guardar:

- seu nome;
- sua idade;
- sua cidade;
- se você está matriculado no curso.

Depois, mostre cada valor no console.

Mostre também o tipo de cada valor usando `typeof`.

## Exercício 2 — Cálculo de compra

Crie as variáveis:

- `precoProduto`;
- `quantidade`;
- `valorTotal`.

Calcule o valor total da compra e mostre no console.

Exemplo:

```js
const precoProduto = 25;
const quantidade = 3;
const valorTotal = precoProduto * quantidade;

console.log(valorTotal);
```

## Exercício 3 — Par ou ímpar

Crie uma variável chamada `numero`.

Use o operador `%` para descobrir se o número é par.

Se o resto da divisão por 2 for `0`, mostre:

```text
Número par
```

Caso contrário, mostre:

```text
Número ímpar
```

## Exercício 4 — Pode dirigir?

Crie uma variável `idade`.

Se a idade for maior ou igual a 18, mostre:

```text
Pode dirigir
```

Caso contrário, mostre:

```text
Não pode dirigir
```

## Exercício 5 — Média do aluno

Crie duas notas.

Calcule a média.

Se a média for maior ou igual a 7, mostre:

```text
Aprovado
```

Se a média for maior ou igual a 5 e menor que 7, mostre:

```text
Recuperação
```

Caso contrário, mostre:

```text
Reprovado
```

## Exercício 6 — Login simples

Crie as variáveis:

- `usuario`;
- `senha`;

Regras:

- usuário correto: `"admin"`;
- senha correta: `"1234"`.

Se usuário e senha estiverem corretos, mostre:

```text
Login realizado com sucesso
```

Caso contrário, mostre:

```text
Usuário ou senha inválidos
```

Use `&&`.

## Exercício 7 — Ternário

Crie uma variável `idade`.

Use operador ternário para criar uma variável `situacao`.

Se a idade for maior ou igual a 18, `situacao` deve receber:

```text
Maior de idade
```

Caso contrário:

```text
Menor de idade
```

Mostre `situacao` no console.

---

## 19. Resumo da aula

Nesta aula, você viu que:

- JavaScript é uma linguagem de programação;
- JavaScript é uma ferramenta importante, mas não resolve tudo sozinho;
- `console.log` será usado para observar saídas;
- variáveis guardam valores;
- `const` é usado quando o valor não deve ser reatribuído;
- `let` é usado quando o valor pode mudar;
- `var` existe, mas não será nosso padrão;
- JavaScript possui tipos como `number`, `string`, `boolean`, `function`, `object`, `undefined` e `null`;
- `typeof` mostra o tipo de um valor;
- JavaScript possui tipagem dinâmica;
- bons nomes de variáveis ajudam a ler e manter o código;
- operadores aritméticos fazem contas;
- operadores condicionais comparam valores;
- `if`, `else if` e `else` permitem tomar decisões;
- ternário pode ser usado em condições simples;
- `&&`, `||` e `!` ajudam a combinar ou inverter condições.

O mais importante agora é praticar.

Você não precisa decorar tudo perfeitamente.

Você precisa testar, observar os resultados e começar a entender como cada parte participa do raciocínio.


