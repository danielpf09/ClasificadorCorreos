# ClasificadorCorreos
📌 1. Descarga de UiPath

UiPath ofrece dos versiones principales:

UiPath Studio Community (gratuita)

UiPath Studio Enterprise (requiere licenciamiento)

Para el proyecto, puede usar la versión Community (recomendado).

Pasos para descargar:

Entra a:
https://cloud.uipath.com

Selecciona “Sign Up” si no tiene cuenta.
Puede registrarse con:

Google

Microsoft

Correo personal

Una vez dentro de la plataforma, entra al menú superior y selecciona:
Admin → Licenses

Verifica que tiene activa la licencia Automation Developer - Pro Trial o Community.

Luego va a:
Resource Center (abajo izquierda)

Y descarga:
UiPath Studio / UiPath Assistant

Este archivo se llama normalmente:

UiPathStudio.msi

📌 2. Instalación de UiPath Studio

Cuando abra el instalador:

Selecciona Install for me (recomendado).

El instalador configurará automáticamente:

UiPath Studio

UiPath Assistant

Componentes del robot local

Al finalizar, aparecerá UiPath Studio para iniciar sesión.

Debe iniciar sesión con la misma cuenta que usó en cloud.uipath.com.

📌 3. Conexión de UiPath Studio con UiPath Cloud

Una vez Studio esté abierto:

Ir a la esquina inferior izquierda:
“Orchestrator Settings” o “Robot Settings”.

UiPath Assistant se abre automáticamente.

En UiPath Assistant:

Asegura que el modo esté en Connected.

Si aparece Disconnected, hace clic en Sign in.

Cuando la conexión queda establecida, Studio muestra un círculo verde indicando que está conectado al Orchestrator.

📌 4. Abrir el proyecto en UiPath Studio

Abrir UiPath Studio

Seleccionar Open Project

Buscar la carpeta del proyecto

Abrir el archivo:

Main.xaml


Este suele ser el flujo principal del robot.

📌 5. Configuración previa antes de ejecutar
✔️ Comprobar dependencias

UiPath Studio suele pedir actualizar paquetes.

ir a:

Manage Packages → Updates → Update All

✔️ Configurar rutas

El robot utiliza rutas como:

FacturasDescargadas
Facturas procesadas
<img width="1043" height="231" alt="image" src="https://github.com/user-attachments/assets/0bb04b83-82af-4f7e-b581-9ebaaa78e314" />

Tener etiquetas en el correo gmail para que el bot pueda realizar la clasificación

<img width="255" height="268" alt="image" src="https://github.com/user-attachments/assets/501af145-2583-41b4-9bb7-640594ffbcdc" />




⚠️ Nota Importante sobre la Configuración del Correo

Este bot viene configurado inicialmente con un correo personal utilizado durante el desarrollo.
Por esta razón, después de descargar el proyecto desde Git, es obligatorio actualizar la cuenta de correo en las actividades relacionadas con el envío y la lectura de emails.

Si este ajuste no se realiza, el bot intentará usar una cuenta que no pertenece al usuario y generará errores de autenticación.

📌 ¿Qué actividades usan correo y deben ser modificadas?

Dentro del proyecto, aparecen actividades que requieren configuración manual según el correo del usuario:

1. Actividades de Gmail (UiPath GSuite Activities)

Send Email

Get Mail Messages

Save Mail Attachments

Reply to Email

Connection / Use Connection

Estas actividades quedan enlazadas a la cuenta con la que se desarrolló el bot.


📌 Cómo cambiar la cuenta de correo en UiPath
✔️ Opción 1: Cambiar la conexión existente

Abrir UiPath Studio

Abrir el archivo Main.xaml

Seleccionar cualquier actividad de correo

En el panel derecho, localizar:

Connection → Use Connection
o
ConnectionAccountName

Presionar Manage Connections

Eliminar la conexión existente

Crear una nueva conexión con el correo del usuario

Autorizar desde Google en el navegador

Guardar los cambios

✔️ Opción 2: Crear una nueva conexión y asignarla a todas las actividades

Abrir UiPath Assistant

Ir a Preferences → Orchestrator Settings → Manage Connections

Añadir una nueva conexión Gmail

Regresar a UiPath Studio

Abrir cualquier actividad de Gmail

Seleccionar la nueva conexión desde el cuadro Connection

Repetir en todas las actividades que usen correo

<img width="712" height="173" alt="image" src="https://github.com/user-attachments/assets/33c9c4f8-b412-4e62-a70b-bda222e5e156" />

