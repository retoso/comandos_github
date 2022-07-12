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
| git stash pop   | Abre a caixa (stash) e revove tudo |
| git stash apply | Recuperando modificações |
| git stash apply stash@{2} | Recuperando um stash de uma lista |
| git stash drop stash@{5} | Removendo Stashes |
| git stash clear | Apagar todas as caixas |

        Notas():
	 1 - Guarda tudo em uma caixa para voce voltar e continuar, neste caso nao precisa fazer um commit.     
	 2 - Colocando nome no stash     
	 3 - guardando tudo na caixa para nao poluir outra branch com as mudanças e arquivos da branch atual,     
             sendo assim nada aparecera no git status e nada para ser commit.   



| Comando | Descrição |
| --- | --- |	
| git log | Visualiza todos os logs |
| git log --graph (gitk) | Interface logica |
| git remote | Exibir os repositórios remotos |
| git remote add origin git@github.com:retoso/teste.git| Vincular repositório local com remoto |
| git remote show origin | Exibir dos repositórios remotos |
| git remote rename origin teste | Renomear um repositório remoto |
| git push -u origin master (1)(2) | Enviar arq./dir. p/o reposit.remoto |
| git push(3) | puxar arq./dir. p/o reposit.remoto |
	Notas():     
	 1 - O primeiro push de um repositório deve conter o nome do repositório remoto e o branch.     
	 2 - Sempre é bom não trabalhar apenas na main para evitar problemas e ter um projeto mais flexível.     
	 3 - Os demais pushes não precisam dessa informação.  

| Comando | Descrição |
| --- | --- |	
| git tag vs-1.1 | Criando uma tag leve |
| git tag -a vs-1.1 -m "Minha versão 1.1" | Criando uma tag anotada |
| git tag -s vs-1.1 -m "Minha tag assinada 1.1 (1)  | Criando uma tag assinada |
| git tag -a vs-1.2 9fceb02 | riando tag a partir d1 commit (hash) |
| git push origin vs-1.2  | Criando tags no repositorio remoto |
	Notas():     
	 1 - Para criar uma tag assinada é necessário uma chave privada (GNU Privacy Guard - GPG).     
	 2 - Caso você queira que ele liste também as branches que estão no repositório remoto, adicione -a     
    
  
  
  Referencia - https://docs.github.com/pt

