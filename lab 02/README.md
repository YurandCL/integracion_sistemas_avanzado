# Administración de módulos en ODOO

## Laboratorio 02

Listado de tareas:
-----------------
1. Verificamos nuestros módulos instalados y  no instalados
2. Instalamos los módulos "Proyecto", "Gestion de inventario", "Gestion de ausencias" y "Punto de venta" y Verificamos las instalaciónes.
3. Activar el modo desarrollador.
4. Creamos un módulo en ODOO.
5. Modificar el módulo creado

### Verificamos nuestros módulos instalados y  no instalados.

Vemos todos nuestros modulos instalados haciendo uso de filtros, estos pueden ya estar especificados o podemos acer uno mas personal.

![pre-instalados](imagenes/1_modulos_instalados.PNG)

De la misma manera podemos ver los que no tengamos instalados, para instalarlos posteriormente

![no-instalados](imagenes/2_modulos_no_instalados.PNG)

### Instalamos los módulos "Proyecto", "Gestion de inventario", "Gestion de ausencias" y "Punto de venta".

Buscamos algunos módulos para poder instalarlos y hacer uso de ellos, como por ejemplo **Proyecto** pero instalamos algunos otros tambien

![instalacion-proyecto](imagenes/3_Instalacion_de_modulo_proyecto.PNG)

![verificacion-proyecto](imagenes/4_modulo_instalado.PNG)

![instalacion-otros](imagenes/5_instalacion_de_mas_modulos.PNG)

![verificacion-otros](imagenes/6_aplicaciones_instaladas.PNG)

### Activamos el modo desarrollador

Hacemos clic en ajustes para poder hacer uso del modo de desarrollo y así poder crear nuevos módulos y demás.

![modo-desarrollador](imagenes/7_activamos_el_modo_desarrollador.PNG)

Creamos el nuevo módulo que denominaremos **_testmodulo1_** haciendo uso del siguiente comando **"c:\Program    Files    (x86)\Odoo    11.0\python\python.exe"    "c:\Program    Files    (x86)\Odoo11.0\server\odoo-bin" scaffold testmodulo1 odoo/addons** todo en una sola líena

y debemos estar ubicados en nuestra carpeta donde se instaló _ODOO_ es decir aqui dentro *_"Folder raiz Odoo"/server/odoo/addons_*

### Creamos un nuevo módulo

Despues de haber ejecutado el comando anterior ingresamos a la carpeta de destino y verificamos que efectivamente se haya creado nuestra carpeta llamada _"testmodulo1"_

![nuevo-modulo](imagenes/8_verificamos_la_creacion_del_modulo.PNG)

revisamos su contenido

![nuevo-modulo](imagenes/9_Verificamos_el_contenido.PNG)

la creación del nuevo módulo fue un exito, ahora modificaremos el módulo para mayor personalización.

### Modificar el modulo creado

Veremos el contenido de nuestro archivo **__init_.py** para saber como es en un principio.

![nuevo-modulo](imagenes/10_Vemos_el_contenido_del_archivo_init.PNG)

Ahora modificaremos el contenido del archivo **__manifest_.py** del cual se extrae la informacion del módulo

![nuevo-modulo](imagenes/11_Modificamos_parametros_en_el_archivo_manifest.PNG)

Para que nos aparezca este nuevo módulo tenemos que actualizar la lista de aplicaciones y confirmamos dicha actualización

![nuevo-modulo](imagenes/12_Actualizamos_la_lista_de_aplicaciones.PNG)

![nuevo-modulo](imagenes/13_confirmacion_de_actualiacion.PNG)

Verificamos la existencia de nuestro módulo y luego  lo instalaremos para verificar que efectvamente se puede usar en ODOO.

![nuevo-modulo](imagenes/14_verificamos_la_existencia_de_nuestro_modulo.PNG)

![nuevo-modulo](imagenes/15_Instalamos_nuestro_modulo_y_verificamos.PNG)

Vemos los detalles para verificar que nuestros cambios si se realizaron con exito en el archivo **__manifest_.py**

![nuevo-modulo](imagenes/16_Vemos_los_detalles_y_comprobamos_que_se_pueda_desinstalar.PNG)

#### Descripción de funcionalidad de cada elemento.
 Nro | Nombre de Módulo | Descripción 
:----- | :----------------: | -----------: 
 1 | _init__.py | Con este archivo podemos hacer la importación desde python. 
 2 | _manifest__.py |  | Este es el archivo que se encarga de la descripción del módulo, módulos del cual depende, carga las vistas involucradas en el módulo, datos demo, datos de seguridad, etc. 
 3 | controllers | Dondes se declaran todos los controladores, con los cuales daremos como su nombre lo dice un control para prácticamente todo el módulo y la extracción e inserción de datos. 
 4 | models | donde se declaran todos los modelos de la base de datos que se representan como tablas en postgres 
 5 | Security | Donde se encuentran las reglas de seguridad de nuestros modelos 
 6 | views | Donde se declaran las vistas xml de nuesto módulo 