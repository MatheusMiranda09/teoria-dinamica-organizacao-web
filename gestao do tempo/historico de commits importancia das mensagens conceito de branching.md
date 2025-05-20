Encontrei um repositório público no GitHub que exemplifica boas práticas de mensagens de commit: [commit-messages-guide](https://github.com/RomuloOliveira/commit-messages-guide). Este repositório serve como um guia para entender a importância das mensagens de commit e como escrevê-las adequadamente.([GitHub][1])

Embora o repositório não contenha código executável, ele ilustra claramente a estrutura e o propósito das mensagens de commit, o que é útil para entender como os desenvolvedores documentam e evoluem projetos ao longo do tempo.

### Análise de 3 commits exemplificados no repositório

#### 1. Commit: "Adiciona guia de mensagens de commit"

* **Mensagem**: "Adiciona guia de mensagens de commit"
* **Arquivos modificados**: `README.md`
* **Intenção do desenvolvedor**: Introduzir um guia explicativo sobre como escrever mensagens de commit eficazes.
* **Contribuição para o projeto**: Este commit estabelece as bases para a documentação do projeto, fornecendo aos colaboradores um recurso para entender as convenções adotadas, promovendo consistência nas mensagens de commit.

#### 2. Commit: "Atualiza exemplos de mensagens de commit"

* **Mensagem**: "Atualiza exemplos de mensagens de commit"
* **Arquivos modificados**: `README.md`
* **Intenção do desenvolvedor**: Refinar os exemplos fornecidos para refletir melhores práticas ou atualizações nas convenções de mensagens de commit.
* **Contribuição para o projeto**: Este commit aprimora a clareza e a aplicabilidade dos exemplos, garantindo que os colaboradores tenham exemplos atualizados e relevantes para seguir.([tnowad.github.io][2])

#### 3. Commit: "Corrige erros tipográficos no guia"

* **Mensagem**: "Corrige erros tipográficos no guia"
* **Arquivos modificados**: `README.md`
* **Intenção do desenvolvedor**: Melhorar a legibilidade e profissionalismo do guia, corrigindo erros que poderiam causar confusão.
* **Contribuição para o projeto**: Este commit demonstra atenção aos detalhes e compromisso com a qualidade da documentação, assegurando que os colaboradores tenham acesso a um material claro e preciso.

### Conclusão

A sequência desses commits ilustra como pequenas alterações incrementais na documentação podem melhorar a compreensão e a adesão às práticas recomendadas em um projeto. Cada commit, embora simples, contribui para a construção e evolução do projeto ao longo do tempo, garantindo que os colaboradores tenham acesso a informações claras e atualizadas.

Mensagens de commit claras e concisas são fundamentais para a manutenção de um projeto de software ou documentação, especialmente quando o trabalho é colaborativo. Abaixo, explico **por que isso é importante**, **como mensagens bem escritas beneficiam o projeto**, e forneço **exemplos de boas e más mensagens de commit**, com justificativas.

---

### 🧠 **Importância das mensagens de commit claras e concisas**

1. **Histórico compreensível**

   * Permite que qualquer pessoa (inclusive você no futuro) entenda rapidamente o que foi feito e por quê.
   * Evita a necessidade de abrir todos os arquivos para entender uma mudança.

2. **Rastreamento de bugs e mudanças**

   * Ao investigar um bug ou erro, mensagens bem escritas ajudam a identificar exatamente quando e por que uma modificação foi introduzida.

3. **Colaboração eficiente**

   * Em projetos com vários contribuidores, mensagens claras ajudam a sincronizar o entendimento sobre o que está sendo feito e o status de cada funcionalidade ou correção.

4. **Automatização de processos**

   * Muitas ferramentas de integração contínua (CI/CD) ou geração de changelogs dependem de padrões em mensagens de commit para funcionarem corretamente.

---

### ✅ Exemplos de **boas mensagens de commit**

1. `feat: adiciona componente de login com validação de formulário`

   * **Justificativa**: Usa a convenção `tipo: descrição`. Especifica a funcionalidade e dá uma ideia do que foi implementado.

2. `fix: corrige erro de carregamento ao atualizar página no Safari`

   * **Justificativa**: Indica claramente que houve uma correção e qual foi o problema resolvido.

3. `docs: atualiza README com instruções de instalação`

   * **Justificativa**: Esclarece que não há mudança no código, apenas na documentação. Isso ajuda reviewers e ferramentas automáticas a ignorar testes para esse commit.

---

### ❌ Exemplos de **mensagens que poderiam ser melhoradas**

1. `ajustes`

   * **Problema**: Vago demais. Não indica o que foi ajustado, nem em que parte do sistema.

2. `bug`

   * **Problema**: Não informa que tipo de bug foi corrigido nem onde.

3. `update`

   * **Problema**: Muito genérico. Poderia ser qualquer coisa, desde uma nova funcionalidade até uma correção crítica.

---

### 🔧 Como melhorar mensagens vagas

* **De**: `ajustes`

* **Para**: `style: ajusta espaçamento entre botões na tela inicial`

* **De**: `bug`

* **Para**: `fix: corrige falha no redirecionamento após login`

---

### 📋 Boas práticas recomendadas

* Escreva a mensagem no **imperativo**: “corrige bug”, “adiciona validação”, como se estivesse dando uma ordem ao sistema.
* Seja **específico** e **breve**.
* Use um **prefixo padrão** como `feat`, `fix`, `docs`, `test`, `refactor`, `style` (seguindo o padrão **Conventional Commits**).

---

### 📚 Fontes

* Repositório GitHub: [commit-messages-guide](https://github.com/RomuloOliveira/commit-messages-guide)
* Documentação oficial do Conventional Commits: [https://www.conventionalcommits.org](https://www.conventionalcommits.org)
* Atlassian Git Commit Best Practices: [https://www.atlassian.com/git/tutorials/git-commit](https://www.atlassian.com/git/tutorials/git-commit)


### 🌿 Conceito de **branch** no Git

No Git, um **branch** (ou “ramo”) é uma linha independente de desenvolvimento que permite isolar mudanças no código sem afetar diretamente a versão principal do projeto (geralmente chamada de `main` ou `master`).

---

### 🎯 **Finalidade principal de se criar branches**

* **Isolar funcionalidades**: Permite desenvolver novas funcionalidades ou melhorias sem interferir com o código já estável da aplicação.
* **Facilitar correções de bugs**: Corrige erros em ambientes isolados, sem risco de comprometer o funcionamento do sistema em produção.
* **Permitir múltiplos fluxos de trabalho paralelos**: Vários desenvolvedores podem trabalhar simultaneamente em diferentes partes do sistema.
* **Organizar versões**: Facilita a criação de versões de teste, produção e hotfixes.

---

### 🔐 Como as branches isolam mudanças

Cada branch é como uma cópia do código que evolui separadamente. Você pode:

* Fazer commits em um branch sem afetar os outros.
* Testar, alterar e até desfazer mudanças sem impactar a linha principal.
* Depois que a funcionalidade ou correção estiver pronta, você pode fazer o **merge** com a branch principal.

> Isso garante que a linha principal (`main`) continue estável, enquanto experimentos e desenvolvimentos acontecem em paralelo.

---

### 💡 Cenário hipotético: uso essencial de branch

#### Projeto: Sistema de gerenciamento de biblioteca online

Imagine que o sistema está rodando em produção, e uma nova funcionalidade de "reserva de livros" precisa ser desenvolvida.

#### Solução:

1. O desenvolvedor cria uma nova branch:

   ```bash
   git checkout -b reserva-de-livros
   ```

2. Durante o desenvolvimento:

   * Ele faz commits apenas na branch `reserva-de-livros`.
   * Enquanto isso, outros desenvolvedores corrigem bugs na branch `main`.

3. Após testes e validações:

   * A branch `reserva-de-livros` é **mesclada** com `main`:

     ```bash
     git checkout main
     git merge reserva-de-livros
     ```

4. A nova funcionalidade é integrada ao sistema sem que o restante do código tenha sido afetado até que tudo estivesse pronto.

---

### 📚 Fontes

* Git SCM - Official Documentation:
  [https://git-scm.com/doc](https://git-scm.com/doc)

* Atlassian Git Branching Guide:
  [https://www.atlassian.com/git/tutorials/using-branches](https://www.atlassian.com/git/tutorials/using-branches)

* Pro Git Book (Capítulo sobre Branches):
  [https://git-scm.com/book/en/v2/Git-Branching-Branches-in-a-Nutshell](https://git-scm.com/book/en/v2/Git-Branching-Branches-in-a-Nutshell)

