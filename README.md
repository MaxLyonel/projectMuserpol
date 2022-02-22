# PLATAFORMA VIRTUAL DE TRÁMITES

## Requerimientos

- Docker version 20.10.12
- PostgreSQL 12
- PHP version 8.1
- composer

## Configuración e instalación

- Clonar el proyecto _PVT-BACKEND_

```bash
git clone https://github.com/MUTUAL-DE-SERVICIOS-AL-POLICIA/PVT-BACKEND
cd PVT-BACKEND
```

- Configurar el archivo **_docker-compose.yml_**. Especificamente las siguientes lineas:

```docker
-   context:./vendor/laravel/sail/runtimes/8.0
+   context:./vendor/laravel/sail/runtimes/8.1

-   image: sail-8.0/app
+   image: sail-8.1/app
```

- Instalar dependencias del proyecto con _Composer_
  Instalando dependencias del proyecto, navegando al directorio de la aplicación y ejecutando el siguiente comando. Dicho comando usa un pequeño contenedor Docker que contiene PHP y Composer para instalar las dependencias necesarias de la aplicación.
