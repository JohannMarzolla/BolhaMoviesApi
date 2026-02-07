# 🎬 BolhaMovies API

API desenvolvida com **Strapi** para fornecer dados de filmes ao projeto **BolhaMovies Front-end**. Esta API é responsável por gerenciar filmes, gêneros e seus relacionamentos, servindo os dados via **REST**.

> ⚠️ **Importante:** esta API **precisa estar rodando antes** de iniciar o projeto front-end, pois todos os dados exibidos na aplicação vêm dela.

---

## 🔗 Projeto relacionado

👉 Front-end que consome esta API:
[https://github.com/JohannMarzolla/BolhaMovies](https://github.com/JohannMarzolla/BolhaMovies)

---

## 🚀 Tecnologias utilizadas

* Strapi
* Node.js
* JavaScript / TypeScript
* SQLite (banco padrão do Strapi em ambiente de desenvolvimento)

---

## 📦 Instalação

Clone o repositório:

```bash
git clone https://github.com/JohannMarzolla/BolhaMoviesApi
cd BolhaMoviesApi
```

Instale as dependências:

```bash
npm install
```

---

## ▶️ Como rodar o projeto

### Modo desenvolvimento (recomendado)

Inicia a aplicação com **auto reload**, ideal para desenvolvimento local:

```bash
npm run develop
```

Após iniciar, a API estará disponível em:

```
http://localhost:1337
```

---

## 📡 Endpoints utilizados na aplicação

### Listar filmes com gêneros relacionados

Este é o **endpoint principal utilizado pelo front-end**.

**Método:** `GET`
**URL completa:**

```
http://localhost:1337/api/movies?populate=genres
```

**Descrição:**

Retorna a lista de filmes cadastrados na API, incluindo os gêneros associados a cada filme.
O parâmetro `populate=genres` garante que os dados relacionais sejam retornados em uma única requisição, evitando múltiplas chamadas no front-end.

**Exemplo de uso no front-end:**

```ts
fetch('http://localhost:1337/api/movies?populate=genres')
```

### Observação

Os endpoints REST desta API são **gerados automaticamente pelo Strapi** a partir dos *Content Types*.
Este README documenta apenas os endpoints **efetivamente consumidos pela aplicação front-end**.

---

## ⚙️ Estrutura básica do projeto (Strapi)

O projeto segue a estrutura padrão do Strapi:

```txt
src/
├── api/           # Content Types (movies, genres, etc)
├── components/    # Componentes reutilizáveis
├── extensions/    # Extensões do Strapi
├── config/        # Configurações do projeto
└── admin/         # Painel administrativo
```

---

## 👨‍💻 Autor

**Johann Marzolla**

GitHub: [https://github.com/JohannMarzolla](https://github.com/JohannMarzolla)

