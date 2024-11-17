# Operaciones en el Espacio de Estados

Este documento detalla cómo realizar operaciones comunes en el espacio de estados, desde la conversión entre funciones de transferencia y espacio de estados, hasta las diferentes formas canónicas más utilizadas en control.

---

## Espacio de Estados a partir de Función de Transferencia

Considerando una función de transferencia de la forma:
\[
G(s) = \frac{N(s)}{D(s)}
\]
Es posible representar dicha función de transferencia en diferentes formas de espacio de estados clásicas.

En control, se utilizan ciertas formas de espacio de estados que pueden facilitar el análisis o diseño de sistemas y controladores.

---

## Formas de Espacio de Estados

Las formas de espacio de estados más utilizadas son:
- **Forma canónica controlable**
- **Forma canónica observable**
- **Forma canónica diagonal (o de Jordan)**

---

### Forma Canónica Controlable

Dada una función de transferencia:
![](https://github.com/andres14guevara/APUNTES-3-corte-semana-13-1/blob/main/imagen%201-2apuntes..png)

Es posible obtener la forma canónica controlable organizando las matrices de la siguiente manera:
![](https://github.com/andres14guevara/APUNTES-3-corte-semana-13-1/blob/main/imagen%202-2apuntes..png)

---

### Forma Canónica Observable

Dada una función de transferencia:
![](https://github.com/andres14guevara/APUNTES-3-corte-semana-13-1/blob/main/imagen%203-2apuntes..png)

La forma canónica observable se puede construir organizando las matrices como:
![](https://github.com/andres14guevara/APUNTES-3-corte-semana-13-1/blob/main/imagen%204-2apuntes..png)

---

### Forma Canónica Diagonal

Si se conocen los polos de la función de transferencia y todos los polos son diferentes, se puede usar la forma canónica diagonal. Esta forma está estructurada como:
_**Espacio para subir una imagen aquí**_

---

## Raíces del Polinomio Característico

Para calcular los polos en el espacio de estados, se utiliza el polinomio característico:

\[
|zI - A| = 0
\]

Esto se puede resolver utilizando el cálculo del determinante por cofactores:
_**Espacio para subir una imagen aquí**_

---

## Conversión de Espacio de Estados a Función de Transferencia

Dado el sistema en espacio de estados:

\[
x(k+1) = A \cdot x(k) + B \cdot u(k)
\]
\[
y(k) = C \cdot x(k) + D \cdot u(k)
\]

Para convertir este sistema a su función de transferencia:

1. **Transformada Z**:
   \[
   z \cdot X(z) = A \cdot X(z) + B \cdot U(z)
   \]

2. **Reorganizar**:
   \[
   (zI - A) \cdot X(z) = B \cdot U(z)
   \]

3. **Resolver para \( X(z) \)**:
   \[
   X(z) = (zI - A)^{-1} \cdot B \cdot U(z)
   \]

4. **Obtener la salida \( Y(z) \)**:
   \[
   Y(z) = C \cdot X(z) + D \cdot U(z)
   \]

5. **Sustituir \( X(z) \)**:
   \[
   Y(z) = C \cdot (zI - A)^{-1} \cdot B \cdot U(z) + D \cdot U(z)
   \]

6. **Forma final**:
   \[
   G(z) = \frac{Y(z)}{U(z)} = C \cdot (zI - A)^{-1} \cdot B + D
   \]

---

## Notas Adicionales

- Las formas canónicas (controlable, observable, diagonal) permiten analizar y diseñar controladores de manera más eficiente.
- La conversión entre funciones de transferencia y espacio de estados es fundamental para modelar sistemas dinámicos en diversos entornos.

### Espacios Reservados para Imágenes

Reemplaza los espacios etiquetados como _**Espacio para subir una imagen aquí**_ con tus diagramas o explicaciones gráficas.

---

### Autor

_Agrega aquí el nombre o equipo que desarrolla este contenido._
