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
  
## 5. Conclusiones 
- La Transformada de Laplace convierte ecuaciones diferenciales complejas en expresiones algebraicas más sencillas, lo que permite analizar sistemas dinámicos con mayor facilidad.
- Con la Función de Transferencia podemos crear un modelo matemático que describe cómo responde un sistema ante diferentes señales de entrada.
- Los ingenieros de control aplican estos conceptos para desarrollar y mejorar sistemas en diversas áreas, como circuitos eléctricos, mecanismos y procesos térmicos.
- Los ceros no afectan directamente la estabilidad del sistema como los polos, pero influyen en la respuesta transitoria 








