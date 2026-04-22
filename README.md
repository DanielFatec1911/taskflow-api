# TaskFlow API 🗂️

API REST para gerenciamento de tarefas desenvolvida com Django e Django REST Framework.
Inspirada no fluxo de trabalho do Jira — organize suas tarefas com status **To Do**, **In Progress** e **Done**.

---

## 🛠️ Tecnologias

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Django](https://img.shields.io/badge/Django-092E20?style=for-the-badge&logo=django&logoColor=white)
![DRF](https://img.shields.io/badge/Django_REST_Framework-ff1709?style=for-the-badge&logo=django&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=for-the-badge&logo=sqlite&logoColor=white)

---

## 🚀 Funcionalidades

- ✅ Criar tarefas com título, descrição e status
- 📋 Listar todas as tarefas
- 🔍 Filtrar tarefas por status
- ✏️ Atualizar tarefas existentes
- 🗑️ Deletar tarefas

---

## 📌 Endpoints

| Método | Endpoint | Descrição |
|--------|----------|-----------|
| `GET` | `/api/tasks/` | Lista todas as tarefas |
| `POST` | `/api/tasks/` | Cria uma nova tarefa |
| `GET` | `/api/tasks/{id}/` | Detalha uma tarefa |
| `PUT` | `/api/tasks/{id}/` | Atualiza uma tarefa |
| `PATCH` | `/api/tasks/{id}/` | Atualiza parcialmente |
| `DELETE` | `/api/tasks/{id}/` | Remove uma tarefa |

---

## 🔍 Filtro por status

```
GET /api/tasks/?status=todo
GET /api/tasks/?status=in_progress
GET /api/tasks/?status=done
```

---

## 📋 Exemplo de payload

```json
{
  "title": "Criar tela de login",
  "description": "Desenvolver o front-end da tela de autenticação",
  "status": "in_progress"
}
```

**Resposta:**

```json
{
  "id": 1,
  "title": "Criar tela de login",
  "description": "Desenvolver o front-end da tela de autenticação",
  "status": "in_progress",
  "created_at": "2026-04-22T19:58:52Z",
  "updated_at": "2026-04-22T19:58:52Z"
}
```

---

## ⚙️ Como rodar localmente

```bash
# Clone o repositório
git clone https://github.com/DanielFatec1911/taskflow-api.git
cd taskflow-api

# Crie e ative o ambiente virtual
python -m venv venv
venv\Scripts\activate  # Windows
source venv/bin/activate  # Linux/Mac

# Instale as dependências
pip install -r requirements.txt

# Rode as migrations
python manage.py migrate

# Suba o servidor
python manage.py runserver
```

Acesse: **http://localhost:8000/api/tasks/**

---

## 📁 Estrutura do projeto

```
taskflow-api/
├── core/
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
├── tasks/
│   ├── migrations/
│   ├── models.py
│   ├── serializers.py
│   ├── views.py
│   └── urls.py
├── manage.py
├── requirements.txt
└── .gitignore
```

---

## 👨‍💻 Autor

Desenvolvido por **Daniel Silva**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/daniel-silva-97a3202a9/)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/DanielFatec1911)
