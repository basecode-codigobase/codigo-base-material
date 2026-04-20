# Material Pré-aula — Aula 01: Unix e Shell

Este material apresenta o conteúdo completo da Aula 01.

Ele serve para o aluno chegar à aula com mais familiaridade e também para consultar depois. Não é necessário decorar tudo antes da aula. Durante o encontro ao vivo, o instrutor vai explicar os pontos principais, mostrar exemplos novos e conduzir uma prática real no terminal.

## Como usar este material

Leia com calma e tente identificar quatro tipos de informação.

| Nível | O que significa |
|---|---|
| Essencial | O aluno precisa entender e praticar na Aula 01. |
| Importante | Ajuda a compreender melhor, mas não precisa virar domínio imediato. |
| Saiba que existe | O aluno só precisa reconhecer que existe, sem aprofundar agora. |
| Não aprofundar agora | Conteúdo que pode aparecer como contexto, mas não é objetivo desta aula. |

Sempre que estiver em dúvida, priorize estas perguntas:

- Onde estou?
- O que existe aqui?
- Para onde quero ir?
- O que quero criar, ler, copiar, mover ou remover?
- Como verifico se funcionou?

---

## O que você vai aprender nesta aula

**Nível: Essencial**

Nesta aula, o aluno vai começar a usar o terminal para:

- identificar em qual pasta está;
- listar arquivos e pastas;
- entrar e sair de pastas;
- criar pastas;
- criar arquivos simples;
- ler arquivos de texto;
- escrever e acrescentar conteúdo em arquivos;
- copiar, renomear, mover e remover arquivos de teste;
- perceber que comandos dependem da pasta atual.

**Nível: Importante**

O aluno também vai começar a entender:

- o que são terminal, shell e kernel;
- a diferença entre terminal, editor, navegador e IDE;
- o que são arquivos, pastas, caminhos e diretório atual;
- por que comandos sem mensagem também podem ter funcionado;
- por que remover arquivos exige cuidado.

**Nível: Saiba que existe**

O aluno verá rapidamente que o terminal também permite:

- buscar texto em arquivos;
- contar linhas e palavras;
- visualizar partes de arquivos grandes;
- combinar comandos;
- usar símbolos como `>`, `>>`, `|`, `*` e `?`;
- consultar ajuda com comandos como `man` e `whatis`.

---

## Por que aprender terminal no começo do curso

**Nível: Importante**

No curso, o terminal será uma ferramenta de apoio para trabalhar com arquivos, pastas, projetos e comandos.

Ele será útil para:

- navegar até uma pasta de projeto;
- executar comandos indicados pelo instrutor;
- criar e organizar arquivos;
- entender melhor onde uma ação está acontecendo;
- preparar a base operacional para usar Git nas próximas aulas.

O objetivo desta aula não é transformar o aluno em especialista em terminal. O objetivo é reduzir o medo inicial e criar uma base operacional mínima para o restante do curso.

---

## Terminal, shell e kernel

**Nível: Importante**

Quando usamos comandos, existem algumas camadas trabalhando juntas.

| Conceito | Ideia principal |
|---|---|
| Kernel | Núcleo do sistema operacional. Controla recursos como arquivos, memória, processos e hardware. |
| Shell | Programa que interpreta comandos digitados pelo usuário. |
| Terminal | Janela onde digitamos comandos e vemos respostas. |

Uma forma simples de lembrar:

- o **terminal** é a janela;
- o **shell** entende o comando;
- o **kernel** executa a ação no sistema.

Exemplo:

```bash
pwd
```

Quando o aluno digita esse comando:

1. escreve no terminal;
2. o shell interpreta o comando;
3. o sistema consulta a pasta atual;
4. o terminal mostra a resposta.

**Nível: Não aprofundar agora**

Nesta aula, não vamos estudar processos, administração de sistema, permissões, estrutura interna completa do Unix ou funcionamento profundo do kernel.

---

## Terminal, editor, navegador e IDE

**Nível: Essencial**

Essas ferramentas aparecem juntas no curso, mas não fazem a mesma coisa.

| Ferramenta | Para que serve |
|---|---|
| Terminal | Digitar comandos e executar ações no computador. |
| Editor de código | Escrever e editar arquivos de código ou texto. |
| Navegador | Acessar sites e visualizar páginas web. |
| IDE | Ambiente mais completo para programar, geralmente com editor, terminal, extensões e ferramentas integradas. |

Exemplo prático:

1. O aluno escreve um arquivo no editor.
2. Usa o terminal para navegar até a pasta desse arquivo.
3. Pode abrir algo no navegador para visualizar uma página.
4. Pode usar uma IDE que reúna editor e terminal no mesmo ambiente.

---

## Arquivo, pasta, caminho e diretório atual

**Nível: Essencial**

Antes de decorar comandos, o aluno precisa entender estes termos.

| Termo | Significado |
|---|---|
| Arquivo | Item que guarda algum conteúdo, como texto, imagem ou código. |
| Pasta ou diretório | Lugar onde arquivos e outras pastas podem ficar guardados. |
| Caminho | Localização de uma pasta ou arquivo. |
| Diretório atual | Pasta em que o terminal está trabalhando neste momento. |

A ideia mais importante aqui é:

```text
Todo comando é executado a partir de algum lugar.
```

Esse lugar é o **diretório atual**.

Por isso, antes de agir no terminal, a pergunta principal é:

```text
Onde estou?
```

O comando para responder isso é:

```bash
pwd
```

---

## Caminho absoluto e caminho relativo

**Nível: Importante**

Um caminho indica onde uma pasta ou arquivo está.

### Caminho absoluto

Começa desde a origem principal do sistema.

Exemplo em Linux/macOS:

```bash
/home/aluno/estudos/aula-01
```

Exemplo em Windows:

```text
C:\Users\Aluno\Documents\estudos\aula-01
```

### Caminho relativo

Parte da pasta onde o terminal está agora.

Se o aluno está dentro de `estudos` e existe uma pasta `aula-01`, pode entrar nela assim:

```bash
cd aula-01
```

Não é preciso escrever o caminho completo.

**Nível: Essencial**

Para a Aula 01, o mais importante é entender:

- caminho absoluto mostra o endereço completo;
- caminho relativo depende de onde o terminal está;
- `pwd` ajuda a descobrir o caminho atual;
- `cd` muda a pasta atual.

---

## Como abrir o terminal

**Nível: Essencial**

Na aula, usaremos um terminal com comandos de shell.

Antes da aula:

- no **Windows**, use o terminal indicado pelo instrutor, preferencialmente **Git Bash** quando estiver disponível;
- no **macOS**, abra o app **Terminal**;
- no **Linux**, abra o app **Terminal** da sua distribuição;
- se estiver usando **VS Code**, localize o terminal integrado em `Terminal > New Terminal`.

Não se preocupe se ainda não souber usar a ferramenta. A aula começa justamente por esse ponto.

---

## Primeiro ciclo: onde estou e o que existe aqui

**Nível: Essencial**

Este é o ciclo mais importante da Aula 01:

```text
Onde estou? -> pwd
O que existe aqui? -> ls
```

### `pwd`

Mostra o caminho do diretório atual.

```bash
pwd
```

Exemplo de saída:

```bash
/home/aluno/estudos
```

Leia como:

```text
O terminal está trabalhando dentro da pasta estudos.
```

### `ls`

Lista arquivos e pastas do diretório atual.

```bash
ls
```

Exemplo de saída:

```bash
aula-01 anotacoes.txt exercicios
```

Isso significa que, na pasta atual, existem itens chamados:

- `aula-01`;
- `anotacoes.txt`;
- `exercicios`.

Alguns podem ser pastas, outros podem ser arquivos.

### Como verificar se um comando funcionou

**Nível: Essencial**

Alguns comandos não mostram mensagem quando dão certo.

Por exemplo, o `mkdir`, que cria uma pasta no diretório atual:

```bash
mkdir teste
```

Pode não aparecer nada na tela.

Para verificar:

```bash
ls
```

Se a pasta `teste` apareceu, o comando funcionou.

---

## Segundo ciclo: entrando e saindo de pastas

**Nível: Essencial**

### `cd`

Muda o diretório atual.

```bash
cd aula-01
```

Depois de entrar, confirme:

```bash
pwd
```

### `cd ..`

Volta uma pasta acima.

```bash
cd ..
```

O `..` representa a pasta anterior, ou seja, a pasta acima da atual.

### Exemplo completo

```bash
pwd
ls
cd aula-01
pwd
ls
cd ..
pwd
```

A ideia não é só executar. A ideia é observar como o caminho muda.

**Nível: Saiba que existe**

Também existem formas como:

```bash
cd ~
cd /
```

Mas elas não serão o foco da prática inicial. Nesta aula, vamos trabalhar principalmente em uma pasta segura de estudos.

---

## Terceiro ciclo: criando pastas e arquivos

**Nível: Essencial**

### `mkdir`

Cria uma pasta.

```bash
mkdir pratica-terminal
```

Verifique:

```bash
ls
```

Entre na pasta:

```bash
cd pratica-terminal
```

Confirme:

```bash
pwd
```

### `touch`

Cria um arquivo vazio ou atualiza a data de modificação de um arquivo existente.

```bash
touch anotacoes.txt
```

Verifique:

```bash
ls
```

Se `anotacoes.txt` apareceu, deu certo.

### Criando mais de um arquivo

**Nível: Importante**

É possível criar mais de um arquivo no mesmo comando:

```bash
touch tarefas.txt duvidas.txt
```

Isso cria dois arquivos:

- `tarefas.txt`;
- `duvidas.txt`.

**Nível: Saiba que existe**

Também existem formas mais avançadas de criar vários arquivos numerados, como:

```bash
touch arquivo-{1..5}.txt
```

Mas isso não será exigido nesta aula.

---

## Quarto ciclo: lendo e escrevendo arquivos com `cat`

**Nível: Essencial**

O comando `cat` pode ser usado para ler arquivos curtos.

```bash
cat anotacoes.txt
```

Se o arquivo estiver vazio, pode não aparecer nada.

### `cat > arquivo.txt`

Escreve conteúdo em um arquivo, substituindo o conteúdo anterior.

```bash
cat > anotacoes.txt
Hoje pratiquei comandos de terminal.
```

Depois de digitar o texto, encerre a entrada conforme o terminal usado. Em muitos terminais, isso é feito com `Ctrl+D`.

Atenção:

```text
o operador ">" subscreve o contéudo do arquivo, alterando-o pelo novo.
```

### `cat >> arquivo.txt`

Acrescenta conteúdo ao final do arquivo.

```bash
cat >> anotacoes.txt
Também pratiquei navegação por pastas.
```

Depois, leia o arquivo:

```bash
cat anotacoes.txt
```

Atenção:

```text
o operador ">>" acrescenta conteúdo, ao final do arquivo, sem apagar o que já existia.
```

### Comparação rápida

| Comando | O que faz |
|---|---|
| `cat arquivo.txt` | Lê o arquivo. |
| `cat > arquivo.txt` | Escreve substituindo o conteúdo. |
| `cat >> arquivo.txt` | Acrescenta conteúdo ao final. |

---

## Quinto ciclo: copiando, movendo, renomeando e removendo

**Nível: Essencial**

Estes comandos mexem diretamente com arquivos. Use apenas em pastas de treino nesta aula.

### `cp`

Copia um arquivo.

```bash
cp anotacoes.txt anotacoes-backup.txt
```

Verifique:

```bash
ls
```

### `mv`

Move ou renomeia um arquivo.

Para renomear:

```bash
mv anotacoes-backup.txt resumo.txt
```

Verifique:

```bash
ls
```

Para mover, informe o arquivo e o destino:

```bash
mv resumo.txt outra-pasta/
```

Nesta aula, o uso principal será renomear ou mover dentro de uma estrutura simples.

### `rm`

Remove um arquivo.

```bash
rm resumo.txt
```

Verifique:

```bash
ls
```

**Atenção:**

Use `rm` apenas em arquivos de teste. Remover arquivo é uma ação sensível e irreversível na CLI.

### `rmdir`

Remove uma pasta vazia.

```bash
rmdir pasta-vazia
```

Se a pasta tiver arquivos dentro, o comando não deve funcionar dessa forma.

**Nível: Não aprofundar agora**

Não vamos trabalhar com remoção forçada de pastas com conteúdo nesta aula.

---

## Visualizando arquivos maiores

**Nível: Saiba que existe**

Quando um arquivo é pequeno, `cat` resolve bem.

Mas, quando um arquivo é grande, existem comandos melhores para leitura.

### `less`

Abre o arquivo para leitura página por página.

```bash
less arquivo.txt
```

Dentro do `less`, normalmente:

- espaço avança;
- `q` sai.

### `head`

Mostra as primeiras linhas.

```bash
head arquivo.txt
```

### `tail`

Mostra as últimas linhas.

```bash
tail arquivo.txt
```

Esses comandos são úteis, mas não são o centro da Aula 01.

---

## Buscando texto e contando informações

**Nível: Saiba que existe**

### `grep`

Procura texto dentro de um arquivo.

```bash
grep "terminal" anotacoes.txt
```

Se encontrar a palavra, mostra a linha correspondente.

### `wc`

Conta linhas, palavras e caracteres/bytes de um arquivo.

```bash
wc anotacoes.txt
```

Também é possível ver contagens específicas:

```bash
wc -l anotacoes.txt
wc -w anotacoes.txt
```

Nesta aula, basta saber que esses comandos existem e que ajudam a investigar arquivos.

---

## Símbolos importantes do terminal

### `>` e `>>`

**Nível: Essencial**

Esses dois símbolos serão usados na Aula 01.

| Símbolo | O que faz |
|---|---|
| `>` | Envia conteúdo para um arquivo, substituindo o conteúdo anterior. |
| `>>` | Envia conteúdo para um arquivo, acrescentando ao final. |

Exemplo:

```bash
cat > nomes.txt
Amanda
```

Depois:

```bash
cat >> nomes.txt
Fernanda
Fabiano
```

Ao ler:

```bash
cat nomes.txt
```

Resultado esperado:

```bash
Amanda
Fernanda
Fabiano
```

### `|`

**Nível: Saiba que existe**

O pipe envia a saída de um comando para outro comando.

Exemplo:

```bash
ls | wc
```

Leia como:

```text
Liste os arquivos e envie essa saída para o wc contar.
```

Não é necessário dominar pipe agora.

### `*` e `?`

**Nível: Saiba que existe**

São curingas usados para representar nomes.

#### `*`

Representa vários caracteres.

```bash
ls *.txt
```

Lista arquivos que terminam com `.txt`.

#### `?`

Representa um único caractere.

```bash
ls aula-0?.txt
```

Pode encontrar arquivos como:

```text
aula-01.txt
aula-02.txt
```

---

## Convenções simples de nome de arquivo

**Nível: Importante**

Evite criar arquivos e pastas com espaços no nome durante o começo do curso.

Prefira:

```text
aula-01
minhas-anotacoes.txt
projeto-dev
```

Evite:

```text
minhas anotacoes.txt
projeto dev
```

Por quê?

Porque o terminal separa partes do comando por espaço. Então nomes com espaço podem gerar confusão para iniciantes.

Também é recomendado usar nomes:

- em letras minúsculas;
- com hífen;
- sem acentos, quando possível;
- com extensão quando for arquivo, como `.txt`, `.html`, `.js`.

---

## Como pedir ajuda no terminal

**Nível: Saiba que existe**

Existem comandos que ajudam a lembrar o que outros comandos fazem.

### `man`

Abre o manual de um comando.

```bash
man ls
```

### `whatis`

Mostra uma descrição curta.

```bash
whatis cp
```

Esses comandos podem ser úteis, mas não é necessário decorar suas saídas.

---

## Comandos que aparecem nesta aula

| Comando | Nível | Função |
|---|---|---|
| `pwd` | Essencial | Mostra a pasta atual. |
| `ls` | Essencial | Lista arquivos e pastas. |
| `cd` | Essencial | Muda de pasta. |
| `mkdir` | Essencial | Cria pasta. |
| `touch` | Essencial | Cria arquivo vazio. |
| `cat` | Essencial | Lê ou escreve conteúdo simples. |
| `cp` | Essencial | Copia arquivo. |
| `mv` | Essencial | Move ou renomeia. |
| `rm` | Essencial | Remove arquivo. |
| `rmdir` | Essencial | Remove pasta vazia. |
| `less` | Saiba que existe | Visualiza arquivo maior. |
| `head` | Saiba que existe | Mostra início do arquivo. |
| `tail` | Saiba que existe | Mostra final do arquivo. |
| `grep` | Saiba que existe | Busca texto. |
| `wc` | Saiba que existe | Conta linhas/palavras. |
| `man` | Saiba que existe | Abre manual. |
| `whatis` | Saiba que existe | Mostra descrição curta. |

---

## Sequência prática para testar antes da aula

**Nível: Essencial**

Se quiser praticar antes da aula, faça apenas esta sequência em uma pasta segura.
Crie uma pasta com o comando `mkdir`, entre nela com o comando `cd`

Não copie tudo de uma vez. Execute uma linha por vez.

```bash
pwd
ls
mkdir aula-01-terminal
cd aula-01-terminal
pwd
touch anotacoes.txt
ls
cat > anotacoes.txt
Estou praticando terminal pela primeira vez.
```

Encerre a entrada com `Ctrl+D`, quando aplicável.

Depois execute:

```bash
cat anotacoes.txt
cat >> anotacoes.txt
Quero entender melhor o que cada comando faz.
```

Encerre novamente a entrada.

Depois:

```bash
cat anotacoes.txt
cp anotacoes.txt anotacoes-backup.txt
ls
mv anotacoes-backup.txt resumo.txt
ls
rm resumo.txt
ls
cd ..
pwd
```

O objetivo é observar:

- onde o terminal está;
- o que muda depois de cada comando;
- como verificar se funcionou.

---

## Erros comuns nesta aula

**Nível: Importante**

### O comando não mostrou mensagem. Deu certo?

Pode ter dado certo. Use `ls`, `pwd` ou `cat` para verificar.

### O terminal disse que o arquivo não existe.

Confira:

```bash
pwd
ls
```

Talvez o terminal esteja na pasta errada ou o nome tenha sido digitado de forma diferente.

### Tentei entrar em um arquivo com `cd`.

`cd` entra em pastas, não em arquivos.

### Usei `cat >` e perdi o conteúdo anterior.

Isso acontece porque `>` substitui o conteúdo. Para acrescentar, use `>>`.

### O terminal ficou "preso" depois de `cat >`.

Provavelmente ele está esperando o conteúdo do arquivo. Encerre com `Ctrl+D`, quando aplicável.

---

## O que será praticado na aula ao vivo

**Nível: Essencial**

Na aula, o instrutor vai praticar com a turma:

- abrir o terminal;
- usar `pwd` e `ls`;
- navegar com `cd`;
- criar pastas com `mkdir`;
- criar arquivos com `touch`;
- ler e escrever arquivos com `cat`;
- usar `>` e `>>`;
- copiar com `cp`;
- renomear ou mover com `mv`;
- remover arquivos de teste com `rm`;
- remover pastas vazias com `rmdir`;
- investigar erros simples.

Os exemplos da aula podem ser diferentes dos exemplos deste material. Isso é intencional: a ideia é entender o raciocínio, não decorar uma sequência.

---

## O que não será aprofundado nesta aula

**Nível: Não aprofundar agora**

Esta aula não vai aprofundar:

- Git;
- GitHub;
- shell scripting;
- permissões Unix;
- administração de sistema;
- instalação de sistemas;
- processos;
- usuários e grupos;
- servidores;
- comandos destrutivos avançados;
- automações no terminal.

Esses assuntos podem aparecer em outros momentos do curso ou como curiosidade, mas não são objetivo da Aula 01.

---

## Checklist antes da aula

**Nível: Essencial**

Antes da aula, confira:

- [ ] consigo abrir o terminal indicado pelo instrutor;
- [ ] consigo abrir o editor de código;
- [ ] tenho acesso à internet;
- [ ] consigo entrar na sala da aula online;
- [ ] li este material pelo menos uma vez, mesmo sem decorar;
- [ ] testei `pwd` e `ls`, se possível;
- [ ] anotei dúvidas para levar à aula.

---

## Resumo final

**Nível: Essencial**

Se o aluno lembrar apenas de uma coisa antes da aula, deve lembrar desta sequência:

```text
Onde estou? -> pwd
O que existe aqui? -> ls
Para onde quero ir? -> cd
O que quero criar? -> mkdir ou touch
O que quero ler? -> cat
Quero substituir ou acrescentar? -> > ou >>
Como verifico se funcionou? -> pwd, ls ou cat
```

O objetivo da Aula 01 é começar a usar o terminal com intenção.

Não é necessário decorar todos os comandos. O mais importante é começar a entender o que se está tentando fazer.
