# CRM en ODOO

## Laboratorio 05

Listado de tareas:
------------------
1. Instalacion y/o verificación del modulo ventas.
2. Creción de cotización a cliente.
3. Entrga de productos de una Cotización.
4. Facturación y registro de pago de una cotización.
5. Configuración de envío de correos.
6. Cambio de Secuencia.
7. Lista de precios.
8. Portal del cliente.

### Instalacion y/o verificación del modulo ventas.

Pasaremos a instalar o a verificar la instalación del módulo "Gestión de ventas"

!['instalcion_modulo_ventas'](imagenes/1_instalacion_modulo_ventas.PNG)

Veremos el módulo por dentro, después de su instalación se habilitara un nuevo menu de acceso hacia el.

!['menu_ventas'](imagenes/2_menu_ventas.PNG)

Con esto podemos verificar que efectivamente el módulo se creo satisfactoriamete.

### Creción de cotización a cliente.

Entramos al menú "Cotizacion" para empezar a crear una nueva cotización.

!['cotización_nueva'](imagenes/3_nueva_cotizacion.PNG)

!['productos_varios'](imagenes/4_productos_varios.PNG)

Seleccionaremos manzanas verdes e ingresaremos 100 unidades.

!['alerta_venta'](imagenes/5_alerta_venta.PNG)

Aún si falta stock creamos la cotización con dos productos por ahora

!['cotizacion'](imagenes/6_cotizacion_dos_productos.PNG)

En la cotización podemos modificar los datos del cliente como la fecha, el plazo de pago, etc.

!['informacion_cotizacion'](imagenes/7_informacion_cotizacion.PNG)

Ahora podemos modificar otra información adicional y modificar cosas como el almacén al cual se diigirá el pedido.

!['otra_informacion'](imagenes/8_otra_informacion.PNG)

Despues guardamos y luego validamos. Al validar esta cotización se mostrarán nuevas opciones como el envio por correo, imprimir, confirmar, etc.

!['guardar'](imagenes/8_guardamos_toda_informacion.PNG)

En caso el cliente no tenga correo electrónico, al momento de enviarle la cotización nos pedirá ingresar uno de todas formas, asi que ingresaremos un correo.

!['ingresamos_email'](imagenes/9_ingresamos_email.PNG)

Despúes de ingresar el correo se nos mostrará un borrador del correo auto-generado por Odoo

!['borrador_email'](imagenes/10_borrador_email.PNG)

Ahora la cotización que hemos creado pasará a ser un presupuesto

!['presupuesto'](imagenes/11_presupuesto.PNG)

También podemos ver la nueva opción de Entrega y crear factura

!['crear_factura'](imagenes/12_creacion_factura.PNG)

### Entrga de productos de una Cotización.

Al entrar al módulo de inventarios, en el tablero principal podemos ver que ahora se ha generado una orden de entrega.

!['orden_entrega'](imagenes/13_informar_entrega.PNG)

Al entrar a la entrega podemos validar nuestra venta, para ello debemos incrementar nuestro stock y lo haremos a 500 unidades

!['validacion_venta'](imagenes/14_validacion_venta.PNG)

!['envio_comprobante'](imagenes/15_envio_comprovante.PNG)

### Facturación y registro de pago de una cotización.

Crearemos una factura, para registrar un comprobante a enviar al cliente. Se nos abrirá una ventana que nos pregunta cómo queremos facturar, usaremos la opción "Líneas a facturar", lueg daremos clic en "Crear y Ver Facturas".
Con esto tendremos una factura lista para emitir, pero en caso algun dato este mal aún tenemos la opción a editarlo en esta ventana.
Despúes de dar clic en "Validar" aparecerán mas opciones en la factura. Y nos permitirá crear un correo adjuntando la factura.

!['envio_factura'](imagenes/15_envio_factura.PNG)

!['Confirmación_de_envio'](imagenes/16_aceptacion_envio_factura.PNG)

Despúes de emitir la factura veremos como el estado del cliente cambia, mostrandonos un inidicador de ventas.

!['verificacion_clientes'](imagenes/17_verificacion_clientes.PNG)

Volviendo a la factura, haremos clic en "registrar pago"

!['registrar_pago'](imagenes/18_realizaremos_pago.PNG)

Por defecto veremos como se autocompleta la cantidad por la total de la factura y así poder cancelarla.

!['monto_a_pagar'](imagenes/19_monto_pagar.PNG)

En este caso no se realizará el pago completo, así que haremos un pago parcial editamos la cantidad puesta por defecto y ponemos lo que realmente se va a pagar, el sistema detectará el cambio y nos mostrara dos opciones, marcaremos "Mantener abierto"

!['monto_parcial'](imagenes/20_monto_parcial.PNG)

Al ver el detalle de la factura, en la parte de los totales veremos registrado el pago y saldo pendiente.

!['pagado_y_saldo'](imagenes/21_pagado_saldo.PNG)

También podemos ver en el modulo de Facturación, al ver el comprobante en estado abierto y cuandto es el saldo.

!['modulo_facturacion'](imagenes/22_modulo_facturacion.PNG)

### Configuración de envío de correos.

Por ahora enviamos dos correos pero ninguno fue enviado, esto se debe a que Odoo usa un servidor smtp de correo y debmos configurarlo.
Para ello activaremos el modo desarrollador y luego en ajustes buscaremos "Email", podemos ver que solo existe un servidor de correos, así que lo seleccionaremos.

!['ajustes_email'](imagenes/23_ajustes_email.PNG)

Editaremos el servidor de correo. Ingresaremos la siguiente información correspondiente a cada uno.

!['editar_informacion'](imagenes/24_editar_informacion.PNG)

También debemos configurar en nuestros correos el uso de "aplicaciones poco seguras" como lo llama gmail, para que nos permita hacer los envios.

!['configurar_correo'](imagenes/25_configurar_correo.PNG)

!['aceptar_app_poco_seguras'](imagenes/26_aceptar_apps_poco_seguras.PNG)

Ahora de vuelta en Odoo probaremos la conexión.

!['Prueba_conexión'](imagenes/27_prueba_exitosa.PNG)

Probaremos enviar otra factura a algún cliente. Para ello usaremos un correo personal distinto al usado anteriormente.

!['corroboracion_envio'](imagenes/28_corroboracion_llegada_correo.PNG)

### Cambio de Secuencia.

Nuestra cotización se creó como la SO001. Esta es una secuencia interna de Odoo que se puede modificar si estamos en modo desarrollador, para lo cual iremos a ajustes, técnico, secuencias e identificadores, y finalmente, secuencias

!['secuencias'](imagenes/29_encontramos_secuencias.PNG)

En el buscador escribiremos "sale" para encontrar nuestra secuencia y después hacemos clic en ella.

!['sales_order'](imagenes/30_sales_order.PNG)

Editamos la informacion como se muestra a continuación y guardamos los cambios.

!['guardamos_cambios'](imagenes/31_guardamos_cambios.PNG)

### Lista de precios.

Veremos la lista de precios. Para esto, debemos ir al módulo Ventas, Ajustes y activamos la opcion "múltiples precios de venta por producto"

!['multiples_precios'](imagenes/32_multiples_precios.PNG)

Ahora tendremos habilitado un Menú de Listas de precios. Crearemos una lista llamada Tarifa Mayorista.

!['crear_tarifa'](imagenes/33_crear_tarifa_mayorista.PNG)

Podemos ver que el detalle del producto, la pestaña de ventas cambia para poder elegir el precio de acuerdo a la lista.

!['modificacion_tarifas'](imagenes/34_modificacion_tarifas.PNG)

Si editamos un cliente, ahora veremos que en la pestaña vetas y compras, ahora aparecerá la opción de lista de precios.

!['lista_precios_cliente'](imagenes/35_lista_precios_cliente.PNG)

### Portal del cliente.

Vamos al detalle del cliente y damos clic en Acción, luego en Administración de acceso al portal

!['administracion_acceso_portal'](imagenes/36_administracion_acceso_portal.PNG)

Le diremos al sistema que este cliente tiene acceso, dandole clic en el check al costado del correo

!['activacion_acceso'](imagenes/37_activacion_acceso.PNG)

Esto nos envia un correo a nuestro portal electrónico.

!['correo_acceso'](imagenes/38_correo_acceso.PNG)

Haremos clic en el enlace para poder establecer nuestra contraseña de cliente.

!['configuracion_contrasenia'](imagenes/configuracion_contrasenia.PNG)

Ahora por fin tendremos acceso al portal del sistema

!['acceso_portal_cliente'](imagenes/acceso_portal_cliente.PNG)
