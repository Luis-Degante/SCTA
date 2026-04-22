# SCTA
Sistema de Control de Tiendas de Abarrotes (Suarez Degante Luis Angel - Santoyo Aparicio Leonardo)

Archivos en Backend

Archivos de la carpeta Conexión

-Archivo: Conexión.java

-Explicación del fragmento:

Este archivo realiza como su nombre lo dice la conexión de nuestro sistema y sobre todo de nuestras interfaces con la base de datos para manipular dichos datos cuando sea necesario. Realiza la conexión mediante el uso del comando Connection cn = DriverManager.getConnection("jdbc:mysql://localhost/scta", "root", ""); y en caso de que haya un error arroja un mensaje de que la conexión ha fallado.

Archivos de la carpeta Controlador

-Archivo: Ctrl_Categoria

-Explicación del fragmento:

Esta clase se encarga de gestionarlas operaciones CRUD para la categoría como entidad, contiene métodos para realizar inserción de una nueva categoría, consultar alguna categoría ya existente, actualizar alguna categoría mediante su id y la eliminación de una categoría. Todo esto con sus respectivas condiciones de identificación y su respectivo mensaje en caso de que exista algún error como que la categoría no existe o no se realizo de manera correcta la operación.

-Archivo: Ctrl_Usuario

-Explicación del fragmento:

Este controlador se encarga de interactuar con la base de datos mediante conexiones JDBC, permitiendo validar credenciales, actualizar información del usuario y manejar mecanismos de recuperación de acceso. Implementa consultas SQL preparadas para garantizar mayor seguridad, evitando ataques como la inyección SQL. Permite validar el acceso al sistema verificando que el nombre de usuario y la contraseña coincidan con los registros almacenados en la base de datos. Facilita la modificación del nombre de usuario y la contraseña, asegurando que los cambios se reflejen correctamente en la base de datos. Implementa un mecanismo alternativo de autenticación basado en una pregunta de seguridad, permitiendo validar la identidad del usuario administrador sin necesidad de credenciales tradicionales. Permite actualizar la pregunta y respuesta de seguridad del usuario, fortaleciendo las medidas de protección del sistema.

Archivos de la carpeta Modelo

-Archivo: Usuario.java

-Explicación del fragmento:

Esta clase actúa como un objeto de transferencia de datos (DTO), ya que contiene los atributos que corresponden directamente a los campos de la tabla usuario en la base de datos, tales como el identificador del usuario, nombre, contraseña y los datos asociados a la seguridad (pregunta y respuesta de recuperación). Incluye un constructor por defecto que inicializa todos los atributos con valores seguros (0 o cadenas vacías), evitando errores comunes como los NullPointerException durante la ejecución del sistema. Además, implementa métodos getter y setter para cada uno de sus atributos, lo que permite acceder a los datos del usuario de manera controlada, modificar los valores de forma segura mantener el principio de encapsulamiento en la programación orientada a objetos.


-Archivo: Categoria.java

-Explicación del fragmento:

Esta clase permite definir y gestionar las clasificaciones de los productos (por ejemplo: refrescos, botanas, abarrotes), facilitando su organización, búsqueda y administración dentro del sistema. Actúa como un objeto de transferencia de datos (DTO) que encapsula la información de una categoría y la transporta entre las diferentes capas del sistema, especialmente entre la base de datos y la lógica de negocio. La clase cuenta con dos atributos que corresponden directamente con los campos de la tabla categoría en la base de datos, un identificador único de la categoría y nombre o descripción de la categoría


