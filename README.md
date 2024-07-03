<h1 align="center">
    <img src=".github/logo-rocketnotes.svg" title="RocketNotes" alt="" width="30px" />
    RocketNotes API
</h1>


## 💻 About

Este repositório se trata do back-end da aplicação RocketNotes ([link do front-end](https://github.com/B3RG5TRON/Explorer_Stage_09_ReactJS_RocketNotes)). Na qual está é uma aplicação web onde os usuários podem realizar um cadastrar e gerar anotações sobre assuntos que desejar.

Vale ressaltar que este projeto faz parte da trilha/curso **Explorer** oferecida pela [Rocketseat](https://www.rocketseat.com.br/).

---

## 🔗 Deploy

O acesso ao deploy da API fica disponível através da seguinte URL base: (disponível em breve)

> Obs: a aplicação pode demorar um pouco para entrar na primeira execução depois de um tempo, devido ao back-end estar rodando através do plano gratuito na plataforma de hospedagem.

---

## 🚀 How it works

### Pré-requisitos

Antes de baixar o projeto você vai precisar ter instalado na sua máquina as seguintes ferramentas:

* [Git](https://git-scm.com)
* [NodeJS](https://nodejs.org/en/)
* [Yarn](https://yarnpkg.com/) ou [NPM](https://www.npmjs.com/)

Além disto é bom ter um editor para trabalhar com o código, como: [VSCode](https://code.visualstudio.com/)

### 🎲 Rodando o Backend (servidor)

```bash
# Clone este repositório
$ gh repo clone B3RG5TRON/Explorer_Stage_08_NodeJS_RocketNotes_API

# Acesse a pasta do projeto no terminal/cmd
$ cd Explorer_Stage_08_NodeJS_RocketNotes_API

# Configure as variáveis de ambiente em um arquivo .env na raiz do projeto (use o arquivo .env.example como base)

# Instale as dependências
$ npm install

# Execute as migrations
$ npm run migrate:dev

# Execute a aplicação em modo de desenvolvimento
$ npm run dev

# O servidor inciará na porta:3333 - acesse http://localhost:3333

# Executar testes (caso queira)
$ npm test
```

### Rotas

| Método | Rota	| Descrição	| Parâmetros | Observação |
| --- | --- | --- | --- | --- |
| POST | /sessions | Retorna os dados de autenticação de um usuário existente | `email`, `password` | enviar parâmetros no `body` | 
| GET	| /users	| Retorna um usuário específico	| `token` |	enviar `token` de autenticação no `header` |
| POST | /users | Cria um novo usuário | `name`, `email`, `password` | enviar parâmetros no `body` da requisição |
| PUT | /users | Atualiza um usuário específico | `token`, `name`, `email`, `password`, `newPassword`(opcional) | enviar `token` pelo `header` e o restante no `body` |
| PATCH | /users/avatar | Atualiza o avatar de um usuário específico | `token`, `avatar` | enviar `token` pelo `header` e o `avatar` no formato `multipart` |
| GET | /notes | Retorna todas as notas de um usuário | `token` | enviar `token` de autenticação no `header` |
| GET | /notes:id | Retorna uma nota específica | `id`, `token` |  enviar `token` pelo `header` e `id` pela rota |
| POST | /notes | Cria uma nota | `title`, `description`, `tags`(array, optional), `links`(array, optional) | enviar `token` pelo `header` e o restante no `body` |
| DELETE | /notes/:id | Deleta uma nota específica | `id`, `token` | enviar `token` pelo `header` e `id` pela rota |
| GET | /tags | Retornas as tags criadas por um usuário | `token` | enviar `token` de autenticação no `header` |
| GET | /files/:filename | Retorna arquivos de avatar | `filename` | enviar `filename` pela rota |

> Obs: todos os parâmetros enviados e respondidos no corpo da requisição e resposta estão no formato `JSON`.

---

## 🛠 Technologies

As seguintes ferramentas foram usadas na construção do projeto:

#### **Server**  ([NodeJS](https://nodejs.org/en/))

-   **[Express](https://expressjs.com/pt-br/)**
-   **[Nodemon](https://www.npmjs.com/package/nodemon)**
-   **[Express-Async-Errors](https://www.npmjs.com/package/express-async-errors)**
-   **[Knex](https://knexjs.org/)**
-   **[PostgreSQL](https://node-postgres.com/)**
-   **[SQLite](https://github.com/mapbox/node-sqlite3)**
-   **[CORS](https://www.npmjs.com/package/cors)**
-   **[Dotenv](https://www.npmjs.com/package/dotenv)**
-   **[bcryptjs](https://www.npmjs.com/package/bcryptjs)**
-   **[jsonwebtoken](https://www.npmjs.com/package/jsonwebtoken)**
-   **[Multer](https://www.npmjs.com/package/multer)**
-   **[PM2](https://pm2.keymetrics.io/)**
-   **[Jest](https://jestjs.io/pt-BR/)**

> Para mais detalhes das dependências gerais da aplicação veja o arquivo: [package.json](https://github.com/B3RG5TRON/Explorer_Stage_08_NodeJS_RocketNotes_API/blob/main/package.json)

---

## ✍ Author

<div align="center">

  <img alt="Perfil Github" title="Perfil Github" src="https://github.com/B3RG5TRON.png" width="100px" />

  <p>Created by Eduardo Bergstron 👋🏽</p>
  
  [Linkedin](https://www.linkedin.com/in/eduardo-bergstron-986108143/) | [Email](mailto:eduardo.goudinho@gmail.com)

</div>

---

## 📝 License

Este projeto está sob a licença MIT. Consulte o arquivo [LICENSE](./LICENSE) para mais informações