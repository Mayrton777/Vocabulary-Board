# 📌 Vocabulary Board

Um sistema web interativo no estilo "mural de post-its" focado em acelerar o aprendizado de vocabulário em inglês. Ao inserir uma palavra, o sistema gera dinamicamente sua tradução, uma explicação contextualizada do dia a dia e um exemplo de uso em uma frase, organizando tudo em blocos coloridos.

## 🚀 Tecnologias Utilizadas

Este projeto foi construído utilizando as seguintes tecnologias:

**Front-end:**
* React + TypeScript
* Vite (Build tool)
* CSS (Grid Layout para o mural)

**Back-end:**
* ASP.NET Core 9 (Web API)
* C#
* Entity Framework Core
* Arquitetura: Clean Architecture & CQRS (Command Query Responsibility Segregation)

**Infraestrutura & Banco de Dados:**
* PostgreSQL
* Docker & Docker Compose

## 🏗️ Arquitetura do Projeto

O repositório segue a estrutura de **Monorepo**, dividindo claramente o Front-end e o Back-end, sendo o Back-end estruturado em camadas (Clean Architecture) para garantir escalabilidade e baixo acoplamento:

* **API:** Controladores RESTful e injeção de dependência.
* **Application:** Casos de uso e regras de negócio.
* **Domain:** Entidades puras do sistema (ex: `PostIt`).
* **Infrastructure:** Comunicação com o banco de dados e integrações externas.

## ⚙️ Como executar localmente

Pré-requisitos: Você precisa ter o [Docker Desktop](https://www.docker.com/products/docker-desktop/) instalado na sua máquina.

1. Clone o repositório:
```bash
git clone [https://github.com/Mayrton777/vocabulary-board.git](https://github.com/Mayrton777/vocabulary-board.git)
```

2. Acesse a pasta do projeto:
```bash
cd vocabulary-board
```

3. Suba a infraestrutura completa (Banco, API e Front-end) com o Docker Compose:
```bash
docker compose up -d --build
```

4. Acesse a aplicação no seu navegador:

* Front-end:```http://localhost:3000```
* Back-end:```http://localhost:8080/weatherforecast```

## 👨‍💻 Autor

Desenvolvido por **Mayrton Eduardo**

* GitHub: [Mayrton777](https://github.com/Mayrton777)
* LinkedIn: [Mayrton Eduardo](https://www.linkedin.com/in/mayrton-eduardo-silva-rocha/)