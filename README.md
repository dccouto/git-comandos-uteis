# git-comandos-uteis
Comandos uteis para utilizar o git

#### Criando um repositório git que sirva de servidor (só irá receber as informação dos outros que enviarem por push)
git init --bare

#### Mosta a linha do tempo das branchs
git log --graph

#### Criando uma conexão com o repositorio remoto, com isso o meu repositório local na minha branch que estou trabalhando irá se concetar com o repositório Servidor (Bare)
git remote add nome-que-eu-quiser   caminho-do-reositorio-git-remoto-do-servidor

#### fazer o push (se adicionar o '-u' ele vai associar o  nome_do_repositorio_remote com nome_da_branch e não precisa escrever na proxima vez)
git push nome_do_repositorio_remote nome_da_branch

#### Para fazer o Merge. Na branch master executa:
git merge nome_da_branch_sprint

#### Para atualizar a branch da sprint com a da Master, faça checkout pra master e de o comando git rebase nome_branch_sprint, com isso ele vai sincronizar com os commits na master e vai colocar as alterações (commites) da banch da sprint antes dos commits que foram feitos na banch master. O merge junta os trabalhos e gera um 'merge commit'. O rebase aplica os commits de outra branch na branch atual.
git rebase nome_branch_sprint

#### Ctrl + Z no Git - Desfazendo commits
git revert hash_do_commit_que_será_desfeito

#### Viajar no tempo para outros commits
git commit hash_do_commit

#### verificar as alterações entre 2 commits
git diff hash_comit .. hash_outro_commit

#### marcar tags na branch para gerar release
git tag -a nome_da_versão_ou_qualquer_outro_nome -m "mensagem_qualquer"

#### Exibe todas as Tags
git tag


#### Juntar vários commits em um só para facilitar a revisão do código no pull request. Após o comando abaixo, é necessário tirar o "pick" e mantar apenas no qual você quer manter como o commit principal, ao retirar o pick DEVE ser colocado a letra s no lugar do pick. (apenas 1 fica com o pick os outros com s) 
git rebase -i HEAD~3 (irá pegar a atual e unir com os 3 ultimos commits)

#### Sair do editor
:x para sair salvando do editor
