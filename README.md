# WorkoutAPI

Esta é uma API de competição de crossfit chamada WorkoutAPI desenvolvida juntamente com o curso da DIO. É uma API pequena, projetada para ser um projeto hands-on e simplificado. Desenvolvemos uma API com poucas tabelas, mas com o necessário para aprender a utilizar o FastAPI.

## Stack da API

A API foi desenvolvida utilizando o FastAPI (async), juntamente com as seguintes bibliotecas:
- Alembic
- SQLAlchemy
- Pydantic

Para salvar os dados, estamos utilizando o PostgreSQL, por meio do Docker.

## Execução da API

Para executar o projeto, utilizei a pyenv, com a versão 3.11.4 do Python para o ambiente virtual.

Caso opte por usar pyenv, após instalar, execute:

```bash
pyenv virtualenv 3.11.4 workoutapi
pyenv activate workoutapi
pip install -r requirements.txt
```

Para subir o banco de dados, caso não tenha o docker-compose instalado, faça a instalação e, em seguida, execute:

```bash
make run-docker
```

Para criar uma nova migration, execute:

```bash
make create-migrations d="nome_da_migration"
```

Para criar o banco de dados, execute:

```bash
make run-migrations
```

## API

Para subir a API, execute:

```bash
make run
```

e acesse: [http://127.0.0.1:8000/docs](http://127.0.0.1:8000/docs)
