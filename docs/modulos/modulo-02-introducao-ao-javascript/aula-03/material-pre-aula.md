# Material Pré-aula — Aula 03: Arrays e Estrutura de Repetição com for

Este material apresenta o conteúdo completo da Aula 03.

Na aula anterior, você aprendeu a criar variáveis, realizar operações, comparar valores e escrever decisões com estruturas condicionais.

Agora vamos avançar para dois problemas muito comuns em programação:

1. Como guardar vários valores relacionados?
2. Como repetir uma ação sem copiar a mesma linha de código várias vezes?

Para resolver esses problemas, vamos estudar arrays e a estrutura de repetição `for`.

## O que você vai estudar nesta aula

Nesta aula, você vai estudar:

- uma retomada de entrada, processamento e saída;
- como usar template literals para montar mensagens;
- o que é um array;
- como criar um array;
- como acessar itens pelo índice;
- por que o primeiro índice é `0`;
- como alterar um item;
- como adicionar e remover itens;
- como consultar a quantidade de itens com `length`;
- por que estruturas de repetição são necessárias;
- como funciona a estrutura de repetição `for`;
- inicialização, condição de parada e atualização;
- como percorrer arrays usando `for`;
- como combinar arrays, repetição e condicionais.

O objetivo não é decorar uma fórmula.

O objetivo é entender qual problema o `for` resolve e acompanhar o fluxo da repetição com clareza.

---

## 1. Retomada: entrada, processamento e saída

Na Aula 01, você aprendeu a organizar problemas usando três partes:

```text
ENTRADA -> PROCESSAMENTO -> SAÍDA
```

Na Aula 02, começamos a transformar esse raciocínio em código JavaScript.

Vamos retomar com um exemplo.

### Problema

Calcular o valor total de uma compra.

### Entrada

Os dados necessários são:

- preço do produto;
- quantidade comprada.

Em JavaScript:

```js
const precoProduto = 25;
const quantidade = 3;
```

### Processamento

Precisamos multiplicar o preço pela quantidade:

```js
const valorTotal = precoProduto * quantidade;
```

### Saída

Precisamos mostrar o resultado:

```js
console.log(valorTotal);
```

### Código completo

```js
const precoProduto = 25;
const quantidade = 3;
const valorTotal = precoProduto * quantidade;

console.log(valorTotal);
```

Resultado:

```text
75
```

Essa estrutura continua importante nesta aula.

Quando trabalharmos com arrays e repetição, ainda teremos:

- dados de entrada;
- processamento;
- resultado de saída.

---

## 2. Template literals

Até agora, usamos `console.log` para mostrar textos e valores.

Exemplo:

```js
const nome = "Ana";
const idade = 20;

console.log("Nome:", nome);
console.log("Idade:", idade);
```

Também podemos montar uma mensagem usando template literals.

Template literal é uma forma de criar textos usando crase:

```js
const nome = "Ana";
const idade = 20;

console.log(`Olá, ${nome}! Você tem ${idade} anos.`);
```

Resultado:

```text
Olá, Ana! Você tem 20 anos.
```

## 2.1 Como funciona?

Uma template literal usa:

- crase para abrir e fechar o texto;
- `${}` para inserir um valor dentro do texto.

Exemplo:

```js
const produto = "Teclado";
const preco = 150;

console.log(`O produto ${produto} custa R$ ${preco}.`);
```

Resultado:

```text
O produto Teclado custa R$ 150.
```

## 2.2 Por que vamos usar template literals?

Elas deixam mensagens com variáveis mais fáceis de ler.

Compare:

```js
const nome = "Carlos";
const nota = 8;

console.log("O aluno " + nome + " tirou a nota " + nota + ".");
```

Com:

```js
const nome = "Carlos";
const nota = 8;

console.log(`O aluno ${nome} tirou a nota ${nota}.`);
```

As duas formas funcionam.

A partir de agora, vamos preferir template literals quando precisarmos montar mensagens com valores.

---

## 3. Arrays: guardando vários valores relacionados

Imagine que queremos guardar o nome de três alunos:

```js
const aluno1 = "Ana";
const aluno2 = "Bruno";
const aluno3 = "Carla";

console.log(aluno1);
console.log(aluno2);
console.log(aluno3);
```

Esse código funciona.

Mas imagine que a turma possui 30 alunos.

Criar uma variável para cada aluno deixaria o código repetitivo e difícil de manter.

Os valores têm algo em comum: todos representam nomes de alunos.

Podemos organizar esses valores em uma única lista.

Em JavaScript, usamos um array para representar essa lista.

```js
const alunos = ["Ana", "Bruno", "Carla"];

console.log(alunos);
```

Resultado:

```text
[ 'Ana', 'Bruno', 'Carla' ]
```

Array é uma estrutura usada para guardar vários valores em uma lista ordenada.

## 3.1 Criando arrays

Arrays são escritos com colchetes.

Cada item é separado por vírgula.

Array com textos:

```js
const frutas = ["maçã", "banana", "uva"];
```

Array com números:

```js
const notas = [8, 6, 9];
```

Array com booleanos:

```js
const presencas = [true, true, false];
```

Array vazio:

```js
const tarefas = [];
```

Use arrays quando precisar guardar vários valores relacionados em uma sequência.

---

## 4. Acessando elementos de um array

Cada item de um array possui uma posição.

Essa posição é chamada de índice.

Em JavaScript, o primeiro índice é `0`.

Observe:

```js
const frutas = ["maçã", "banana", "uva"];
```

Podemos representar as posições assim:

```text
Índice:   0         1         2
Valor:  maçã      banana     uva
```

Para acessar um item, escrevemos o nome do array e o índice entre colchetes:

```js
const frutas = ["maçã", "banana", "uva"];

console.log(frutas[0]);
console.log(frutas[1]);
console.log(frutas[2]);
```

Resultado:

```text
maçã
banana
uva
```

## 4.1 O primeiro índice é zero

Este ponto exige atenção:

- primeiro item: índice `0`;
- segundo item: índice `1`;
- terceiro item: índice `2`.

O índice não é a quantidade de itens.

Ele representa a posição usada para acessar um item.

## 4.2 Índice inexistente

Se tentarmos acessar uma posição que não existe, o resultado será `undefined`.

```js
const frutas = ["maçã", "banana", "uva"];

console.log(frutas[5]);
```

Resultado:

```text
undefined
```

---

## 5. Alterando valores de um array

Podemos substituir um item existente usando o índice.

```js
const frutas = ["maçã", "banana", "uva"];

frutas[1] = "laranja";

console.log(frutas);
```

Resultado:

```text
[ 'maçã', 'laranja', 'uva' ]
```

O item do índice `1` foi alterado.

## 5.1 Array criado com const pode mudar?

Observe que usamos `const`:

```js
const frutas = ["maçã", "banana", "uva"];
```

Mesmo assim, conseguimos alterar um item:

```js
frutas[1] = "laranja";
```

Isso acontece porque não estamos colocando outro array na variável.

Estamos alterando um item dentro do array existente.

Este código gera erro:

```js
const frutas = ["maçã", "banana"];

frutas = ["uva", "laranja"];
```

A variável criada com `const` não pode receber outro valor.

Por enquanto, guarde esta regra prática:

- podemos alterar itens dentro de um array criado com `const`;
- não podemos reatribuir a variável para outro array.

---

## 6. Adicionando e removendo elementos

Arrays podem ganhar ou perder itens.

Nesta aula, vamos começar com dois métodos:

- `push`;
- `pop`.

## 6.1 Adicionando um item com push

O método `push` adiciona um item no final do array.

```js
const frutas = ["maçã", "banana"];

frutas.push("uva");

console.log(frutas);
```

Resultado:

```text
[ 'maçã', 'banana', 'uva' ]
```

## 6.2 Removendo um item com pop

O método `pop` remove o último item do array.

```js
const frutas = ["maçã", "banana", "uva"];

frutas.pop();

console.log(frutas);
```

Resultado:

```text
[ 'maçã', 'banana' ]
```

O método `pop` também retorna o item removido.

```js
const frutas = ["maçã", "banana", "uva"];
const frutaRemovida = frutas.pop();

console.log(`Fruta removida: ${frutaRemovida}`);
console.log(frutas);
```

Resultado:

```text
Fruta removida: uva
[ 'maçã', 'banana' ]
```

---

## 7. Tamanho do array com length

A propriedade `length` informa quantos itens existem em um array.

```js
const frutas = ["maçã", "banana", "uva"];

console.log(frutas.length);
```

Resultado:

```text
3
```

## 7.1 Índice e quantidade são diferentes

Observe novamente:

```text
Índice:   0         1         2
Valor:  maçã      banana     uva
```

O array possui:

- três itens;
- índices `0`, `1` e `2`;
- `length` igual a `3`.

O último índice é uma unidade menor que a quantidade de itens.

Podemos acessar o último item assim:

```js
const frutas = ["maçã", "banana", "uva"];
const ultimoIndice = frutas.length - 1;

console.log(frutas[ultimoIndice]);
```

Resultado:

```text
uva
```

---

## 8. Por que precisamos aprender estruturas de repetição?

Imagine que queremos mostrar uma mensagem para cada aluno:

```js
const alunos = ["Ana", "Bruno", "Carla", "Diego"];

console.log(`Olá, ${alunos[0]}!`);
console.log(`Olá, ${alunos[1]}!`);
console.log(`Olá, ${alunos[2]}!`);
console.log(`Olá, ${alunos[3]}!`);
```

Resultado:

```text
Olá, Ana!
Olá, Bruno!
Olá, Carla!
Olá, Diego!
```

Esse código funciona.

Mas existe um problema: repetimos quase a mesma linha várias vezes.

Se existissem 100 alunos, precisaríamos escrever 100 linhas.

Isso tornaria o código:

- longo;
- repetitivo;
- cansativo de escrever;
- difícil de alterar;
- mais sujeito a erros.

Podemos resolver o mesmo problema usando uma estrutura de repetição:

```js
const alunos = ["Ana", "Bruno", "Carla", "Diego"];

for (let indice = 0; indice < alunos.length; indice++) {
  console.log(`Olá, ${alunos[indice]}!`);
}
```

Resultado:

```text
Olá, Ana!
Olá, Bruno!
Olá, Carla!
Olá, Diego!
```

A saída é a mesma.

Mas agora o código funciona mesmo se adicionarmos mais alunos ao array.

```js
const alunos = ["Ana", "Bruno", "Carla", "Diego", "Elisa", "Fábio"];

for (let indice = 0; indice < alunos.length; indice++) {
  console.log(`Olá, ${alunos[indice]}!`);
}
```

Não foi necessário copiar novos `console.log`.

Estruturas de repetição existem para executar uma ação várias vezes de forma controlada.

Elas também são chamadas de loops ou laços de repetição.

---

## 9. Estrutura de repetição for

O `for` é uma estrutura de repetição.

Ele é muito útil quando precisamos controlar:

- onde a repetição começa;
- até quando ela continua;
- como o valor de controle muda a cada repetição.

Exemplo:

```js
for (let contador = 1; contador <= 5; contador++) {
  console.log(contador);
}
```

Resultado:

```text
1
2
3
4
5
```

## 9.1 Estrutura geral do for

Observe:

```js
for (let contador = 1; contador <= 5; contador++) {
  console.log(contador);
}
```

O `for` possui três partes principais:

```text
inicialização; condição de parada; atualização
```

Visualmente:

```js
for (let contador = 1; contador <= 5; contador++) {
  console.log(contador);
}
```

Podemos separar:

```text
Inicialização:     let contador = 1
Condição:          contador <= 5
Atualização:       contador++
Código repetido:   console.log(contador)
```

## 9.2 Inicialização

A inicialização define o valor inicial da variável de controle.

```js
let contador = 1
```

Neste exemplo, a repetição começa com o valor `1`.

## 9.3 Condição de parada

A condição define até quando a repetição deve continuar.

```js
contador <= 5
```

Enquanto essa comparação resultar em `true`, o bloco será executado.

Quando resultar em `false`, a repetição termina.

## 9.4 Atualização

A atualização modifica a variável de controle depois de cada repetição.

```js
contador++
```

Esse código aumenta o contador em `1`.

Sem atualização, o contador não avançaria corretamente.

## 9.5 Bloco de código

O código entre chaves será executado em cada repetição:

```js
{
  console.log(contador);
}
```

## 9.6 Acompanhando o fluxo passo a passo

Considere:

```js
for (let contador = 1; contador <= 3; contador++) {
  console.log(`Contador: ${contador}`);
}
```

O computador executa assim:

| Etapa | Valor de `contador` | `contador <= 3` | Ação |
| --- | --- | --- | --- |
| 1 | `1` | `true` | mostra `Contador: 1` |
| 2 | `2` | `true` | mostra `Contador: 2` |
| 3 | `3` | `true` | mostra `Contador: 3` |
| 4 | `4` | `false` | encerra a repetição |

Resultado:

```text
Contador: 1
Contador: 2
Contador: 3
```

---

## 10. Percorrendo arrays com for

Podemos combinar arrays e `for`.

Exemplo:

```js
const frutas = ["maçã", "banana", "uva"];

for (let indice = 0; indice < frutas.length; indice++) {
  console.log(frutas[indice]);
}
```

Resultado:

```text
maçã
banana
uva
```

## 10.1 Entendendo cada parte

Observe:

```js
for (let indice = 0; indice < frutas.length; indice++) {
  console.log(frutas[indice]);
}
```

### Inicialização

```js
let indice = 0
```

Começamos no índice do primeiro item.

### Condição de parada

```js
indice < frutas.length
```

Continuamos enquanto o índice for menor que a quantidade de itens.

### Atualização

```js
indice++
```

Avançamos para o próximo índice depois de cada repetição.

### Código repetido

```js
console.log(frutas[indice]);
```

Mostramos o item da posição atual.

## 10.2 Por que usamos menor que?

O array possui três itens:

```js
const frutas = ["maçã", "banana", "uva"];
```

Seu `length` é `3`.

Mas seus índices válidos são:

```text
0
1
2
```

Por isso, usamos:

```js
indice < frutas.length
```

Se usarmos `<=`, tentaremos acessar o índice `3`, que não existe:

```js
const frutas = ["maçã", "banana", "uva"];

for (let indice = 0; indice <= frutas.length; indice++) {
  console.log(frutas[indice]);
}
```

Resultado:

```text
maçã
banana
uva
undefined
```

Esse é um erro comum no início.

---

## 11. Combinando for e condicionais

Podemos usar uma condicional dentro de uma repetição.

Exemplo:

```js
const notas = [8, 5, 9, 4];

for (let indice = 0; indice < notas.length; indice++) {
  const nota = notas[indice];

  if (nota >= 7) {
    console.log(`Nota aprovada: ${nota}`);
  } else {
    console.log(`Nota abaixo de 7: ${nota}`);
  }
}
```

Resultado:

```text
Nota aprovada: 8
Nota abaixo de 7: 5
Nota aprovada: 9
Nota abaixo de 7: 4
```

O código percorre cada nota.

Para cada valor, ele toma uma decisão.

## 11.1 Relembrando entrada, processamento e saída

Neste exemplo:

### Entrada

```js
const notas = [8, 5, 9, 4];
```

### Processamento

```js
for (let indice = 0; indice < notas.length; indice++) {
  const nota = notas[indice];

  if (nota >= 7) {
    console.log(`Nota aprovada: ${nota}`);
  } else {
    console.log(`Nota abaixo de 7: ${nota}`);
  }
}
```

O processamento percorre o array e verifica cada nota.

### Saída

As mensagens são mostradas no console:

```text
Nota aprovada: 8
Nota abaixo de 7: 5
Nota aprovada: 9
Nota abaixo de 7: 4
```

---

## 12. Somando valores com for

Também podemos usar `for` para somar valores.

```js
const precos = [10, 20, 15];
let total = 0;

for (let indice = 0; indice < precos.length; indice++) {
  total += precos[indice];
}

console.log(`Total: R$ ${total}`);
```

Resultado:

```text
Total: R$ 45
```

## 12.1 Acompanhando a soma

A variável `total` começa com `0`.

Depois:

1. Soma `10`, então o total vira `10`.
2. Soma `20`, então o total vira `30`.
3. Soma `15`, então o total vira `45`.

A variável `total` guarda o resultado acumulado ao longo da repetição.

---

## 13. Exercício-modelo comentado

Este exercício pode ser resolvido junto com o instrutor.

### Enunciado

Crie um programa que analise uma lista de números.

O programa deve:

- mostrar cada número;
- informar se o número é par ou ímpar;
- contar quantos números são pares;
- mostrar a quantidade final de números pares.

Use este array:

```js
const numeros = [3, 8, 10, 7, 12];
```

### Antes do código: entrada, processamento e saída

#### Entrada

```js
const numeros = [3, 8, 10, 7, 12];
```

#### Processamento

Precisamos:

1. percorrer o array;
2. acessar um número por vez;
3. verificar se o resto da divisão por `2` é igual a `0`;
4. aumentar um contador quando o número for par.

#### Saída

Precisamos mostrar:

- a classificação de cada número;
- a quantidade final de números pares.

### Resolução comentada

```js
const numeros = [3, 8, 10, 7, 12];
let quantidadePares = 0;

for (let indice = 0; indice < numeros.length; indice++) {
  const numero = numeros[indice];

  if (numero % 2 === 0) {
    console.log(`${numero} é par`);
    quantidadePares++;
  } else {
    console.log(`${numero} é ímpar`);
  }
}

console.log(`Quantidade de números pares: ${quantidadePares}`);
```

Resultado:

```text
3 é ímpar
8 é par
10 é par
7 é ímpar
12 é par
Quantidade de números pares: 3
```

### O que observar

Neste código:

- `numeros` guarda os dados de entrada;
- `quantidadePares` começa com `0`;
- o `for` percorre todos os índices válidos;
- `numeros[indice]` acessa o número atual;
- `% 2 === 0` verifica se o número é par;
- `quantidadePares++` aumenta o contador;
- template literals montam mensagens com os valores;
- o último `console.log` apresenta o resultado final.

---

## 14. Código completo para testar

Copie este código para um arquivo chamado `aula-03.js` e execute no ambiente indicado pelo instrutor.

```js
const notas = [8, 5, 9, 6, 7];
let soma = 0;
let quantidadeAprovadas = 0;

console.log(`Quantidade de notas: ${notas.length}`);

for (let indice = 0; indice < notas.length; indice++) {
  const nota = notas[indice];

  soma += nota;

  if (nota >= 7) {
    quantidadeAprovadas++;
  }
}

const media = soma / notas.length;

console.log(`Soma das notas: ${soma}`);
console.log(`Média: ${media}`);
console.log(`Quantidade de notas aprovadas: ${quantidadeAprovadas}`);
```

Resultado:

```text
Quantidade de notas: 5
Soma das notas: 35
Média: 7
Quantidade de notas aprovadas: 3
```

Depois de executar, tente:

- alterar uma nota;
- adicionar uma nota com `push`;
- remover a última nota com `pop`;
- observar como a soma, a média e a quantidade mudam.

---

## 15. Exercícios de fixação

Faça estes exercícios em um arquivo `.js`.

Use `console.log` e template literals para mostrar os resultados.

## Exercício 1 — Lista de cidades

Crie um array com quatro cidades.

Mostre:

- o array completo;
- a primeira cidade;
- a última cidade usando `length`;
- a quantidade de cidades.

## Exercício 2 — Lista de tarefas

Crie um array com duas tarefas.

Depois:

- adicione uma tarefa com `push`;
- altere a primeira tarefa;
- remova a última tarefa com `pop`;
- mostre o array final.

## Exercício 3 — Contagem simples

Use `for` para mostrar os números de `1` até `10`.

## Exercício 4 — Percorrendo nomes

Crie um array com quatro nomes.

Use `for` para mostrar cada nome em uma mensagem:

```text
Olá, Ana!
```

## Exercício 5 — Soma de valores

Crie:

```js
const valores = [10, 20, 30, 40];
```

Use `for` para somar todos os valores.

Mostre o resultado final.

## Exercício 6 — Números pares

Crie:

```js
const numeros = [3, 8, 10, 7, 12];
```

Use `for` e uma condicional para mostrar apenas os números pares.

---

## 16. Resumo da aula

Nesta aula, você viu que:

- entrada, processamento e saída continuam ajudando a organizar problemas;
- template literals facilitam a criação de mensagens com valores;
- arrays guardam vários valores relacionados em uma lista;
- arrays usam colchetes;
- cada item possui um índice;
- o primeiro índice é `0`;
- podemos alterar um item usando seu índice;
- `push` adiciona um item no final;
- `pop` remove um item do final;
- `length` informa a quantidade de itens;
- estruturas de repetição evitam repetir manualmente o mesmo código;
- `for` possui inicialização, condição de parada e atualização;
- podemos usar `for` para percorrer arrays;
- condicionais podem ser usadas dentro de repetições;
- variáveis podem acumular resultados ou contar ocorrências.

O mais importante agora é praticar.

Preste atenção especial:

- ao índice inicial `0`;
- à diferença entre índice e quantidade;
- à condição de parada;
- à atualização;
- ao item atual acessado com `array[indice]`.

