- O que é Git?

Git é um sistema de controle de versão distribuído que é usado para rastrear mudanças em arquivos de computador. Ele é amplamente utilizado por desenvolvedores de software para gerenciar seus projetos de código.

Aqui estão algumas das principais características do Git:

- **Distribuído:** Cada cópia do repositório Git é um clone completo do repositório central. Isso significa que você pode trabalhar offline e ainda ter acesso a todo o histórico do projeto.
- **Rápido:** O Git é conhecido por sua velocidade, especialmente em operações comuns como commit, checkout e branch.
- **Poderoso:** O Git oferece uma ampla variedade de recursos, como merge, rebase, stash e revert, que permitem que você gerencie seu código de forma eficaz.
- **Versátil:** O Git pode ser usado para rastrear qualquer tipo de arquivo, não apenas código-fonte.

Se você está interessado em aprender mais sobre o Git, recomendo que consulte a documentação oficial ou um tutorial online.

- [ ] Para que serve

O Git serve para rastrear e gerenciar mudanças em arquivos de computador, principalmente em projetos de desenvolvimento de software. Ele é uma ferramenta essencial para desenvolvedores, pois permite:

- **Manter histórico de mudanças:** O Git registra todas as alterações feitas nos arquivos do projeto, permitindo que você visualize o que foi modificado e quando.
    
- **Colaborar com outros desenvolvedores:** O Git facilita a colaboração entre equipes, pois permite que vários desenvolvedores trabalhem simultaneamente no mesmo projeto e mesclem suas alterações de forma eficiente.
    
- **Criar versões diferentes do projeto:** O Git permite que você crie diferentes versões do seu projeto, o que é útil para experimentar novas ideias ou reverter a alterações indesejadas.
    
- **Desfazer alterações:** Se você cometer um erro, o Git permite que você desfaça as alterações e volte a uma versão anterior do seu projeto.
    
- Como Instalar  
    O Git é uma ferramenta essencial para desenvolvedores e pode ser instalado em diversos sistemas operacionais. A seguir, apresentamos um guia básico para a instalação em Windows, macOS e Linux.
    

### Windows

1. **Baixar o instalador:** Acesse o site oficial do Git ([https://git-scm.com/](https://git-scm.com/)) e clique no botão de download para Windows.
2. **Executar o instalador:** Execute o arquivo baixado e siga as instruções do assistente de instalação.
3. **Personalizar a instalação:** Durante a instalação, você pode personalizar algumas opções, como o editor de texto padrão e o local de instalação. No entanto, para a maioria dos usuários, as configurações padrão são suficientes.

### macOS

**Opção 1: Usando o Homebrew**

1. **Instalar o Homebrew:** Se você ainda não tem o Homebrew instalado, execute o seguinte comando no Terminal:
    
    ```bash
    /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"   
    ```
    
2. **Instalar o Git:** Com o Homebrew instalado, execute o seguinte comando:
    
    ```bash
    brew install git
    ```
    

**Opção 2: Usando o pacote oficial**

1. **Baixar o pacote:** Acesse o site oficial do Git e baixe a versão mais recente para macOS.
2. **Instalar o pacote:** Siga as instruções do instalador.

### Linux

A instalação do Git em distribuições Linux varia um pouco, mas geralmente é feita através do gerenciador de pacotes.

- **Debian/Ubuntu:** Bash  
    

```bash
sudo apt update
sudo apt install git
```

- **Fedora/CentOS:** Bash  
    

```bash
sudo dnf install git
```

**Verificando a instalação:** Após a instalação, você pode verificar a versão do Git instalada no seu sistema executando o comando:

```bash
git --version
```

**Configuração inicial:** Após a instalação, é recomendado configurar seu nome e e-mail, que serão associados aos seus commits:

```bash
git config --global user.name "Seu Nome"
git config --global user.email "seu.email@exemplo.com"
```

**Onde encontrar mais informações:**

- **Documentação oficial:** [https://git-scm.com/book/en/v2/Getting-Started-Installing-Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)    
    
- **Tutoriais online:** Existem diversos tutoriais detalhados disponíveis online, tanto em texto quanto em vídeo, que podem te ajudar com a instalação e configuração do Git.

**Observações:**

- **Atualizações:** É importante manter o Git atualizado para ter acesso aos novos recursos e correções de bugs.
- **Configurações avançadas:** O Git oferece muitas opções de configuração para personalizar seu fluxo de trabalho. Consulte a documentação oficial para mais informações.

**Recursos adicionais:**

- **Kinsta:** [https://kinsta.com/pt/base-de-conhecimento/instalar-git/](https://kinsta.com/pt/base-de-conhecimento/instalar-git/)
- **Cursa:** [https://cursa.app/fr/page/instalacao-do-git-em-diferentes-sistemas-operacionais](https://cursa.app/fr/page/instalacao-do-git-em-diferentes-sistemas-operacionais)

Com o Git instalado e configurado, você estará pronto para começar a gerenciar seus projetos de forma mais eficiente e colaborativa.

- [ ] Como Iniciar um Repositorio

## Iniciando um Projeto com Git

**1. Criar um novo diretório:** Comece escolhendo um local adequado para o seu projeto e crie um novo diretório para ele. Por exemplo:

```bash
mkdir uige-training-day
cd uige-training-day
```

**2. Inicializar o repositório Git:** Navegue até o diretório recém-criado e execute o comando `git init` para inicializar um novo repositório Git:

```bash
git init
```

Isso criará um diretório oculto chamado `.git` que armazenará o histórico do seu projeto.

**3. Criar arquivos:** Adicione os arquivos necessários para o seu projeto. Por exemplo, se você está criando um projeto web, pode criar arquivos como `index.html`, `style.css` e `script.js`.

**4. Commitar as alterações:** Use o comando `git add` para adicionar arquivos ao "staging area", que é um local intermediário antes de serem comprometidos. Em seguida, use o comando `git commit` para criar um novo commit com uma mensagem descritiva:

```
git add .
git commit -m "Initial commit"
```

**5. Criar um repositório remoto (opcional):** Se você deseja compartilhar seu projeto com outras pessoas ou fazer backup online, pode criar um repositório remoto em um serviço como GitHub, GitLab ou Bitbucket. Siga as instruções do serviço escolhido para criar um novo repositório e conectar seu repositório local a ele.

**6. Enviar as alterações para o repositório remoto (opcional):** Se você criou um repositório remoto, use o comando `git push` para enviar suas alterações para ele:

```bash
git remote add origin <url_do_repositorio_remoto>
git push -u origin main
```

**Exemplo completo:**

```bash
mkdir uige-training-day # Criar o projecto
cd uige-training-day # acessar(abrir) o projecto
git init # Inicializar o projecto como repositorio git
touch index.html # Criar um arquivo com nome index.html
git add . #Adicionar todos os arquivos para serem regsitrados no git
git commit -m "Primeiro Commit" # Adicionar um registo de informações
git remote add origin https://github.com/seu_usuario/uige-training-day.git
git push -u origin main # Enviar as alterações do git no repositorio remoto
```

Isso criará um novo projeto Git, adicionará um arquivo inicial, fará um commit e enviará as alterações para um repositório remoto no GitHub.

**Observações:**

- O comando `git add .` adiciona todos os arquivos novos ou modificados no diretório atual. Você também pode adicionar arquivos individualmente usando `git add <arquivo>`.
- A mensagem de commit deve ser descritiva e explicar as alterações feitas.
- O nome da branch padrão é `main`, mas você pode alterar isso durante a inicialização do repositório.

Agora você tem um projeto Git configurado e pronto para começar a trabalhar!

- [ ] Working Area, Staging Area  
    A **staging area** (ou área de preparação) é um conceito fundamental no Git, onde você prepara os arquivos que serão incluídos no próximo commit. No entanto, o Git oferece um sistema mais rico de estados em que um arquivo pode se encontrar durante o seu ciclo de vida dentro de um repositório.

**Principais estados de um arquivo no Git:**

- **Untracked:**
    - Arquivos que foram adicionados ao diretório do projeto, mas ainda não foram adicionados ao controle do Git. Eles não aparecem em nenhum dos comandos `git status` ou `git log`.
    - Para começar a rastrear um arquivo, use o comando `git add`.
- **Staged:**
    - Arquivos que foram marcados para inclusão no próximo commit. Eles aparecem na seção "Changes to be committed" do comando `git status`.
    - Para desfazer o staging de um arquivo, use `git reset HEAD <arquivo>`.
- **Committed:**
    - Arquivos que foram incluídos em um commit e fazem parte do histórico do projeto. Eles estão seguros e podem ser recuperados a qualquer momento.
    - Para ver o histórico de um arquivo, use `git log <arquivo>`.
- **Modified:**
    - Arquivos que foram modificados desde o último commit, mas ainda não foram adicionados à staging area. Eles aparecem na seção "Changes not staged for commit" do comando `git status`.
- **Removed:**
    - Arquivos que foram removidos do diretório do projeto, mas ainda estão sendo rastreados pelo Git. Eles aparecem na seção "Changes not staged for commit" do comando `git status`.
    - Para remover um arquivo do controle do Git, use `git rm <arquivo>`.

**Diagrama ilustrativo:**

![Pasted image 20240918214309.png](app://ece2163a40ada11389e2b4798b839286ae35/home/balduino/MEGA/Obsidian/Pasted%20image%2020240918214309.png?1726692189585)

**Outros conceitos importantes:**

- **HEAD:** Um ponteiro que aponta para o último commit na branch atual.
- **Branch:** Uma linha de desenvolvimento independente do projeto.
- **Merge:** A ação de combinar duas ou mais branches em uma única branch.
- **Rebase:** Uma operação para reescrever a história de uma branch, geralmente para simplificar o histórico do projeto.

Sugestão: Ler sobre `git stah`

**Gostaria de explorar algum desses conceitos com mais profundidade?** Por exemplo, podemos discutir como utilizar o `git stash` para salvar alterações temporariamente ou como trabalhar com diferentes branches.

- [ ] Adicionar o primeiro comit

**O primeiro commit é como tirar uma foto do estado inicial do seu projeto.** É a primeira vez que você registra as mudanças feitas nos arquivos e inicia o histórico de versões do seu projeto.

**Passo a passo:**

1. **Verifique o status:**
    
    - Antes de fazer o commit, é sempre bom verificar o status do seu repositório. Isso mostra quais arquivos foram modificados, adicionados ou removidos. Use o comando:

```bash
git status
```

2. **Adicione os arquivos à staging area:**
    
    - Para adicionar todos os arquivos novos ou modificados à staging area, use:

```bash
git add .
```

Se você quiser adicionar apenas um arquivo específico, use:

```bash
git add <nome_do_arquivo>
```

3. **Faça o commit:**
    
    - Agora, você pode criar o commit com uma mensagem descritiva sobre as mudanças:

```bash
git commit -m "Sua mensagem aqui"
```

A mensagem de commit é importante, pois serve como um marcador para futuras referências. Seja claro e conciso ao descrever as alterações.

**Exemplo completo:**

```bash
# Verifica o status
git status

# Adiciona todos os arquivos à staging area
git add .

# Faz o commit com uma mensagem descritiva
git commit -m "Inicializando o projeto"
```

**O que acontece quando você faz um commit:**

- O Git cria um instantâneo do seu projeto naquele momento.
- A mensagem que você escreve é associada a esse instantâneo, servindo como uma descrição das mudanças.
- O Git armazena esse instantâneo e a mensagem em seu histórico de versões.

**Dicas adicionais:**

- **Mensagens de commit:**
    - Seja claro e conciso.
    - Use verbos no imperativo (ex: "Add", "Fix", "Improve").
    - Evite mensagens muito longas ou vagas.
    - Use convenções de mensagens de commit (como Conventional Commits) para facilitar a automatização e a colaboração.

**Exemplos:**

|**Mensagem incorreta**|**Mensagem correta (imperativo)**|**Explicação**|
|---|---|---|
|"Corrigi o bug da pesquisa"|**Corrige bug da pesquisa**|A forma imperativa "Corrige" indica a ação realizada.|
|"Adicionei nova funcionalidade de login"|**Adiciona nova funcionalidade de login**|O verbo "Adiciona" no imperativo é mais direto.|
|"Foi feito um ajuste na interface"|**Ajusta interface do usuário**|O verbo "Ajusta" no imperativo é mais claro e conciso.|

**O imperativo é a forma verbal ideal para mensagens de commit.** Ele transmite uma ação de forma clara e direta, como se você estivesse dando uma ordem ao Git.

**Por que usar o imperativo?**

- **Clareza:** As mensagens ficam mais concisas e fáceis de entender.
    
- **Consistência:** Cria um padrão uniforme para todas as mensagens do projeto.
    
- **Facilidade de leitura:** Facilita a compreensão do que foi feito em cada commit, mesmo para quem não escreveu o código.
    
- **Commits frequentes:**
    
    - É recomendado fazer commits com frequência, mesmo para pequenas mudanças.
    - Isso permite que você tenha um histórico mais detalhado do seu projeto e facilita a reversão de alterações, se necessário.

**Por que fazer o primeiro commit?**

- **Criar um ponto de partida:** O primeiro commit estabelece a base para o seu projeto.
- **Iniciar o histórico de versões:** A partir desse primeiro commit, você pode acompanhar todas as mudanças feitas no seu código.
- **Facilitar a colaboração:** Se você estiver trabalhando em um projeto com outras pessoas, o primeiro commit é essencial para compartilhar o código e colaborar de forma eficiente.

**Estrutura de uma mensagem de commit no imperativo:**

- **Verbo no infinitivo:** Indica a ação realizada (ex: adicionar, remover, corrigir).
- **Objeto:** Especifica o que foi afetado pela ação (ex: arquivo, funcionalidade, bug).
- **Detalhes adicionais:** Informações complementares sobre a mudança, se necessário.

**Exemplo completo:**

```
# Adiciona validação de email no formulário de cadastro
* Implementa regex para validar formato de email.
* Exibe mensagem de erro caso o email seja inválido.
```

**Dicas adicionais:**

- **Seja conciso:** Evite mensagens muito longas e detalhadas.
- **Use verbos fortes:** Escolha verbos que transmitam a ação de forma clara e precisa.
- **Mantenha um estilo consistente:** Use sempre a mesma estrutura para todas as mensagens.
- **Evite frases negativas:** Em vez de "Não faz mais tal coisa", diga "Remove tal funcionalidade".
- **Utilize convenções de commit:** Adote uma convenção como Conventional Commits para padronizar as mensagens e facilitar a automatização de tarefas.

**Convenção Conventional Commits (exemplo):**

```
feat: adiciona nova funcionalidade de busca
fix: corrige bug na exibição de datas
refactor: melhora a estrutura do código do componente de login
```

- [ ] Verificando as alterações e Logs (`git status` e `git log`)

Para acompanhar o histórico de modificações em um projeto Git e entender quais alterações foram feitas e quando, utilizamos alguns comandos essenciais.

### Comando `git status`

- **Função:** Mostra o estado atual do seu repositório, indicando quais arquivos foram modificados, adicionados à staging area ou não estão sendo rastreados.
- **Uso:**

```bash
git status
```

- **Saída:** Exibe uma lista de arquivos com suas respectivas mudanças, informando se estão prontos para serem commitados ou não.

### Comando `git log`

- **Função:** Exibe o histórico de commits do seu repositório, mostrando a mensagem de cada commit, o autor, a data e o hash do commit.
- **Uso:**

```bash
git log  # Mostra todos os commits
git log -n 5  # Mostra os últimos 5 commits
git log --oneline  # Mostra cada commit em uma única linha
```

- **Saída:** Uma lista de commits em ordem cronológica inversa, com informações detalhadas sobre cada um.

**Opções adicionais para `git log`:**

- **`--graph`:** Exibe um gráfico ASCII mostrando as branches e a relação entre os commits.
- **`--pretty=format:"%h - %an, %ar : %s"`:** Personaliza a saída do log, mostrando apenas o hash abreviado, o autor, a data relativa e a mensagem do commit.
- **`--author="Seu Nome"`:** Filtra os commits por autor.
- **`--since="2.weeks ago"`:** Filtra os commits realizados a partir de uma data específica.

### Exemplo Completo:

```bash
# Verifica o estado atual do repositório
git status

# Mostra o histórico dos últimos 10 commits em uma linha cada
git log -10 --oneline

# Mostra o histórico dos commits feitos por João, nos últimos 2 meses
git log --author="João" --since="2 months ago"
```

**Visualizando o Histórico de Forma Gráfica:**

- **Gitk:** Uma ferramenta gráfica para visualizar o histórico de um repositório Git.
- **Outras GUIs:** Muitas IDEs e editores de código oferecem interfaces gráficas para visualizar o histórico do Git.

**Dicas Adicionais:**

- **Aliases:** Crie aliases para comandos longos e complexos para facilitar o uso.
- **Configuração:** Personalize a saída do `git log` com opções como `--pretty`.
- **Busca:** Use `git log -S "palavra-chave"` para encontrar commits que contenham uma determinada palavra em suas mensagens.
- **Branches:** Utilize `git log <branch>` para ver o histórico de uma branch específica.

Ao dominar esses comandos, você terá uma visão completa do histórico do seu projeto Git e poderá facilmente rastrear as alterações feitas ao longo do tempo.

- [ ] Conectado o Git Local ao GitHub

Após criar um repositório remoto no GitHub ou GitLab, você precisa conectá-lo ao seu repositório local. Isso permite que você sincronize as alterações entre os dois repositórios.

### Criando um Repositório Remoto no GitHub ou GitLab

1. **Crie uma conta:** Se você ainda não tem uma conta no GitHub ou GitLab, crie uma.
2. **Crie um repositório:** Vá para a página principal do seu perfil e clique em "New repository".
3. **Configure o repositório:** Dê um nome ao seu repositório, adicione uma descrição (opcional) e selecione se deseja que o repositório seja público ou privado.
4. **Clique em "Create repository".**

### Conectando o Repositório Local ao Remoto

1. **Navegue para o diretório do seu projeto local:** Abra o terminal e use o comando `cd` para navegar até o diretório onde está localizado o seu projeto Git.
2. **Verifique o status do repositório:** Use o comando `git status` para verificar se o seu repositório está limpo (sem alterações não commitadas).
3. **Adicione o repositório remoto:** Use o comando `git remote add` para adicionar o repositório remoto ao seu projeto local. Substitua `<url_do_repositorio_remoto>` pelo endereço do seu repositório no GitHub ou GitLab:

```bash
git remote add origin <url_do_repositorio_remoto>
```

4. **Envie as alterações para o repositório remoto:** Use o comando `git push` para enviar as alterações do seu repositório local para o remoto:

```bash
git push -u origin main
```

O parâmetro `-u` configura a branch local `main` para rastrear a branch remota `main`.

**Exemplo completo:**

```bash
cd meu-projeto
git remote add origin https://github.com/seu-usuario/meu-projeto.git
git push -u origin main
```

### Sincronizando Alterações

- **Para puxar alterações do repositório remoto para o local:**

```bash
git pull origin main
```

- **Para enviar alterações do local para o remoto:**

```bash
git push origin main
```

**Observações:**

- Se você tiver feito alterações no seu repositório remoto após conectá-lo ao local, é possível que ocorra um conflito de merge ao tentar sincronizar as alterações. Nesse caso, você precisará resolver o conflito manualmente antes de poder enviar as alterações.
- Para trabalhar em diferentes branches, você pode criar branches locais e sincronizá-las com branches remotas.

# Resumo

Com certeza, o Git é uma ferramenta essencial no dia a dia de qualquer desenvolvedor, e dominar alguns comandos básicos é fundamental para garantir um fluxo de trabalho eficiente.

**Comandos mais utilizados:**

- **`git status`:** Verifica o estado atual do repositório, mostrando quais arquivos foram modificados, adicionados ou removidos.
- **`git add`:** Adiciona arquivos à staging area, preparando-os para serem commitados.    
    
- **`git commit`:** Cria um novo commit, salvando as alterações da staging area no histórico do projeto.
- **`git push`:** Envia as alterações locais para o repositório remoto (por exemplo, GitHub ou GitLab).
- **`git pull`:** Baixa as alterações do repositório remoto para o local.

**Outros comandos úteis:**

- **`git log`:** Mostra o histórico de commits.
- **`git diff`:** Mostra as diferenças entre duas versões de um arquivo ou entre o seu diretório de trabalho e a staging area.
- **`git reset`:** Desfaz as últimas alterações.
- **`git revert`:** Desfaz um commit específico, criando um novo commit para reverter as alterações.

**Exemplo de um fluxo de trabalho típico:**

1. **`git pull`:** Baixa as últimas alterações do repositório remoto.
2. **`git checkout -b nova-feature`:** Cria uma nova branch para uma nova funcionalidade.
3. **[Faz as alterações no código]**
4. **`git add .`:** Adiciona todas as alterações à staging area.
5. **`git commit -m "Descrição clara da alteração"`:** Cria um novo commit com uma mensagem descritiva.
6. **`git push origin nova-feature`:** Envia as alterações para a nova branch no repositório remoto.
7. **[Cria um pull request para mesclar a branch com a main]**

# Próximos Passos

- Branches
- Tags
- HEAD
- Rebase
- Colaboração (Forks, Pull Requests, Resolução de Conflitos)

Links Úteis:

[https://gist.github.com/gfda/858e71dad5765c564c8a1a7c5f812d5e](https://gist.github.com/gfda/858e71dad5765c564c8a1a7c5f812d5e)

[https://docs.github.com/pt/enterprise-cloud@latest/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent](https://docs.github.com/pt/enterprise-cloud@latest/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)