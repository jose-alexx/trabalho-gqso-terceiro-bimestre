## Git Merge e Rebase

<div align="center">
  <table>
    <tr>
      <td><b>💻 O que é merge?  </b></td>
      <td><b>💻 O que é rebase? </b></td>
    </tr>
    <tr>
      <td>O Merge combina as mudanças de uma branch (feature-branch) em outra (main), assim o Git cria um commit especial chamado  **commit de merge** que une os históricos das duas branches. Ele preserva o histórico completo de ambas as branches.</td>
      <td>O Rebase reaplica os commits de uma branch (feature-branch) no topo de outra branch (main), criando um histórico linear. Ele reescreve os commits da branch atual.</td>
    </tr>
  </table>
</div>

---

## Index

<details align="left">
  <summary color="#FFBD59">Semelhança...</summary>
 
 <p align="justify">

 <ul>
  <li>O <a href="https://git-scm.com/docs/git-merge"><strong>Merge</strong></a> e o <a href="https://git-scm.com/docs/git-rebase"><strong>Rebase</strong></a> são dois comandos do Git usados para combinar mudanças de diferentes ramificações (branches).</li>
  <li>Ambos têm o mesmo objetivo geral — <strong>integrar alterações</strong> —, mas funcionam de maneiras distintas, resultando em diferentes históricos de commits.</li>
  <li>Basicamente o git merge e o git rebase servem para a mesma coisa: mesclar alterações de duas branches diferentes.</li>
 </ul>

 **[⬆ Voltar ao Inicio](#Apresentação:)**

</p>

---

</details>

<details align="left">
  <summary style="color: #FFBD59">Diferenças entre Merge e Rebase...</summary> <br>

  <div align="center">
    <table style="width: 100%; border-collapse: collapse;">
      <tr>
        <td><b>Aspecto</b></td>
        <td><b>Merge</b></td>
        <td><b>Rebase</b></td>
      </tr>
      <tr>
        <td>Histórico</td>
        <td>Preserva o histórico original com um commit de merge.</td>
        <td>Reescreve o histórico para ser linear.</td>
      </tr>
      <tr>
        <td>Conflitos</td>
        <td>Resolvidos no commit de merge.</td>
        <td>Resolvidos durante o rebase.</td>
      </tr>
      <tr>
        <td>Colaboração</td>
        <td>Ideal para trabalho em equipe.</td>
        <td>Ideal para trabalho individual.</td>
      </tr>
    </table>
  </div>

  **[⬆ Voltar ao Inicio](#Apresentação:)**

  ---
  
</details>

<details align="left">
  <summary color="#FFBD59">Antes e depois do Merge e Rebase...</summary> <br>

 ```plaintext

-------- Merge --------              | ## Preserva o histórico das branches.
                                     |
  main:     A --- B                  | main:     A --- B --- E
                   \                 |                  \   
  feature-branch:    C --- D         | feature-branch:    C --- D

---------------------------------------------------------------------------

-------- Rebase --------             | ## histórico linear
                                     |
  main:     A --- B                  | 
                   \                 | main:     A --- B --- C' --- D'
  feature-branch:    C --- D         |
```

  <ul>
  <li><strong>Merge:</strong> Cria um <em>commit de merge</em> que une os históricos das branches.</li>
  <li><strong>Rebase:</strong> Reescreve o histórico, reaplicando os commits no topo de outra branch.</li>
</ul>

**[⬆ Voltar ao Inicio](#Apresentação:)**

---

</details>

<details align="left">
  <summary color="#FFBD59">Quando Usar Merge ou Rebase?...</summary> <br>

  <p align="justify">
Ao decidir entre usar <strong>merge</strong> ou <strong>rebase</strong>, considere o fluxo de trabalho do projeto e as preferências de histórico. Por exemplo, o <code>merge</code> é ideal para trabalho em equipe, enquanto o <code>rebase</code> é ótimo para um histórico mais limpo.
</p>

--- 

 - **Use Merge quando:**
   - O merge, na maioria das vezes, gera um novo commit, o que pode complicar o histórico, mas nunca o reescreve. (mas é mais seguro)
   - Está colaborando com outras pessoas e quer manter o histórico detalhado.
   - Não se importa com um histórico mais complexo.
   - Você quer preservar o histórico completo.

---

- **Use Rebase quando:**
   - Cuidado com rebase, você pode ter que forçar a reescrita para enviar as modificações, e com isso outros contribuidores podem ter conflitos quando tentarem enviar seus commits para a "nova" branch reescrita.
   - Já o rebase deixa o histórico linear e mais simples, mas alguns commits são reescritos, é muito útil para não “sujar” o histórico do repositório (mas possui mais riscos).
   - Quer aplicar mudanças da branch base antes de compartilhar seu trabalho.
   - Está trabalhando sozinho ou em branches que ninguém mais usa.
   - Você quer um histórico linear e limpo.

   **[⬆ Voltar ao Inicio](#Apresentação:)**
 
---

</details>

<details align="left">
  <summary color="#FFBD59">Comandos...</summary> <br>

 <div align="center">

| **Ação**               | **Merge**                       | **Rebase**                       |
|-------------------------|----------------------------------|-----------------------------------|
| Trocar para a branch base | `git checkout main`             | `git checkout feature-branch`            |
| Atualizar a branch base  | `git pull origin main`          | `git pull origin main`            |
| Combinar as branches     | `git merge feature-branch`             | `git rebase main`                 |
| Resolver conflitos       | Editar arquivos e `git add`     | Editar arquivos e `git add`       |
| Continuar operação       | `git commit`                   | `git rebase --continue`           |
| Enviar alterações        | `git push origin main`          | `git push origin feature-branch --force` |
</div>

**[⬆ Voltar ao Inicio](#Apresentação:)**

---

</details>

<details align="left">
  <summary color="#FFBD59">Trabalho terceiro bimestre de Gestão de qualidade de Software...</summary> <br>

   - [Branches no Git - <a href="https://shields.io/">Rebase</a><br>](https://git-scm.com/book/pt-br/v2/Branches-no-Git-Rebase)
   - [Tutorial Git - <a href="https://shields.io/">Merge</a><br>](https://www.atlassian.com/br/git/tutorials/using-branches/git-merge)
   - [Tutorial Git - <a href="https://shields.io/">Rebase</a><br>](https://www.atlassian.com/br/git/tutorials/rewriting-history/git-rebase)

   **[⬆ Back to Index](#index)**
   
</details>
