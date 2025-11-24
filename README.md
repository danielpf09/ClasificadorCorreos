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
