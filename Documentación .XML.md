# Documentación .Xml's



Este MD consta de la explicación de funcionamiento de XML presentes en la carpeta "LayOut" del proyecto RealTech-Master el cual consta de ser una APP de tienda virtual 

***- activity\_carrito.xml:***

Este LayOut define principalmente la pantalla de "Carrito de compras" sobre el proyecto. Usa un "LinearLayout" vertical como contenedor principal, se caracteriza por un título centrado que indica el apartado (Carrito de compras), se usa un "RecyclerView" para poder listar los productos agregados al carrito. Para terminar, se muestra el total de la compra y un botón para poder finalizar la compra decorado con fondo blanco y sombra 



***- activity\_detalle.xml:***

Este XML define el diseño de la pantalla de detalle de un producto en el proyecto presente**.** Usa un ScrollView para permitir desplazamiento vertical si el contenido es largo, Dentro hay un LinearLayout vertical que contiene: 
1). Una imagen del producto (ImageView). 
2). El nombre del producto (TextView grande y en negrita) 
3). El precio del producto (TextView destacado en azul)

4). La descripción del producto (TextView). y terminando, 

5). Un botón para agregar el producto al carrito



***- activity\_formulario.xml:***

Textualmente este file es un visual de un formulario de vinculación simple acompañado de un QR donde se solicitan datos como: el nombre, email, teléfono y dirección. Terminando con un botón donde se sube el formulario



***- activity\_login.xml:***

Este es un login simple donde se solicita los datos del usuario (Correo) y una contraseña, sus adicionales visuales son un texto centrado "Iniciar sesión" acompañado de botones inferiores de "Ingresar" y "¿no tiene cuenta? Regístrese aquí"



***- activity\_main.xml:*** 

Este archivo XML define el diseño principal de la pantalla inicial de la app. Específicamente: Usa un "LinearLayout" vertical como contenedor. Arriba muestra una barra con el logo, el nombre de la app y un botón para cerrar sesión, en el centro hay un "FrameLayout" que sirve como contenedor para fragments (donde se muestran diferentes pantallas o secciones), abajo incluye una barra de navegación (BottomNavigationView) para cambiar entre las principales secciones de la app



***- activity\_mapa.xml:*** 

textualmente es un botón con texto de "Abrir en googleMaps" acompañado de un pequeño complemento de google maps que nos ayuda a mostrar un mapa pequeño en la APP para referenciar a los clientes 



***- activity\_option\_form.xml:***

Este archivo Es formulario largo para que los usuarios den su opinión sobre la app de tienda virtual, consta de su respectivo título y descripción del formulario:

1). Sección de datos del usuario: nombre, email y rango de edad.

2). Sección de experiencia: calificación general, facilidad de registro, organización de productos, satisfacción con el carrito, uso del QR y utilidad del mapa.

3). Sección de opinión y sugerencias: aspectos que gustaron, aspectos a mejorar y si recomendarían la app.

4). Botón para enviar el formulario

falta adicionar que en las líneas 15, 36, 47, 59, 82, 105, 161, 173, 200, 248, 275, 302, 350, 398, 410, 436, 462, y 502 se especifica en que apartado se encuentra que linea de ejecución, porque entendemos que este File es un poco extenso y decidimos fragmentarlo con documentación interna. 



***- activity\_qr\_generator.xml:*** 

Sobre este file se muestran 2 apartados en 1 sola pantalla, la imagen con texto que dice "Escanea este código QR para acceder al formulario de datos personales" y un texto preventivo donde es un botón para abrir mediante un Texto con vinculo abrir el formulario 



***- activity\_qr\_scanner.xml:*** 

este layout consta de mostrar un texto arriba ("Escanea el código QR"), mostrar la vista previa de la cámara en el centro (PreviewView), donde se escanea el QR, y mostrar otro texto abajo ("Apunta la cámara al código QR").



***- activity\_registrer.xml:*** 

Este es un file dividido y documentado internamente, donde sus funciones constan de crear la interfaz simple al usuario para que este coloque sus datos de Nombre, correo y Password acompañado de su respectivo titulo, logo y botón para continuar 



***- activity\_verify\_code.xml:*** 

Este consta de 3 Partes principales donde se muestra un texto de "Verifica tu teléfono", un EditText para entrada de código y un botón para validación 



***- fragment\_carrito.xml:*** 

Un apartado simple donde es un texto de carga donde aparece un "Redirigiendo al carrito...", únicamente informativo



***- fragment\_productos.xml:*** 

Muestra una lista de productos usando un RecyclerView. El RecyclerView ocupa toda la pantalla y se usa para mostrar productos en forma de lista o cuadrícula. El layout solo organiza el espacio para esa lista.



***- fragment\_qr.xml:*** 
Una pantalla de carga para el apartado del QR donde solamente muestra un texto de "Redirigiendo al QR"



***- fragment\_ubicación.xml:***

Este LayOut muestra información adicional de la tienda, tal como la ubicación, nombre de tienda, teléfono, Horarios y una función para abrir ubicación en googleMaps



***- item\_carrito.xml:*** 

<b>Apartado horizontal donde nos muestra la imagen del producto, su nombre y su precio, la estructura es una imagen al costado izquierdo acompañado de la anterior info a su derecha. </b>



<b>*- item\_producto.xml:*</b>

<b>De la misma funcionalidad anterior, imagen del producto la izquierda acompañado de su nombre, precio y precio por fuera del carrito, como producto exhibido en la tienda </b>

