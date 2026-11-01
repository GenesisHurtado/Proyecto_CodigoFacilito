---
name: marca-yoga
description: Diseño de marca del estudio de yoga de Andrea. Úsala al crear o cambiar cualquier pantalla, componente, color, tipografía o texto de la app.
---

# Marca: estudio de yoga

Personalidad: calmada, cercana, clara. Nada de adornos ni urgencia.

## Colores (variables CSS; modo oscuro automático con prefers-color-scheme)
| Variable | Claro | Oscuro | Uso |
|---|---|---|---|
| --fondo | #EEF3EE | #141A17 | fondo verde salvia muy claro |
| --tarjeta | #FCFDFB | #1D2521 | tarjetas casi blancas, borde suave |
| --texto | #1F2A25 | #E6EDE8 | texto |
| --acento | #1F7A78 | #4FB3AF | único acento verde azulado: botones principales |
| --espera | #6B4FA3 | #B7A0E6 | todo lo de lista de espera |
| --llena | #B7791F | #E3B04B | etiqueta "clase llena" |
| --cancela | #A34848 | #E08A8A | rojo apagado: cancelar |

## Tipografía
- Young Serif para títulos y números grandes. Figtree para el texto. Fallback: Georgia / system-ui.
- Sin mayúsculas sostenidas, sin etiquetas decorativas.

## Layout y componentes
- Una columna de máximo 640 px, mobile-first. Botones de mínimo 44 px de alto, un solo botón de acción por clase.
- Estados con etiqueta de texto, nunca solo color.

## Texto
- Español simple, oración normal, verbos claros. Una acción mantiene su nombre en todo el flujo ("Reservar" → "Reservado.").
- Estados vacíos explican qué hacer. Los errores dicen qué pasó y cómo resolverlo, sin disculpas.

## Accesibilidad
Foco visible, contraste suficiente, respetar prefers-reduced-motion, sin animaciones innecesarias.
