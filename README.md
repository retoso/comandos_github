# comandos_github

Desafio de projeto sobre Git/Github



# Projetos
| Comando | Descrição |
| --- | --- |
| git init | criar pasta e dar o comando |
| git config --global user.email "tonelli.renato@gmai.com" | Autor |
| git config --globa user.name "retoso" | Nome |
| git add *  | Adiciona o conteúdo do arq índice |
| git commit -m "arquivo .js criado para ..." | Comentando  |
| git remote add origin https://github.com/retoso/workspace.git | Vincular gitRemote |
| git remote -v  | Checar o vincuo |
| git status  | Reconfirmar pendendias |
| git push origin master | Enviar tudo |
| git pull origin master | Puxar |
     
# GitBash
| Comando | Descrição |
| --- | --- |
| ls | lista todos os arquivos |
| crtl+l | limpar a tela |
| git config --list | checar as configurações do git |
| git config --global --unset user.email | apagar credencias no computado |
| git config --global --unset user.nickname | apagar credencias no computado |
| git config --global --unset user.name | apagar credencias no computado |
| git config --global core.editor "code --wait" | definindo o editor do Commit |
| git config --global --unset core.editor  | removendo o editor do commit |


# Vim
| Comando | Descrição |
| --- | --- |
| git config --global merge.tool vimdiff | Configuracao |
| esc | Sair do modo de edição |
| : | Iniciar o comand |
| wq | fechar a mensage |
| q | sair e salvar |
| q! | sem salvar nada |

# Git
| Comando | Descrição |
| --- | --- |
| git init  | Iniciando um Repositório  |
| git status  | Listando Arquivos Modificados |

| Comando | Descrição |
| --- | --- |
| git checkout (1)  | Desfazendo Alterações  |
| git git clean -df (2) | Arquivos não monitorados  |
| git reset (3) | Removendo arquivos do Stage |
| git revert HEAD  | Desfazendo o último commit  |
	Notas():    
	 1 - Existe varios cenarios!    
	 2 - Para apagar novos arquivos que ainda não foram adicionados ao Stage.     
	 3 - Se você executou git add e quer desfazer, use o reset 
	 
| Comando | Descrição |
| --- | --- |	 
| git commit -m "texto" | Criando um commnit |
| git log | Visualizando o Histórico de Commits  |
| git log -p meus-arquivo  | Histórico de um ou mais arquivos |
| git log --autor=nome-autor | Histórico de um autor |
| git log --after="MMM DD YYYY"  | Histórico por Data |
| git log --before="MMM DD YYYY"  | Histórico por Data |
| git branch | Listando Branches |
| git branch -a | istando Branches |
| git checkout outra-branch | Indo para outra branch |
| git checkout -b minha-nova-branch  | Criar uma nova branch  |
| git checkout -d minha-nova-branch (1) | Excluindo branches |
| git branch -m novo-nome-da-branch | Renomeando branches |
| git branch -m nome-atual novo-nome (2) | Renomeando branche |
        Notas():     
	 1 - A opção -d é mais segura, pois ela só apaga a branch se você já tiver feito merge ou enviado      
	     as alterações para seu repositório remoto, evitando perda de código. A opção -D ignora o      
	     estado da sua branch, forçando a sua remoção.     
	 2 - Se você estiver em uma branch e quiser renomear outra, você deve passar primeiro o nome atual da      
	     branch que quer renomear. 
# Stash	     
| Comando | Descrição |
| --- | --- |	
| git stash (1) | Salvando modificações em um Stash |
| git stash push -m meu-novo-stash (2) |  |
| git stash save "adicionando" (3) |  |
| git stash list | Listando Stashes |
|  | Abre a caixa (stash) e revove tudo |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |
 
    
	    8.1 - Listando Stashes........	.................: git stash list     
	    8.2 - Abre a caixa (stash) e	 revove tudo.......: git stash pop 3     
	    8.2 - Recuperando modificações.................: git stash apply     
	    8.3 - Recuperando um stash de uma lista........: git stash apply stash@{2}     
	    8.4 - Removendo Stashes........................: git stash drop stash@{5}     
        8.5 - Apagar todas as caixas...................: git stash clear     
	Notas():     
	 1 - Guarda tudo em uma caixa para voce voltar e continuar, neste caso nao precisa fazer um commit.     
	 2 - Colocando nome no stash     
	 3 - guardando tudo na caixa para nao poluir outra branch com as mudanças e arquivos da branch atual,     
             sendo assim nada aparecera no git status e nada para ser commit.     
 9 - log.............................................: comandos     
	    9.1 - Visualiza todos os logs................: git log     
        9.2 - visualiza todos os logs de um diretorio: git log contributing     
 	    9.3 - resumo de tudo em uma linha............: git log --onine     
	    9.4 - Interface logica.......................: git log --graph (gitk)     
10 - Repositorios Remotos............................: comandos     
	    10.1 - Exibir os repositórios remotos........: git remote     
	    10.2 - Vincular repositório local com remoto.: git remote add origin git@github.com:retoso/teste.git     
	    10.3 - Exibir dos repositórios remotos.......: git remote show origin     
	    10.4 - Renomear um repositório remoto........: git remote rename origin teste     
	    10.5 - Enviar arq./dir. p/o reposit.remoto...: git push -u origin master (1)(2)     
        .............................................: git push(3)     
	Notas():     
	 1 - O primeiro push de um repositório deve conter o nome do repositório remoto e o branch.     
	 2 - Sempre é bom não trabalhar apenas na main para evitar problemas e ter um projeto mais flexível.     
	 3 - Os demais pushes não precisam dessa informação.     

11 - Tags...........................................: comandos     
	    11.1 - Criando uma tag leve.................: git tag vs-1.1     
	    11.2 - Criando uma tag anotada..............: git tag -a vs-1.1 -m "Minha versão 1.1"     
	    11.3 - Criando uma tag assinada.............: git tag -s vs-1.1 -m "Minha tag assinada 1.1 (1)     
	    11.4 - Criando tag a partir d1 commit (hash): git tag -a vs-1.2 9fceb02     
	    11.5 - Criando tags no repositorio remoto...: git push origin vs-1.2     
	Notas():     
	 1 - Para criar uma tag assinada é necessário uma chave privada (GNU Privacy Guard - GPG).     
	 2 - Caso você queira que ele liste também as branches que estão no repositório remoto, adicione -a     
       

