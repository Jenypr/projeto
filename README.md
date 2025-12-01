# projeto


---

### `/docs/visao_do_produto.md`
```markdown
# VISÃO DO PRODUTO – SchoolManager

## 1. Nome do Produto
**SchoolManager – Sistema Integrado de Gestão Escolar**

## 2. Problema a Ser Solucionado e Oportunidades

### Problemas Identificados
- Processos escolares feitos manualmente ou em múltiplas plataformas desconectadas.
- Comunicação ineficiente entre escola, responsáveis e alunos.
- Controle fragmentado de matrículas, notas e frequência.
- Geração de relatórios acadêmicos e administrativos lenta e propensa a erros.
- Professores sobrecarregados com tarefas administrativas.

### Oportunidades
- Automatizar processos e centralizar informações.
- Agilizar emissão de documentos e relatórios.
- Melhorar a comunicação e o acompanhamento pedagógico.
- Reduzir trabalho burocrático dos professores.
- Oferecer dashboards e indicadores para a direção.

## 3. Stakeholders e Necessidades

- **Direção Escolar:** relatórios gerenciais, indicadores e relatórios de desempenho.
- **Secretaria:** cadastro/matrícula, controle de turmas, emissão de documentos.
- **Professores:** lançamento de notas e faltas, consulta a turmas e alunos.
- **Alunos:** acesso a boletins, tarefas e calendário.
- **Responsáveis:** acompanhamento de desempenho e comunicação com a escola.
- **Equipe de TI:** sistema seguro, modular e com fácil manutenção.

## 4. Requisitos Funcionais (mínimos)

- **RF01** Cadastro e gerenciamento de alunos (CRUD).
- **RF02** Gerenciamento de turmas, disciplinas e horários.
- **RF03** Matrícula, rematrícula e transferência entre turmas.
- **RF04** Lançamento de notas e frequências pelos professores.
- **RF05** Emissão de boletins, histórico e relatórios.
- **RF06** Controle de usuários e permissões (direção, secretaria, professor, aluno, responsável).
- **RF07** Comunicação interna: avisos, mensagens e comunicados.
- **RF08** Geração de documentos: declaração de matrícula, atestados, etc.
- **RF09** Autenticação segura (login, recuperação de senha).

## 5. Requisitos Não-Funcionais

- **RNF01 — Segurança:** autenticação, autorização e criptografia de dados sensíveis.
- **RNF02 — Performance:** carregamento de telas em tempo aceitável.
- **RNF03 — Usabilidade:** interface intuitiva e responsiva.
- **RNF04 — Escalabilidade:** suportar crescimento de usuários e dados.
- **RNF05 — Disponibilidade:** alta disponibilidade, backup e recuperação.
- **RNF06 — Compatibilidade:** acesso via web, mobile (responsivo).
- **RNF07 — Manutenibilidade:** código modular e documentado.

## 6. Restrições e Premissas

- A implantação pode usar um banco SQL (MySQL/Postgres).
- Usuários possuem e-mail válido para comunicação e recuperação de senha.
- A escola fornecerá matriz curricular e horários iniciais para parametrização.

## 7. Métricas de Sucesso

- Redução do tempo gasto em tarefas administrativas (meta: -40%).
- Satisfação dos usuários (pesquisa interna > 80% positiva).
- Taxa de uso dos professores para lançamento de notas > 95%.
