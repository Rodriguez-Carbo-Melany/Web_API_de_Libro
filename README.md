# Web_API_de_Libro
El código está dividido en varios archivos y utiliza el framework de Spring Boot para crear una aplicación web que maneja libros. A continuación te explico cada parte del código:
![image](https://github.com/Rodriguez-Carbo-Melany/Web_API_de_Libro/assets/170265718/489b9a48-a331-4332-9bb2-7ea8bd38ee1d)

LibroController.java
Este archivo define el controlador que maneja las peticiones HTTP relacionadas con los libros.
![image](https://github.com/Rodriguez-Carbo-Melany/Web_API_de_Libro/assets/170265718/0ebe0a3d-521d-410b-b81b-f070afd12568)
@RestController: Indica que esta clase es un controlador de Spring que manejará las peticiones HTTP.

@RequestMapping("/libros"): Define la ruta base para todas las peticiones manejadas por este controlador.

@Autowired: Inyección de dependencias de Spring para que el LibroService sea inyectado automáticamente.

@GetMapping: Maneja peticiones GET para obtener todos los libros o un libro específico por su ID.

@PostMapping: Maneja peticiones POST para crear un nuevo libro.

Libro.java
Este archivo define el modelo de datos para un libro.
![image](https://github.com/Rodriguez-Carbo-Melany/Web_API_de_Libro/assets/170265718/bcaa231b-c6e4-4298-ba92-b1126e094ccb)

Clase Libro: Contiene atributos como id, titulo, autor, editorial y anioPublicacion.

Getters y Setters: Métodos para acceder y modificar los atributos.

toString, equals, y hashCode: Métodos sobreescritos para facilitar la manipulación y comparación de objetos Libro.

LibroRepository.java

Este archivo actúa como un repositorio en memoria para gestionar los libros.

![image](https://github.com/Rodriguez-Carbo-Melany/Web_API_de_Libro/assets/170265718/cc2d414d-2466-4df2-ac57-bb2f74d5d1dc)

@Repository: Indica que esta clase es un componente de acceso a datos en Spring.

Métodos:

obtenerTodosLosLibros: Devuelve todos los libros.

obtenerLibroPorId: Busca un libro por su ID.

agregarLibro: Añade un nuevo libro a la lista.

LibroService.java

Este archivo define el servicio que maneja la lógica de negocio relacionada con los libros.

![image](https://github.com/Rodriguez-Carbo-Melany/Web_API_de_Libro/assets/170265718/650e04df-aad3-4850-ace1-2f2d4890a0d9)

@Service: Indica que esta clase es un componente de servicio en Spring.

Métodos:

obtenerTodosLosLibros: Devuelve todos los libros llamando al repositorio.

obtenerLibroPorId: Busca un libro por su ID llamando al repositorio.

agregarLibro: Añade un nuevo libro llamando al repositorio.

Deber2Application.java

Este archivo contiene el punto de entrada de la aplicación Spring Boot.

![image](https://github.com/Rodriguez-Carbo-Melany/Web_API_de_Libro/assets/170265718/4717b37f-cf15-4f60-b447-f12b5f3fa7c9)

El objetivo de este proyecto es crear una aplicación web básica que permita gestionar (crear, obtener) una colección de libros utilizando el framework Spring Boot. La 
aplicación ofrece una API REST que permite realizar operaciones CRUD (Create, Read) sobre los libros.

Funcionalidades

Obtener todos los libros: La aplicación permite recuperar una lista de todos los libros disponibles.

![image](https://github.com/Rodriguez-Carbo-Melany/Web_API_de_Libro/assets/170265718/e1882da5-32f4-4cd8-8d1b-d909e4afb01a)

Obtener un libro por ID: La aplicación permite recuperar la información de un libro específico utilizando su ID.

![image](https://github.com/Rodriguez-Carbo-Melany/Web_API_de_Libro/assets/170265718/b65338e7-65ea-4a68-b09c-bad474030d67)

Crear un nuevo libro: La aplicación permite agregar un nuevo libro a la colección.

![image](https://github.com/Rodriguez-Carbo-Melany/Web_API_de_Libro/assets/170265718/fb32e29b-93d3-449d-929a-0bd771b6e31b)

Comportamiento Esperado en Pantalla

En el Navegador

Obtener todos los libros

Cuando se accede a http://localhost:8080/libros mediante una solicitud GET, la aplicación devuelve una lista en formato JSON con todos los libros disponibles.

![image](https://github.com/Rodriguez-Carbo-Melany/Web_API_de_Libro/assets/170265718/ba002225-d06a-46bd-9a23-5019388d0b92)






