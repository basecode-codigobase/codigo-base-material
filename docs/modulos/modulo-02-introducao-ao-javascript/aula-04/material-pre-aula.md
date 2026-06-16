# Material Pré-aula — Aula 04: Funções

Este material apresenta o conteúdo completo da Aula 04.

Na aula anterior, você aprendeu a usar arrays para guardar vários valores e `for` para repetir ações.

Agora vamos estudar funções.

Funções são uma das estruturas mais importantes da programação, porque ajudam a organizar código, evitar repetição e dar nome a uma sequência de passos.

## O que você vai estudar nesta aula

Nesta aula, você vai estudar:

- por que usamos funções;
- como criar uma função;
- como chamar uma função;
- funções sem parâmetros;
- funções com parâmetros;
- diferença inicial entre parâmetro e argumento;
- funções com mais de um parâmetro;
- `return`;
- diferença entre mostrar um valor e retornar um valor;
- tipos de valores que parâmetros podem receber;
- funções recebendo arrays;
- arrow functions.

O objetivo não é decorar todos os formatos possíveis de função.

O objetivo é entender que função é uma forma de organizar uma ação para poder reutilizá-la com clareza.

---

## 1. Por que usamos funções?

Imagine que queremos mostrar mensagens de boas-vindas para três pessoas:

```js
const nome1 = "Ana";
console.log(`Olá, ${nome1}! Seja bem-vinda.`);

const nome2 = "Bruno";
console.log(`Olá, ${nome2}! Seja bem-vindo.`);

const nome3 = "Carla";
console.log(`Olá, ${nome3}! Seja bem-vinda.`);
```

Esse código funciona.

Mas ele tem um problema: a mesma ideia está sendo repetida várias vezes.

A parte que muda é o nome.

A ação é praticamente a mesma:

```text
mostrar uma mensagem de boas-vindas
```

Podemos criar uma função para representar essa ação.

```js
function mostrarSaudacao(nome) {
  console.log(`Olá, ${nome}! Seja bem-vindo(a).`);
}

mostrarSaudacao("Ana");
mostrarSaudacao("Bruno");
mostrarSaudacao("Carla");
```

Resultado:

```text
Olá, Ana! Seja bem-vindo(a).
Olá, Bruno! Seja bem-vindo(a).
Olá, Carla! Seja bem-vindo(a).
```

Agora temos uma ação com nome: `mostrarSaudacao`.

Isso deixa o código mais organizado e mais fácil de reaproveitar.

## 1.1 O que uma função ajuda a fazer?

Funções ajudam a:

- evitar repetição desnecessária;
- organizar o código em partes menores;
- dar nome a uma ação;
- reutilizar uma lógica;
- testar uma parte do código com mais facilidade;
- separar entrada, processamento e saída.

---

## 2. O que é uma função?

Função é um bloco de código que recebe um nome e pode ser executado quando for chamado.

Exemplo:

```js
function mostrarMensagem() {
  console.log("Olá, JavaScript!");
}

mostrarMensagem();
```

Resultado:

```text
Olá, JavaScript!
```

Nesse exemplo:

- `function` indica que estamos criando uma função;
- `mostrarMensagem` é o nome da função;
- o bloco entre chaves contém o código da função;
- `mostrarMensagem()` chama a função.

## 2.1 Criar não é a mesma coisa que chamar

Este código cria a função:

```js
function mostrarMensagem() {
  console.log("Olá, JavaScript!");
}
```

Mas nada aparece no console ainda.

Para executar a função, precisamos chamá-la:

```js
mostrarMensagem();
```

Código completo:

```js
function mostrarMensagem() {
  console.log("Olá, JavaScript!");
}

mostrarMensagem();
```

---

## 3. Funções sem parâmetros

Uma função sem parâmetros não precisa receber informação externa para executar sua tarefa.

Exemplo:

```js
function mostrarBoasVindas() {
  console.log("Boas-vindas ao Código Base!");
}

mostrarBoasVindas();
```

Resultado:

```text
Boas-vindas ao Código Base!
```

Outro exemplo:

```js
function mostrarLinha() {
  console.log("--------------------");
}

mostrarLinha();
console.log("Relatório de notas");
mostrarLinha();
```

Resultado:

```text
--------------------
Relatório de notas
--------------------
```

Use funções sem parâmetros quando a ação não depende de um valor recebido na chamada.

---

## 4. Funções com parâmetros

Parâmetros permitem que uma função receba informações.

Exemplo:

```js
function mostrarSaudacao(nome) {
  console.log(`Olá, ${nome}!`);
}

mostrarSaudacao("Ana");
mostrarSaudacao("Bruno");
```

Resultado:

```text
Olá, Ana!
Olá, Bruno!
```

Nesse exemplo:

- `nome` é o parâmetro;
- `"Ana"` e `"Bruno"` são argumentos enviados na chamada;
- a função usa o valor recebido para montar a mensagem.

## 4.1 Parâmetro e argumento

Parâmetro é o nome usado na criação da função.

```js
function mostrarSaudacao(nome) {
  console.log(`Olá, ${nome}!`);
}
```

Argumento é o valor enviado quando chamamos a função.

```js
mostrarSaudacao("Ana");
```

Para começar, pense assim:

- parâmetro: o que a função espera receber;
- argumento: o valor que você entrega para a função.

---

## 5. Funções com mais de um parâmetro

Uma função pode receber mais de um parâmetro.

Exemplo:

```js
function mostrarDadosAluno(nome, idade) {
  console.log(`Aluno: ${nome}`);
  console.log(`Idade: ${idade}`);
}

mostrarDadosAluno("Ana", 20);
```

Resultado:

```text
Aluno: Ana
Idade: 20
```

A ordem dos argumentos importa.

```js
mostrarDadosAluno(20, "Ana");
```

Neste caso, o JavaScript colocaria:

- `nome` recebendo `20`;
- `idade` recebendo `"Ana"`.

O código até pode executar, mas a lógica fica errada.

Por isso, escolha bons nomes e respeite a ordem dos argumentos.

---

## 6. return

Até agora, várias funções apenas mostraram mensagens com `console.log`.

Mas uma função também pode devolver um valor.

Para isso, usamos `return`.

Exemplo:

```js
function somar(numero1, numero2) {
  return numero1 + numero2;
}

const resultado = somar(10, 5);

console.log(`Resultado: ${resultado}`);
```

Resultado:

```text
Resultado: 15
```

## 6.1 Mostrar não é o mesmo que retornar

`console.log` mostra uma informação no console.

`return` devolve um valor para quem chamou a função.

Compare:

```js
function mostrarSoma(numero1, numero2) {
  console.log(numero1 + numero2);
}

const resultado = mostrarSoma(10, 5);

console.log(resultado);
```

Resultado:

```text
15
undefined
```

A função mostrou `15`, mas não retornou esse valor.

Agora veja:

```js
function somar(numero1, numero2) {
  return numero1 + numero2;
}

const resultado = somar(10, 5);

console.log(resultado);
```

Resultado:

```text
15
```

Agora a função devolveu o resultado, e conseguimos guardar esse valor na variável `resultado`.

## 6.2 O return encerra a função

Quando o JavaScript encontra um `return`, a função termina.

```js
function verificarIdade(idade) {
  if (idade >= 18) {
    return "Maior de idade";
  }

  return "Menor de idade";
}

console.log(verificarIdade(20));
console.log(verificarIdade(15));
```

Resultado:

```text
Maior de idade
Menor de idade
```

---

## 7. Tipos de valores que uma função pode receber

Parâmetros podem receber diferentes tipos de valores.

Nesta aula, vamos praticar principalmente:

- `number`;
- `string`;
- `boolean`;
- arrays.

Existem outros tipos e estruturas, mas vamos manter o foco no que já foi trabalhado até aqui.

## 7.1 Parâmetro recebendo number

```js
function dobrar(numero) {
  return numero * 2;
}

console.log(dobrar(4));
```

Resultado:

```text
8
```

## 7.2 Parâmetro recebendo string

```js
function montarMensagem(nome) {
  return `Olá, ${nome}!`;
}

const mensagem = montarMensagem("Ana");

console.log(mensagem);
```

Resultado:

```text
Olá, Ana!
```

## 7.3 Parâmetro recebendo boolean

```js
function verificarCadastroAtivo(cadastroAtivo) {
  if (cadastroAtivo) {
    return "Cadastro ativo";
  }

  return "Cadastro inativo";
}

console.log(verificarCadastroAtivo(true));
console.log(verificarCadastroAtivo(false));
```

Resultado:

```text
Cadastro ativo
Cadastro inativo
```

## 7.4 Parâmetro recebendo array

Uma função também pode receber um array.

Exemplo:

```js
function mostrarNomes(nomes) {
  for (let indice = 0; indice < nomes.length; indice++) {
    console.log(`Nome: ${nomes[indice]}`);
  }
}

const alunos = ["Ana", "Bruno", "Carla"];

mostrarNomes(alunos);
```

Resultado:

```text
Nome: Ana
Nome: Bruno
Nome: Carla
```

---

## 8. Função que processa array e retorna resultado

Podemos combinar:

- função;
- parâmetro;
- array;
- `for`;
- acumulador;
- `return`.

Exemplo:

```js
function calcularMedia(notas) {
  let soma = 0;

  for (let indice = 0; indice < notas.length; indice++) {
    soma += notas[indice];
  }

  return soma / notas.length;
}

const notasDaTurma = [8, 7, 9];
const media = calcularMedia(notasDaTurma);

console.log(`Média: ${media}`);
```

Resultado:

```text
Média: 8
```

## 8.1 Entrada, processamento e saída

Neste exemplo:

### Entrada

```js
const notasDaTurma = [8, 7, 9];
```

O array é enviado para a função.

### Processamento

```js
function calcularMedia(notas) {
  let soma = 0;

  for (let indice = 0; indice < notas.length; indice++) {
    soma += notas[indice];
  }

  return soma / notas.length;
}
```

A função percorre o array, soma as notas e calcula a média.

### Saída

```js
const media = calcularMedia(notasDaTurma);

console.log(`Média: ${media}`);
```

A função retorna a média, e o `console.log` mostra o resultado.

---

## 9. Arrow functions

Arrow function é outra forma de escrever funções em JavaScript.

Exemplo usando `function`:

```js
function somar(numero1, numero2) {
  return numero1 + numero2;
}

console.log(somar(10, 5));
```

Exemplo usando arrow function:

```js
const somar = (numero1, numero2) => {
  return numero1 + numero2;
};

console.log(somar(10, 5));
```

Resultado:

```text
15
```

As duas versões acima resolvem o mesmo problema.

## 9.1 Arrow function com retorno curto

Quando a função é simples e apenas retorna um valor, podemos escrever de forma mais curta:

```js
const dobrar = (numero) => numero * 2;

console.log(dobrar(4));
```

Resultado:

```text
8
```

Essa forma significa:

> receba `numero` e retorne `numero * 2`.

## 9.2 Quando usar arrow function agora?

Neste momento, use arrow functions para exemplos simples.

Priorize entender:

- qual é a entrada;
- qual é o processamento;
- qual é a saída;
- se a função apenas mostra algo ou retorna algo.

Comparações mais avançadas entre funções declaradas e arrow functions ficam para depois.

---

## 10. Exercício-modelo comentado

Este exercício pode ser resolvido junto com o instrutor.

### Enunciado

Crie uma função chamada `calcularTotalCompra`.

A função deve:

- receber um array de preços;
- somar todos os preços;
- retornar o total.

Depois, chame a função usando este array:

```js
const precos = [20, 15, 30];
```

Mostre o resultado no console.

### Antes do código: entrada, processamento e saída

#### Entrada

```js
const precos = [20, 15, 30];
```

#### Processamento

Precisamos:

1. criar uma função;
2. receber o array por parâmetro;
3. criar uma variável `total`;
4. percorrer o array com `for`;
5. somar cada preço;
6. retornar o total.

#### Saída

Mostrar o total no console.

### Resolução comentada

```js
function calcularTotalCompra(precos) {
  let total = 0;

  for (let indice = 0; indice < precos.length; indice++) {
    total += precos[indice];
  }

  return total;
}

const precos = [20, 15, 30];
const totalCompra = calcularTotalCompra(precos);

console.log(`Total da compra: R$ ${totalCompra}`);
```

Resultado:

```text
Total da compra: R$ 65
```

### O que observar

Neste código:

- `calcularTotalCompra` é o nome da função;
- `precos` é o parâmetro;
- `[20, 15, 30]` é o array usado como argumento;
- `total` é um acumulador;
- o `for` percorre o array;
- `return total` devolve o resultado;
- `console.log` mostra o resultado final.

---

## 11. Código completo para testar

Copie este código para um arquivo chamado `aula-04.js` e execute no ambiente indicado pelo instrutor.

```js
function calcularQuantidadeAprovadas(notas) {
  let quantidadeAprovadas = 0;

  for (let indice = 0; indice < notas.length; indice++) {
    if (notas[indice] >= 7) {
      quantidadeAprovadas++;
    }
  }

  return quantidadeAprovadas;
}

function montarResumo(nomeDaTurma, notas) {
  const quantidadeAprovadas = calcularQuantidadeAprovadas(notas);

  return `A turma ${nomeDaTurma} teve ${quantidadeAprovadas} notas aprovadas.`;
}

const notas = [8, 5, 9, 6, 7];
const resumo = montarResumo("Fundamentos", notas);

console.log(resumo);
```

Resultado:

```text
A turma Fundamentos teve 3 notas aprovadas.
```

Depois de executar, tente:

- alterar as notas;
- alterar o nome da turma;
- criar outra chamada para `montarResumo`;
- explicar qual função chama a outra.

---

## 12. Exercícios de fixação

Faça estes exercícios em um arquivo `.js`.

Use `console.log` e template literals para mostrar os resultados.

## Exercício 1 — Mensagem fixa

Crie uma função sem parâmetros chamada `mostrarMensagemInicial`.

Ela deve mostrar:

```text
Iniciando o sistema...
```

Depois, chame a função.

## Exercício 2 — Saudação personalizada

Crie uma função chamada `mostrarSaudacao`.

Ela deve receber um nome e mostrar:

```text
Olá, Ana!
```

Teste com pelo menos dois nomes diferentes.

## Exercício 3 — Dobro

Crie uma função chamada `calcularDobro`.

Ela deve receber um número e retornar o dobro.

Mostre o resultado no console.

## Exercício 4 — Maior de idade

Crie uma função chamada `verificarMaioridade`.

Ela deve receber uma idade.

Se a idade for maior ou igual a `18`, retorne `"Maior de idade"`.

Caso contrário, retorne `"Menor de idade"`.

## Exercício 5 — Mostrar nomes

Crie uma função chamada `mostrarNomes`.

Ela deve receber um array de nomes e mostrar cada nome usando `for`.

## Exercício 6 — Calcular média

Crie uma função chamada `calcularMedia`.

Ela deve receber um array de notas, calcular a média e retornar o resultado.

## Exercício 7 — Arrow function

Crie uma arrow function chamada `calcularTriplo`.

Ela deve receber um número e retornar o triplo.

---

## 13. Resumo da aula

Nesta aula, você viu que:

- funções ajudam a organizar código;
- funções evitam repetição desnecessária;
- funções dão nome a uma sequência de passos;
- criar uma função não é o mesmo que chamar uma função;
- funções sem parâmetros executam uma ação sem receber valor externo;
- funções com parâmetros recebem informações;
- parâmetro é o nome esperado pela função;
- argumento é o valor enviado na chamada;
- `return` devolve um valor;
- `console.log` mostra uma informação;
- parâmetros podem receber `number`, `string`, `boolean` e arrays;
- funções podem processar arrays usando `for`;
- arrow functions são outra forma de escrever funções.

O mais importante agora é praticar.

Preste atenção especial:

- ao nome da função;
- à chamada da função;
- aos parâmetros;
- aos argumentos;
- à diferença entre `console.log` e `return`;
- ao tipo de valor que a função espera receber.


