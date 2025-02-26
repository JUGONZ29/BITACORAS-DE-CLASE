# Modelamiento de Sistemas Dinámicos
Un modelo matemático de un sistema dinámico es básicamente un conjunto de ecuaciones que describen con bastante precisión, o al menos con una buena aproximación, cómo se comporta dinámicamente el sistema. Hay que tener en cuenta que un mismo sistema puede representarse de varias maneras diferentes, lo que quiere decir que no existe un único modelo matemático, sino que hay múltiples enfoques posibles dependiendo de cómo lo mires.
La dinámica de un montón de sistemas se expresa mediante ecuaciones diferenciales. Estas ecuaciones vienen de las leyes físicas que gobiernan cada sistema, como las leyes de Newton en sistemas mecánicos y las leyes de Kirchhoff en sistemas eléctricos. Conseguir un modelo matemático adecuado es una de las partes más importantes cuando analizas cualquier sistema.

## 2. Definiciones
> 🔑 *Sistema dinámico:* Un sistema cuyo estado cambia con el tiempo debido a la interacción de sus elementos internos o con el entorno.

> 🔑 *Modelo matemático:* Representación de un sistema físico mediante ecuaciones matemáticas que describen su comportamiento. 

> 🔑 *Ecuación diferencial:* Ecuación que relaciona una función con sus derivadas y describe la dinámica de un sistema.

## 3. Ejemplos de Sistemas Mecánicos

### 3.1. Sistema Masa-Resorte-Amortiguador
Este sistema está compuesto por una masa unida a un resorte y un amortiguador. Se modela con la ecuación diferencial:
```math
m \ddot{y} + c \dot{y} + ky = F(t)
```
Donde:
- *m* es la masa,
- *c* es la constante de amortiguamiento,
- *k* es la constante del resorte,
- *y* es el desplazamiento,
- *F(t)* es la fuerza aplicada.

### 3.2. Péndulo Simple
Un péndulo simple consta de una masa suspendida de un hilo que oscila bajo la acción de la gravedad. Se modela mediante la ecuación:
```math
\ddot{\theta} + \frac{g}{L} \sin\theta = 0
```
Donde:
- *\theta* es el ángulo de oscilación,
- *g* es la aceleración debido a la gravedad,
- *L* es la longitud del péndulo.

## 4. Ecuaciones resultantes

| Sistema | Ecuación de Movimiento |
|---------|----------------------|
| Masa-Resorte-Amortiguador | \$m \ddot{x} + c \dot{x} + kx = F(t)$ |
| Péndulo Simple | $\ddot{\theta} + \frac{g}{L} \sin\theta = 0$ |

Tabla 1. Resumen de ecuaciones de sistemas mecánicos.

## 5. Ejercicios

# Ejercicios
📚 **Ejercicio 1**
Determine la ecuación de movimiento de un sistema masa-resorte con *m = 3 kg*, *c = 2 Ns/m* y *k = 4 N/m*.

📚 **Ejercicio 2**
Simule la respuesta de un péndulo simple en MATLAB para *L = 2 m* y un ángulo inicial de 10 grados.

## 6. Conclusiones
El modelamiento de sistemas dinámicos permite predecir el comportamiento de sistemas mecánicos mediante ecuaciones diferenciales. Comprender estas ecuaciones es fundamental para el análisis y diseño de sistemas en ingeniería.

## 7. Referencias
- Ogata, K. (2010). *Ingeniería de Control Moderna*. Pearson.
- Dorf, R. C., & Bishop, R. H. (2017). *Sistemas de control moderno*. Pearson.


