# **Documentación .KT's**



Este MD consta de la explicación de funcionamiento de KT presentes en la carpeta "OnlineStore" del proyecto RealTech-Master el cual consta de ser una APP de tienda virtual. 



***- Carrit.kt:*** 

KT con funcionamiento estructurado del apartado "Carrito", dividido en las siguientes fases:

1). **package com.example.onlinestore** — define el espacio de nombres del archivo.

2). **object Carrito** — declara un singleton en Kotlin (una única instancia global).

3). **val productos = mutableListOf<Producto>()** — lista mutable que guarda objetos Producto.

4). Aquí hay 4 funciones donde se añade un producto **(fun agregar)**, **(fun total)** suma y devuelve el precio total, **fun limpiar** que nos ayuda a vacía la lista, y **fun cantidad** la cual devuelve el número de productos en el carrito.



***- CarritoActivity.kt:***

para este KT necesitamos importar 8 librerías las cuales nos van a ayudar a implementar de mejor manera nuestras ideas y propósitos
	**- android.os.Bundle:** Contenedor con el estado de la Activity (parametro en onCreate).

	**- android.widget.Button:** Clase de botón UI; usada para btnFinalizarCompra.

	**- android.widget.TextView:** Componente para mostrar texto; usada para txtTotalCarrito.

	**- android.widget.Toast:** Mensaje breve tipo "popup" en pantalla; se usa para indicar "Compra realizada con éxito".

	**- androidx.appcompat.app.AlertDialog:** Builder para crear diálogos modales (confirmación de compra).

	**- androidx.appcompat.app.AppCompatActivity:** Activity base con compatibilidad hacia atrás; la clase CarritoActivity extiende de esta.

&nbsp;	**- androidx.recyclerview.widget.LinearLayoutManager:** LayoutManager que organiza los ítems del RecyclerView en una lista vertical u horizontal; aquí se usa para lista vertical.

&nbsp;	**- androidx.recyclerview.widget.RecyclerView:** Componente para listas/colecciones eficientes; aquí muestra los productos del carrito mediante un adapter (CarritoAdapter).



***- CarritoAdapter.kt:*** 

"RecyclerView" conecta la lista de productos con las filas visuales. "ViewHolder" guarda referencias a las vistas de cada fila (nombre, precio, imagen) para reutilizarlas. "onCreateViewHolder" infla el layout de una fila (item\_carrito). "onBindViewHolder" coloca los datos del producto en las vistas según la posición. "getItemCount" devuelve cuántos productos hay.



***- CarritoFragment.kt:***

Este KT sigue siendo un complemento del carito, especificamente y su paso a paso es: crear la vista del fragment.

Crea un Intent para abrir CarritoActivity y lo lanza inmediatamente con startActivity(intent), programa con view.postDelayed un runnable a los 100 ms que llama (activity as? MainActivity)?.selectProductosTab() — intenta cambiar la pestaña del MainActivity a la pestaña "Productos", y Devuelve la vista del fragment.



***- DetalleActivity.kt:***

Este KT nos muestra la información de un producto seleccionado y nos permite agregarlo al carrito. Es una pantalla que se muestra cuando se selecciona un producto, consta de la recepción de productos mediante variables, si no los tiene usa unos por default. Se conecta con una interfaz gráfica definidos en "activity\_detalle.xml", muestra los datos importados y los muestra en pantalla. Adicionalmente (linea 32) nos ayuda creando un Objeto "Producto" el cual implementa la opción de añadir al carrito con su mensaje de confirmación. adicionalmente decora el precio cambindolo de Num a String decorado (- Ejemplo: 1234.56 → $1,235)



***- FormularioActivity.kt:*** 

Este KT nos ayuda implementando todo el formulario, importamos el "activity\_formulario.xml" el cual nos trae el QR, Nombre, Email, Tlf y dirección. 
Seguido de esto, valida el QRform, con un condicional IF el cual nos ayuda a validar si el formulario tiene todos los campos completos. Sino, muestra un mensaje de error, tmbn nos ayuda a saber si todos los cambos están completos. Para terminar se "Envía" un mensaje al servidor (En este caso solamente damos un mensaje de confirmación al User). Finalmente se limpian los campos 



***- LoginActivity.kt:***

Este KT es bastante estructurado ya que viene con diferentes opciones de registro para el usuario. damos la opción de registro por teléfono (32:64) donde se divide en el acceso por teléfono, una condicional que decide y actúa si el usuario coloca Enteros para registro automatico por Tlf y su valizdación en FireBase. Tenemos otra opción de login mediante Email con autenticación mediante Token enciado por sms. Terminando con una validación exitosa o errónea de ingreso 



***- MainActivity.kt:***

Esencialmente este KT muestra un menú inferior (bottom navigation) con varias secciones, permite cambiar entre ellas usando fragments, y gestiona el cierre de sesión del usuario (incluyendo Firebase y preferencias locales). Este KT viene acompañado de comentarios internos que nos ayuda a saber en que parte del code se ejecuta que acción. 



***- MapaActivity.kt:*** 
WOW este file jeje. Consta de varias importaciones de librerías para crear un correcto apartado de información y mapa de ubicación de empresa. Tenemos complementos de tecto, dirección y nombre de empresa acompañado de link en maps que nos guía a la tienda. Visualmente nos aporta un marcador sobre el mapa donde muestra la tienda, acompañado de movimiento de camara, zoom y solicitud de permisos de ubicación, estos para ser evaluados y permitir saber la ubicación el usuario. COn esto evaluado se genera una posición, si no se concede esto aun asi se abre la app de Maps con la ubi de la tienda. si esta no está instalada se abre para que se instale, si no abre muestra un error. 



***- OpinionFromActivity.kt:*** 

Este Kt es extenso, pero de manera resumida importa la información del usuario y mediante condicionales evalúa un puntaje de encuesta dando un resultado, teniendo previamente condicionales de error de usuario como "Campos vacíos" o "Valores erroneos" (Mostrados en KT). Terminando con una futura conexión a DB mediante la creación de un Objeto con los datos obtenidos (Line:223) (Por ahora solo se muestra un mensaje de éxito). Terminando con los datos recolectados listos para el envío a DB. 



***- Producto.kt:*** 

KT de definición de "Producto" con respectivos valores admitidos.  



***- ProductoAdapter.kt:***

Se importa el XML item\_producto para poder mostrar una lista de productos adicionando una acción cuando se hace clic en un producto.



***- ProductosFragment.kt:*** 

Una lista de 25 productos divididos en 10 categorías diferentes, cada uno con su correspondiente nombre, precio, imagen y descripción. 



***- QRFragment.kt:*** 

cada vez que se muestra este fragmento, se abre la actividad para generar un código QR y, casi al mismo tiempo, se intenta volver a la pestaña de productos en la actividad principal



***- QRGeneratorActivity.kt:*** 

Esta actividad genera un código QR que, al ser escaneado, abrirá un formulario de opinión dentro de la aplicación. Además, permite al usuario abrir el formulario directamente al hacer clic en un botón.



***- QRScannerActivity.kt:*** 

Esta actividad escanea códigos QR y, dependiendo del contenido, puede abrir un formulario de opinión o mostrar el contenido escaneado. constituido por 5 pasos 

**1). Inicialización:**

Configura PreviewView para mostrar la vista previa de la cámara.

Crea un cameraExecutor para manejar la ejecución en un hilo separado.

Inicializa el barcodeScanner para procesar códigos de barras.

**2). Permisos de cámara:**

Verifica si se tiene permiso para usar la cámara. Si no, solicita el permiso.

Si se concede el permiso, inicia la cámara.

**3). Inicio de la cámara:**

Configura la cámara para mostrar la vista previa y analizar las imágenes en tiempo real.

Usa ImageAnalysis para procesar cada cuadro de la cámara.

**4). Procesamiento de imágenes:**

Convierte el ImageProxy en un InputImage y lo envía al barcodeScanner.

Si se detecta un código QR, maneja el contenido del código.

**5). Manejo del contenido del QR:**

Si el contenido del QR es un esquema personalizado (como onlinestore://opinionform), abre OpinionFormActivity.

Para otros códigos QR, muestra un mensaje con el contenido escaneado.



***- RegisterActivity.kt:*** 

Este KT evalúa y compara los datos ingresados a la hora de hacer un nuevo usuario sobre la app, con mensajes de "campos incompletos o erróneos" y operadores donde almacenan los datos nuevos ingrsados. tirando un mensaje exitoso o de error al crear el user



***- UbicacionFragment.kt:*** 

Fragmento complementario donde se almacena mayor información de la Ubicación y la tienda en general con aun el complement de abrir la ubicaión de la tienda, si no tiene la app da la opcion de instalarla o un mensaje de error 



***- VerifyCodeActivity.kt:*** 

VerifyCodeActivity permite completar la verificación por SMS con Firebase Phone Auth.

Recibe por Intent un String "verificationId" (ID enviado por Firebase cuando se pidió el SMS).

Tiene un EditText (edtCodigo) para que el usuario ingrese el código recibido y un botón (btnVerificar).

Al pulsar el botón:

Toma el código del EditText.

Crea un PhoneAuthCredential con PhoneAuthProvider.getCredential(verificationId, code).

Llama a auth.signInWithCredential(credential).

Si la verificación es exitosa muestra un Toast, abre MainActivity y cierra esta Activity.

Si falla muestra un Toast con el error.

Dependencias: FirebaseAuth y PhoneAuthProvider (Firebase Phone Authentication).





