# Sistemas de Primer Orden
Los sistemas de primer orden son aquellos cuya dinámica puede describirse con una ecuación diferencial de primer grado. Estos sistemas tienen una sola derivada en su ecuación de movimiento y presentan una respuesta exponencial ante una entrada.

## 1. Introducción a los Sistemas de Primer Orden
Un sistema de primer orden se modela matemáticamente mediante una ecuación diferencial de la forma:
```math
\tau \frac{d y(t)}{dt} + y(t) = K u(t)
```
donde:
- *y(t)* es la salida del sistema,
- *u(t)* es la entrada,
- *K* es la ganancia,
- tau: es la constante de tiempo.


Estos sistemas son comunes en circuitos eléctricos (RC), sistemas térmicos y sistemas mecánicos con amortiguamiento alto.

## 2. Definiciones
> 🔑 *Sistema de primer orden:* Aquel cuya ecuación diferencial es de primer grado y describe su dinámica con una sola constante de tiempo.
> 
> 🔑 *Constante de tiempo (tau):* Mide la rapidez con la que el sistema responde a una entrada.
> 
> 🔑 *Respuesta transitoria:* Parte de la respuesta que desaparece con el tiempo.
> 
> 🔑 *Respuesta en estado estable:* Comportamiento final del sistema cuando el tiempo tiende a infinito.

## 3. Ejemplos de Sistemas de Primer Orden

### 3.1. Circuito RC
Un circuito de resistencia y capacitancia (RC) tiene la ecuación diferencial:
```math
RC \frac{dV}{dt} + V = V_{fuente}
```
donde:
- *R* es la resistencia,
- *C* es la capacitancia,
- *V* es el voltaje del condensador,
- *V_{fuente}* es la entrada.

### 3.2. Sistema Mecánico con Fricción
Un bloque deslizante con fricción viscosa tiene la ecuación:
```math
m \frac{dv}{dt} + b v = F
```
donde:
- *m* es la masa del bloque,
- *b* es el coeficiente de fricción viscosa,
- *v* es la velocidad,
- *F* es la fuerza aplicada.

## 4. Ejemplos
💡 **Ejemplo 1:**
Si un circuito RC tiene *R = 1 k\Omega* y *C = 1 \muF*, la constante de tiempo es:
```math
\tau = RC = (1k)(1\mu) = 1 ms
```

💡 **Ejemplo 2:**
Para un sistema mecánico con *m = 5 kg* y *b = 10 Ns/m*, la constante de tiempo es:
```math
\tau = \frac{m}{b} = \frac{5}{10} = 0.5 s
```

## 5. Tablas

💡 **Ejemplo 3:**

| Sistema | Ecuación de Movimiento |
|---------|----------------------|
| Circuito RC | $RC \frac{dV}{dt} + V = V_{\text{fuente}}$ |
| Sistema Mecánico con Fricción | $m \frac{dv}{dt} + b v = F$ |

Tabla 1. Resumen de ecuaciones de sistemas de primer orden.

## 6. Ejercicios

## Definición del Problema

### **Ejercicio 1: Sistema de Control de Temperatura en un Horno**  

La ecuación diferencial del sistema es:

$$
C \frac{dT}{dt} + \frac{T}{R} = P(t)
$$

Aplicamos la Transformada de Laplace suponiendo condiciones iniciales nulas:

$$
C s T(s) + \frac{T(s)}{R} = P(s)
$$

Factorizamos $T(s)$:

$$
T(s) \left( C s + \frac{1}{R} \right) = P(s)
$$

Despejamos la función de transferencia:

$$
G(s) = \frac{T(s)}{P(s)} = \frac{1}{C s + \frac{1}{R}}
$$

La constante de tiempo es $\tau = C R$. Si $P(t) = 100 u(t)$, en el dominio de Laplace:

$$
P(s) = \frac{100}{s}
$$

La salida en el dominio de Laplace es:

$$
T(s) = \frac{100 R}{s} \cdot \frac{1}{C s + 1}
$$

Transformada inversa:

$$
T(t) = 100 R \left( 1 - e^{-t / (C R)} \right)
$$

---

### **Ejercicio 2: Sistema de Suspensión de un Vehículo**  

La ecuación diferencial es:

$$
M \frac{dx}{dt} + Bx = F(t)
$$

Aplicamos la Transformada de Laplace suponiendo condiciones iniciales nulas:

$$
M s X(s) + B X(s) = F(s)
$$

Factorizamos $X(s)$:

$$
X(s) \left( M s + B \right) = F(s)
$$

Despejamos la función de transferencia:

$$
G(s) = \frac{X(s)}{F(s)} = \frac{1}{M s + B}
$$

La constante de tiempo es $\tau = M / B$. Si $F(t) = 500 u(t)$, en el dominio de Laplace:

$$
F(s) = \frac{500}{s}
$$

La salida en el dominio de Laplace es:

$$
X(s) = \frac{500}{B} \cdot \frac{1}{s} \cdot \frac{1}{1 + \frac{M}{B}s}
$$

Transformada inversa:

$$
x(t) = \frac{500}{B} \left( 1 - e^{-t / (M/B)} \right)
$$


## 7. Conclusiones
Los sistemas de primer orden tienen una dinámica caracterizada por una respuesta exponencial. La constante de tiempo determina la velocidad de respuesta del sistema, siendo un concepto clave en el diseño y análisis de sistemas dinámicos.

## 8. Referencias
- Ogata, K. (2010). *Ingeniería de Control Moderna*. Pearson.
- Dorf, R. C., & Bishop, R. H. (2017). *Sistemas de control moderno*. Pearson.

