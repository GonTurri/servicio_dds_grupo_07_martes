# Descripción del servicio

### Servicio 1: Recomendación de Donación
Este servicio permite a la ONG a cargo del sistema extender la posibilidad de donaciones a otras comunidades. A partir de una ubicación geográfica, el sistema recomienda los lugares donde puedes acercar tus donaciones.

## Guía completa y detallada de uso

- ### Paso 1: Instalar Node.js
Asegurate de tener [Node.js instalado](https://nodejs.org/en/download/prebuilt-installer).

- ### Paso 2: Instalar MySQL Server
Debes tener MySQL Server instalado y configurado en tu sistema.

- ### Paso 3: Clonar el repositorio
Clona este repositorio en tu computadora con el siguiente comando:

```bash
git clone https://github.com/GonTurri/servicio_dds_grupo_07_martes.git
```

- ### Paso 4: Instalar dependencias
Abri una consola en la carpeta del proyecto y ejecuta el siguiente comando para instalar las dependencias:
```bash
npm i
```
Luego de este paso deberías tener una carpeta llamda `node_modules` en el proyecto

- ### Paso 5: Configurar las variables de entorno
Crea un archivo .env en la raíz del proyecto y configura las credenciales de la base de datos. Aca tienes un ejemplo de cómo debería quedar:
``` env
DB_COMUNIDADES_USER=root
DB_COMUNIDADES_PORT=3306
DB_COMUNIDADES_PSWD=mysql
DB_COMUNIDADES_DBNAME=tp_dds_comunidades
DB_COMUNIDADES_HOST=localhost
```

Asegurate de tener creada una base de datos vacía con el mismo nombre que está en DB_COMUNIDADES_DBNAME para que se genere el esquema correctamente.

- ### Paso 6: Insertar datos de prueba
Inserta algunos datos de prueba en la base de datos. Puedes usar el siguiente SQL como ejemplo:
 ``` sql
 INSERT INTO comunidad (id, nombre, lat, lon) VALUES
(1, 'Comunidad A', -34.61178, -58.417308),
(2, 'Comunidad B', -34.613466, -58.419659),
(3, 'Comunidad C', -34.582345, -58.43329),
(4, 'Comunidad D', -34.609897, -58.386682),
(5, 'Comunidad E', -34.630202, -58.471633),
(6, 'Comunidad F', -34.59868, -58.373928),
(7, 'Comunidad G', -34.617104, -58.362669),
(8, 'Comunidad H', -34.634981, -58.41324),
(9, 'Comunidad I', -34.609234, -58.445187),
(10, 'Comunidad J', -34.583449, -58.418373);
```
- ### Paso 7: una vez todo configurado ya podemos levantar el server ejecutando el siguiente comando en la terminal
```bash 
npm run start
```

- ### Si salió todo bien,  ya podes empezar a usar el servicio. Para acceder a la documentación en local, visita:
```url
http://localhost:3000/docs/
```

**Nota:** Para poder solicitar comunidades, primero debes generar una API Key y añadirla en los Headers como `Authorization`. Si estás hace mas de 5 minutos y no te funciona, nos podes contactar! Abz.



