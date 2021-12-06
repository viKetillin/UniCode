---
sidebar_position: 2
---

# Backend com JSON Server
*	Criar uma pasta chamada “CRUD” para armazenar tanto a aplicação frontend, quanto a aplicação backend. O foco não será backend, por isso será feito uma API bem simples.
*	Abrir o VS code.
*	Criar uma pasta chamada “backend” dentro da pasta “CRUD”.
*	Digitar no terminal cd CRUD -> backend -> npm init -y. Ele irá criar um arquivo chamado package.json, e nesse arquivo poderemos colocar as dependências, mas não vamos colocar diretamente.
*	Digitar no terminal npm i json-server para que seja instalado essa dependência que será utilizada para construirmos a API. Ela será colocada automaticamente dentro do arquivo package,json.
*	O JSON server lê um arquivo que contém JSON e cria uma API baseada nesse arquivo JSON.
*	Dentro da pasta “backend” criar um arquivo chamado “db.json”.

- Criar esse array de objetos dentro do arquivo `db.json`:

```md title="db.json"
{
    "products": [
        {
            "id": 1,
            "name": "Caneta BIC Preta",
            "price": 5.89
        },
        {
            "id": 2,
            "name": "Notebook MAC Pro",
            "price": 12000.89
        },
        {
            "id": 3,
            "name": "Samsung S20+",
            "price": 5000.89
        }
    ]
}
```

-	Dentro do arquivo `package.json`, remover o script de teste e criar um script chamado start e definir o comando que usado para iniciar o `db.json`. Nesse caso chamaremos de `json-server` e vamos colocar para ele fazer um watch em cima do `db.json`. Podemos definir a porta que será usada, por exemplo `3001`.

```md title="package.json"
{
    "name": "backend",
    "version": "1.0.0",
    "description": "",
    "main": "index.js",
    "scripts": {
        "start": "json-server --watch db.json –port 3001"
    },
    "keywords": [],
    "author": "",
    "license": "ISC",
    "dependencies": {
        "json-server": "^0.16.3"
    }
}
```

**O que foi feito:** Dentro dos scripts chamamos o json-server que foi instalado anteriormente, o - -watch serve para ficar monitorando o arquivo na porta 3001. Após fazer isso, já temos a nossa API funcionando e para iniciar basta digitar no terminal `npm start` dentro da pasta backend.
