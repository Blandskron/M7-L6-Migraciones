# **Django Migrations Project**

### **Descripción del Proyecto**
Este proyecto está diseñado para enseñar el uso de migraciones en Django, una funcionalidad esencial para manejar el esquema de bases de datos en proyectos web. Aprenderás cómo:
- Crear y aplicar migraciones para reflejar cambios en los modelos.
- Inspeccionar las migraciones y el SQL generado antes de aplicarlas.
- Resolver conflictos entre migraciones y manejar dependencias.

El proyecto incluye un ejemplo práctico de dos modelos relacionados (Autores y Libros), así como un script para poblar la base de datos con datos iniciales.

---

### **Características**
- **Gestión de Migraciones**: Uso de comandos como `makemigrations`, `migrate`, `sqlmigrate`, y `showmigrations`.
- **Relaciones Entre Modelos**: Demostración de relaciones `ForeignKey` entre autores y libros.
- **Población de Datos Automatizada**: Incluye un script (`dataShell.py`) para poblar la base de datos.
- **Estructura Sencilla y Escalable**: Fácil de entender y ampliar según las necesidades del desarrollador.

---

### **Requisitos Previos**
- Python 3.8 o superior.
- Django 4.2 o superior.
- Base de datos SQLite (por defecto en Django).

---

### **Instalación**
1. Clona este repositorio en tu máquina local:
   ```bash
   git clone https://github.com/tuusuario/django-migrations.git
   cd django-migrations
   ```

2. Instala las dependencias necesarias:
   ```bash
   pip install -r requirements.txt
   ```

3. Realiza las migraciones iniciales:
   ```bash
   python manage.py makemigrations
   python manage.py migrate
   ```

4. Pobla la base de datos con datos iniciales ejecutando el script:
   ```bash
   python dataShell.py
   ```

5. Inicia el servidor de desarrollo:
   ```bash
   python manage.py runserver
   ```

---

### **Estructura del Proyecto**
```plaintext
django-migrations/
├── app/
│   ├── migrations/
│   │   ├── 0001_initial.py
│   │   └── __init__.py
│   ├── models.py
│   ├── views.py
│   ├── urls.py
│   ├── templates/
│       └── index.html
├── dataShell.py
├── manage.py
├── db.sqlite3
├── requirements.txt
├── README.md
```

---

### **Uso del Proyecto**
#### **1. Crear Migraciones**
- Modifica los modelos en `models.py` según tus necesidades.
- Ejecuta el comando:
  ```bash
  python manage.py makemigrations
  ```

#### **2. Aplicar Migraciones**
- Aplica las migraciones a la base de datos con:
  ```bash
  python manage.py migrate
  ```

#### **3. Inspeccionar Migraciones**
- Ver todas las migraciones:
  ```bash
  python manage.py showmigrations
  ```
- Ver el SQL generado para una migración específica:
  ```bash
  python manage.py sqlmigrate app 0001
  ```

---

### **Comandos Esenciales**
- Crear migraciones:
  ```bash
  python manage.py makemigrations
  ```
- Aplicar migraciones:
  ```bash
  python manage.py migrate
  ```
- Ver el estado de las migraciones:
  ```bash
  python manage.py showmigrations
  ```
- Generar SQL para inspección previa:
  ```bash
  python manage.py sqlmigrate <app_name> <migration_name>
  ```

---

### **Población de Datos**
Para poblar la base de datos con datos iniciales, ejecuta el script `dataShell.py`:
```bash
python dataShell.py
```
Este script creará ejemplos de autores y libros que pueden ser visualizados en la página principal del proyecto.

---

### **Visualización**
Accede al proyecto en tu navegador en [http://localhost:8000/](http://localhost:8000/) para ver:
- Autores y sus correos electrónicos.
- Libros y los autores correspondientes.

---

### **Contribuciones**
¡Las contribuciones son bienvenidas! Si tienes sugerencias, abre un *issue* o envía un *pull request*.

---

### **Licencia**
Este proyecto está bajo la Licencia MIT. Consulta el archivo `LICENSE` para más detalles.

---
