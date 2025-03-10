- sistema
- planta
- proceso
- actuador
- lazo cerrado
- lazo abierto
# Transformada de Laplace
Es una herramienta matematica que permite convertir ecuaciones algebraicas en el dominio de la frecuencia. esto facilita el analisis de sistemas dinamicos, ya que en lugar de resolver ecuaciones diferenciales en el tiempo, se puede trabajar con expresiones algebraicas en s, lo que simplifica la resolucion de problemas.
Una de sus ventajas es la facilidad con la que maneja derivadas e integrales, nos permite transformar ecuaciones diferenciales en ecuaciones polinomicas. Ademas se puede obtener funciones de transferencia
# Funcion de transferencia
## Definicion
Es una herramienta fundamental para analizar y diseñar sistemas dinamicos. se utiliza para representar la relacion matematica entre la entrada y la salida de un sistema en el dominio de Laplace

$$ G(s) = \frac{Y(s)}{U(s)} $$

donde Y(s) es la salida y U(s) es la entrada del sistema, asumiendo condiciones iniciales nulas
## forma general
la forma general de una funcion de transferencia es 

$$ G(s) = \frac{N(s)}{D(s)} $$

- N(s) es el numerador, contiene los ceros del sistema
- D(s) es el denominador, contiene los polos del sistema
## ejemplo
suponiendo un sistema masa-resorte-amortiguador

$$m\ddot{x}+b\dot{x}+kx = F(t)$$

Aplicando la transformada de Laplace (condiciones inciales en cero)

$$ ms^{2}X(s)+bsX(s)+kX(s)=F(s) $$

despejando G(s):

$$G(s)=\frac{X(s)}{F(s)} =\frac{1}{ms^{2}+bs+k}$$

## Clasificacion 
