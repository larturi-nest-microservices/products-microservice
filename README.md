# Product Microservice

## Dev

1. Clonar el repositorio
2. Instalar dependencias
3. Crear un archivo .env basado en el env.template
4. Ejecutar migración de la base de datos con Prisma

```bash
npx prisma migrate dev
```

Si eliminas la carpeta node modules, recordar correr `npx prisma generate`

5. Insertar Productos en la BD /prisma/products.sql
6. Levantar el servidor NATS

```bash
docker run -d --name nats-main -p 4222:4222 -p 6222:6222 -p 8222:8222 nats
```

7. Levantar el servidor

```bash
nvm use 20.12.2

npm install

npx prisma migrate dev

npm run start:dev
```

Si eliminas la carpeta node modules, recordar correr `npx prisma generate`
