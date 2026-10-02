# DevOps Todo App

A compact Todo lab used to practice static frontend delivery, a minimal Node.js backend, Docker packaging, and GitHub Actions deployment workflow basics.

This is a supporting lab project. It is useful for demonstrating delivery fundamentals, while larger portfolio projects show deeper DevOps and operations work.

## What is included

```text
app/                    Static frontend
backend/                Express backend with /health endpoint
Dockerfile              NGINX container for the static frontend
.github/workflows/      GitHub Actions deployment workflow
.gitignore              Local dependency hygiene
```

## DevOps evidence

- GitHub Actions deployment workflow using SSH secrets
- Static frontend containerization with NGINX
- Backend health endpoint for basic service verification
- Reproducible Node.js dependency lock file
- Runnable backend scripts: `npm start` and `npm test`

## Local backend run

```bash
cd backend
npm install
npm test
npm start
```

Health check:

```bash
curl http://localhost:3000/health
```

## Static frontend run

Open `app/index.html` directly in a browser, or build the static container:

```bash
docker build -t devops-todo-static .
docker run --rm -p 8080:80 devops-todo-static
```

Then open `http://localhost:8080`.

## Portfolio role

Use this repo as a small DevOps practice example. For resume-facing projects, lead with:

- [employee-portal](https://github.com/Chandrumgchandu/employee-portal)
- [ebook-store](https://github.com/Chandrumgchandu/ebook-store)
- [todo_app_jenkins](https://github.com/Chandrumgchandu/todo_app_jenkins)
- [Milk Ledger demo](https://milk-ledger-pink.vercel.app)

## Improvement backlog

- Add real API routes for Todo CRUD operations.
- Add automated HTTP tests for `/` and `/health`.
- Add Docker Compose if a database or additional service is introduced.
- Add environment-variable based configuration before using it for any real deployment.
