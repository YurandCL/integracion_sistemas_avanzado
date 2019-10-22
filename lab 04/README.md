# CRM en ODOO

## Laboratorio 04

Listado de tareas:
------------------
1. Instalacion y/o verificación del modulo inventarios.
2. Configuración de almacenes.
3. Tipos de operaciones.
4. Gestión de productos.
5. Importación y exportación masiva de productos.
6. Ajustes de inventarios.
7. Transferencias internas.
8. Informes.

### Instalacion y/o verificación del modulo inventarios.

Buscamos e instalamos el módulo CRM en la ventana de aplicaciones, esperamos a que finalze el proceso y después ingresamos al nuevo módulo.

!['instalacion'](imagenes/1_instalacion_gestion_inventario.PNG)

Dentro del módulo deberia verse de esta manera.

!['vista_almacenes'](imagenes/2_vista_almacenes.PNG)

### Configuración de almacenes.

En los submenus podemos ver uno que dice configuración y dentro de este modificaremos para que acepte tener multialmacén, despues de habilitar la opción guardaremos los cambios.

!['configuracion_almacén](imagenes/3_configuracion_almacenes.PNG)

Ahora ya podemos crear almacenes secundarios, asi que haremos uno dando clic en la opcion "crear"

!['creacion_nuevo_alamcen'](imagenes/4_creamos_nuevo_almacen.PNG)

Ahora editamos la informacion que trae por defecto y lo personalizamos un poco.

!['edicion_almacen](imagenes/5_editamos_almacen.PNG)

Agregaremos una nueva dirección del almacén y editaremos la informacion del mismo.

!['crear_direccion'](imagenes/6_creamos_direccion.PNG)

!['editar_direccion'](imagenes/7_editamos_direccion_nueva.PNG)

!['guardar_almacen'](imagenes/8_guardamos_direccion.PNG)

Tambien veremos algunas rutas que se han creado automaticamente para el almacén.

!['vista_rutas'](imagenes/9_vista_rutas.PNG)

### Tipos de operaciones.

En el submenú de gestión de almacenes encontraremos la opción "Tipos de Operaciones", con estas podemos restringir a un usuario a que solo ralice ciertas cosas y no pueda hacer algunas otras

!['operaciones'](imagenes/10_operaciones.PNG)

!['editar_operaciones'](imagenes/11_vista_editar_recepción.PNG)

Tambien podemos encontrar en las configuraciones una opción para las rutas multietapa, esto nos permite realizar una operación que deba pasar por varias ubicaciones antes de que sea considerada completa.

!['rutas_multietapa'](imagenes/12_rutas_multietapa.PNG)

### Gestión de productos.

Veremos el submenu de "Productos" y pasaremos a crear un nuevo producto.

!['creacion_productos'](imagenes/13_creamos_productos.PNG)

Cuando creamos un producto viene seleccionada por defecto la opcion de "producto almacenable", por tanto está habilitado el control de stock y así le inficamos a Odoo que es un producto cuyas transferencias deben tener seguimiento.

!['edicion_producto'](imagenes/14_edicion_del_producto_almacenable.PNG)

Cuando modificamos a tipo servicio, desaparecen las opciones relacionadas al stock.

!['servicio'](imagenes/15_servicio.PNG)

Y si seleccionamos consumible, habilitaremos el control de movimientos del producto, mas no el de stock.

!['consumible'](imagenes/16_consumible.PNG)

En la pestaña inventario, veremos algunos detalles del producto, como el peso, volumen, etc.

Pasaremos a crear el producto manzana verde con estos datos:

!['producto_manzana'](imagenes/17_producto_manzana.PNG)

Actualizaremos el stock del producto haciend clic en el botón "actualizar cantidad disponible" y modificaremos el valor por defecto a 10

!['actualizamos_cantidad'](imagenes/18_actualizamos_cantidad.PNG)

Después de la modificación y guardar los datos haremos clic en la opción que dice "a mano" y nos mostrará el stock total de todos tus almacenes.

!['almacen_editado'](imagenes/19_almacen_editado.PNG)

Otra cosa mas que nos da odoo es la opcion de imprimir etiquetas, para pegar en los anaqueles de venta.

!['impresion_etiquetas'](imagenes/20_imprimir_etiquetas.PNG)

Con la opción de movimientos de producto, nos permite rastrear los traslados del producto con almacenes o salidas de este.

!['movimientos_producto](imagenes/21_movimientos_del_producto.PNG)

### Importación y exportación masiva de productos.

En la vista de productos, haremos clic en el botón "lista", ubicado a la derecha debajo del filtro de buquedas.

!['listado_productos'](imagenes/22_lista_prductos.PNG)

Seleccionamos todos los productos y después haremos clic en la opción de "acción" y seguidamente en "exportar"

!['exportamos_informacion'](imagenes/23_exportamos_informacion.PNG)

Nos mostrará un asistente para poder descargar un formato conocido como excel y la tarea de revisar los datos sea mas sencilla.
Esta opción no solo se da en la vista de productos, por lo que podemos extraer datos de todo tipo.

!['exportamos_fichero'](imagenes/24_exportamos_fichero.PNG)

Ahora abrimos el excel que se ha generado después de exportado, veremos los datos de manera ordenada.

Añadiremos nuevos produtos como naranja, platano, etc.

!['excel'](imagenes/25_vista_desde_excel.PNG)

Ahora guardamos los cambios de nuestro archivo y procedemos a importarlo desde Odoo

!['importacion_excel'](imagenes/26_impotacion_excel.PNG)

Con esto podemos ver los nuevos cambios subidos al sistema. toos los productos han sido importados correctamente y asi podemos agregar muchos mas productos eh importarlos de manera mas sencilla.

!['ver_importacion'](imagenes/27_ver_datos_importados.PNG)

Nuestros productos estan registrados pero no tienen un stock, para ello pasaremos a crear un inventario de la siguiente manera.

!['creacion_inventario'](imagenes/28_creamos_nuevo_inventario.PNG)

### Ajustes de inventarios.

Editaremos la informacion que aparecerá por defecto, por ejemplo el nombre sera modificado a "Inventario inicial".

!['editamos_inventario'](imagenes/29_llenado_inventario.PNG)

Si vemos la parte de "detalle del inventario" podemos verificar que los datos se han jalado de todos los productos que tenemos actualmente, entonces tambien pasaremos a modificarlo, ya que por defecto todo estara en cero (excepto manzana que ya tenia definido un stock).

![modificamos_stock](imagenes/30_modificamos_stocks.PNG)

Despúes de hacer las modificaciones validaremos los cambios haciendo clic en "validar inventario"

!['validar_inventario'](imagenes/31_validamos_inventario.PNG)

Como ya tenemos la información validada, entonces podemos ver reflejado el ajuste del stock de todos los productos.

!['cambios_en_stock](imagenes/32_cambio_cantidad.PNG)

### Transferencias internas.

Hacemos clic en "transfrencias" dentro del panel de "Operaciones" al lado izquierdo de la página y luego haremos clic en "crear"

!['creamos_transferencia](imagenes/33_creamos_transferencia.PNG)

Agregamos algunos productos a la transferencia creada anteriormente.

!['agregamos_productos](imagenes/34_agregamos_productos_a_la_transferencia.PNG)

Nos generará un error debido a que no se ha seleccionado ningun tipo de operación hasta ahora, para ello haremos clic en "Info adicional" y despues en "Tipo de operación"

!['asignamos_operacion'](imagenes/35_asignamos_tipo_operacion.PNG)

Entonces daremos clic en validar para hacer la transferencia.

Si entramos a un producto que haya sido trasladado, vemos que el stock no ha cambiado.

!['stock_no_cambia'](imagenes/36_stock_no_varia.PNG)

Si hacemos clic en "stock a mano" podemos ver que el stock se ha dividido en dos ubicaciones diferentes.

### Informes.

En el submenú de informes podemos encontrar la opción de valoración, que nos permitirá saber cuanto vale nuestro almacén actualmente o de acuerdo a la fecha que se seleccione.

!['valoracion_inventario'](imagenes/37_valoracion_inventario.PNG)

Otra opción que encontramos es "Inventario", que me permite saber de manera rápida cuanto stock tengo de cada producto y en que almacén tengo cuanta cantidad.

!['inventario_normal'](imagenes/38_inventario_normal.PNG)

Por último tenemos la opción "Movimientos de productos" el cual nos muestra cuantos y que movimientos se hicieron de todos los productos en el sistema.

!['movimientos_productos'](imagenes/39_movimientos_de_productos.PNG)