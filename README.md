
# FastAPI Boilerplate

Este é um modelo básico de API utilizando o framework FastAPI, com configuração para rodar em um container Docker. Este projeto serve como um ponto de partida para construir APIs com FastAPI.

## Funcionalidades

- Estrutura simples com uma rota de exemplo (`GET /`) que retorna uma mensagem.
- Configuração pronta para Docker, facilitando a implantação.
- Arquivo `requirements.txt` com dependências mínimas para iniciar o desenvolvimento.

## Estrutura do Projeto

```
fastapi-boilerplate/
├── app/
│   ├── main.py         # Código principal da aplicação
├── Dockerfile          # Configuração do Docker
├── requirements.txt    # Dependências do projeto
```

## Pré-requisitos

- [Python 3.10+](https://www.python.org/downloads/)
- [Docker](https://www.docker.com/get-started) (para rodar a aplicação em um container)

## Como Usar Este Projeto

### 1. Clonar o Repositório

Para criar um novo projeto a partir deste modelo, clique em **Use this template** no GitHub e crie um novo repositório. Ou clone este repositório:

```bash
git clone <URL_DO_REPOSITORIO>
cd fastapi-boilerplate
```

### 2. Instalar Dependências

Caso queira rodar a aplicação localmente sem Docker, você pode instalar as dependências com:

```bash
pip install -r requirements.txt
```

### 3. Executar a Aplicação

Para rodar a aplicação localmente:

```bash
uvicorn main:app --reload
```

Acesse a aplicação em: [http://127.0.0.1:8000](http://127.0.0.1:8000)

### 4. Usar Docker para Executar a Aplicação

Para construir e rodar a aplicação em um container Docker:

1. **Build da imagem Docker**:

    ```bash
    docker build -t fastapi-boilerplate .
    ```

2. **Rodar o container**:

    ```bash
    docker run -d -p 8000:8000 fastapi-boilerplate
    ```

A aplicação estará disponível em [http://localhost:8000](http://localhost:8000).

### 5. Endpoints

- `GET /`: Retorna uma mensagem de exemplo:
    ```json
    {
      "message": "Olá!"
    }
    ```

### 6. Personalização

Para expandir a API, você pode adicionar novas rotas e funcionalidades no arquivo `app/main.py`.

## Contribuindo

Sinta-se à vontade para abrir issues ou fazer pull requests para melhorias neste boilerplate.

## Licença

Este projeto é distribuído sob a licença MIT. Consulte o arquivo `LICENSE` para mais detalhes.
