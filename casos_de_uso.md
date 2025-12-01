# CASOS DE USO

---

## 📌 Diagrama de Casos de Uso

```markdown
![Diagrama de Casos de Uso](/.workpaces/projeto/imagens/diagrama_casos_de_uso.png)
)

```

---

## UC01 – Login e Autenticação

**Atores:** Secretaria, Professor, Aluno
**Descrição:** Permite que usuários autenticados acessem o sistema com o perfil adequado.

**Pré-condições**

* Usuário cadastrado no sistema.
* Conexão com o banco de dados.

**Pós-condições**

* Usuário autenticado e direcionado ao painel correspondente.

**Fluxo Principal**

1. Usuário acessa a tela de login.
2. Sistema solicita e-mail ou nome de usuário e senha.
3. Usuário informa credenciais.
4. Sistema valida os dados no banco.
5. Sistema identifica o perfil (professor, aluno, secretaria).
6. Sistema redireciona para o painel correspondente.

**Fluxos Alternativos**

* **A1 — Esqueceu a senha:** Usuário solicita recuperação; sistema envia link por e-mail; usuário redefine senha.

**Exceções**

* Credenciais inválidas → mensagem de erro.
* Usuário inexistente → sugestão de contatar a secretaria.
* Falha de conexão → tentar novamente mais tarde.

---

## UC02 – Realizar Matrícula

**Atores:** Secretaria
**Descrição:** Registrar a matrícula de um aluno em uma turma para o período letivo.

**Pré-condições**

* Turmas configuradas no sistema.
* Aluno cadastrado.

**Pós-condições**

* Aluno matriculado e vinculado à turma selecionada.

**Fluxo Principal**

1. Secretaria acessa o módulo de matrículas.
2. Sistema exibe lista de alunos cadastrados.
3. Secretaria seleciona o aluno.
4. Sistema exibe turmas com vagas disponíveis.
5. Secretaria escolhe uma turma.
6. Sistema verifica disponibilidade.
7. Matrícula é confirmada e salva.
8. Sistema gera comprovante.

**Fluxos Alternativos**

* **A1 — Cadastro novo:** Se aluno não existir, secretaria realiza cadastro antes da matrícula.
* **A2 — Lista de espera:** Caso turma esteja cheia.

**Exceções**

* Turma lotada → exibir opção de lista de espera.
* Dados insuficientes → sistema impede conclusão.
* Erro na gravação → matrícula não concluída.

---

## UC03 – Lançar Notas e Frequência

**Atores:** Professor
**Descrição:** Permite que o professor registre notas e faltas dos alunos das turmas atribuídas.

**Pré-condições**

* Professor autenticado.
* Turma vinculada ao professor.

**Pós-condições**

* Notas e frequências registradas e atualizadas no sistema.

**Fluxo Principal**

1. Professor acessa o Diário de Classe.
2. Sistema exibe turmas do professor.
3. Professor seleciona a turma.
4. Sistema mostra lista de alunos.
5. Professor insere notas e faltas.
6. Professor confirma o lançamento.
7. Sistema salva informações.

**Fluxos Alternativos**

* **A1 — Lançamento parcial:** professor salva rascunho.
* **A2 — Edição:** professor edita antes do fechamento.

**Exceções**

* Nota inválida → sistema alerta e impede.
* Falha ao salvar → mensagem de erro.

---