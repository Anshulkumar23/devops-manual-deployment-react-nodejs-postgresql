# Troubleshooting

## Check Backend Status

```bash
pm2 status
pm2 logs devops-backend
```

## Check Backend Port

```bash
ss -lntp | grep :8000
```

## Check Backend API

```bash
curl http://localhost:8000/users/all
```

## Check Prisma Migration Status

```bash
cd server
npx prisma migrate status
```

## Check PostgreSQL

```bash
systemctl status postgresql
```

Connect to the database:

```bash
psql -h localhost -U devopsuser -d devopsdb
```

## Check Nginx

```bash
nginx -t
systemctl status nginx
```

Check Nginx logs:

```bash
tail -f /var/log/nginx/error.log
```

## Check Frontend

Rebuild the frontend after changes:

```bash
cd client
npm run build
systemctl reload nginx
```
