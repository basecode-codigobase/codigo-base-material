---
layout: default
title: Material Pré-aula
---

# Material Pré-aula — Aula 03: GitHub

## Como usar este material

Este material é a base completa da Aula 03.

Leia com calma, sem tentar decorar todos os comandos de uma vez. O objetivo é entender o papel do GitHub no curso: para que ele serve, como ele se conecta ao Git e como será usado para acessar e entregar atividades.

Durante a aula ao vivo, o instrutor vai retomar estes pontos, demonstrar o fluxo no GitHub e conduzir a prática.

Se alguma etapa de login, autenticação ou acesso não funcionar antes da aula, não force. Anote o que apareceu na tela e leve para o encontro ao vivo.

## O que você vai aprender nesta aula

Nesta aula, você vai aprender:

- a diferença entre Git, GitHub e GitHub Classroom;
- o que é um repositório remoto;
- para que serve uma conta no GitHub;
- qual é a diferença entre o repositório central do curso e um repositório de atividade;
- como uma atividade pode ser distribuída pelo GitHub Classroom;
- o que significa aceitar uma atividade;
- o que é clonar um repositório;
- como conectar o que está no GitHub com uma pasta no seu computador;
- como revisar o fluxo básico de `git status`, `git add` e `git commit`;
- como enviar alterações para o GitHub com `git push`;
- quando o `git pull` pode ser necessário;
- quais erros comuns aparecem nesse primeiro contato com GitHub.

Ao final da aula, você não precisa dominar GitHub por completo.

O mais importante é entender o fluxo básico:

```text
acessei a atividade -> abri ou clonei o repositório -> alterei um arquivo -> fiz commit -> enviei para o GitHub
```

## Retomando a Aula 02

Na Aula 02, você viu que Git é uma ferramenta de versionamento.

Git ajuda a registrar alterações feitas em arquivos de um projeto.

O fluxo principal foi:

```text
alterar -> verificar -> preparar -> registrar
```

Em comandos:

```bash
git status
git add nome-do-arquivo
git commit -m "Mensagem do commit"
git status
```

Esse fluxo acontece localmente, ou seja, dentro de uma pasta no seu computador.

Agora, na Aula 03, vamos conectar essa ideia ao ambiente online do curso.

## Git não é GitHub

Essa diferença é uma das mais importantes do módulo.

Git e GitHub trabalham juntos, mas não são a mesma coisa.

| Termo | Ideia principal |
|---|---|
| Git | Ferramenta que registra alterações em um projeto. |
| GitHub | Plataforma online que hospeda repositórios Git. |
| GitHub Classroom | Ferramenta ligada ao GitHub usada para distribuir e receber atividades do curso. |

Uma forma simples de pensar:

```text
Git registra a história do projeto.
GitHub guarda essa história online.
GitHub Classroom organiza atividades e entregas do curso.
```

Na Aula 02, o foco foi Git.

Nesta aula, o foco é GitHub e GitHub Classroom em nível operacional.

## Por que usar GitHub no curso?

O GitHub será usado porque o curso precisa de um lugar organizado para:

- acessar materiais;
- distribuir atividades;
- criar repositórios de prática;
- registrar entregas;
- acompanhar o progresso dos alunos;
- manter um fluxo parecido com o usado em desenvolvimento real.

Isso não significa que GitHub será o assunto principal do curso inteiro.

O foco do curso continua sendo fundamentos de programação.

GitHub entra como ferramenta de apoio para organizar estudo, prática e entrega.

## O problema que o GitHub ajuda a resolver

Na Aula 02, você viu que Git ajuda a organizar o histórico de um projeto.

Mas imagine uma situação um pouco maior.

Você fez commits no seu computador.

Agora surgem perguntas novas:

- como acessar esse projeto de outro computador?
- como guardar uma cópia online do histórico?
- como entregar uma atividade para o instrutor?
- como o instrutor consegue ver o que você fez?
- como manter o material do curso separado do trabalho de cada aluno?

É aqui que o GitHub começa a fazer sentido.

Ele não substitui o Git.

Ele hospeda repositórios Git online.

Isso permite que um projeto exista em dois lugares:

```text
no seu computador -> repositório local
na internet -> repositório remoto
```

O Git continua registrando alterações.

O GitHub permite que essas alterações sejam guardadas, consultadas e compartilhadas em um ambiente online.

## Trabalho em equipe e trabalho individual

A base comparativa desta aula apresenta GitHub também como ferramenta de colaboração.

Isso é verdadeiro.

Em desenvolvimento de software, GitHub é muito usado para que várias pessoas trabalhem em um mesmo projeto.

Com GitHub, um time pode:

- guardar o código em um lugar comum;
- acompanhar o histórico de alterações;
- revisar mudanças antes de juntar no projeto principal;
- discutir partes do código;
- manter versões diferentes de trabalho;
- evitar que arquivos soltos circulem por mensagens ou anexos.

Mas nesta aula, o foco não será colaboração profissional.

Neste momento do curso, o uso mais importante do GitHub será:

```text
acessar uma atividade -> trabalhar em um repositório -> enviar a entrega
```

Então, se aparecerem termos como revisão de código, pull request ou colaboração, entenda como repertório inicial.

Você não precisa dominar esses fluxos agora.

## Repositório local e repositório remoto

Na Aula 02, você conheceu a ideia de repositório local.

Agora vamos acrescentar a ideia de repositório remoto.

| Termo | Significado |
|---|---|
| Repositório local | Repositório que está no seu computador. |
| Repositório remoto | Repositório hospedado online, por exemplo no GitHub. |

Quando você trabalha apenas no seu computador, suas alterações ficam locais.

Quando você envia essas alterações para o GitHub, elas passam a estar também no repositório remoto.

O fluxo fica assim:

```text
computador do aluno <-> GitHub
```

Ou, com os nomes que aparecem bastante:

```text
repositório local <-> repositório remoto
```

## O que é GitHub?

GitHub é uma plataforma online que hospeda repositórios Git.

Em termos práticos, ele permite que você:

- guarde projetos online;
- acesse projetos de outros computadores;
- compartilhe código;
- consulte histórico de alterações;
- veja arquivos diretamente pelo navegador;
- use repositórios como parte do fluxo de atividades do curso.

Nesta etapa, o mais importante é entender GitHub como lugar online onde repositórios ficam hospedados.

Não vamos explorar GitHub como rede social, portfólio completo ou ferramenta profissional avançada.

## GitHub não é a única plataforma

GitHub é uma das plataformas mais conhecidas para hospedar repositórios Git.

Existem outras, como:

- GitLab;
- Bitbucket;
- Azure Repos.

Todas elas se relacionam com a mesma ideia geral:

```text
hospedar repositórios Git online
```

Neste curso, usaremos GitHub porque ele faz parte do fluxo operacional definido para materiais, atividades e entregas.

Você não precisa comparar plataformas agora.

O importante é entender o funcionamento básico do GitHub dentro do curso.

## Conta, usuário e identidade

Para usar GitHub, você precisa de uma conta.

Essa conta identifica você dentro da plataforma.

Ela pode aparecer em:

- repositórios criados por você;
- commits associados ao seu e-mail;
- atividades aceitas pelo GitHub Classroom;
- permissões de acesso;
- histórico de entrega.

Por isso, é importante cuidar de três coisas:

1. conseguir acessar sua conta;
2. saber qual e-mail está ligado a ela;
3. configurar o Git local com nome e e-mail corretos.

Na Aula 02, apareceu esta configuração:

```bash
git config --global user.name "Seu Nome"
git config --global user.email "seu-email@exemplo.com"
```

Ela continua importante.

O Git usa essas informações para registrar quem fez os commits.

Para conferir:

```bash
git config --global user.name
git config --global user.email
```

Se o nome ou e-mail estiverem errados, avise o instrutor antes de seguir criando entregas.

## O que é GitHub Classroom?

GitHub Classroom é uma ferramenta usada por cursos para distribuir atividades usando repositórios do GitHub.

No curso, ele funciona como mecanismo de distribuição e entrega.

Isso significa que o instrutor pode criar uma atividade e disponibilizar um link.

Quando o aluno aceita essa atividade, o GitHub Classroom cria ou libera um repositório próprio para aquela entrega.

Esse repositório pode conter:

- instruções;
- arquivos iniciais;
- starter code, quando houver;
- espaço para o aluno fazer alterações;
- histórico de commits;
- registro da entrega.

O GitHub Classroom não é a biblioteca principal do curso.

A fonte principal de estudo e consulta é o repositório central do curso.

O GitHub Classroom é usado principalmente para atividades e entregas.

## Repositório central do curso e repositório de atividade

É comum confundir esses dois lugares no começo.

Eles têm funções diferentes.

| Ambiente | Função |
|---|---|
| Repositório central do curso | Fonte oficial de materiais, aulas, orientações e consulta. |
| Repositório de atividade | Lugar onde o aluno realiza ou entrega uma atividade específica. |

O repositório central responde:

```text
onde estudo e consulto o material?
```

O repositório de atividade responde:

```text
onde faço ou envio esta atividade?
```

Essa separação existe para evitar mistura entre material oficial e trabalho do aluno.

## Antes da aula: conta e acesso

Para acompanhar a Aula 03, você precisa ter acesso ao GitHub.

Antes da aula, confira:

- se você consegue abrir o site do GitHub no navegador;
- se você consegue fazer login na sua conta;
- se lembra o usuário ou e-mail usado;
- se consegue acessar o link de atividade enviado pelo instrutor, quando houver;
- se consegue abrir o terminal;
- se consegue abrir o editor de código;
- se o Git está instalado ou disponível no ambiente indicado.

Se ainda não tiver conta ou se tiver problema de login, avise o instrutor.

Problemas de acesso são esperados no início. O importante é não esconder o erro nem tentar resolver por comandos aleatórios.

## Autenticação: por que pode aparecer?

Quando você acessa o GitHub pelo navegador, normalmente usa login e senha.

Quando você usa Git pelo terminal para conversar com o GitHub, pode ser necessário autenticar sua conta de outra forma.

Isso acontece porque o GitHub precisa saber que você tem permissão para acessar ou enviar alterações para aquele repositório.

Em geral, existem duas formas comuns de conexão:

| Forma | Ideia geral |
|---|---|
| HTTPS | Usa uma URL iniciada por `https://` e pode exigir autenticação por token ou pelo gerenciador de credenciais. |
| SSH | Usa uma chave SSH cadastrada na conta do GitHub para autorizar o computador. |

Nesta aula, você não precisa decorar todos os detalhes de autenticação.

O ponto principal é:

```text
para clonar, enviar ou atualizar um repositório privado ou de atividade, o GitHub precisa reconhecer quem você é.
```

Se aparecer uma tela de login, pedido de autorização, token, chave SSH ou permissão, pare e peça orientação.

## Autenticação em duas etapas

Autenticação em duas etapas também pode aparecer como:

```text
2FA
Two Factor Authentication
autenticação de dois fatores
```

A ideia é simples.

Em vez de proteger sua conta apenas com senha, o GitHub pode pedir uma segunda confirmação.

Essa segunda confirmação pode vir por:

- aplicativo autenticador;
- código temporário;
- dispositivo já autorizado;
- outro mecanismo indicado pela plataforma.

Isso aumenta a segurança da conta.

Para esta aula, você não precisa aprender todos os detalhes de segurança digital.

Você precisa entender apenas que:

```text
se o GitHub pedir uma segunda confirmação, isso faz parte do processo de proteger sua conta.
```

Se travar nessa etapa, anote:

- em qual tela estava;
- qual mensagem apareceu;
- se estava no navegador ou no terminal;
- se a atividade era do GitHub Classroom ou um repositório comum.

Essas informações ajudam o instrutor a destravar o problema.

## SSH em visão geral

SSH é uma forma de autenticar seu computador no GitHub.

Quando o SSH está configurado, o GitHub reconhece que aquele computador está autorizado a interagir com a sua conta.

Na prática, isso pode permitir clonar, enviar e atualizar repositórios sem digitar senha a cada comando.

A base comparativa mostra um passo a passo longo de criação e cadastro de chave SSH.

Esse processo envolve, em geral:

1. gerar uma chave no computador;
2. localizar a chave pública;
3. copiar essa chave;
4. cadastrar a chave na conta do GitHub;
5. testar se a conexão funcionou.

Nesta aula, esse processo pode ser demonstrado ou orientado pelo instrutor se for necessário para a turma.

Mas ele não deve virar o centro da aula.

O essencial agora é entender:

```text
SSH é uma forma de autorizar meu computador a conversar com o GitHub.
```

Se o curso adotar SSH como padrão, o instrutor vai indicar o passo a passo correto para o sistema operacional usado.

## HTTPS em visão geral

HTTPS é outra forma de acessar repositórios no GitHub.

URLs HTTPS costumam ter este formato:

```text
https://github.com/usuario/repositorio.git
```

Ao usar HTTPS, pode ser necessário fazer login pelo navegador, usar um token ou passar por um gerenciador de credenciais.

Para iniciante, o mais importante não é escolher sozinho entre SSH e HTTPS.

O mais importante é seguir a orientação do curso e perceber que ambas as formas servem para conectar Git local e GitHub remoto.

## Criar um repositório no GitHub

Além de aceitar atividades pelo GitHub Classroom, também é útil reconhecer como um repositório comum é criado no GitHub.

Esse conhecimento ajuda você a entender o que acontece quando o Classroom cria um repositório para uma atividade.

Na criação manual de um repositório, normalmente aparecem campos como:

- dono do repositório;
- nome do repositório;
- descrição;
- visibilidade;
- opção de criar um `README.md`;
- opções adicionais, como `.gitignore` e licença.

### Dono do repositório

O dono pode ser seu usuário pessoal ou uma organização.

No curso, alguns repositórios podem estar ligados a uma organização ou sala do GitHub Classroom.

Antes de criar ou acessar algo, observe quem é o dono do repositório.

### Nome do repositório

O nome identifica o repositório.

Exemplos:

```text
aula-03-github
atividade-primeiro-push
meu-primeiro-repositorio
```

Use nomes simples, com letras minúsculas e hífen quando fizer sentido.

Evite nomes confusos como:

```text
teste2
final
atividade-certa-agora-vai
```

### Descrição

A descrição é opcional.

Ela serve para explicar rapidamente a finalidade do repositório.

Exemplo:

```text
Repositório de prática da Aula 03 sobre GitHub.
```

### Visibilidade

Um repositório pode ser público ou privado.

| Visibilidade | Ideia geral |
|---|---|
| Público | Pode ser acessado por qualquer pessoa com internet. |
| Privado | Só pessoas autorizadas conseguem acessar. |

No curso, siga sempre a orientação do instrutor.

Não mude a visibilidade de repositórios de atividade sem instrução.

### README

O `README.md` é um arquivo muito comum em repositórios.

Ele costuma explicar:

- o que é o projeto;
- como usar;
- quais instruções seguir;
- qual é o objetivo da atividade;
- quais passos o aluno deve cumprir.

Para iniciantes, criar um repositório com README ajuda porque o repositório já começa com pelo menos um arquivo.

Isso facilita a primeira leitura e evita um repositório totalmente vazio.

## Criar no GitHub e depois clonar

Quando você cria um repositório no GitHub e depois clona para o computador, o fluxo fica assim:

```text
1. criar repositório no GitHub
2. copiar a URL de clone
3. usar git clone no computador
4. entrar na pasta criada
5. trabalhar localmente
6. fazer commit
7. fazer push
```

Esse fluxo é comum porque já começa com um repositório remoto definido.

No GitHub Classroom, algo parecido acontece, mas com uma diferença:

```text
o Classroom cria ou libera o repositório da atividade para você.
```

Depois disso, você trabalha no repositório indicado.

## O que é clonar um repositório?

Clonar um repositório significa copiar um repositório remoto do GitHub para o seu computador.

O comando usado é:

```bash
git clone url-do-repositorio
```

No GitHub, normalmente você encontra essa URL no botão chamado `Code`.

Dependendo da configuração, esse botão pode mostrar opções como:

- HTTPS;
- SSH;
- GitHub CLI.

No curso, use a opção orientada pelo instrutor.

Se o instrutor orientar HTTPS, copie a URL HTTPS.

Se o instrutor orientar SSH, copie a URL SSH.

Depois do clone, você passa a ter uma pasta local com os arquivos daquele repositório.

Exemplo:

```bash
git clone https://github.com/usuario/repositorio-de-pratica.git
```

Esse comando cria uma pasta chamada, por exemplo:

```text
repositorio-de-pratica/
```

Depois de clonar, é muito importante entrar na pasta criada:

```bash
cd repositorio-de-pratica
```

Em seguida, confira:

```bash
pwd
ls
git status
```

Um erro muito comum é clonar o repositório e continuar executando comandos fora da pasta clonada.

## Onde clonar o repositório?

Antes de clonar, escolha uma pasta segura e organizada.

Por exemplo, uma pasta de estudos do curso.

Evite clonar repositórios em locais aleatórios, como:

- área de downloads;
- pasta temporária;
- dentro de outro repositório sem saber;
- lugares difíceis de encontrar depois.

Um fluxo simples pode ser:

```bash
cd caminho/da/pasta/de/estudos
git clone url-do-repositorio
cd nome-do-repositorio
```

Depois, sempre confira:

```bash
pwd
ls
git status
```

O objetivo é responder:

```text
estou dentro da pasta certa, do repositório certo?
```

## Clonar não é a mesma coisa que baixar ZIP

No GitHub, pode existir a opção de baixar um projeto como arquivo `.zip`.

Essa opção baixa os arquivos, mas não cria o mesmo fluxo de Git usado no curso.

Quando você usa `git clone`, o Git baixa os arquivos e mantém a conexão com o repositório remoto.

Para o curso, quando houver orientação de trabalhar com Git e GitHub, o caminho esperado será clonar o repositório ou usar o fluxo indicado pelo instrutor.

## Abrindo o repositório no editor

Depois de clonar e entrar na pasta do repositório, você pode abrir o projeto no editor de código.

Se o VS Code estiver configurado para abrir pelo terminal, um comando comum é:

```bash
code .
```

O ponto final significa:

```text
abra o editor na pasta atual
```

Antes de usar esse comando, confira onde você está:

```bash
pwd
```

Se você abrir o editor na pasta errada, pode editar arquivos que não pertencem à atividade.

Também é possível abrir o editor manualmente e escolher a pasta do repositório.

O importante é garantir que o editor e o terminal estejam olhando para o mesmo projeto.

## O que é `origin`?

Quando você clona um repositório, o Git costuma criar automaticamente um apelido para o repositório remoto.

Esse apelido geralmente se chama `origin`.

Você pode pensar assim:

```text
origin = apelido do repositório remoto de onde este projeto veio
```

Para ver os remotos configurados, use:

```bash
git remote -v
```

Você pode ver algo parecido com:

```text
origin  https://github.com/usuario/repositorio.git (fetch)
origin  https://github.com/usuario/repositorio.git (push)
```

Por enquanto, basta reconhecer que `origin` aponta para o GitHub.

## O fluxo básico da Aula 03

O fluxo principal desta aula será:

```text
1. acessar a atividade ou repositório no GitHub
2. clonar o repositório, se for orientado
3. entrar na pasta clonada
4. conferir o estado com git status
5. alterar um arquivo simples
6. preparar a alteração com git add
7. registrar a alteração com git commit
8. enviar a alteração com git push
9. conferir no GitHub se a alteração apareceu
```

Em comandos, a parte local pode ficar assim:

```bash
git clone url-do-repositorio
cd nome-do-repositorio
git status
git add nome-do-arquivo
git commit -m "Atualiza arquivo da atividade"
git push
```

Dependendo do repositório e da branch, o instrutor pode orientar um comando mais específico de `push`.

## Criando ou acessando uma atividade pelo GitHub Classroom

Quando o instrutor enviar um link do GitHub Classroom, o fluxo pode ser parecido com:

1. abrir o link da atividade;
2. fazer login no GitHub, se necessário;
3. aceitar a atividade;
4. aguardar o GitHub Classroom preparar o repositório;
5. abrir o repositório criado;
6. ler o `README.md` ou as instruções;
7. seguir o fluxo indicado para trabalhar na atividade.

O link de atividade não é apenas uma página comum.

Ele pode gerar um repositório próprio para você.

Por isso, leia a tela com calma antes de clicar em muitas opções ao mesmo tempo.

## Lendo a página de um repositório no GitHub

Na página de um repositório, você pode encontrar:

- nome do repositório;
- lista de arquivos e pastas;
- branch atual exibida;
- botão ou área para copiar a URL de clone;
- histórico de commits;
- conteúdo do `README.md`;
- informações de visibilidade e acesso.

No começo, não é necessário conhecer todos os botões.

Procure primeiro:

- o nome do repositório;
- se é o repositório certo;
- se existe um `README.md`;
- onde está a URL para clonar;
- se a alteração enviada apareceu depois do `git push`.

## Alterando um arquivo simples

Depois de clonar e entrar na pasta do repositório, a prática pode envolver uma alteração simples.

Por exemplo, editar um arquivo `README.md`:

```md
# Atividade de GitHub

Estou praticando o fluxo entre Git local e GitHub.
```

Depois de salvar o arquivo, volte ao terminal e confira:

```bash
git status
```

O Git deve indicar que o arquivo foi modificado.

## Branch nesta aula

Na Aula 02, você viu que branch é um ramo de trabalho.

Na base comparativa da Aula 03, aparece um fluxo usando branch antes de enviar alterações para o GitHub.

Esse fluxo é importante no desenvolvimento profissional, mas nesta etapa precisa ser tratado com cuidado.

O plano oficial do módulo indica que a Aula 03 deve evitar transformar colaboração, pull request e estratégias de branch em conteúdo central.

Então, nesta aula, branch pode aparecer de duas formas:

- como retomada do que foi visto na Aula 02;
- como detalhe operacional caso o repositório de atividade exija uma branch específica.

Se o instrutor orientar trabalhar na `main`, siga a `main`.

Se o instrutor orientar criar uma branch, o fluxo pode ser:

```bash
git branch
git checkout -b atualiza-readme
```

Depois da alteração:

```bash
git status
git add README.md
git commit -m "Atualiza README"
git push -u origin atualiza-readme
```

O importante é não criar branches aleatórias sem entender onde a atividade espera receber a entrega.

## Registrando a alteração localmente

Antes de enviar para o GitHub, você precisa registrar a alteração no Git local.

O fluxo continua sendo o mesmo da Aula 02:

```bash
git status
git add README.md
git commit -m "Atualiza README da atividade"
git status
```

O commit cria o registro local.

Até esse momento, a alteração ainda pode estar apenas no seu computador.

Para aparecer no GitHub, você precisa enviar.

## Enviando alterações com `git push`

O comando `git push` envia commits locais para o repositório remoto.

Uma forma simples pode ser:

```bash
git push
```

Em alguns casos, especialmente quando uma branch ainda não existe no remoto, pode aparecer uma orientação para usar algo como:

```bash
git push -u origin nome-da-branch
```

Não tente adivinhar o comando se aparecer uma mensagem diferente.

Leia a mensagem com calma e peça orientação.

O mais importante agora é entender a ideia:

```text
commit registra no meu computador.
push envia meus commits para o GitHub.
```

## Conferindo se o envio funcionou

Depois do `git push`, volte ao GitHub no navegador.

Confira:

- se está no repositório certo;
- se está na branch correta, quando isso for indicado;
- se o arquivo alterado aparece atualizado;
- se o commit aparece no histórico do repositório.

Esse passo é importante porque ajuda a confirmar se a entrega chegou ao ambiente remoto.

Não basta pensar "rodei o comando". É preciso conferir o resultado.

## O que é `git pull`?

O comando `git pull` traz alterações do repositório remoto para o seu repositório local.

Ele responde a uma situação como:

```text
algo mudou no GitHub e eu preciso atualizar minha pasta local
```

Exemplo:

```bash
git pull origin main
```

Nesta aula, o `pull` deve aparecer apenas como noção inicial.

Você não precisa dominar todos os casos.

Por enquanto, guarde:

```text
push envia do local para o remoto.
pull traz do remoto para o local.
```

## Pull request: saiba que existe

A base comparativa apresenta pull request como parte do fluxo de GitHub.

Pull request é uma solicitação para juntar alterações de uma branch em outra, geralmente com possibilidade de revisão.

Em projetos profissionais, um fluxo comum é:

```text
criar branch -> fazer commit -> fazer push -> abrir pull request -> revisar -> fazer merge
```

Esse fluxo é muito importante no trabalho em equipe.

Mas nesta aula, pull request não será conteúdo central.

Você deve apenas reconhecer a ideia:

```text
pull request é um pedido de integração de alterações.
```

Não é esperado que você domine abertura, revisão ou merge de pull requests agora.

Se o instrutor usar pull request em alguma demonstração, trate como visão geral.

O fluxo mínimo da Aula 03 continua sendo:

```text
clonar -> alterar -> commit -> push -> conferir no GitHub
```

## Merge no GitHub: saiba que existe

Na Aula 02, merge foi apresentado como junção de alterações entre branches.

No GitHub, um merge também pode acontecer pela interface, especialmente depois de um pull request.

Isso significa que uma alteração enviada em uma branch pode ser incorporada à branch principal.

Nesta aula, basta reconhecer:

```text
merge junta alterações.
pull request pode ser usado para pedir esse merge no GitHub.
```

Não vamos praticar merge de pull request como habilidade obrigatória desta aula.

## Fluxo mental com GitHub

Quando estiver trabalhando com GitHub, pense nesta sequência:

```text
1. Estou no repositório certo no navegador?
2. Aceitei a atividade correta?
3. Clonei o repositório certo?
4. Entrei na pasta clonada?
5. O git status funciona aqui?
6. Alterei e salvei o arquivo?
7. Fiz git add?
8. Fiz git commit?
9. Fiz git push?
10. Conferi no GitHub se apareceu?
```

Essa sequência ajuda a evitar grande parte dos erros iniciais.

## Comandos que aparecem nesta aula

### Terminal

```bash
pwd
ls
cd
```

### Git

```bash
git clone url-do-repositorio
git status
git add nome-do-arquivo
git commit -m "Mensagem do commit"
git push
git push -u origin nome-da-branch
git pull origin main
git remote -v
git branch
```

Você não precisa decorar todos de uma vez.

Os comandos mais importantes da aula são:

```bash
git clone
git status
git add
git commit
git push
```

## Erros comuns nesta aula

### Clonei o repositório, mas o Git diz que não é um repositório

Provavelmente você ainda não entrou na pasta clonada.

Depois de `git clone`, use:

```bash
ls
cd nome-do-repositorio
git status
```

### Estou no repositório errado

Confira o nome do repositório no GitHub e o nome da pasta no seu computador.

Use:

```bash
pwd
ls
git remote -v
```

O `git remote -v` ajuda a ver para qual endereço remoto aquela pasta aponta.

### Fiz alteração, mas ela não apareceu no `git status`

Verifique se você salvou o arquivo.

Também confira se está dentro da pasta correta.

### Fiz commit, mas não apareceu no GitHub

O commit registra localmente.

Para enviar ao GitHub, ainda falta:

```bash
git push
```

Depois, confira no navegador.

### O `git push` pediu login ou autorização

Isso está relacionado à autenticação.

Não tente muitas senhas aleatórias.

Leia a mensagem, veja se o navegador abriu alguma autorização e peça ajuda ao instrutor se necessário.

### O `git push` disse que não tenho permissão

Possíveis causas:

- você está no repositório errado;
- você não aceitou a atividade corretamente;
- você está tentando enviar para um repositório onde não tem acesso;
- sua autenticação não foi reconhecida.

Antes de tentar resolver sozinho, confira o link da atividade e peça orientação.

### O GitHub mostra uma branch diferente

O repositório pode ter mais de uma branch.

Use:

```bash
git branch
```

No GitHub, observe também o seletor de branch na página do repositório.

Nesta etapa, siga a branch indicada pelo instrutor.

### Fiz push em uma branch e procurei a alteração em outra

Alterações enviadas para uma branch não aparecem automaticamente em outra branch.

Se você fez push para uma branch chamada `atualiza-readme`, mas está olhando a `main` no GitHub, talvez não veja a alteração ali.

Confira:

```bash
git branch
```

E confira também o seletor de branch no GitHub.

Nesta etapa, não tente fazer merges sozinho se a atividade não pediu isso.

Peça orientação para confirmar onde a entrega deve aparecer.

### Executei `git init` dentro de um repositório clonado

Ao clonar um repositório, ele já vem preparado como repositório Git.

Normalmente, não é necessário executar:

```bash
git init
```

dentro de uma pasta clonada.

Se você fez isso sem querer e algo ficou estranho, avise o instrutor antes de tentar apagar arquivos.

### Baixei ZIP em vez de clonar

Se você baixou `.zip`, talvez esteja com os arquivos, mas sem o fluxo Git configurado da forma esperada.

Quando a atividade exigir Git, siga a orientação de clonar o repositório.

Se estiver em dúvida, peça ajuda antes de começar a atividade.

### O repositório foi criado sem README e parece vazio

Um repositório recém-criado no GitHub pode ficar vazio se nenhum arquivo inicial foi adicionado.

Isso não significa que ele está quebrado.

Mas, para iniciantes, um repositório com `README.md` costuma ser mais fácil de entender.

Se o repositório da atividade vier vazio, siga exatamente a orientação do instrutor.

### A tela do GitHub tem muitos botões

Isso é normal.

No começo, concentre-se em poucos elementos:

- nome do repositório;
- lista de arquivos;
- arquivo `README.md`;
- botão `Code`;
- branch atual;
- histórico de commits;
- indicação de que seu push apareceu.

Não é necessário explorar todas as abas do GitHub nesta aula.

## O que não precisa dominar nesta aula

Nesta aula, você não precisa dominar:

- pull request;
- code review;
- issues;
- GitHub Actions;
- GitHub Pages;
- GitHub como portfólio completo;
- colaboração com várias pessoas no mesmo repositório;
- estratégias profissionais de branch;
- resolução avançada de conflito remoto;
- configuração avançada de SSH, token ou credenciais.

Alguns desses temas podem aparecer no futuro.

Agora, o foco é conseguir participar do fluxo inicial do curso.

## Prática sugerida antes da aula

Antes da aula, faça apenas uma preparação leve:

1. Abra o navegador.
2. Acesse o GitHub.
3. Faça login na sua conta.
4. Abra o terminal.
5. Verifique onde está com `pwd`.
6. Verifique se o Git responde com:

```bash
git --version
```

7. Revise mentalmente a diferença entre Git, GitHub e GitHub Classroom.

Não é necessário clonar repositórios por conta própria antes da aula, a menos que o instrutor envie uma orientação específica.

## Checklist antes da aula

Antes da aula, confira:

- [ ] consigo acessar o GitHub no navegador;
- [ ] consigo fazer login na minha conta;
- [ ] sei que Git e GitHub não são a mesma coisa;
- [ ] entendi que GitHub hospeda repositórios online;
- [ ] entendi que GitHub Classroom será usado para atividades e entregas;
- [ ] entendi a diferença entre repositório central do curso e repositório de atividade;
- [ ] consigo abrir o terminal;
- [ ] consigo abrir o editor de código;
- [ ] consigo usar `pwd`, `ls` e `cd` em nível básico;
- [ ] lembro o fluxo básico `git status`, `git add` e `git commit`;
- [ ] consigo verificar se o Git está instalado com `git --version`;
- [ ] anotei dúvidas de acesso, login ou autenticação para levar para a aula.

## Resumo final

Git é a ferramenta que registra alterações em um projeto.

GitHub é a plataforma online que hospeda repositórios Git.

GitHub Classroom é a ferramenta usada para distribuir e receber atividades do curso.

Um repositório local fica no seu computador.

Um repositório remoto fica online, por exemplo no GitHub.

Clonar um repositório é trazer uma cópia do GitHub para o seu computador mantendo a conexão com o remoto.

Commit registra alterações localmente.

Push envia commits para o GitHub.

Pull traz alterações do GitHub para o seu computador.

Nesta aula, o mais importante é entender a lógica:

```text
eu acesso a atividade, trabalho no repositório correto, registro minha alteração com Git e envio para o GitHub
```

Com prática, GitHub deixa de parecer uma página cheia de botões e passa a fazer sentido como parte do fluxo de estudo, prática e entrega do curso.
