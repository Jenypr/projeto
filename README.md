# YTTrack: Sistema de Gerenciamento de Conteúdo do YouTube

## 1. Documento de Visão

### 1.1 Nome do Produto

YTTrack – Sistema de Gerenciamento de Conteúdo do YouTube.

### 1.2 Problema a ser solucionado e oportunidades

Criadores de conteúdo do YouTube enfrentam dificuldades para gerenciar, de forma organizada e estratégica, seus vídeos, métricas de desempenho, cronogramas de publicação e histórico de alterações. Atualmente, muitas dessas informações ficam dispersas em diferentes ferramentas ou são acompanhadas manualmente, o que aumenta o risco de erros e perda de produtividade.

O YTTrack surge como uma oportunidade de centralizar o gerenciamento de conteúdo do YouTube em um único sistema, permitindo melhor controle, acompanhamento de desempenho e apoio à tomada de decisões estratégicas para crescimento do canal.

### 1.3 Stakeholders e suas necessidades

* **Criador de Conteúdo**: gerenciar vídeos, acompanhar métricas, organizar publicações e melhorar o desempenho do canal.
* **Administrador do Sistema**: manter o sistema funcionando corretamente, gerenciar usuários e garantir a segurança das informações.
* **Equipe de Marketing/Produção**: acessar dados de desempenho e planejar estratégias de conteúdo.

### 1.4 Requisitos Funcionais

* RF01: Permitir cadastro e autenticação de usuários.
* RF02: Permitir o cadastro de canais do YouTube no sistema.
* RF03: Permitir o registro e gerenciamento de vídeos publicados.
* RF04: Permitir o acompanhamento de métricas (visualizações, curtidas, comentários).
* RF05: Permitir o planejamento e controle de cronograma de publicações.
* RF06: Gerar relatórios de desempenho dos vídeos e do canal.

### 1.5 Requisitos Não Funcionais

* RNF01: O sistema deve possuir interface web responsiva.
* RNF02: O sistema deve garantir a segurança dos dados dos usuários.
* RNF03: O sistema deve ter boa usabilidade e facilidade de navegação.
* RNF04: O sistema deve ser escalável para suportar múltiplos usuários.

---

## 2. Modelo de Casos de Uso

### 2.1 Diagrama de Casos de Uso

![Diagrama de Casos de Uso do YTTrack](casos_de_uso.png)


> O diagrama representa graficamente os atores do sistema YTTrack e suas interações com os principais casos de uso, utilizando a notação padrão da UML.

### 2.1 Atores

* Usuário (Criador de Conteúdo)
* Administrador

### 2.2 Lista de Casos de Uso Principais

* UC01: Autenticar Usuário
* UC02: Cadastrar Canal do YouTube
* UC03: Gerenciar Vídeos
* UC04: Visualizar Métricas e Relatórios

---

### UC01 – Autenticar Usuário

* **Ator**: Usuário
* **Pré-condições**: Usuário possuir cadastro no sistema.
* **Pós-condições**: Usuário autenticado e com acesso ao sistema.
* **Fluxo Principal**:

  1. Usuário informa login e senha.
  2. Sistema valida as credenciais.
  3. Sistema libera o acesso.
* **Fluxo Alternativo**:

  * Credenciais inválidas → sistema exibe mensagem de erro.

---

### UC02 – Cadastrar Canal do YouTube

* **Ator**: Usuário
* **Pré-condições**: Usuário autenticado.
* **Pós-condições**: Canal registrado no sistema.
* **Fluxo Principal**:

  1. Usuário informa dados do canal.
  2. Sistema valida as informações.
  3. Sistema salva o canal.

---

### UC03 – Gerenciar Vídeos

* **Ator**: Usuário
* **Pré-condições**: Canal cadastrado.
* **Pós-condições**: Vídeos cadastrados ou atualizados.
* **Fluxo Principal**:

  1. Usuário seleciona um canal.
  2. Usuário cadastra ou edita informações do vídeo.
  3. Sistema salva as alterações.

---

### UC04 – Visualizar Métricas e Relatórios

* **Ator**: Usuário
* **Pré-condições**: Vídeos cadastrados.
* **Pós-condições**: Relatório exibido.
* **Fluxo Principal**:

  1. Usuário solicita relatório.
  2. Sistema processa os dados.
  3. Sistema exibe métricas e gráficos.
