To-Do List App
Esta aplicación web ofrece una lista de tareas básica con funcionalidades de agregar, eliminar, completar y editar tareas.

Características:

Agregar Tareas: Utiliza el formulario para agregar nuevas tareas a la lista.
Eliminar Tareas: Elimina las tareas existentes con un simple clic en el ícono de bote de basura.
Completar Tareas: Marca las tareas como completadas al hacer clic en ellas.
Editar Tareas: Permite editar el contenido de una tarea haciendo clic en el ícono de edición.

Tecnologías Utilizadas:

React: La aplicación está desarrollada utilizando la biblioteca React para la interfaz de usuario.
LocalStorage: Se emplea para almacenar las tareas localmente en el navegador.

Cómo Usar:

Clona el repositorio a tu máquina local.
Ejecuta npm install para instalar las dependencias.
Inicia la aplicación usando npm start.
Abre tu navegador y accede a http://localhost:3000.

Estructura del Proyecto:

/src: Contiene el código fuente de la aplicación.
/Components: Componentes reutilizables de React.
/hooks: Directorio que contiene hooks personalizados.
app.jsx: Archivo principal de la aplicación.
/hooks: Contiene hooks personalizados para la gestión de formularios y tareas.

Funcionalidades Principales:

Agregar Tareas: Los usuarios pueden agregar nuevas tareas a la lista. Esto se logra mediante el componente TodoAdd.


Función: handleNewTodo
Método en TodoAdd: onFormSubmit



Eliminar Tareas: Los usuarios pueden eliminar tareas existentes de la lista. Esto se realiza con el botón de eliminar en cada elemento de la lista, utilizando el componente TodoList.


Función: handleDeleteTodo
Método en TodoItem: onClick={() => handleDeleteTodo(todo.id)}


Marcar Tareas como Completadas/Pendientes: Las tareas pueden marcarse como completadas o pendientes. Este cambio de estado se refleja visualmente y afecta al recuento de tareas pendientes. La funcionalidad se implementa en el componente TodoItem y se gestiona mediante el estado local y el contexto de React.


Función: handleCompleteTodo
Método en TodoItem: onClick={() => handleCompleteTodo(todo.id)}


Actualizar Descripción de Tarea: Los usuarios pueden editar la descripción de una tarea existente. Esta funcionalidad se activa al hacer clic en el botón de edición y se implementa mediante el componente TodoUpdate.


Función: handleUpdateTodo
Método en TodoUpdate: onSubmitUpdate


Contador de Tareas: Muestra el número total de tareas en la lista y Actualización automática del contador cuando se agregan o eliminan tareas.

Variable: todosCount
Cálculo: const todosCount = todos.length;
Ubicación: En el hook useTodo


Contador de Tareas Pendientes: Indica el número de tareas pendientes o no completadas en la lista y Se actualiza automáticamente al marcar tareas como completadas.

Variable: pendingTodosCount
Cálculo: const pendingTodosCount = todos.filter(todo => !todo.done).length;
Ubicación: En el hook useTodo


Persistencia de Datos: El estado de la lista de tareas se guarda y recupera del almacenamiento local (localStorage) para que los datos persistan incluso después de recargar la página. Esto se logra a través del hook useEffect en el hook useTodo.


LocalStorage: Utilizado en el hook useEffect de useTodo para guardar y cargar tareas.


Interfaz de Usuario Intuitiva: Ofrece una interfaz fácil de usar para que los usuarios puedan interactuar con las tareas de manera sencilla y ofrece una navegación clara entre las diferentes funciones y tareas disponibles.


Cómo Contribuir
¡Siéntete libre de contribuir a este proyecto! Puedes:

Agregar nuevas funcionalidades.
Mejorar el diseño o la experiencia de usuario.
Reportar problemas o errores.

Autor

Jair Uribe.

