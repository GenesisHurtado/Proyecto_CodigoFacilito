# Spec 001: Reservar con cupo, lista de espera y promoción automática

## Problema
Andrea controla cupos y paquetes con tarjetas de papel. Las clases de la tarde se llenan (12), quien llega sin lugar se va molesta y no hay lista de espera. Las alumnas discuten cuántas clases les quedan y no se puede comprobar.

## Diseño de la solución
- Reservar: si hay cupo y saldo ≥ 1, la alumna queda inscrita y se descuenta 1 clase (se registra −1 en el historial).
- Clase llena: el botón pasa a "Entrar a lista de espera". En espera no se descuenta nada; se exige saldo ≥ 1 para entrar.
- Cancelar: con 12 h o más de anticipación se devuelve la clase (+1); con menos, no. Salir de la lista de espera no cuesta nada.
- Promoción: al liberarse un lugar, la primera en espera con saldo pasa a inscrita, se descuenta 1 y se crea un aviso de WhatsApp listo para ella. Si no tiene saldo, se salta a la siguiente.
- Clase cancelada: se devuelve 1 clase a cada inscrita y se crea un aviso por inscrita y por cada alumna en espera.
- Fuera de alcance: pagos, vencimiento de paquetes, recordatorios automáticos.

## Criterios de aceptación
1. Con una clase de 12 inscritas, 20 intentos de reserva más dejan inscritas = 12 y las demás en espera en orden, sin cambiar su saldo.
2. Reservar con lugar descuenta exactamente 1 y agrega un movimiento −1; con saldo 0 no reserva y muestra "No tienes clases disponibles".
3. Cancelar con 12 h o más devuelve 1 clase (+1 en historial); con menos de 12 h no devuelve nada.
4. Al cancelar una inscrita de una clase llena, la primera en espera con saldo queda inscrita, se le descuenta 1 y se crea 1 aviso suyo con enlace de WhatsApp; inscritas nunca supera 12.
5. Cancelar una clase devuelve 1 clase a cada inscrita y crea un aviso por cada inscrita y en espera.

## Verificación
`node tests/reglas.test.js` cubre los 5 criterios.
