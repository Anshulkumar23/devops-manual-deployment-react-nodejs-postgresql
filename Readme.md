# DevOps React Node.js PostgreSQL Project

This project is a full-stack web application deployed on an Ubuntu server.

The application consists of a React frontend, Node.js/Express backend, PostgreSQL database, and Prisma ORM.

## Technology Stack

- Ubuntu 24.04
- Node.js v22
- React
- Vite
- Node.js
- Express.js
- PostgreSQL
- Prisma ORM
- PM2
- Nginx
- Git and GitHub

## Project Architecture

```text
User Browser
     |
     v
Nginx
     |
     v
React Frontend
     |
     | API Requests
     v
Node.js + Express Backend
     |
     | Managed by PM2
     v
Prisma ORM
     |
     v
PostgreSQL Database
