# Grupo Permaneo
## Teste técnico para posições de Back-end

## Visão Geral

Você irá construir uma APIs RESTful usando Python, com foco em estrutura de dados complexa, integração de testes automatizados e uso de Docker como ambiente de desenvolvimento.

## Requisitos

1. **Desenvolvimento de uma API RESTful**:
    
    - Utilize Flask ou Django REST Framework para criar uma API RESTful que gerencie cursos em uma plataforma de ensino, usando SQLite como banco de dados e a estrutura json abaixo como referencia:
```javascript
{
  "cursos": [
    {
      "id": 1,
      "nome": "Aprendendo Python",
      "categoria": "Programação",
      "aulas": [
        {
          "id": 1,
          "titulo": "Introdução ao Python",
          "descricao": "Uma visão geral do Python",
          "comentarios": [
            {
              "usuario": "Pedro",
              "texto": "Ótima aula, muito clara!",
              "data": "2023-10-01"
            }
          ]
        },
        {
          "id": 2,
          "titulo": "Estruturas de Dados",
          "descricao": "Aprendendo listas, tuples e dicionários",
          "comentarios": []
        }
      ]
    }
  ]
}
```

2. **Endpoints requeridos**:

**Cursos**
- GET /cursos: Retornar todos os cursos.

- POST /cursos: Criar um novo curso (campos: nome, categoria).

- GET /cursos/{id}: Retornar detalhes de um curso específico (utilizando a estrutura json citada acima)

- PUT /cursos/{id}: Atualizar um curso específico.

- DELETE /cursos/{id}: Remover um curso específico.

**Aulas:**

- GET /cursos/{id}/aulas: Listar aulas de um curso.

- POST /cursos/{id}/aulas: Criar uma nova aula para um curso (campos: título, descrição).

- GET /cursos/{id}/aulas/{aula_id}: Detalhes de uma aula específica.

- PUT /cursos/{id}/aulas/{aula_id}: Atualizar uma aula.

- DELETE /cursos/{id}/aulas/{aula_id}: Remover uma aula.

**Comentários:**

- POST /cursos/{id}/aulas/{aula_id}/comentarios: Adicionar um comentário a uma aula (campos: usuário, texto, data).

## Entrega do teste

- Submeta o código-fonte, incluindo os testes, em um repositório Git (ex.: GitHub ou GitLab).
- No repositório inclua o Dockerfile e docker-compose.yml e README.md com a documentação de como utilizar as rotas e como executar o projeto.
- Passe o link do repositório para o recrutador que está em contato

## Melhorias Opcionais

- Adicione testes automatizados para as rotas.
- Utilize o Postgres como DB dentro do ambiente docker em um container apartado.

Boa sorte e bom código!
