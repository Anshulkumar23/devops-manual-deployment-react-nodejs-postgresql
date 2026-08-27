# Project Architecture

## Overview

This project is a full-stack web application consisting of:

- React frontend built using Vite
- Node.js and Express backend
- PostgreSQL database
- Prisma ORM
- PM2 for backend process management
- Nginx for serving the frontend

## Architecture Flow
##========================
User Browser
     |
     v
Nginx
     |
     v
React Frontend
     |
     | API Request
     v
Node.js + Express Backend
     |
     | Managed by PM2
     v
Prisma ORM
     |
     v
PostgreSQL Database
#=======================
