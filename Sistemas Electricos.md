# Sistemas Electricos 
Los sistemas eléctricos juegan un papel esencial en el desarrollo de circuitos para control automático y aplicaciones electrónicas. Para comprender su comportamiento, utilizamos ecuaciones diferenciales que describen cómo varían los voltajes y corrientes a lo largo del tiempo. En este texto, nos enfocaremos en el modelamiento de sistemas RLC (resistencia-inductancia-capacitancia)
## 1. Definiciones 
>🗝️ *Voltaje:* Es la diferencia de potencial eléctrico entre dos puntos en un circuito. Se mide en voltios (V) y representa la "fuerza" que impulsa la corriente eléctrica.

>🗝️*Corriente:* Es el flujo de cargas eléctricas a través de un conductor en un circuito. Se mide en amperios (A) y depende del voltaje y la resistencia del sistema.

>🗝️*Resistencia:* Es la oposición que presenta un material al paso de la corriente eléctrica. Se mide en ohmios (Ω) y su valor depende de las propiedades del material.

>🗝️ *Inductancia:* Es la capacidad de un componente (bobina) para almacenar energía en forma de campo magnético cuando circula corriente a través de él. Se mide en henrios (H) y afecta la respuesta del circuito ante cambios de corriente.

>🗝️*Capacitancia:* Es la capacidad de un componente (condensador) para almacenar energía en forma de campo eléctrico. Se mide en faradios (F) y se relaciona con la cantidad de carga que puede almacenar por unidad de voltaje.

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
#### 4.1 
![Imagen de WhatsApp 2025-03-11 a las 19 46 07_bdbb61bf](https://github.com/user-attachments/assets/c5abb617-98dc-4a69-bba6-d44876c115b7)

- Primero que nada, definimos las representaciones de voltaje correspondientes a cada uno de los elementos que componen el circuito:

$$V_{c}(t)=\frac{1}{C}\int_{}^{}i_{T}(t)dt$$

$$V_{L}(t)=L\frac{di_{T}(t)}{dt}$$

$$V_{R1}(t)=i_{T}(t)R_{1}$$

- Ahora, se define la ecuacion que identifica a la malla del circuito por medio de la ley de voltaje de Kirchhoff

$$V_{e}(t)=V_{R1}(t)+V_{L}(t)+V_{R2}(t)+V_{C}(t)$$           

- Sustituimos estos voltajes con sus representaciones, obteniendo:

$$ V_{e}(t)=i_{T}(t)R_{1}+L\frac{di_{T}(t)}{dt}+i_{T}(t)R_{2}+\frac{1}{C}\int_{}^{}i_{T}(t)dt$$

- Sustituyendo estos voltajes por sus representaciones:

$$V_{s}(t)=i_{T}(t)R_{2}+\frac{1}{C}\int_{}^{}i_{T}(t)dt$$

- Calculamos la ecuación que representa el voltaje de salida Vs(t)

$$V_{s}(t)=V_{R2}(t)+V_{C}(t)$$

#### 4.2 
![image](https://github.com/user-attachments/assets/d9a008b0-32fe-4451-aacb-f344b9899341)

##### 4.2.1 identificar elementos y mallas
- hay dos lazos con corrientes i_{1}(t) y i_{2}(t)
  
#### 4.2.2 Aplicar la Ley de voltajes de Kirchhoff (LVK)
- Se analiza cada lazo usando la LVK
  
**Ecuacion del lazo 1**

$$R*i_{1}(t)+L\frac{d_{i}(t)}{dt}+R(i_{1}(t)-i_{2}(t))+\frac{1}{C}\int_{}^{}(i_{1}(t)-i_{2}(t))dt=V(s)$$

- reemplazando valores
  
$$2*i_{1}(t)+3\frac{d_{i}(t)}{dt}+4(i_{1}(t)-i_{2}(t))+\frac{1}{5}\int_{}^{}(i_{1}(t)-i_{2}(t))dt=V(s)$$

**Ecuación del lazo 2**

$$L\frac{di_{2}(t)}{dt}+R*i_{2}(t)+R(i_{1}(t)-i_{2}(t))+\frac{1}{C}\int_{}^{}(i_{2}(t)-i_{1}(t))dt=0$$

- reemplazando valores
  
$$6\frac{di_{2}(t)}{dt}+7i_{2}(t)+4(i_{1}(t)-i_{2}(t))+\frac{1}{5}\int_{}^{}(i_{2}(t)-i_{1}(t))dt=0$$

### 5. Conclusiones
El modelamiento de sistemas eléctricos ayuda a predecir su comportamiento y respuesta ante diferentes entradas. Los circuitos RLC, que son de segundo orden, tienen similitudes con los sistemas mecánicos, lo que permite un análisis más completo. Usando las leyes de Kirchhoff y ecuaciones diferenciales, es posible diseñar y entender circuitos en control automático y electrónica. Este enfoque no solo mejora la comprensión teórica, sino que también facilita soluciones prácticas en ingeniería.
### 6. Referencias
*Dorf, R. C., & Bishop, R. H. (2011). Sistemas de Control Automático. Prentice Hall.*   

*Universidad de Cantabria. (s.f.). Ejercicios 1. OCW Universidad de Cantabria. https://ocw.unican.es/pluginfile.php/1829/course/section/1439/ejercicios_1.pdf*

    



