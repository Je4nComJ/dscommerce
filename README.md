# DSCommerce - Backend

Este é o backend de uma aplicação de e-commerce desenvolvida com **Spring Boot**, que oferece uma API RESTful completa para gerenciamento de produtos, categorias, usuários e pedidos. O projeto serve como base para um sistema de vendas online e pode ser facilmente integrado a um frontend (web ou mobile).

---

## 🔧 Tecnologias utilizadas

- Java 17
- Spring Boot
- Spring Data JPA
- Spring Security
- Spring Web
- Bean Validation
- JWT (JSON Web Token)
- PostgreSQL ou H2
- Maven

---

## 🗂️ Estrutura do Projeto

```
dscommerce/
└── src/
    ├── main/
    │   ├── java/com/devsuperior/dscommerce/
    │   │   ├── controllers/
    │   │   ├── dtos/
    │   │   ├── entities/
    │   │   ├── repositories/
    │   │   ├── services/
    │   │   └── config/
    │   └── resources/
    │       ├── application.properties
    │       └── data.sql
```

---

## ⚙️ Configuração

### Banco de dados (PostgreSQL ou H2)

No arquivo `src/main/resources/application.properties`, configure sua conexão com o banco:

```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/dscommerce
spring.datasource.username=seu_usuario
spring.datasource.password=sua_senha
spring.jpa.hibernate.ddl-auto=update
```

Ou utilize o banco em memória H2 para testes:

```properties
spring.datasource.url=jdbc:h2:mem:dscommerce
spring.h2.console.enabled=true
```

---

## ▶️ Como executar

1. Clone o repositório:
```bash
git clone https://github.com/Je4nComJ/dscommerce.git
cd dscommerce
```

2. Compile e rode o projeto:
```bash
./mvnw spring-boot:run
```

3. Acesse:
- API: `http://localhost:8080`
- H2 Console (se habilitado): `http://localhost:8080/h2-console`

---

## 🧪 Endpoints principais (exemplos)

| Método | Endpoint | Descrição |
|--------|----------|------------|
| `GET`  | `/products` | Lista todos os produtos |
| `GET`  | `/products/{id}` | Retorna detalhes de um produto |
| `POST` | `/orders` | Cria um novo pedido |
| `GET`  | `/orders/{id}` | Consulta um pedido por ID |
| `POST` | `/auth/login` | Realiza login e retorna token JWT |

> ⚠️ Alguns endpoints exigem autenticação JWT.

---

## 🔐 Segurança

O projeto utiliza autenticação via **JWT** e autorização baseada em roles:

- Usuários com perfil `ROLE_CLIENT` podem consultar produtos e criar pedidos.
- Usuários com perfil `ROLE_ADMIN` podem cadastrar, editar e remover produtos.

---

## 📚 Aprendizados e objetivos

Este projeto foi criado com foco em:

- Construção de APIs REST com boas práticas.
- Validações com Bean Validation.
- Segurança com Spring Security + JWT.
- Acesso a dados com JPA/Hibernate.
- Estruturação profissional de um backend Java.

---

## 🤝 Contribuições

Contribuições são bem-vindas! Sinta-se à vontade para abrir issues ou pull requests.

---
