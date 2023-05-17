# Configuración de MSSQL en Docker

    modifica el archivo setup.sql para crear la base de datos y las tablas necesarias para el proyecto.

## Ejecución con docker

-   Para crear la imágen Docker se debe ejecutar el siguiente comando:

```bash
    docker build -t mssql .
```

-   Para ejecutar el contenedor se debe ejecutar el siguiente comando:

```bash
    docker run -d -p 1433:1433 -p:1434:1434 -e 'ACCEPT_EULA=1' -e 'SA_PASSWORD=StrongPassw0rd' -e 'MSSQL_PID=Developer' --name sql mssql
```

NOTA: las contraseñas de MASSQL deben tener al menos 8 caracteres, una letra mayúscula, una letra minúscula y un número

-   El contenedor se ejecuta en segundo plano, para ver los logs se debe ejecutar el siguiente comando:

```bash
    docker logs mssql
```

-   Para detener el contenedor se debe ejecutar el siguiente comando:

```bash
    docker stop mssql
```

-   Para eliminar el contenedor se debe ejecutar el siguiente comando:

```bash
    docker rm mssql
```
