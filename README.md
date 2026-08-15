# Cierre de gastos

Web app estatica para registrar gastos compartidos, liquidaciones, estados de cuenta y sincronizacion opcional con Google Sheets mediante Apps Script.

Ahora tambien funciona como PWA: incluye manifest, iconos y service worker para instalacion desde el navegador y uso con cache local.

## GitHub Pages

Activa Pages en:

`Settings > Pages > Build and deployment > Source: Deploy from a branch > Branch: main > /root`

URL esperada:

https://42571634-gif.github.io/gastos_compartidos/

## Google Sheets

La URL de Apps Script se pega desde la interfaz de la app. No esta hardcodeada en el repositorio para evitar publicar el token.

La copia local queda como referencia. Al abrir la app con una URL configurada se trae el estado de Google Sheets. Cada gasto, pago de liquidacion o borrado sube automaticamente el estado completo con `replaceState`, el mismo flujo que usa el boton "Subir copia local"; la lectura desde la nube queda para el inicio de la app o el boton "Traer datos" para evitar pisar cambios locales con una lectura remota vieja.
