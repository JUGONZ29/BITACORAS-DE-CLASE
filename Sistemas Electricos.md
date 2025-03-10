# Sistemas Electricos 
Los sistemas eléctricos juegan un papel esencial en el desarrollo de circuitos para control automático y aplicaciones electrónicas. Para comprender su comportamiento, utilizamos ecuaciones diferenciales que describen cómo varían los voltajes y corrientes a lo largo del tiempo. En este texto, nos enfocaremos en el modelamiento de sistemas RLC (resistencia-inductancia-capacitancia)
## 1. Variables fundamentales
- Voltaje
- Corriente
- Resistencia
- Inductancia
- Capacitancia
## 2. Leyes basicas de los sistemas electricos
- ley de Ohm: Establece la relacion entre voltaje (V), corriente (I) y resistencia (R)

 $$ V = I*R $$
- Ley de Kirchhoff de Corrientes (KCL): Establece la suma de corrientes que entran a un nodo debe ser igual a la suma de las corrientes que salen

 $$ \sum_{}^{}I=0 $$
- Ley de Kirchhoff de voltaje (KVL): Establece que la suma de los voltajes en un lazo cerrado debe ser cero

$$ \sum_{}^{}V=0 $$
## 3. Redes RLC
los circuitos en redes RLC esta conformados por resistencias, capacitores e inductancias. se utilizan en filtros, osciladores y regulaciones de energia

### 3.1 Circuito RLC serie
Un circuito serie ofrece un unico camino por el cual la corriente puede fluir

![image](https://github.com/user-attachments/assets/4f314a98-ff75-4336-aa9e-d7100a515b51)

La corriente total en este tipo de circuitos es igual en cada uno de sus componentes

$$ I_{T}=I_{R}+I_{L}+I_{C} $$

### 3.2 Circuito RLC paralelo

![image](https://github.com/user-attachments/assets/6e58af20-89e7-49e5-b6a1-8c35abec4116)

El voltaje total en este tipo de circuitos es igual en cada uno de sus componentes

$$ V_{T}=V_{R}+V_{L}+V_{C} $$

### 4. Ejercicios
### 5. Conclusiones
El modelamiento de sistemas eléctricos ayuda a predecir su comportamiento y respuesta ante diferentes entradas. Los circuitos RLC, que son de segundo orden, tienen similitudes con los sistemas mecánicos, lo que permite un análisis más completo. Usando las leyes de Kirchhoff y ecuaciones diferenciales, es posible diseñar y entender circuitos en control automático y electrónica. Este enfoque no solo mejora la comprensión teórica, sino que también facilita soluciones prácticas en ingeniería.
### 6. Referencias
Dorf, R. C., & Bishop, R. H. (2011). Sistemas de Control Automático. Prentice Hall.
