Trabalho terceiro bimestre de Gestão de qualidade de Software

https://git-scm.com/docs/git-rebase

asicamente o git merge e o git rebase servem para a mesma coisa: mesclar alterações de duas branches diferentes.

O merge, na maioria das vezes, gera um novo commit, o que pode complicar o histórico, mas nunca o reescreve. (mas é mais seguro)

Já o rebase deixa o histórico linear e mais simples, mas alguns commits são reescritos, é muito útil para não “sujar” o histórico do repositório (mas possui mais riscos).

Cuidado com rebase, você pode ter que forçar a reescrita para enviar as modificações, e com isso outros contribuidores podem ter conflitos quando tentarem enviar seus commits para a "nova" branch reescrita.