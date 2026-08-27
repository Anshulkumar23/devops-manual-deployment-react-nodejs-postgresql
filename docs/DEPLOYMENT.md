# Deployment Guide

## Overview

This application is deployed on Ubuntu using:

- React + Vite for the frontend
- Node.js + Express for the backend
- PostgreSQL as the database
- Prisma ORM
- PM2 for backend process management
- Nginx for serving the frontend

## Backend Deployment

```bash
cd server
npm install
npx prisma generate
npx prisma migrate deploy
pm2 start src/app.js --name devops-backend
```

The backend runs on:

```text
Port 8000
```

## Frontend Deployment

```bash
cd client
npm install
npm run build
```

The production build is generated in:

```text
client/dist/
```

## Nginx

Nginx serves the React production build on port 80.

```bash
nginx -t
systemctl reload nginx
```

## Application Flow

```text
Browser
   ↓
Nginx
   ↓
React Frontend
   ↓
Node.js Backend (PM2)
   ↓
Prisma
   ↓
PostgreSQL
```

## Verification

```bash
pm2 status
curl http://localhost:8000/users/all
curl -I http://localhost
```

## Security

Environment files containing credentials are not committed to GitHub.

```text
.env
server/.env
client/.env
```
