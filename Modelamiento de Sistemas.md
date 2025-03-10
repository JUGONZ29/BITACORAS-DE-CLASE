# Modelamiento de Sistemas Dinámicos
Un modelo matemático de un sistema dinámico es básicamente un conjunto de ecuaciones que describen con bastante precisión, o al menos con una buena aproximación, cómo se comporta dinámicamente el sistema. Hay que tener en cuenta que un mismo sistema puede representarse de varias maneras diferentes, lo que quiere decir que no existe un único modelo matemático, sino que hay múltiples enfoques posibles dependiendo de cómo se mire.
La dinámica de un montón de sistemas se expresa mediante ecuaciones diferenciales. Estas ecuaciones vienen de las leyes físicas que gobiernan cada sistema, como las leyes de Newton en sistemas mecánicos y las leyes de Kirchhoff en sistemas eléctricos. Conseguir un modelo matemático adecuado es una de las partes más importantes cuando se analiza cualquier sistema.


# 1. Sistemas Mecánicos
Un sistema mecánico es un conjunto de componentes diseñados para transmitir, transformar o controlar el movimiento y la energía mecánica. entre los cuales podemos encontrar los siguientes tipos de sistemas 

# 2. Definiciones
> 🔑 *Sistema dinámico:* Un sistema cuyo estado cambia con el tiempo debido a la interacción de sus elementos internos o con el entorno.

> 🔑 *Modelo matemático:* Representación de un sistema físico mediante ecuaciones matemáticas que describen su comportamiento.

> 🔑 *Ecuación diferencial:* Ecuación que relaciona una función con sus derivadas y describe la dinámica de un sistema.
## 2.1 Sistema Masa-Resorte-Amortiguador
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

## 2.2 Péndulo Simple
Un péndulo simple consta de una masa suspendida de un hilo que oscila bajo la acción de la gravedad. Se modela mediante la ecuación:
```math
\ddot{\theta} + \frac{g}{L} \sin\theta = 0
```
Donde:
- *\theta* es el ángulo de oscilación,
- *g* es la aceleración debido a la gravedad,
- *L* es la longitud del péndulo.

# 3. Ecuaciones resultantes

| Sistema | Ecuación de Movimiento |
|---------|----------------------|
| Masa-Resorte-Amortiguador | \$m \ddot{x} + c \dot{x} + kx = F(t)$ |
| Péndulo Simple | $\ddot{\theta} + \frac{g}{L} \sin\theta = 0$ |

Tabla 1. Resumen de ecuaciones de sistemas mecánicos.


# 4. Rotacionales 
En los sistemas rotacionales se ven involucradas las variables como son el torque, el desplazamiento angular y velocidad angulas. Son comunes en motores eléctricos, engranajes, volantes de inercia y sistemas de transmisión de potencia
## 4.1 Variables del sistema
Es importante destacar que las magnitudes en un sistema rotacional se pueden definir mediante tres parámetros

- Ángulo de giro * 1* es la posición angular del sistema medida en radianes
- velocidad angular *2* la rapidez con la que gira
- Aceleración angular *3* es la variación de la velocidad angular, medida en (rad/s^2)
## 4.2 Ecuaciones de movimiento en sistemas rotacionales
Utilizando la segunda Ley de Newton para estos sistemas se determina como:

- suma de los momentos de torsión
- Momento de inercia rotacional
- Aceleración angular

# 5. Ejercicios

📚 **Ejercicio 1**

![Imagen de WhatsApp 2025-03-10 a las 14 32 59_5db6b950](https://github.com/user-attachments/assets/b58881b9-747d-4167-b407-e3ef061cd431)



## Solución Paso a Paso

## Paso 1: Definir el Sistema y las Variables

- **M₁**: Masa del vehículo  
- **M₂**: Masa del remolque  
- **Kₕ**: Constante elástica del acoplamiento  
- **Bₕ**: Coeficiente de amortiguamiento del acoplamiento  
- **Bᵢ**: Coeficiente de fricción viscosa del remolque  
- **y₁(t)**: Desplazamiento del vehículo  
- **y₂(t)**: Desplazamiento del remolque  
- **f(t)**: Fuerza aplicada al vehículo  

---

## Paso 2: Establecer las Ecuaciones de Movimiento

Usando la segunda ley de Newton, se pueden escribir las ecuaciones de movimiento para el vehículo y el remolque.

### Para el vehículo (M₁):

```math
M_1 \ddot{y}_1 (t) = f(t) - K_h (y_1 (t) - y_2 (t)) - B_h (\dot{y}_1 (t) - \dot{y}_2 (t))
```

### Para el remolque (M₂):

```math
M_2 \ddot{y}_2 (t) = K_h (y_1 (t) - y_2 (t)) + B_h (\dot{y}_1 (t) - \dot{y}_2 (t)) - B_i \dot{y}_2 (t)
```

---

## Paso 3: Simplificar las Ecuaciones

Combinamos términos para simplificar las ecuaciones.

### Para el vehículo (M₁):

```math
M_1 \ddot{y}_1 (t) = f(t) - K_h y_1 (t) + K_h y_2 (t) - B_h \dot{y}_1 (t) + B_h \dot{y}_2 (t)
```

### Para el remolque (M₂):

```math
M_2 \ddot{y}_2 (t) = K_h y_1 (t) - K_h y_2 (t) + B_h \dot{y}_1 (t) - (B_h + B_i) \dot{y}_2 (t)
```

---

## Respuesta Final

El sistema de ecuaciones diferenciales que representa el movimiento del vehículo y el remolque es:

### Para el vehículo (M₁):

```math
M_1 \ddot{y}_1 (t) = f(t) - K_h y_1 (t) + K_h y_2 (t) - B_h \dot{y}_1 (t) + B_h \dot{y}_2 (t)
```

### Para el remolque (M₂):

```math
M_2 \ddot{y}_2 (t) = K_h y_1 (t) - K_h y_2 (t) + B_h \dot{y}_1 (t) - (B_h + B_i) \dot{y}_2 (t)
```

Estas ecuaciones describen el comportamiento dinámico del sistema vehículo-remolque bajo la influencia de la fuerza aplicada `f(t)`. 

📚 **Ejercicio 2**

![Imagen de WhatsApp 2025-03-10 a las 14 38 14_14743131](https://github.com/user-attachments/assets/4a29b56d-ace7-4831-baaf-74a01d857f23)

### Dinamica del sistema
![Imagen de WhatsApp 2025-03-10 a las 14 38 14_5f5de316](https://github.com/user-attachments/assets/3ca24e62-1956-496e-bb59-232a1a11a1cc)

### Para la ecuacion 
![Imagen de WhatsApp 2025-03-10 a las 14 38 14_ebe8fe0a](https://github.com/user-attachments/assets/9e9aea27-89ce-480f-91f7-25f251bb9978)

# 6. Conclusiones
- El análisis de sistemas dinámicos mediante ecuaciones diferenciales y funciones de transferencia nos ayuda a ver cómo estos sistemas reaccionan a diversos estímulos. Los sistemas que contienen masa, un resorte y un amortiguador (así como sus versiones rotacionales) se pueden describir matemáticamente a través de ecuaciones diferenciales de segundo grado. Al solucionar estas ecuaciones, podemos averiguar si el sistema es estable y medir su rendimiento en diferentes situaciones. Este método matemático es clave para crear sistemas de control automático que funcionan bien.

- El modelamiento de sistemas que cambian con el tiempo ayuda a anticipar cómo funcionarán sistemas mecánicos usando ecuaciones que involucran derivadas. Entender estas ecuaciones es clave para el estudio y la creación de sistemas en el campo de la ingeniería.

- Después de tener un modelo matemático, es posible hacer simulaciones para anticipar cómo reaccionará el sistema en diferentes situaciones. Esto es vital en el desarrollo de sistemas de control, porque facilita la adopción de métodos para optimizar la estabilidad, el desempeño y la efectividad.

# 7. Referencias
- Ogata, K. (2010). *Ingeniería de Control Moderna*. Pearson.
- Dorf, R. C., & Bishop, R. H. (2017). *Sistemas de control moderno*. Pearson.
