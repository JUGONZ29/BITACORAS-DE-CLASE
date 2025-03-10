# Sistemas Eléctricos
Los sistemas hidráulicos se utilizan en diversas aplicaciones industriales y mecánicas debido a su capacidad para transmitir grandes fuerzas con precisión. Funcionan mediante el uso de fluidos incompresibles para generar y controlar energía mecánica. Se emplean en maquinaria pesada, sistemas de frenos, actuadores y en la industria aeroespacial.
## 1. Definiciones
> 🔑 *Presion:* Es la fuerza ejercida por unidad de area en un fluido

> 🔑 *Caudal:* Volumen de fluido que pasa por una seccion transversal por unidad de tiempo

> 🔑 *Actuador hidraulico:* Dispositivo que convierte la energia hidraulica en movimiento mecanico

> 🔑 *Valvula de control:* Regula la direccion, presion y flujo del fluido en el sistema 
## 2. Principios Fundamentales
Para crear un modelo preciso de cualquier sistema de fluidos, es esencial considerar tres principios básicos:
 - Conservación de la Masa (Ecuación de Continuidad): nos indica que el volumen del fluido en un sistema varia segun la diferencia entre el flujo de entrada y de salida 

$$ \frac{dV}{dt} = Q_{in}-Q_{out} $$
 - Conservación de la Energía (Ecuación de Bernoulli): la suma de la presion, energia cinetica y energia potencial en un punto del fluido se mantiene constante 

$$P_{1}+\frac{1}{2}\rho\upsilon_{1}^{2}+\rho gh_{1} = P_{2}+\frac{1}{2}\rho\upsilon_{2}^{2}+\rho gh_{2}+P_{perdidas} $$

# Amplificadores Operacionales
Son dispositivos electronicos fundamentales en circuitos analogicos. se utilizan para amplificar señales, realizar operaciones matematicas, diseñar sistemas de control, filtros, osciladores entre otros.
Son circuitos monoliticos los cuales tienen tres terminales: dos entradas y una salida 
## 1. Caracteristicas
- alta ganancia de voltaje
- Alta impedancia de entrada
- Baja impedancia de salida
- Diferencial: opera con dos entradas, $V^{+}$ (no inversora) y $V^{-}$ (inversora) y la tension en ambas entradas es igual
## 2. Configuraciones Basicas
Se puede utilizar condensadores o resistencias externas para configurar el amplificador operacional de diferentes maneras como el amplificador inversor, no inversor, seguidor de voltaje, comparador, integrador, sumador, etc. 
### 2.1 Amplificador Inversor
Son ampliamente utilizados principalmente cuando se consideran señales analogicas 
Tiene menor impedancia de entrada

$$ V_{out} = -\frac{R_{f}}{R_{1}}V_{in} $$

una desventaja de esta configuracion es que la señal de entrada aplicada no debe tener ruido por muy minimo que sea, ya que un valor pequeño puede multiplicarse y reflejarse en la salida
#### 2.1.1 Ejemplo
Diseñe un amplificador inversor con una ganancia de -10 y una resistencia de entrada igual a 10kΩ.

$$ R_{f} = -A_{v}R_{1} $$

$$ R_{f}= -(-10)10k\Omega = 100k\Omega $$
### 2.2 Amplificador No Inversor
A diferencia del inversor, esta configuracion cuenta con una alta impedancia de entrada

$$ A_{v}=1+\frac{R_{f}}{R_{1}} $$
#### 2.2.1 Ejemplo
Si $R_{f} = 10k\Omega$ y $R_{1} = 2k\Omega $, la ganancia sera:

$$ A_{v}=1+\frac{10k}{2k} = 6 $$ 

Si la entrada es de 1V, la salida sera de 6V
## 3. Conclusiones 
- Los sistemas hidraulicos permiten la transmision eficiente de energia a traves de fluidos incompresibles. son ampliamente utilizados en sistemas de control y maquinaria industrial para general movimiento y fuerza controlada
- Los amplificadores operacionales son fundamentales en sistemas electronicos y de control. las diversas configuraciones permiten el preocesamiento de señales y la implementacion de operaciones matematicas.
- Los amplificadores inversor y no inversor son esenciales para amplificar señales sin causar distorsión significativa en diversas aplicaciones. Por su parte, el integrador juega un papel clave en el procesamiento de señales y sistemas de control, permitiendo realizar operaciones matemáticas fundamentales en circuitos electrónicos avanzados.
## 4. Referencias
Ogata, K. (2010). Ingeniería de Control Moderna. Pearson.


