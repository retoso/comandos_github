Comandos_github
Desafio de projeto sobre Git/Github

Projetos
Criar pasta e dar o comando ———————> git init
Autor —————————————————-> git config —global user.email “tonelli.renato@gmai.com”
Nome—————————————————-> git config —globa user.name “retoso”
Adiciona o conteúdo do arq índice—————> git add *
Comentando ——————————————> git commit -m “este teste foi realizado com sucesso”
Vincular gitRemote ———————————-> git remote add origin https://github.com/retoso/workspace.git
Checar o vincuo ————————————-> git remote -v
Reconfirmar pendendias —————————> git status
Enviar tudo ———————————————> git push origin master
Puxar —————————————————-> git pull origin master
GitBash
1 - lista todos os arquivos———————> ls
2 - limpar a tela ———————————> crtl+l
3 - checar as configurações do git ———> git config —list
4 - apagar credencias no computador —-> git config —global —unset user.email
——————————————————-> git config —global —unset user.nickname
——————————————————-> git config —global —unset user.name
5 - definindo o editor do Commit ————> git config —global core.editor “code —wait”
6 - removendo o editor do commit ———-> git config —global —unset core.editor
7 - Remover diretório —————————> git rm -r diretorio

Vim
——————————————> git config —global merge.tool vimdiff (1)
1 - Sair do modo de edição ——> esc
2 - Iniciar o comando —————> :
3 - fechar a mensagem ————> wq
4 - sair e salvar ———————-> q
5 - sem salvar nada —————-> q!

Git
1 - Iniciando um Repositório —————————-> git init
2 - Apagando um repositório —————————-> rm -rf .git
3 - Listando Arquivos Modificados ———————> git status
4 - Desfazendo Alterações ——————————-> git checkout (1)

4.1 - Arquivos não monitorados………………….: git git clean -df (2)
4.2 - Removendo arquivos do Stage……………….: git reset (3)
4.3 - Desfazendo o último commit………………..: git revert HEAD
Notas():
1 - Existe varios cenarios!
2 - Para apagar novos arquivos que ainda não foram adicionados ao Stage.
3 - Se você executou git add e quer desfazer, use o reset

5 - Commit

1 - Criando um commnit ————> git commit -m “texto”
2 - reverter o commit —————-> (antes de enviar a para nuvel)

6 - Visualizando o Histórico de Commits…………….: git log

1 - Histórico de um ou mais arquivos ——————-> git log -p meus-arquivos
2 - Histórico de um autor ———————————-> git log —autor=nome-autor
3 - Histórico por Data —————————————> git log —after=”MMM DD YYYY”
———————————————————————> git log —before=”MMM DD YYYY”

7 - Branches

1 - Listando Branches ————————————> git branch
——————————————————————> git branch -a (2)
2 - Indo para outra branch ——————————> git checkout outra-branch
3 - Criar uma nova branch ——————————> git checkout -b minha-nova-branch
4 - Excluindo branches ———————————-> git checkout -d minha-nova-branch (1)
5 - Renomeando branches —————————-> git branch -m novo-nome-da-branch
—————————————————————-> git branch -m nome-atual novo-nome (2)
Notas():
1 - A opção -d é mais segura, pois ela só apaga a branch se você já tiver feito merge ou enviado
as alterações para seu repositório remoto, evitando perda de código. A opção -D ignora o
estado da sua branch, forçando a sua remoção.
2 - Se você estiver em uma branch e quiser renomear outra, você deve passar primeiro o nome atual da branch que quer renomear.

8 - Salvando modificações em um Stash.——-> git stash (1)
————————————————————-> git stash push -m meu-novo-stash (2)
————————————————————-> git stash save “adicionando” (3)

1 - Listando Stashes———————————> git stash list
2 - Abre a caixa (stash) e revove tudo———-> git stash pop 3
3 - Recuperando modificações——————-> git stash apply
4 - Recuperando um stash de uma lista——-> git stash apply stash@{2}
5 - Removendo Stashes—————————> git stash drop stash@{5}
6 - Apagar todas as caixas————————> git stash clear
Notas():
1 - Guarda tudo em uma caixa para voce voltar e continuar, neste caso nao precisa fazer um commit.
2 - Colocando nome no stash
3 - guardando tudo na caixa para nao poluir outra branch com as mudanças e arquivos da branch atual, sendo assim nada aparecera no git status e nada para ser commit.

9 - log………………………………………: comandos

1 - Visualiza todos os logs…………………: git log
2 - visualiza todos os logs de um diretorio.:.git log contributing
3 - resumo de tudo em uma linha…………: git log —onine
4 - Interface logica………………………….: git log —graph (gitk)

10 - Repositorios Remotos……………………….: comandos

1 - Exibir os repositórios remotos………………: git remote
2 - Vincular repositório local com remoto……..: git remote add origin git@github.com:retoso/teste.git
3 - Exibir dos repositórios remotos…………….: git remote show origin
4 - Renomear um repositório remoto………….: git remote rename origin teste
5 - Enviar arq./dir. p/o reposit.remoto………….: git push -u origin master (1)(2)
…………………………………………………….: git push(3)
Notas():
1 - O primeiro push de um repositório deve conter o nome do repositório remoto e o branch.
2 - Sempre é bom não trabalhar apenas na main para evitar problemas e ter um projeto mais flexível. 3 - Os demais pushes não precisam dessa informação.

11 - Tags……………………………………….: comandos

1 - Criando uma tag leve……………………: git tag vs-1.1
2 - Criando uma tag anotada………………: git tag -a vs-1.1 -m “Minha versão 1.1”
3 - Criando uma tag assinada……………..: git tag -s vs-1.1 -m “Minha tag assinada 1.1 (1)
4 - Criando tag a partir d1 commit (hash)..: git tag -a vs-1.2 9fceb02
5 - Criando tags no repositorio remoto……: git push origin vs-1.2
Notas():
1 - Para criar uma tag assinada é necessário uma chave privada (GNU Privacy Guard - GPG).
2 - Caso você queira que ele liste também as branches que estão no repositório remoto, adicione -a.
