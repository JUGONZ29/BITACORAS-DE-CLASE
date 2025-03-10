# Sistemas Hidraulicos
Los sistemas de fluidos, que pueden contener líquidos o gases en movimiento, son estudiados mediante la mecánica de fluidos. Esta disciplina científica examina el comportamiento de los fluidos bajo diversas condiciones.
## Principios Fundamentales
ara crear un modelo preciso de cualquier sistema de fluidos, es esencial considerar tres principios básicos:
 - Conservación de la Masa (Ecuación de Continuidad): nos indica que el volumen del fluido en un sistema varia segun la diferencia entre el flujo de entrada y de salida 

$$ \frac{dV}{dt} = Q_{in}-Q_{out} $$
 - Conservación de la Energía (Ecuación de Bernoulli): la suma de la presion, energia cinetica y energia potencial en un punto del fluido se mantiene constante 

$$P_{1}+\frac{1}{2}\rho\upsilon_{1}^{2}+\rho gh_{1} = P_{2}+\frac{1}{2}\rho\upsilon_{2}^{2}+\rho gh_{2}+P_{perdidas} $$

# Amplificadores Operacionales
Son dispositivos electronicos fundamentales en circuitos analogicos. se utilizan para amplificar señales, realizar operaciones matematicas, diseñar sistemas de control, filtros, osciladores entre otros.
Son circuitos monoliticos los cuales tienen tres terminales: dos entradas y una salida 
## Caracteristicas
- alta ganancia de voltaje
- Alta impedancia de entrada
- Baja impedancia de salida
- Diferencial: opera con dos entradas, $V^{+}$ (no inversora) y $V^{-}$ (inversora) y la tension en ambas entradas es igual
## Configuraciones Basicas
Se puede utilizar condensadores o resistencias externas para configurar el amplificador operacional de diferentes maneras como el amplificador inversor, no inversor, seguidor de voltaje, comparador, integrador, sumador, etc. 
### Amplificador Inversor
Son ampliamente utilizados principalmente cuando se consideran señales analogicas 
Tiene menor impedancia de entrada

$$ V_{out} = -\frac{R_{f}}{R_{1}}V_{in} $$

una desventaja de esta configuracion es que la señal de entrada aplicada no debe tener ruido por muy minimo que sea, ya que un valor pequeño puede multiplicarse y reflejarse en la salida
#### ejemplo
Diseñe un amplificador inversor con una ganancia de -10 y una resistencia de entrada igual a 10kΩ.

$$ R_{f} = -A_{v}R_{1} $$

$$ R_{f}= -(-10)10k\Omega = 100k\Omega $$
### Amplificador No Inversor
A diferencia del inversor, esta configuracion cuenta con una alta impedancia
