# ON TASK
ON TASK es un gestor de tareas simple creado con React :atom_symbol: y Spring.<br>

Durante este verano he estado aprendiendo React de forma autodidacta con el objetivo de utilizarlo en mi Trabajo Fin de Grado que comenzaré en los próximos meses. <br>
Para poner en práctica todo lo aprendido, he desarrollado este proyecto. Además, me ha servido para profundizar un poco más en tecnologías como Spring o Bootstrap, y aprender otras como JsonWebTokens.
<br><br>
Los repositorios con el código del proyecto son:<br>
- [Frontend con React](https://github.com/SergioCarrascosaSanchez/ON-TASK-React)
- [Backend con Spring](https://github.com/SergioCarrascosaSanchez/ON-TASK-SpringBoot)

## Breve explicación
ON TASK es un gestor de tareas en el que los usuarios se organizan en grupos. <br>
Cualquier usuario puede crear un nuevo grupo o unirse a otros mediante un número identificador. <br>
Una vez dentro, se pueden crear las tareas. Cada tarea tendrá un título y una descripción, y estará asignada a uno o varios integrantes.<br>
El objetivo de los grupos es que los usuarios puedan agrupar sus tareas en diferentes temáticas o ámbitos, facilitando así la organización.<br>
<br>
Por ejemplo, imagínate que vas a crear una aplicación con un par de amigos y queréis utilizar ON TASK para organizaros.<br>
Uno de vosotros puede crear un grupo y compartir con el resto el identificador. <br>
Cuando estéis todos en el grupo, podéis empezar a crear y asignar las principales tareas entre vosotros.<br>
De esta forma, si utilizas ON TASK para organizar otro tipo de tareas, como las del hogar con tu familia o las de clase, estas quedarán diferenciadas de aquellas que tengan que ver con la aplicación que vais a crear.

<br>
Al final encontraréis un vídeo con una demostración de la aplicación completa para ver mejor cómo funciona realmente.

## Funciones

### Login y Signup
Para registrarse o iniciar sesión se deberá rellenar un formulario. Esa información se enviará a la API de Spring para poder validarla adecuadamente. <br><br>
En el caso de iniciar sesión, si el usuario es correcto, la API devolverá un JsonWebToken para poder realizar el resto de llamadas. De esta forma la API podrá rechazar aquellas que no tengan token o no sea válido.<br>
Además, se guardará el usuario que ha iniciado sesión, los grupos a los que pertenece y el token en un Contexto de React. Esa información se usará en el resto de componentes.

### Perfil de usuario
Se mostrarán los grupos a los que pertenece el usuario y las tareas que tiene pendientes dentro de ellos.<br>
Si el perfil es del usuario que ha iniciado sesión, se muestran dos botones para crear un nuevo grupo y unirse a uno ya existente.<br> 
Esa compobación del perfil se hace mediante un Contexto de React.<br>
<br>
<img src="/resources/profile_1.png" alt="" width="768" height="432"/> 
<img src="/resources/profile_2.png" alt="" width="768" height="432"/>

### Grupos
En la parte superior tenemos el nombre del grupo junto con el identificador.<br>
También se mostrarán los integrantes y todas las tareas que aún no se han completado. 
Si pertenecemos al grupo (se comprueba también mediante Contexto), nos aparecerán la opción de crear una nueva tarea. <br>
A la hora de crearla podemos asignarsela a uno o varios integrantes.<br>
<br>
<img src="/resources/group_1.png" alt="" width="768" height="432"/> 
<img src="/resources/group_2.png" alt="" width="768" height="432"/>

### Tareas
Una tarea está compuesta por un título y una descripción.<br>
Cuando hacemos click en una tarea, ya sea desde un grupo o un usuario, podemos verla en detalle.<br>
Además, si nos han asignado a ella tendremos la posibilidad de marcarla como completada.<br>
<br>
<img src="/resources/task_1.png" alt="" width="768" height="432"/> 
<img src="/resources/task_2.png" alt="" width="768" height="432"/>

### Video demostración
https://user-images.githubusercontent.com/19820916/188886121-4a74fe2d-fd34-4407-a865-305b7ad4501f.mp4


