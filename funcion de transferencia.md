# Funciones de transferencia
## 1. Introducción 
El control de sistemas es una rama que estudia cómo hacer que un sistema se comporte según lo deseamos. Usamos herramientas matemáticas como la Transformada de Laplace y la Función de Transferencia para convertir ecuaciones diferenciales complicadas en expresiones algebraicas más manejables. Esto nos facilita analizar y diseñar sistemas en campos como la mecatrónica, robótica y automatización industrial.
## 2. Definiciones claves 
> 🔑 *sistema:* Conjunto de componentes interconectados que trabajan juntos para un objetivo especifico.

> 🔑 *planta:* parte del sistema que se desea controlar

> 🔑 *proceso:* Se refiere a la serie de cambios o transformaciones que ocurren en un sistema para convertir una entrada en una salida.

> 🔑 *actuador:* Dispositivo que convierte una señal de control en una accion fisica sobre la planta

> 🔑 *lazo cerrado:* Sistema de control que usa retroalimentacion, es decir, la salida se compara con la referencia

> 🔑 *lazo abierto:* sistema de control en el cual la salida no influye en la accion de control
## 3. Transformada de Laplace
Es una herramienta matematica que permite convertir ecuaciones algebraicas en el dominio de la frecuencia. esto facilita el analisis de sistemas dinamicos, ya que en lugar de resolver ecuaciones diferenciales en el tiempo, se puede trabajar con expresiones algebraicas en s, lo que simplifica la resolucion de problemas.
Una de sus ventajas es la facilidad con la que maneja derivadas e integrales, nos permite transformar ecuaciones diferenciales en ecuaciones polinomicas. Ademas se puede obtener funciones de transferencia

$$ F(s) = \mathcal{L} \{ f(t) \} = \int_{0}^{\infty} e^{-st} f(t) dt $$

### 3.1 Ejemplo
Dada la funcion $f(t)=e^{-at}$, su transformada de Laplace es:

$$F(s)=\frac{1}{s+a}$$
## 4. Funcion de transferencia
### 4.1 Definicion
Es una herramienta fundamental para analizar y diseñar sistemas dinamicos. se utiliza para representar la relacion matematica entre la entrada y la salida de un sistema en el dominio de Laplace

$$ G(s) = \frac{Y(s)}{U(s)} $$

donde Y(s) es la salida y U(s) es la entrada del sistema, asumiendo condiciones iniciales nulas
### 4.2 forma general
la forma general de una funcion de transferencia es 

$$ G(s) = \frac{N(s)}{D(s)} $$

- N(s) es el numerador, contiene los ceros del sistema
- D(s) es el denominador, contiene los polos del sistema
#### 4.2.1 ejemplo
suponiendo un sistema masa-resorte-amortiguador

$$m\ddot{x}+b\dot{x}+kx = F(t)$$

Aplicando la transformada de Laplace (condiciones inciales en cero)

$$ ms^{2}X(s)+bsX(s)+kX(s)=F(s) $$

despejando G(s):

$$G(s)=\frac{X(s)}{F(s)} =\frac{1}{ms^{2}+bs+k}$$

### 4.3 Clasificacion 
- Estrictamente propia: si el grado del polinomio del denominador es mayor que el del numerador

$$ \frac{2}{s+2} $$

- impropia: si el grado del polinomio del numerador es mayor que el del denominador

$$ s^{2}+1 $$
- Bipropia: Cuando el grado de ambos polinomios es igual

$$ 3 $$
### 4.4 Zeros
Son los valores de *s* que hacen que la funcion de trasferencia sea igual a cero. Se obtiene al igualar a cero el numerador de la funcion. Los valores pueden ser reales o complejos y se pueden ubicar en un plano cartesiano.
Los ceros modifican la forma de la respuesta del sistema al influir en la amplitud y la fase de la señal de salida
Si estan cerca del origen, tienen un gran impacto en la dinámica del sistema.
### 4.5 Polos 
Son los valores de *s* que hacen que la funcion de transferencia se vuelva infinita. Se tiene que igualar a cero el denominador de la funcion.
#### 4.5.1 Clasificacion de los polos
se pueden clasificar en:
- Polos reales iguales

$$ s_{1,2}= 5 $$
- Polos reales diferentes

$$ s_{1} =-1, s_{2} = -6 $$
- Polos complejos conjugados

$$ s=-1\pm 2j $$

 ## 5. ejercicios

![image](https://github.com/user-attachments/assets/103d2c0f-3829-41fb-afbc-e6dfe56a66f2)


# Solución Paso a Paso

## Definición del Problema

Se tienen dos tanques o columnas abiertas, de las cuales solo una es alimentada por un caudal $Q_e$. La segunda columna recibe líquido a través de una conexión con la primera y lo libera mediante otra tubería. Ambas conexiones presentan una resistencia al flujo del caudal, denominadas $R_1$ y $R_2$. El objetivo es determinar cómo varía la altura del segundo tanque en función del caudal que ingresa en el primero.

## Análisis del Flujo

Analicemos $q_1$: Como ambos tanques están abiertos a la atmósfera, la presión en su superficie es la presión ambiente. Aplicando la ecuación de Bernoulli en ambos lados y considerando las simplificaciones del problema (como que la velocidad del fluido a ambos lados del canal es la misma), la expresión para el caudal depende únicamente de la diferencia de alturas:

$$
q_1= \frac{h_1 - h_2}{R_1}
$$

Para el caudal $q_2$, la situación es similar, con la diferencia de que no hay un tercer tanque que imponga una resistencia adicional al flujo del líquido. Por lo tanto:

$$
q_2= \frac{h_2}{R_2}
$$

## Aplicación de la Transformada de Laplace

Por otro lado, se sabe que el volumen acumulado en cada tanque depende del balance de caudales. Aplicando esta relación y realizando la transformación de Laplace, se obtienen las siguientes ecuaciones:

$$
q_e - q_1 = A_1 \cdot \frac{\partial h_1}{\partial t} \quad \Rightarrow \quad \text{Reemplazo y transformación} \quad \Rightarrow \quad Q_1(s) = \frac{H_1(s) - H_2(s)}{R_1} = Q_e(s) - A_1 \cdot s \cdot H_1(s)
$$

$$
q_1 - q_2 = A_2 \cdot \frac{\partial h_2}{\partial t} \quad \Rightarrow \quad \text{Reemplazo y transformación} \quad \Rightarrow \quad Q_2(s) = \frac{H_2(s)}{R_2} = Q_1(s) - A_2 \cdot s \cdot H_2(s)
$$

## Ejercicios de Función de Transferencia

### Ejercicio 1: Sistema de Dos Tanques en Serie

Se tienen dos tanques interconectados, donde el primero recibe un caudal de entrada $Q_e(s)$. La resistencia al flujo entre los tanques es $R_1$, y la resistencia de salida del segundo tanque es $R_2$. Obtenga la función de transferencia $H_2(s)/Q_e(s)$.

**Solución:**
A partir del balance de caudales y aplicando la transformada de Laplace:

$$
Q_1(s) = \frac{H_1(s) - H_2(s)}{R_1} = Q_e(s) - A_1 s H_1(s)
$$

$$
Q_2(s) = \frac{H_2(s)}{R_2} = Q_1(s) - A_2 s H_2(s)
$$

Despejando $H_2(s)$ en función de $Q_e(s)$:

$$
\frac{H_2(s)}{Q_e(s)} = \frac{1}{(A_1 R_1 s + 1)(A_2 R_2 s + 1)}
$$

### Ejercicio 2: Tanque con Salida Restringida

Un tanque recibe un caudal de entrada $Q_e(s)$ y descarga a través de una resistencia $R$. Determine la función de transferencia $H(s)/Q_e(s)$.

**Solución:**
El balance de caudales es:

$$
Q_e(s) - Q_s(s) = A s H(s)
$$

Dado que la salida del tanque sigue la ecuación:

$$
Q_s(s) = \frac{H(s)}{R}
$$

Sustituyendo en la ecuación de balance:

$$
Q_e(s) - \frac{H(s)}{R} = A s H(s)
$$

Despejando $H(s)/Q_e(s)$:

$$
\frac{H(s)}{Q_e(s)} = \frac{1}{A s + 1/R}
$$

 
## 6. Conclusiones 
- La Transformada de Laplace convierte ecuaciones diferenciales complejas en expresiones algebraicas más sencillas, lo que permite analizar sistemas dinámicos con mayor facilidad.
- Con la Función de Transferencia podemos crear un modelo matemático que describe cómo responde un sistema ante diferentes señales de entrada.
- Los ingenieros de control aplican estos conceptos para desarrollar y mejorar sistemas en diversas áreas, como circuitos eléctricos, mecanismos y procesos térmicos.
- Los ceros no afectan directamente la estabilidad del sistema como los polos, pero influyen en la respuesta transitoria 








