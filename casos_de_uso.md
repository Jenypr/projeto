# CASOS DE USO – SchoolManager

---

## UC01 – Login e Autenticação

**Atores:** Usuário (Direção, Secretaria, Professor, Aluno, Responsável)  
**Descrição:** Permite que usuários autenticados acessem o sistema com o perfil adequado.

**Pré-condições**
- Usuário cadastrado no sistema.
- Conexão com o banco de dados.

**Pós-condições**
- Usuário autenticado e direcionado ao painel correspondente.

**Fluxo Principal**
1. Usuário acessa a tela de login.
2. Sistema solicita e-mail/usuário e senha.
3. Usuário informa credenciais.
4. Sistema valida credenciais no banco.
5. Sistema identifica perfil (direção, professor, etc.).
6. Sistema redireciona para o painel apropriado.

**Fluxos Alternativos**
- **A1 — Esqueceu a senha:** usuário solicita recuperação; sistema envia link por e-mail; usuário redefine senha e retorna ao fluxo principal.

**Exceções**
- Credenciais inválidas → mensagem de erro.
- Conta inexistente → sugestão de contato com secretaria.
- Falha de conexão → notificar e recomendar tentativa posterior.

---

## UC02 – Realizar Matrícula

**Atores:** Secretaria, Sistema de Matrículas  
**Descrição:** Registrar a matrícula de um aluno em uma turma para um período letivo.

**Pré-condições**
- Turmas e períodos definidas.
- Aluno cadastrado (ou cadastro realizado durante o processo).

**Pós-condições**
- Matrícula registrada e aluno associado à turma.

**Fluxo Principal**
1. Secretário acessa o módulo de matrículas.
2. Sistema lista alunos pré-cadastrados.
3. Secretário seleciona aluno ou escolhe "Novo Cadastro".
4. Sistema exibe turmas disponíveis para o período.
5. Secretário seleciona turma.
6. Sistema verifica disponibilidade de vagas.
7. Sistema confirma matrícula e grava no banco.
8. Sistema emite comprovante e atualiza histórico.

**Fluxos Alternativos**
- **A1 — Cadastro novo:** novo aluno é cadastrado, depois segue processo normal.
- **A2 — Lista de espera:** em caso de lotação, aluno é registrado em fila de espera.

**Exceções**
- Turma lotada → sistema oferece fila de espera.
- Dados insuficientes → solicita correção.
- Erro no banco → operação abortada e mensagem de erro.

---

## UC03 – Lançar Notas e Frequência

**Atores:** Professor, Sistema Acadêmico  
**Descrição:** Permite ao professor lançar notas e presença dos alunos de suas turmas.

**Pré-condições**
- Professor autenticado.
- Turma e disciplina vinculadas ao professor.

**Pós-condições**
- Notas e frequências salvas; boletins atualizados.

**Fluxo Principal**
1. Professor acessa "Diário de Classe".
2. Sistema exibe turmas/disciplinas vinculadas.
3. Professor seleciona turma e data/período de lançamento.
4. Sistema lista alunos.
5. Professor insere notas e faltas.
6. Professor submete as informações.
7. Sistema valida os valores e salva no banco.

**Fluxos Alternativos**
- **A1 — Lançamento parcial:** professor salva rascunho e finaliza depois.
- **A2 — Edição:** após salvar, professor pode editar antes do fechamento do período.

**Exceções**
- Valor de nota inválido → alerta e impedimento.
- Falha ao salvar → sugestão para tentar novamente.

---

## Observações
- Para cada UC principal, recomenda-se criar diagrama de sequência que mostre chamadas ao repositório (DAO) e validações.
- Priorizar UC02 e UC03 para modelagem detalhada (envolvem regras de negócio e múltiplos atores).