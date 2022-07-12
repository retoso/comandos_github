# comandos_github

Desafio de projeto sobre Git/Github



# Projetos

 1) criar pasta e dar o comando *Tabspace*  git init  
 2) Autor*Tabspace* git config --global user.email "tonelli.renato@gmai.com"   
 3) Nome *Tabspace*  git config --globa user.name "retoso"  
 4) Adiciona o conteúdo do arq índice..: git add *   
 5) Comentando ........................: git commit -m "este teste foi realizado com sucesso"    
 6) Vincular gitRemote.................: git remote add origin https://github.com/retoso/workspace.git     
 7) Checar o vincuo....................: git remote -v    
 8) Reconfirmar pendendias.............: git status    
 9) Enviar tudo........................: git push origin master    
 10) Puxar.............................: git pull origin master
    
     
a) GitBash..........................................: Comandos     
>>a.1 - lista todos os arquivos...................: ls     
>>a.2 - limpar a tela.............................: crtl+l     
>>a.3 - checar as configurações do git............: git config --list     
>>a.4 - apagar credencias no computador...........: git config --global --unset user.email     
                                                      git config --global --unset user.nickname    
                                                      git config --global --unset user.name    
>>a.5 - definindo o editor do Commit..............: git config --global core.editor "code --wait"    
>>a.6 - removendo o editor do commit..............: git config --global --unset core.editor     
>>a.7 - Remover diretório.........................: git rm -r diretorio    
         
     

b) Vim..............................................: git config --global merge.tool vimdiff (1)    
	b.1 - Sair do modo de edição....................: esc    
	b.2 - Iniciar o comando.........................: :    
        b.3 - fecghar a mensagem....................: wq    
        b.4 - sair e salvar.........................: q     
               b.4.1 - sem salvar nada..............: q!     
     
# G I T     
      
 1 - Iniciando um Repositório...........................: git init     
 2 - Apagando um repositório............................: $ rm -rf .git     
 3 - Listando Arquivos Modificados......................: git status     
 4 - Desfazendo Alterações..............................: git checkout (1)     
	4.1 - Arquivos não monitorados......................: git git clean -df (2)     
 	4.2 - Removendo arquivos do Stage...................: git reset (3)     
	4.3 - Desfazendo o último commit....................: git revert HEAD     
	Notas():    
	 1 - Existe varios cenarios!    
	 2 - Para apagar novos arquivos que ainda não foram adicionados ao Stage.     
	 3 - Se você executou git add e quer desfazer, use o reset     
 5 - Commit.............................................:      
	5.1 - Criando um commnit............................: git commit -m "texto"     
        5.2 - reverter o commit.........................: (antes de enviar a para nuvel)     
     
 6 - Visualizando o Histórico de Commits................: git log     
	7.1 - Histórico de um ou mais arquivos..............: git log -p meus-arquivos    
	7.2 - Histórico de um autor.........................: git log --autor=nome-autor    
	7.3 - Histórico por Data............................: git log --after="MMM DD YYYY"     
    ....................................................: git log --before="MMM DD YYYY"     
     
 7 - Branches...........................................: (1)     
	7.1 - Listando Branches.........................: git branch     
    ................................................: git branch -a (2)     
	7.2 - Indo para outra branch....................: git checkout outra-branch     
	7.3 - Criar uma nova branch.....................: git checkout -b minha-nova-branch     
	7.4 - Excluindo branches........................: git checkout -d minha-nova-branch (1)     
	7.5 - Renomeando branches.......................: git branch -m novo-nome-da-branch     
    ................................................: git branch -m nome-atual novo-nome (2)     
        Notas():     
	 1 - A opção -d é mais segura, pois ela só apaga a branch se você já tiver feito merge ou enviado      
	     as alterações para seu repositório remoto, evitando perda de código. A opção -D ignora o      
	     estado da sua branch, forçando a sua remoção.     
	 2 - Se você estiver em uma branch e quiser renomear outra, você deve passar primeiro o nome atual da      
	     branch que quer renomear.     
     
 8 - Salvando modificações em um Stash.................: git stash (1)     
     ..................................................: git stash push -m meu-novo-stash (2)     
     ..................................................: git stash save "adicionando" (3)     
	    8.1 - Listando Stashes.........................: git stash list     
	    8.2 - Abre a caixa (stash) e revove tudo.......: git stash pop 3     
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
       

