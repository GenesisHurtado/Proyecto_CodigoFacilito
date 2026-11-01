# Reservas del estudio de yoga

Abre `index.html` en el navegador (o súbelo a GitHub Pages). Usa las pestañas Alumna, Andrea e Instructora. Los datos de ejemplo se reinician al recargar.

Flujo para probar: en Alumna elige "Camila" → reserva una clase → en "Vinyasa tarde" (llena) entra a lista de espera → cancela con otra alumna → en Andrea abre el aviso de WhatsApp de quien fue promovida.

Pruebas: `node tests/reglas.test.js`

## Decisiones
Se descuenta al quedar inscrita; cancelar con 12 h o más devuelve; sin saldo no se reserva ni se entra a espera; paquetes sin vencimiento; clase cancelada devuelve a todas.

## Mejoras futuras
Guardar datos de forma permanente, recordatorios automáticos, pagos, vencimiento de paquetes, aviso por WhatsApp API.
