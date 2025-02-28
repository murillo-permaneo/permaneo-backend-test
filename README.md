# Grupo Permaneo

## Teste técnico para posições de Back-end

## Visão Geral

Você irá construir uma API RESTful usando algum framework Node.js, preferencialmente NestJS, com foco em estrutura de dados, integração de testes automatizados e uso de Docker como ambiente de desenvolvimento.

## Requisitos

1. **Desenvolvimento de uma API RESTful**:
    
    - Utilize NestJS para criar uma API RESTful que gerencie cursos em uma plataforma de ensino. A estrutura do banco de dados pode seguir o modelo JSON abaixo como referência:
    
    ```json
    {
      "courses": [
        {
          "id": 1,
          "name": "Learning JavaScript",
          "category": "Programming",
          "lessons": [
            {
              "id": 1,
              "title": "Introduction to JavaScript",
              "description": "An overview of JavaScript",
              "comments": [
                {
                  "user": "Pedro",
                  "text": "Great lesson, very clear!",
                  "date": "2023-10-01"
                }
              ]
            },
            {
              "id": 2,
              "title": "Data Structures",
              "description": "Learning arrays, objects, and functions",
              "comments": []
            }
          ]
        }
      ]
    }
    ```

2. **Endpoints requeridos**:

   **Courses**
   - GET /courses: Return all courses.

   - POST /courses: Create a new course (fields: name, category).

   - GET /courses/{id}: Return details of a specific course (using the JSON structure mentioned above).

   - PUT /courses/{id}: Update a specific course.

   - DELETE /courses/{id}: Remove a specific course.

   **Lessons:**

   - GET /courses/{id}/lessons: List lessons of a course.

   - POST /courses/{id}/lessons: Create a new lesson for a course (fields: title, description).

   - GET /courses/{id}/lessons/{lesson_id}: Details of a specific lesson.

   - PUT /courses/{id}/lessons/{lesson_id}: Update a lesson.

   - DELETE /courses/{id}/lessons/{lesson_id}: Remove a lesson.

   **Comments:**

   - POST /courses/{id}/lessons/{lesson_id}/comments: Add a comment to a lesson (fields: user, text, date).

### Considerações Técnicas Adicionais

- Use o **TypeORM** (ou outra ORM) para gerenciar o banco de dados.
- **MySQL** ou **PostgreSQL** são recomendados para o ambiente de produção, mas pode-se usar **SQLite** para simplificar a avaliação inicial.
- **Jest** para integração de testes unitários das funcionalidades.
- Utilize o **Swagger** para gerar automaticamente a documentação da API.
  
### Estrutura de Diretórios Sugerida

- `src/`
  - `courses/`
  - `modules/`
  - `lessons/`
  - `comments/`
  - `common/` (para decorators, pipes, guards, etc.)
  - `app.module.ts`
  - `main.ts`

## Entrega do teste

- Submeta o código-fonte, incluindo os testes, em um repositório Git (ex.: GitHub ou GitLab).
- Inclua uma estrutura dockerizada e um README.md no repositório, com a documentação de como utilizar as rotas e como executar o projeto.
- Passe o link do repositório para o recrutador que está em contato.

## Melhorias Opcionais

- Adicione testes automatizados para as rotas.
- Utilize o Postgres como banco de dados dentro do ambiente Docker em um container apartado.

Boa sorte e bom código!
