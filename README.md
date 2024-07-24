# 📋 SistemaEstudiantesMySQL

## 📖 Descripción
SistemaEstudiantesMySQL es una aplicación de consola para gestionar un catálogo de estudiantes. Permite agregar, listar, buscar, modificar y eliminar estudiantes, almacenando la información en una base de datos MySQL.

## 🌟 Características
- 📥 **Agregar Estudiante**: Añade un nuevo estudiante al sistema proporcionando su nombre, apellido, teléfono y email.
- 📜 **Listar Estudiantes**: Muestra todos los estudiantes en el sistema.
- 🔍 **Buscar Estudiante**: Busca un estudiante específico en el sistema por su ID.
- ✏️ **Modificar Estudiante**: Modifica la información de un estudiante existente.
- 🗑️ **Eliminar Estudiante**: Elimina un estudiante del sistema por su ID.
- 🚪 **Salir**: Opción para salir de la aplicación.

## 📝 Código Principal

### 📂 Estudiante.java
Define una clase `Estudiante` con los siguientes atributos y métodos:
- **Atributos**: `idEstudiante`, `nombre`, `apellido`, `telefono`, `email`
- **Métodos**:
  - Constructores: uno vacío, uno con `idEstudiante`, otro con `nombre`, `apellido`, `telefono` y `email`, y otro con todos los atributos
  - Getters y Setters para todos los atributos
  - `toString()`: para una representación en cadena del objeto `Estudiante`

### 📂 EstudianteDAO.java
Implementa el acceso a datos para gestionar estudiantes en la base de datos MySQL:
- **Métodos**:
  - `ListarEstudiantes()`: Lista todos los estudiantes.
  - `buscarEstudiantePorId(Estudiante estudiante)`: Busca un estudiante por su ID.
  - `agregarEstudiante(Estudiante estudiante)`: Agrega un nuevo estudiante.
  - `modificarEstudiante(Estudiante estudiante)`: Modifica un estudiante existente.
  - `eliminarEstudiante(Estudiante estudiante)`: Elimina un estudiante por su ID.

### 📂 Conexion.java
Define la clase para gestionar la conexión a la base de datos MySQL:
- **Método `getConexion()`**:
  - Establece una conexión con la base de datos `estudiantes_db` en MySQL.
  - Maneja las excepciones de conexión.

### 📂 SistemaEstudiantesApp.java
Define la clase principal que gestiona la interacción con el usuario:
- **Menú Principal**:
  1. Listar Estudiantes
  2. Buscar Estudiante
  3. Agregar Estudiante
  4. Modificar Estudiante
  5. Eliminar Estudiante
  6. Salir
- **Métodos**:
  - `mostrarMenu()`: Muestra el menú principal.
  - `ejecutarOpciones(Scanner consola, EstudianteDAO estudianteDAO)`: Ejecuta la operación seleccionada del menú.

## ⚙️ Requisitos
- Java 8 o superior
- MySQL
- IDE recomendado: IntelliJ IDEA o Eclipse

## 🚀 Ejecución
1. Clona el repositorio:
   ```bash
   git clone https://github.com/Martincho83/SistemaEstudiantesApp.git

2. Configura la base de datos MySQL:
  ```sql
  CREATE DATABASE estudiantes_db;
  USE estudiantes_db;
  CREATE TABLE estudiante (
      id_estudiante INT AUTO_INCREMENT PRIMARY KEY,
      nombre VARCHAR(50),
      apellido VARCHAR(50),
      telefono VARCHAR(20),
      email VARCHAR(50)
  );
 ```

3. Importa el proyecto en tu IDE preferido.
4. Ejecuta la clase SistemaEstudiantesApp para iniciar la aplicación.

## 🤝 Contribuciones
Si deseas contribuir a este proyecto, por favor realiza un fork del repositorio y crea un pull request con tus cambios.

## 👨‍💻 Autor
Martín - Desarrollador Principal - [Martincho83](https://github.com/Martincho83)
