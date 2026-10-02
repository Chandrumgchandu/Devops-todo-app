# DevOps Todo App

A compact Todo application used to practice frontend/backend separation, Docker packaging, and GitHub Actions deployment workflow basics.

This is a supporting lab project. It is useful for demonstrating delivery fundamentals, while larger portfolio projects show deeper DevOps and operations work.

## What is included

```text
app/                    Static frontend
backend/                Node.js backend service
Dockerfile              Container packaging example
.github/workflows/      GitHub Actions deployment workflow
.gitignore              Local dependency hygiene
```

## DevOps evidence

- Containerization with a root `Dockerfile`
- GitHub Actions workflow in `.github/workflows/deploy.yml`
- Backend dependency lock file for reproducible installs
- Clear separation between static frontend and API service

## Local run

Install backend dependencies:

```bash
cd backend
npm install
```

Start the backend if the package scripts support it:

```bash
npm start
```

Open the static frontend from `app/index.html` or serve it with a simple local static server.

## Portfolio role

Use this repo as a small DevOps practice example. For resume-facing projects, lead with:

- [employee-portal](https://github.com/Chandrumgchandu/employee-portal)
- [ebook-store](https://github.com/Chandrumgchandu/ebook-store)
- [todo_app_jenkins](https://github.com/Chandrumgchandu/todo_app_jenkins)
- [Milk Ledger demo](https://milk-ledger-pink.vercel.app)

## Improvement backlog

- Add a health endpoint to the backend.
- Add automated backend tests.
- Add Docker Compose if a database or additional service is introduced.
- Add environment-variable based configuration before using it for any real deployment.
