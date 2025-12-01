# projeto

# SchoolManager – Sistema Integrado de Gestão Escolar

## Visão geral
O **SchoolManager** é um sistema para apoiar rotinas administrativas e pedagógicas de instituições de ensino. Centraliza matrículas, turmas, lançamentos de notas/frequências, emissão de documentos e comunicação entre escola, professores, alunos e responsáveis.

## Estrutura do repositório
- `docs/` — documentos do projeto (Visão do Produto, Casos de Uso, diagramas).
- `scripts/` — scripts de apoio (por exemplo, geração de PDFs).
- `README.md` — este arquivo.

## Como abrir no Visual Studio Code
1. Abra o VS Code.
2. `File -> Open Folder...` e selecione a pasta `schoolmanager`.
3. Abra um terminal integrado (`Ctrl+` ` ou Terminal -> New Terminal`).

## Como executar (gerar PDFs dos documentos)
Recomendado criar um ambiente virtual Python:

```bash
python -m venv .venv
# Windows
.venv\Scripts\activate
# Linux / macOS
source .venv/bin/activate

pip install reportlab
python scripts/generate_pdfs.py