# Python Project Template

Template básico para projetos Python com configuração mínima pronta para uso.

## Visão geral

Este repositório serve como base para iniciar novos projetos em Python com:

- estrutura simples de aplicação
- configuração com `pyproject.toml`
- testes com `pytest`
- lint/format com `ruff`
- suporte para tarefas com `taskipy`
- containerização com `Docker` e `docker-compose`

## Estrutura do projeto

- `main.py`: ponto de entrada da aplicação. Atualmente está vazio e deve ser substituído pela lógica principal do projeto.
- `tests/`: pasta para testes automatizados.
- `pyproject.toml`: configuração do projeto, dependências e tarefas.
- `Dockerfile`: imagem para executar a aplicação em container.
- `docker-compose.yml`: base para orquestração local, ainda a ser configurada conforme o projeto.

## Pré-requisitos

- Python 3.13+
- `uv` instalado
- opcionalmente: Docker e Docker Compose

## Configuração inicial

1. Clone o repositório:

   ```bash
   git clone <url-do-repositorio>
   cd python_project_template
   ```

2. Instale as dependências do projeto:

   ```bash
   uv sync --dev
   ```

## Como usar

### Executar a aplicação

```bash
uv run python main.py
```

> O arquivo `main.py` está como placeholder. Ajuste-o para a lógica real da aplicação.

### Executar testes

```bash
uv run pytest
```

### Verificar lint

```bash
uv run ruff check
```

### Formatar o código

```bash
uv run ruff format
```

### Executar tarefas definidas no projeto

Este template já inclui tarefas configuradas no `pyproject.toml`, como:

```bash
uv run task lint
uv run task test
uv run task format
```

## Docker

### Build da imagem

```bash
docker build -t python-project-template .
```

### Rodar o container

```bash
docker run --rm -p 8000:8000 python-project-template
```

### Com Docker Compose

```bash
docker compose up --build
```

## Personalização

Para adaptar este template ao seu projeto, você pode:

- alterar o nome do pacote no `pyproject.toml`
- substituir `main.py` pela aplicação principal
- adicionar dependências necessárias
- criar módulos e serviços conforme a arquitetura do projeto
- expandir a estrutura de testes e scripts

## Observação

Este é um template inicial e pode ser ajustado conforme a necessidade de cada aplicação. O objetivo principal é fornecer uma base limpa, padronizada e pronta para evolução.
