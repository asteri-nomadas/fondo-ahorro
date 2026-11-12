# Fondo de Ahorro

Calculadora interactiva y accesible para proyectar un fondo de ahorro personal.

**En línea:** https://asteri-nomadas.github.io/fondo-ahorro/

Toda la página está en `index.html`. Carga Chart.js y la fuente Inter desde CDN y hace todos los cálculos en el navegador. Las librerías para el PDF (jsPDF) y el Excel (ExcelJS) solo se descargan al pulsar su botón.

## Qué incluye

### Calculadora
- Al inicio, un bloque destacado reúne el título, la introducción y, justo debajo, los seis indicadores del resultado:
  - saldo final después de ISR;
  - valor en pesos de hoy;
  - total depositado;
  - intereses ganados;
  - retención de ISR;
  - ganancia real.
- En ese mismo bloque están los botones «Cambiar supuestos ↓» (lleva a los campos editables) y los de descargar o imprimir el reporte.
- Al bajar más allá de los indicadores, aparece fija arriba una barra compacta con los mismos números, que se actualiza al cambiar cualquier supuesto:
  - muestra los seis indicadores en pantallas anchas, y menos (empezando por el saldo final) en pantallas angostas o con el texto agrandado, para que ningún número se corte;
  - al hacer clic en ella se vuelve al resultado completo;
  - desaparece al regresar arriba y no se imprime.
- Proyección mes a mes del plan: $100,000 iniciales y $10,000 mensuales durante 10 años. Todos los supuestos se pueden editar.
- Los campos en pesos muestran separadores de miles (100,000) al escribir.
- Cada campo numérico tiene botones − / + grandes (y responde a las flechas ↑/↓ del teclado).
- El texto de introducción y la nota del tope cambian según los supuestos y el instrumento elegido.
- Escenarios de tasa (bajo, base y alto).
- Cuatro estrategias completas:
  - solo Mifel;
  - Mifel + un segundo banco con IPAB;
  - Mifel + CETES;
  - todo en CETES.

### Datos actualizados a noviembre de 2026
- Inflación de 3.62% (INEGI, 1ª quincena de octubre).
- Tasa objetivo de Banxico de 6.25% (decisión del 5 de noviembre). CETES a 28 días se toma como ≈ 6.25%; la tasa de cada subasta semanal se confirma en cetesdirecto.
- Retención de ISR de 0.90% anual sobre el saldo que exceda 5 UMA (Ley de Ingresos 2026).
- Tope de $500,000 de la Cuenta Digital Mifel: arriba de esa cantidad el saldo no genera intereses.

### Comparativo de 20 instrumentos
- Para cada uno:
  - tasa y tipo de tasa (anunciada o rendimiento pasado);
  - tasa real;
  - saldo final;
  - calificación de riesgo (publicada o estimada);
  - riesgo global de 1 a 5;
  - protección;
  - requisito.
- Gráfica de tasas con la inflación marcada.
- Gráfica de límites, en escala logarítmica, con dos barras por instrumento y el saldo final del plan marcado:
  - hasta qué saldo genera rendimiento (por ejemplo, Mifel: $500,000);
  - hasta qué saldo está protegido (IPAB ≈ $3.5 M, PROSOFIPO ≈ $221 mil).
- Un resumen indica qué instrumentos generan rendimiento y protegen todo el saldo del plan.
- Mapa de cuadrantes con ejes seleccionables:
  - por defecto, riesgo global frente a tasa real;
  - otras opciones: tasa anual, saldo final, saldo en pesos de hoy, % del saldo protegido y % del saldo que genera rendimiento;
  - el cuadrante mejor en ambos ejes aparece sombreado y un resumen lista qué instrumentos caen ahí.
- Tabla que explica las diferencias entre los tipos de protección: IPAB, PROSOFIPO, fondo de inversión, Gobierno federal y sin seguro.
- Cada instrumento enlaza a su sitio oficial: en la columna «Fuente» y al hacer clic en su barra de la gráfica.

### Tablas
- Se ordenan al hacer clic en el encabezado de cada columna; otro clic invierte el orden.
- Búsqueda y filtros por protección y tipo de tasa en la tabla de instrumentos.
- Cuando una tabla se muestra como tarjetas (sin encabezados), aparece un menú «Ordenar por» en su lugar.
- Se adaptan a cualquier ancho de ventana: si una tabla no cabe completa, se muestra como tarjetas con cada dato rotulado.

### Exportar e imprimir
- **Descargar reporte en PDF**: reporte de 5 páginas generado en el navegador. Incluye:
  - supuestos y resultados;
  - ambas gráficas;
  - escenarios y estrategias;
  - comparativo de instrumentos;
  - resumen anual;
  - fuentes con enlaces.
- **Descargar Excel**: libro de 6 hojas con los valores actuales de la calculadora:
  - Supuestos, con las celdas editables en amarillo;
  - Calendario mensual y Resumen, con fórmulas reales de Excel que se recalculan al cambiar un supuesto;
  - Escenarios y estrategias;
  - Instrumentos, con enlace al sitio oficial;
  - Fuentes.
- **Imprimir** (o Ctrl/Cmd+P): versión para papel con:
  - el resultado al inicio, justo debajo de la introducción;
  - colores claros;
  - tablas completas;
  - gráficas ajustadas;
  - sin cortes a media sección;
  - las direcciones de las fuentes escritas completas.
- Fuera de claude.ai, las descargas se hacen directo con el navegador. Dentro de claude.ai usan el permiso de descargas del visor, que pide confirmar cada archivo.

### Accesibilidad para baja visión
- Texto base de 18 px y alto contraste.
- Contornos de foco visibles y botones de al menos 48 px.
- La información nunca depende solo del color.
- Panel abajo a la derecha con:
  - tamaño del texto (A−/A+, de 90% a 200%);
  - selector de colores: Clásico (predeterminado), aptos para daltonismo, Alto contraste o Cálido;
  - selector de tema: Claro (predeterminado), Automático u Oscuro.
- Efectos al pasar el cursor sobre enlaces, botones y campos.
- La barra compacta del resultado es solo visual: los lectores de pantalla leen los indicadores una vez, en el bloque inicial. Los enlaces a cada sección dejan el título visible debajo de la barra.
- Sin animaciones si el sistema pide reducir el movimiento.

### Celular
- Los ajustes se pliegan en un botón «Aa Ajustes».
- Las gráficas usan etiquetas cortas.
- No hay desplazamiento horizontal ni con el texto al 200%.

## Fuentes

Solo se usan fuentes oficiales o documentales:
- INEGI.
- Banxico.
- cetesdirecto.
- IPAB y PROSOFIPO.
- Los términos y sitios oficiales de cada institución.
- La Ley de Ingresos 2026, citada en notas fiscales.

Cada sección enlaza a su fuente, y la lista completa, con fechas, está al final de la página. Las tasas de algunas cuentas se recopilaron en junio de 2026; conviene confirmarlas con cada institución.

## Ver la página en tu computadora

```bash
python3 -m http.server 8766
```

Después abre http://localhost:8766/ en el navegador.

---

Este resumen es informativo y no es una recomendación de un asesor financiero.
