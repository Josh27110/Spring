<h1>Tarea 1.- Herramientas para el desarrollo de proyectos de Software</h1>
<h2>Ejercicio 1: Instalación y configuración de herramientas</h2>
<h3>Descripción de la actividad: </h3>
  <p>En esta primera instrucción, se les solicita instalar y configurar en su sistema (macOS, Linux o Windows) las siguientes herramientas, que serán fundamentales para el desarrollo de sus proyectos:</p>
  1.    Java Development Kit (JDK): Se sugiere utilizar la versión Amazon Corretto, que es una distribución gratuita y certificada de OpenJDK. Deberá descargar e instalar la versión más reciente del JDK, que será necesaria para compilar y ejecutar programas     en Java. 
  
  ![image](https://github.com/user-attachments/assets/b44fde85-8601-4954-8416-1192fd3df9ac)

  2.    Maven: Esta herramienta les permitirá automatizar la construcción de proyectos y gestionar sus dependencias. Una vez instalada, deberán configurarla en su sistema.
  ![image](https://github.com/user-attachments/assets/df53bddc-0977-4ac8-a6e2-eca601098083)
  3.    Spring Boot: Descargar y configurar Spring Boot, un framework que facilita la creación de aplicaciones empresariales en Java. Pueden iniciar con un proyecto básico utilizando Spring Initializr.
  ![image](https://github.com/user-attachments/assets/2371d5e4-a5e5-458a-9e38-4499a961d8b3)
  4.    Git: Instalar Git para el control de versiones de sus proyectos. Además, configurar Git en su equipo para trabajar con repositorios remotos.
    ![image](https://github.com/user-attachments/assets/0e410d29-e6cd-45d4-9008-5dfacb81e476)

  5.    GitHub: Crear una cuenta en GitHub (si no la tienen) y un repositorio público donde deberán almacenar sus proyectos durante el curso.
    ![image](https://github.com/user-attachments/assets/793fa867-7db4-4fb4-afdf-9dea35c8e90c)

  6.    XAMPP: Sistema de gestión de bases de datos MySQL, el servidor web Apache y los intérpretes para lenguajes de script PHP y Perl.
    ![image](https://github.com/user-attachments/assets/4cc0fe19-e155-4413-a955-821c3371e41b)


Pasos a seguir:
  1.    Descargue, instale y configure las herramientas mencionadas.
  2.    Asegúrese de que estén funcionando correctamente.
    <p>Ejemplos:</p>
      <p>o    Para el JDK, ejecute el comando java -version para validar su instalación.</p>
      ![image](https://github.com/user-attachments/assets/c1559613-7f05-4899-b1f8-53804712eba1)
       <p>o    Para Maven, ejecute mvn -version y asegúrese de que las variables de entorno estén configuradas.</p>
       ![image](https://github.com/user-attachments/assets/2cb42430-4dd3-4866-a653-4e9a481fdf1c)

  4.    Utilizando Spring Initializr, cree un proyecto básico de Spring Boot con las dependencias de Spring Web.
        Configure las propiedades necesarias en el archivo application.properties.
    ![image](https://github.com/user-attachments/assets/686996cc-3a66-4f54-a0ee-a6042d5c08e3)

  5.    Agregue un controlador REST que devuelva un mensaje "¡Hola Spring!" a través de un endpoint básico.
    o    Pruebe el endpoint accediendo al navegador o utilizando herramientas como Postman.
    Inicialmente para esta sección corrí el programa en terminal donde si se imprime el mensaje, generando tambien una contraseña que podemos poner en una página de login en el puerto 8080
    ![image](https://github.com/user-attachments/assets/c6c69833-f8fe-4184-b1d3-60e07d87628d)

        Si usamos un navegador y ponemos "http://localhost:8080" aparecera la siguiente página:
        ![image](https://github.com/user-attachments/assets/f0aa0a24-7e2a-462d-a026-199d13d914fa)
     <p> Para las credenciales de usuario debemos poner "user" y en contraseña la que sale en la terminal</p>
     Pero como observamos nos envía una página enunciando el error "Whitelabel Error Page":
   
  ![image](https://github.com/user-attachments/assets/eb167ea6-1239-4986-bf0a-46a9c781e140)
   <p> Pero se nos solicita que hagamos un nuevo controlador REST que devuelva un mensaje, para esta sección al desconer en que consiste la API REST, solicite ayuda de la IA,
    siendo este el siguient código:</p>
      
    import org.springframework.web.bind.annotation.GetMapping;
    import org.springframework.web.bind.annotation.RestController;

    @RestController
    public class HolaController {

    @GetMapping("/hola")
    public String decirHola() {
        return "¡Hola Spring!";
      }
    }
  La implementación de la clase y la creación de una función es común, también la importación de otras librerías, lo nuevo son los @ResController y @GetMapping.
  1. @RestController
    Propósito: Indica que la clase es un controlador REST, es decir, un componente que maneja solicitudes HTTP y devuelve respuestas en formato JSON, XML u otro tipo de dato.

      Funcionamiento:

      Combina las anotaciones @Controller y @ResponseBody.

      @Controller: Marca la clase como un controlador de Spring MVC.

     @ResponseBody: Indica que el valor devuelto por los métodos del controlador se serializa directamente en el cuerpo de la respuesta HTTP (por ejemplo, en formato JSON).
  
  2. @GetMapping
        Propósito: Mapea una solicitud HTTP GET a un método específico en el controlador.

        Funcionamiento:

       Define la ruta (endpoint) que el método manejará.

        Cuando se realiza una solicitud GET a la ruta especificada, Spring Boot ejecuta el método anotado y devuelve su resultado como respuesta.
     En este caso, cuando se accede a http://localhost:8080/hola con un método GET, el método decirHola() se ejecuta y devuelve el mensaje "¡Hola Spring!".

      ![image](https://github.com/user-attachments/assets/f6e55ab6-dd27-44ca-b77d-d6efcf6da8f4)



7.Cree un repositorio público en GitHub y suba el proyecto con una estructura adecuada.
    o    Incluya un archivo README.md que explique brevemente cómo ejecutar su proyecto en un entorno local.

    Este es un proyecto Spring Boot simple que expone un endpoint REST para devolver un mensaje "¡Hola Spring!".

## Requisitos
- Java 17 o superior.
- Maven o Gradle.

## Cómo ejecutar el proyecto
1. Clona el repositorio:
   ```bash
   git clone https://github.com/Josh27110/Spring.git


