# thiago

# Principais Comandos do Git

## Configuração inicial
- `git config --global user.name "Seu Nome"` – Define seu nome de usuário para os commits.
- `git config --global user.email "seu@email.com"` – Define seu e-mail para os commits.
- `git config --list` – Exibe as configurações atuais.

## Criar e clonar repositórios
- `git init` – Inicializa um novo repositório Git no diretório atual.
- `git clone <url>` – Clona um repositório remoto para sua máquina local.

## Registro de alterações (stage e commit)
- `git status` – Mostra o estado atual dos arquivos (modificados, adicionados, etc.).
- `git add <arquivo>` – Adiciona um arquivo específico à área de staging.
- `git add .` – Adiciona todos os arquivos modificados e novos ao staging.
- `git commit -m "mensagem"` – Cria um commit com as alterações que estão no staging.
- `git commit -am "mensagem"` – Adiciona todos os arquivos modificados e já versionados ao staging e faz o commit em um único passo.

## Sincronização com repositório remoto
- `git push` – Envia os commits locais para o repositório remoto.
- `git pull` – Busca e mescla as alterações do repositório remoto no branch atual.
- `git fetch` – Baixa as alterações do remoto sem mesclá-las automaticamente.

## Branches (ramificações)
- `git branch` – Lista os branches locais.
- `git branch <nome>` – Cria um novo branch.
- `git checkout <branch>` – Muda para o branch especificado.
- `git checkout -b <branch>` – Cria um novo branch e já muda para ele.
- `git merge <branch>` – Mescla o branch especificado no branch atual.
- `git branch -d <branch>` – Deleta um branch (se já estiver mesclado).
- `git branch -D <branch>` – Força a exclusão de um branch.

## Histórico e inspeção
- `git log` – Exibe o histórico de commits.
- `git log --oneline` – Mostra o histórico de forma resumida (uma linha por commit).
- `git diff` – Mostra as diferenças entre o diretório de trabalho e o staging.
- `git diff --staged` – Mostra as diferenças entre o staging e o último commit.

## Desfazer alterações
- `git restore <arquivo>` – Descarta alterações não commitadas em um arquivo (volta ao estado do último commit).
- `git restore --staged <arquivo>` – Remove o arquivo da área de staging, mantendo as alterações no diretório de trabalho.
- `git reset --soft HEAD~1` – Desfaz o último commit, mas mantém as alterações no staging.
- `git reset --hard HEAD~1` – Desfaz o último commit e descarta todas as alterações (cuidado!).

## Trabalhando com remotos
- `git remote -v` – Lista os repositórios remotos configurados.
- `git remote add origin <url>` – Adiciona um repositório remoto chamado "origin".
- `git push -u origin main` – Envia o branch local "main" para o remoto "origin" e configura o upstream.

## Stash (área temporária)
- `git stash` – Guarda temporariamente alterações não commitadas.
- `git stash list` – Lista os stashes salvos.
- `git stash apply` – Aplica o último stash, mas mantém na lista.
- `git stash pop` – Aplica o último stash e o remove da lista.

## Tags (marcações)
- `git tag` – Lista as tags existentes.
- `git tag <nome>` – Cria uma tag simples no commit atual.
- `git push --tags` – Envia todas as tags para o repositório remoto.