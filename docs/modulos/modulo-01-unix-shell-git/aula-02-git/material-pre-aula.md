---
layout: default
title: Material Pré-aula
---

# Material Pré-aula — Aula 02: Git

## Como usar este material

Este material é a base completa da Aula 02.

Leia com calma, sem tentar decorar todos os comandos de uma vez. O objetivo é entender a lógica do Git: por que ele existe, que problema ele resolve e como ele registra alterações em um projeto.

Durante a aula ao vivo, o instrutor vai retomar estes pontos, demonstrar os comandos e conduzir a prática.

Se algum comando não funcionar no seu computador antes da aula, não force. Anote o erro e leve para o encontro ao vivo.

## O que você vai aprender nesta aula

Nesta aula, você vai aprender:

- o que é versionamento;
- por que Git é importante para quem programa;
- o que é um repositório Git;
- a diferença inicial entre Git e GitHub;
- como verificar se o Git está instalado;
- como configurar nome e e-mail no Git;
- como criar um repositório local;
- como verificar o estado de um projeto com `git status`;
- como preparar alterações com `git add`;
- como registrar alterações com `git commit`;
- o que são branch, merge e conflito;
- como resolver um conflito simples.

Ao final da aula, você não precisa dominar Git por completo.

O mais importante é entender o fluxo básico:

```text
alterei um arquivo -> verifiquei o estado -> preparei a alteração -> registrei a alteração
```

## Por que falar de versionamento?

Imagine que você está trabalhando em um projeto e cria vários arquivos com nomes parecidos:

```text
projeto-final
projeto-final-agora-vai
projeto-final-certo
projeto-final-certo-mesmo
projeto-final-valendo
```

Esse tipo de organização parece resolver o problema no começo, mas rapidamente fica confuso.

Depois de algum tempo, você pode não saber:

- qual arquivo é o mais recente;
- o que mudou entre uma versão e outra;
- qual versão estava funcionando;
- quem fez determinada alteração;
- como voltar para um ponto anterior.

Em programação, esse problema aparece o tempo todo.

Um projeto muda várias vezes:

- arquivos são criados;
- linhas de código são alteradas;
- partes são removidas;
- erros são corrigidos;
- novas funcionalidades são adicionadas;
- decisões antigas precisam ser consultadas.

Versionamento é a prática de registrar essas mudanças ao longo do tempo.

Em vez de criar várias cópias soltas de uma pasta, usamos uma ferramenta própria para acompanhar a evolução do projeto.

Essa ferramenta é o Git.

## O que é Git?

Git é uma ferramenta de controle de versão.

Isso significa que ele acompanha alterações feitas nos arquivos de um projeto e permite registrar momentos importantes da evolução desse projeto.

Você pode pensar no Git como uma linha do tempo do seu projeto.

Nessa linha do tempo, você cria pontos de registro. Cada ponto representa uma mudança ou um conjunto de mudanças que você decidiu salvar no histórico.

Esses pontos de registro são chamados de commits.

Git não salva apenas "o arquivo final". Ele ajuda a responder perguntas como:

- o que mudou?
- quando mudou?
- por que essa mudança foi registrada?
- qual era o estado do projeto antes?
- qual é o estado atual do projeto?

Git é muito usado no desenvolvimento de software porque projetos de código mudam constantemente.

## Git não é GitHub

Git e GitHub são coisas diferentes.

Git é a ferramenta de versionamento.

GitHub é uma plataforma online que hospeda repositórios Git.

Nesta aula, o foco principal é Git.

Você vai aprender a registrar alterações localmente, no seu computador.

GitHub será aprofundado na próxima aula, quando o curso conectar o repositório local ao ambiente online usado para acessar, entregar e organizar atividades.

Por enquanto, guarde esta diferença:

| Termo | Ideia principal |
|---|---|
| Git | Ferramenta que registra alterações em um projeto. |
| GitHub | Plataforma online que hospeda repositórios Git. |

## O que é um repositório?

Um repositório é uma pasta de projeto acompanhada pelo Git.

Quando uma pasta comum passa a ser controlada pelo Git, ela vira um repositório Git.

Antes do Git:

```text
minha-pasta/
├── README.md
└── anotacoes.txt
```

Depois de iniciar o Git nessa pasta, ela continua parecendo uma pasta comum para você, mas passa a ter um controle interno de histórico.

Esse controle fica dentro de uma pasta oculta chamada `.git`.

Você não precisa mexer manualmente nessa pasta.

O importante é entender que, quando existe uma pasta `.git`, o Git consegue acompanhar as alterações daquele projeto.

## Repositório local e repositório remoto

Existem dois termos que aparecem bastante quando falamos de Git:

| Termo | Significado inicial |
|---|---|
| Repositório local | Repositório que está no seu computador. |
| Repositório remoto | Repositório hospedado na internet, por exemplo no GitHub. |

Nesta aula, vamos trabalhar principalmente com repositório local.

O repositório remoto será retomado na Aula 03.

## Antes de usar Git: esteja na pasta certa

Git depende muito do lugar onde você executa os comandos.

Na Aula 01, você viu comandos como:

```bash
pwd
ls
cd
```

Eles continuam importantes.

Antes de usar Git, você precisa saber:

- onde estou?
- esta é a pasta do projeto?
- os arquivos que quero acompanhar estão aqui?

Use `pwd` para ver o caminho atual:

```bash
pwd
```

Use `ls` para listar o conteúdo da pasta:

```bash
ls
```

Use `cd` para entrar em uma pasta:

```bash
cd nome-da-pasta
```

Se você executar comandos Git fora da pasta correta, pode receber mensagens de erro ou acabar olhando para o projeto errado.

## Verificando se o Git está instalado

Para verificar se o Git está disponível no seu computador, abra o terminal e execute:

```bash
git --version
```

Se o Git estiver instalado, você verá uma resposta parecida com:

```bash
git version 2.43.0
```

O número pode ser diferente. Isso não é um problema.

Se aparecer uma mensagem dizendo que o comando não foi encontrado, o Git provavelmente não está instalado ou não está disponível no terminal que você está usando.

Nesse caso, anote o erro e avise o instrutor.

## Configuração inicial do Git

Antes de criar commits, o Git precisa saber quem está registrando alterações.

Para isso, configuramos nome e e-mail.

O comando para configurar o nome é:

```bash
git config --global user.name "Seu Nome"
```

O comando para configurar o e-mail é:

```bash
git config --global user.email "seu-email@exemplo.com"
```

Use o nome e o e-mail orientados pelo instrutor.

Para conferir a configuração, você pode usar:

```bash
git config --global user.name
git config --global user.email
```

Essa configuração é importante porque cada commit registra também quem fez aquela alteração.

## Criando uma pasta para praticar

Para praticar sem mexer em projetos importantes, crie uma pasta de teste.

Escolha um local simples do seu computador e execute:

```bash
mkdir meu-primeiro-repositorio-git
cd meu-primeiro-repositorio-git
```

Depois, confira se você entrou na pasta:

```bash
pwd
ls
```

No começo, a pasta pode estar vazia.

Isso é esperado.

## Iniciando um repositório com `git init`

Para transformar uma pasta comum em um repositório Git, usamos:

```bash
git init
```

Esse comando cria a estrutura interna que o Git usa para acompanhar o projeto.

A resposta pode ser parecida com:

```bash
Initialized empty Git repository in /caminho/da/pasta/.git/
```

Depois disso, a pasta já é um repositório Git.

## A branch principal

Ao iniciar um repositório, o Git trabalha com uma branch principal.

Uma branch é um ramo de desenvolvimento do projeto.

Por enquanto, pense na branch principal como o caminho principal da história do projeto.

Hoje é comum chamar essa branch principal de `main`.

Em algumas instalações, o Git pode criar a branch inicial com o nome `master`. Esse nome ainda aparece em sistemas e materiais antigos, mas neste curso usaremos `main`.

Para renomear a branch atual para `main`, use:

```bash
git branch -m main
```

Também é possível configurar o Git para usar `main` como nome padrão em novos repositórios:

```bash
git config --global init.defaultBranch main
```

Se algum desses comandos gerar dúvida, não se preocupe. O instrutor vai orientar esse ponto na aula.

## Verificando o estado do projeto com `git status`

Um dos comandos mais importantes para quem está começando é:

```bash
git status
```

Esse comando mostra o estado atual do repositório.

Ele ajuda a responder:

- existe algum arquivo novo?
- algum arquivo foi modificado?
- alguma alteração já foi preparada?
- existe algo para registrar em commit?

Logo depois de criar um repositório vazio, o `git status` pode mostrar algo indicando que ainda não há commits.

Isso é normal.

O Git está dizendo que o repositório existe, mas ainda não possui nenhum registro no histórico.

## Criando o primeiro arquivo

Vamos criar um arquivo simples para praticar.

Você pode criar um arquivo chamado `README.md`:

```bash
touch README.md
```

Depois, confira:

```bash
ls
```

Agora execute:

```bash
git status
```

O Git deve indicar que existe um arquivo novo ainda não acompanhado.

Em inglês, essa ideia aparece como `untracked files`.

Isso significa que o arquivo existe na pasta, mas ainda não foi preparado para entrar no histórico do Git.

## Salvando conteúdo no arquivo

Abra o arquivo `README.md` no editor de código e escreva algo simples:

```md
# Meu primeiro repositório Git

Este repositório foi criado para praticar Git.
```

Salve o arquivo.

Depois, volte ao terminal e execute:

```bash
git status
```

O Git deve continuar indicando que existe um arquivo novo.

Até agora, você apenas criou e salvou um arquivo na pasta.

Ainda não registrou essa alteração no histórico do Git.

## O ciclo básico do Git

O fluxo inicial do Git pode ser entendido em três etapas:

```text
modificar -> preparar -> registrar
```

Em comandos:

```text
alterar arquivo -> git add -> git commit
```

Antes e depois dessas etapas, usamos `git status` para entender o estado do projeto.

Uma sequência comum é:

```bash
git status
git add README.md
git status
git commit -m "Adiciona README inicial"
git status
```

Vamos entender cada parte.

## Preparando alterações com `git add`

Quando você executa:

```bash
git add README.md
```

você está dizendo ao Git:

```text
quero preparar este arquivo para o próximo registro
```

O `git add` não cria o commit.

Ele apenas prepara a alteração.

Depois de usar `git add`, execute:

```bash
git status
```

O Git deve mostrar que a alteração está pronta para ser registrada.

Essa área de preparação costuma ser chamada de stage ou staging area.

Não precisa decorar o nome agora. O mais importante é entender a ideia:

```text
o arquivo mudou, mas eu ainda preciso escolher o que será registrado
```

## Registrando alterações com `git commit`

Depois de preparar a alteração, usamos `git commit` para criar um registro no histórico.

Exemplo:

```bash
git commit -m "Adiciona README inicial"
```

O commit cria um ponto na linha do tempo do projeto.

A mensagem depois de `-m` deve explicar, de forma curta, o que foi feito.

Bons exemplos de mensagem:

```text
Adiciona README inicial
Cria arquivo de anotações
Atualiza descrição do projeto
Corrige instruções de instalação
```

Mensagens ruins:

```text
coisas
alterei
teste
final
agora vai
```

A mensagem não precisa ser perfeita, mas deve ajudar você e outras pessoas a entenderem o histórico depois.

## Verificando depois do commit

Depois do commit, execute:

```bash
git status
```

Se tudo estiver registrado, o Git deve indicar que não há nada para commitar.

Em outras palavras:

```text
o projeto está limpo do ponto de vista do Git
```

Isso não significa que o projeto acabou.

Significa apenas que, naquele momento, não existem alterações pendentes.

## Visualizando o histórico com `git log`

Para ver os commits já criados, use:

```bash
git log
```

Esse comando mostra o histórico de commits.

Ele pode exibir:

- identificador do commit;
- autor;
- data;
- mensagem do commit.

Se a tela parecer "presa" dentro do histórico, pressione:

```text
q
```

A tecla `q` sai da visualização do log.

## Fazendo uma segunda alteração

Agora que já existe um primeiro commit, faça uma segunda alteração no `README.md`.

Por exemplo:

```md
# Meu primeiro repositório Git

Este repositório foi criado para praticar Git.

Nesta aula, estou aprendendo a registrar alterações.
```

Salve o arquivo.

Depois, execute:

```bash
git status
```

Agora o Git deve indicar que o arquivo foi modificado.

Prepare a alteração:

```bash
git add README.md
```

Registre:

```bash
git commit -m "Atualiza descrição do README"
```

Confira novamente:

```bash
git status
```

Com isso, você criou mais um ponto na linha do tempo do projeto.

## Entendendo branch

Uma branch é um ramo do projeto.

Ela permite que você trabalhe em uma linha separada sem mexer diretamente na linha principal.

Imagine que a branch `main` representa o caminho principal do projeto.

Se você precisa testar uma ideia nova, pode criar uma nova branch para fazer essa alteração.

Assim, você evita bagunçar diretamente a branch principal.

Em projetos profissionais, branches são muito usadas para:

- testar uma funcionalidade;
- corrigir um erro;
- trabalhar em uma parte do projeto sem interferir no restante;
- organizar contribuições de várias pessoas.

Nesta aula, vamos ver o conceito e um exemplo simples.

## Verificando branches

Para ver as branches do repositório, use:

```bash
git branch
```

A branch atual aparece marcada com um asterisco:

```bash
* main
```

Isso significa que você está trabalhando na branch `main`.

## Criando uma nova branch

Para criar uma nova branch e já entrar nela, use:

```bash
git checkout -b atualiza-readme
```

Esse comando faz duas coisas:

- cria uma branch chamada `atualiza-readme`;
- muda o trabalho atual para essa nova branch.

Depois, confira:

```bash
git branch
```

Você deve ver algo parecido com:

```bash
* atualiza-readme
  main
```

O asterisco indica que você está na branch `atualiza-readme`.

## Fazendo uma alteração na nova branch

Com a nova branch ativa, altere o `README.md`.

Exemplo:

```md
# Meu primeiro repositório Git

Este repositório foi criado para praticar Git.

Nesta aula, estou aprendendo a registrar alterações.

Agora estou testando uma alteração em uma branch separada.
```

Salve o arquivo.

Depois, execute:

```bash
git status
```

Prepare a alteração:

```bash
git add README.md
```

Registre:

```bash
git commit -m "Atualiza README em branch separada"
```

Agora a alteração está registrada na branch `atualiza-readme`.

## Voltando para a branch principal

Para voltar para a branch `main`, use:

```bash
git checkout main
```

Agora abra ou visualize o `README.md`.

Você pode perceber que a alteração feita na outra branch não aparece na `main`.

Isso acontece porque a alteração foi feita em outro ramo do projeto.

Essa é a ideia central de branch:

```text
eu posso trabalhar em uma linha separada sem alterar imediatamente a linha principal
```

## Entendendo merge

Merge significa mesclar.

No Git, fazer merge é trazer alterações de uma branch para outra.

Se você criou uma branch, fez alterações nela e agora quer levar essas alterações para a `main`, você faz um merge.

Antes do merge, confirme que você está na branch que deve receber as alterações.

Neste caso, queremos trazer a branch `atualiza-readme` para a `main`.

Então primeiro entramos na `main`:

```bash
git checkout main
```

Depois fazemos o merge:

```bash
git merge atualiza-readme
```

Se tudo correr bem, as alterações da branch `atualiza-readme` passam a fazer parte da branch `main`.

Depois, confira:

```bash
git status
```

E veja o conteúdo do arquivo.

## O que é conflito?

Um conflito acontece quando o Git não consegue decidir sozinho como juntar alterações.

Isso pode acontecer quando duas branches alteram a mesma parte de um mesmo arquivo de maneiras diferentes.

Exemplo simples:

- na branch `main`, uma linha foi alterada de um jeito;
- na branch `teste`, a mesma linha foi alterada de outro jeito;
- na hora do merge, o Git não sabe qual versão deve ficar.

Quando isso acontece, o Git pede ajuda.

Resolver conflito é decidir manualmente qual conteúdo deve permanecer no arquivo.

## Criando um conflito simples para entender

Este exemplo serve apenas para entender o conceito.

Comece na branch `main`.

```bash
git checkout main
```

Crie um arquivo chamado `frase.txt`:

```bash
echo "Git ajuda a registrar mudanças." > frase.txt
```

Prepare e registre:

```bash
git add frase.txt
git commit -m "Adiciona frase inicial"
```

Agora crie uma nova branch:

```bash
git checkout -b altera-frase
```

Altere a mesma linha do arquivo:

```bash
echo "Git ajuda a organizar o histórico do projeto." > frase.txt
```

Prepare e registre:

```bash
git add frase.txt
git commit -m "Altera frase na branch"
```

Volte para a `main`:

```bash
git checkout main
```

Agora altere a mesma linha, mas de outro jeito:

```bash
echo "Git ajuda a acompanhar alterações em arquivos." > frase.txt
```

Prepare e registre:

```bash
git add frase.txt
git commit -m "Altera frase na main"
```

Agora tente juntar a branch `altera-frase` na `main`:

```bash
git merge altera-frase
```

O Git deve indicar um conflito.

## Como o conflito aparece no arquivo

Abra o arquivo `frase.txt`.

Ele pode aparecer parecido com isto:

```text
<<<<<<< HEAD
Git ajuda a acompanhar alterações em arquivos.
=======
Git ajuda a organizar o histórico do projeto.
>>>>>>> altera-frase
```

Essas marcações foram colocadas pelo Git.

Elas mostram as duas versões que entraram em conflito.

A parte acima de `=======` é uma versão.

A parte abaixo de `=======` é a outra versão.

Agora você precisa decidir qual texto final faz sentido.

## Resolvendo o conflito

Para resolver o conflito, edite o arquivo manualmente.

Você pode escolher uma das versões ou combinar as duas.

Por exemplo:

```text
Git ajuda a acompanhar alterações em arquivos e organizar o histórico do projeto.
```

Depois de editar, remova todas as marcações do Git:

```text
<<<<<<< HEAD
=======
>>>>>>> altera-frase
```

O arquivo final não pode ficar com essas marcações.

Depois de salvar o arquivo corrigido, prepare a resolução:

```bash
git add frase.txt
```

Finalize o merge com um commit:

```bash
git commit -m "Resolve conflito em frase"
```

Por fim, confira:

```bash
git status
```

Se estiver tudo certo, o Git deve indicar que não há alterações pendentes.

## O que você precisa entender sobre conflitos agora

Conflitos podem assustar no começo, mas a ideia principal é simples:

```text
o Git encontrou duas versões diferentes e precisa que uma pessoa decida o resultado final
```

Resolver conflito envolve:

1. abrir o arquivo;
2. localizar as marcações;
3. decidir o conteúdo correto;
4. remover as marcações;
5. salvar o arquivo;
6. usar `git add`;
7. finalizar com `git commit`.

Você não precisa decorar todos os detalhes agora.

O importante é não apagar tudo sem ler e não entrar em pânico quando vir as marcações.

## Comandos que aparecem nesta aula

### Terminal

```bash
pwd
ls
cd
mkdir
touch
echo
```

### Git

```bash
git --version
git config --global user.name "Seu Nome"
git config --global user.email "seu-email@exemplo.com"
git config --global init.defaultBranch main
git init
git branch
git branch -m main
git status
git add README.md
git add .
git commit -m "Mensagem do commit"
git log
git checkout main
git checkout -b nome-da-branch
git merge nome-da-branch
```

## Sequência mental recomendada

Quando estiver usando Git, pense nesta sequência:

```text
1. Onde estou?
2. Esta é a pasta do projeto?
3. O que mudou?
4. O que eu quero preparar?
5. O que eu quero registrar?
6. Estou na branch certa?
7. O repositório ficou limpo depois?
```

Comandos associados:

```bash
pwd
ls
git status
git add nome-do-arquivo
git commit -m "Mensagem"
git branch
git status
```

## Erros comuns nesta aula

### O terminal diz que `git` não é reconhecido

Provavelmente o Git não está instalado ou não está disponível nesse terminal.

Anote a mensagem e avise o instrutor.

### O Git diz que não é um repositório

Você pode estar fora da pasta do projeto ou ainda não executou `git init`.

Confira:

```bash
pwd
ls
```

Se necessário, entre na pasta correta com `cd`.

### Fiz alteração, mas o Git não mostrou nada

Verifique se você salvou o arquivo.

Também confira se está na pasta correta.

### Usei `git add`, mas nada apareceu diferente no arquivo

Isso é esperado.

`git add` não muda o conteúdo visível do arquivo. Ele apenas prepara a alteração para o próximo commit.

### O commit falhou pedindo nome ou e-mail

Configure nome e e-mail:

```bash
git config --global user.name "Seu Nome"
git config --global user.email "seu-email@exemplo.com"
```

Depois tente o commit novamente.

### Entrei no `git log` e não sei sair

Pressione:

```text
q
```

### Criei uma branch e me perdi

Use:

```bash
git branch
```

A branch com `*` é a branch atual.

### Apareceram símbolos estranhos no arquivo depois do merge

Esses símbolos provavelmente são marcações de conflito:

```text
<<<<<<<
=======
>>>>>>>
```

Não ignore essas marcações.

Você precisa editar o arquivo, decidir o conteúdo final, remover as marcações, salvar, usar `git add` e finalizar com `git commit`.

## O que não precisa dominar nesta aula

Nesta aula, você não precisa dominar:

- GitHub;
- GitHub Classroom;
- pull request;
- clone;
- push;
- pull;
- rebase;
- stash;
- tags;
- estratégias profissionais de branch;
- resolução de conflitos grandes;
- colaboração em equipe com várias pessoas.

Alguns desses temas aparecerão depois.

Agora, o foco é construir a base.

## Prática sugerida antes da aula

Se você se sentir confortável, faça apenas uma prática leve:

1. Abra o terminal.
2. Verifique onde está com `pwd`.
3. Crie uma pasta de teste.
4. Entre na pasta.
5. Execute `git init`.
6. Crie um `README.md`.
7. Execute `git status`.

Não precisa avançar sozinho se ficar inseguro.

A prática completa será conduzida em aula.

## Checklist antes da aula

Antes da aula, confira:

- [ ] consigo abrir o terminal;
- [ ] consigo abrir o editor de código;
- [ ] sei usar `pwd`, `ls` e `cd` em nível básico;
- [ ] consigo verificar se o Git está instalado com `git --version`;
- [ ] entendi que Git e GitHub não são a mesma coisa;
- [ ] entendi que Git registra alterações em uma pasta de projeto;
- [ ] entendi que `git status` mostra o estado do projeto;
- [ ] entendi que `git add` prepara alterações;
- [ ] entendi que `git commit` registra alterações;
- [ ] anotei dúvidas para levar para a aula.

## Resumo final

Git é uma ferramenta de versionamento.

Versionar significa registrar mudanças ao longo do tempo.

Um repositório Git é uma pasta de projeto acompanhada pelo Git.

O comando `git status` mostra o estado atual do repositório.

O comando `git add` prepara alterações para registro.

O comando `git commit` cria um ponto no histórico.

Branch é um ramo de trabalho.

Merge junta alterações de uma branch em outra.

Conflito acontece quando o Git não consegue decidir sozinho como combinar mudanças.

Nesta aula, o mais importante é entender a lógica:

```text
eu modifico arquivos, observo o estado, preparo o que quero registrar e crio um commit
```

Com prática, Git deixa de parecer uma lista de comandos soltos e passa a fazer sentido como uma ferramenta de organização do trabalho.

