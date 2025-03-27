# Guía de Instalación - Proyecto Laravel con Docker
## 1️⃣ Clonar el repositorio
Primero, clona el repositorio en tu máquina local:

```bash
git clone https://github.com/tu-usuario/tu-repositorio.git
```
Una vez clonado el repositorio difijete a al proyecto
```bash
cd tu_repositorio
```
## 2️⃣  Construir y levantar los contenedores de Docker

```bash
./vendor/bin/sail up -d
```
## 3️⃣ Verificar los contenedores activos
```bash
docker ps
```

## 4️⃣ Instalar las dependencias de PHP con Composer
  Entra a la siguiente ruta y verifica si Composer está instalado:
  ```bash
  ./vendor/bin/sail shell
  composer --version
  ```
  instalar las depencias las depencais de lavarel
  ```bash
  composer install
  ```

  desde esa ruta verifica si npm está instalado
  ```bash
  npm --v 
  npm install && npm run dev
  ```


### Cada integrante debe crear su archivo .env basado en el ejemplo .env.example:





## 6️⃣ Migrar la base de datos
  ```bash
./vendor/bin/sail artisan migrate
```
## 7️⃣ Acceder a la base de datos
Si necesitas acceder a la base de datos en el contenedor MySQL, utiliza el siguiente comando:
  ```bash
docker exec -it equipo4_toturias-mysql-1 mysql -u root -p
```

Si no sabes la contraseña de MySQL, puedes obtenerla ejecutando:
  ```bash
docker inspect [Contenedor]-mysql-1 | grep MYSQL_ROOT_PASSWORD
```
Por ejemplo, puede salir algo como esto:
  ```bash
"MYSQL_ROOT_PASSWORD=password123"
```
## 8️⃣ Abrir el proyecto en Visual Studio Code
  ```bash
code . -r
```




pasos para instalar paquetes 
  ```bash
composer show laravel/sail

composer install

composer require laravel/sail --dev

php artisan sail:install

sudo apt install php-xml php-dom

php artisan sail:install


```