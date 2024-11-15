# Git Merge e Rebase

O [**merge**](https://git-scm.com/docs/git-merge) e o [**rebase**](https://git-scm.com/docs/git-rebase) são dois comandos do Git usados para combinar mudanças de diferentes ramificações (branches). Ambos têm o mesmo objetivo geral — **integrar alterações** —, mas funcionam de maneiras distintas, resultando em diferentes históricos de commits.

---
<br>

 <a href="https://github.com/jose-alexx">
    <img align="center" src="https://raw.githubusercontent.com/gist/jose-alexx/46db7915f5fcea4e0a93a27e3879dbff/raw/2e041a4a617fc224827786d5a57d11dd49391af7/apresentacao-merge-rebase.svg">
  </a> 

## **O que é Merge?**

O **merge** combina as mudanças de uma branch em outra, criando um **commit de merge** que une os históricos das branches. Ele preserva o histórico completo de ambas as branches.

### Exemplo de Merge:
```plaintext
main:     A --- B --- M
                  \     
feature:           C --- D





Trabalho terceiro bimestre de Gestão de qualidade de Software


https://git-scm.com/book/pt-br/v2/Branches-no-Git-Rebase
https://www.atlassian.com/br/git/tutorials/using-branches/git-merge#:~:text=Como%20funciona&text=Nestes%20cen%C3%A1rios%2C%20o%20git%20merge,sequ%C3%AAncia%20de%20merge%20commit%20enfileirada.
https://www.atlassian.com/br/git/tutorials/rewriting-history/git-rebase

Basicamente o git merge e o git rebase servem para a mesma coisa: mesclar alterações de duas branches diferentes.

O merge, na maioria das vezes, gera um novo commit, o que pode complicar o histórico, mas nunca o reescreve. (mas é mais seguro)

Já o rebase deixa o histórico linear e mais simples, mas alguns commits são reescritos, é muito útil para não “sujar” o histórico do repositório (mas possui mais riscos).

Cuidado com rebase, você pode ter que forçar a reescrita para enviar as modificações, e com isso outros contribuidores podem ter conflitos quando tentarem enviar seus commits para a "nova" branch reescrita.

Alex passou por aquidssffefe
tesrte
olá
Hello World
TESTANDO
cachorro