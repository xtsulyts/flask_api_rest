# API REST para Productos y Carrito de Compras

## Descripción
Esta API REST permite gestionar productos, consultar su información, crear, editar y eliminar registros. Además, ofrece funcionalidades para administrar un carrito de compras, permitiendo a los usuarios agregar, actualizar y eliminar productos del mismo.

## Tecnologías Utilizadas
- **Backend:** Python con Flask
- **Frontend:** TypeScript y Next.js
- **Base de datos:** MySQL server
- **Autenticación:** JWT (JSON Web Tokens)
- **Entorno de desarrollo:** Docker (opcional)

---

## Características
- **Productos:**
  - Consultar lista de productos
  - Consultar un producto por ID
  - Crear un nuevo producto
  - Editar un producto existente
  - Eliminar un producto

- **Carrito de Compras:**
  - Agregar productos al carrito
  - Consultar contenido del carrito
  - Actualizar cantidades de productos en el carrito
  - Eliminar productos del carrito

---

## Instalación

### Requisitos previos
- Python (v3.8 o superior)
- Node.js (v14 o superior)
- MySQL server





### Backend (Flask)
# Crear un entorno virtual

```bash
python3 -m venv venv
source venv/bin/activate
```

# Instalar dependencias
pip install -r requirements.txt

# Configurar variables de entorno

```bash
export FLASK_APP=app.py
export FLASK_ENV=development
```

# Iniciar el servidor

```bash
flask run
```


### Frontend (Next.js)
cd frontend

```bash
npm install
npm run dev
```

### Configuración
1. Crear un archivo `.env` en la raíz del proyecto con las siguientes variables:
   
   ```env
   PORT=3000
   DB_TYPE=MySQL
   DB_HOST=localhost
   DB_PORT=3036 # cambiar a 27017 para MongoDB
   DB_NAME=nombre_base_datos
   ```

---

## Endpoints

### Productos
- **GET** `/api/productos` - Obtener todos los productos
- **GET** `/api/productos/:id` - Obtener un producto por ID
- **POST** `/api/productos` - Crear un nuevo producto
- **PUT** `/api/productos/:id` - Actualizar un producto
- **DELETE** `/api/productos/:id` - Eliminar un producto

### Carrito de Compras
- **POST** `/api/carrito` - Crear un nuevo carrito
- **POST** `/api/carrito/:id/productos` - Agregar un producto al carrito
- **GET** `/api/carrito/:id` - Consultar el contenido del carrito
- **PUT** `/api/carrito/:id/productos/:productoId` - Actualizar la cantidad de un producto
- **DELETE** `/api/carrito/:id/productos/:productoId` - Eliminar un producto del carrito


---


## Contribución
1. Hacer un fork del repositorio
2. Crear una rama con la nueva funcionalidad: `git checkout -b feature/nueva-funcionalidad`
3. Hacer commit de los cambios: `git commit -m 'Agregar nueva funcionalidad'`
4. Hacer push a la rama: `git push origin feature/nueva-funcionalidad`
5. Abrir un Pull Request

---

