### nestor alexander avila rojas 
# Fucnion de transferencia 14/05/2025
Una función de transferencia es una herramienta matemática que se utiliza en ingeniería y control de sistemas para describir la relación entre la entrada y la salida de un sistema dinámico lineal, en el dominio de Laplace.

$$G(s) = \frac{Y(s)}{U(s)}$$

La función de transferencia representa cómo un sistema responde a una entrada en términos de sus componentes dinámicos (como integradores, derivadores, y constantes de ganancia). Incluye el comportamiento transitorio y en estado estacionario.

### Clasificaciones 
Las funciones de transferencia se pueden expresar de diferentes maneras, esto dependera de su denominador y numerador, teniendo tres casos particulares los cuales son 

[![image.png](https://i.postimg.cc/CKXqw3Jn/image.png)](https://postimg.cc/GBP2QSWb)

Teniendo esto en cuenta podremos analizar varios ejemplos como los sigientes 

$s^2 + 1 \quad \text{(impropia)}$
$2 \quad \text{(bipropia)}$
$\frac{1}{s + 1} \quad \text{(Estrictamente propia)}$
$\frac{s^2 - 1}{s + 1} \quad \text{(impropia)}$
$\frac{s - 1}{s + 1} \quad \text{(bipropia)}$

## Zeros en una funcion de transferencia 
Para la solucion de los zeros debemos igualar el numerador a 0 para obter los valores de (S), si de casualidad el numerador se hace 0 toda la funcion de transferencia se vuelve 0 de ahi el nombre, la solucion de (S) pueden ser numeros reales o complejos esto con el fin de ubicarlos en el plano cartesiano 

$G(s) = \frac{Y(s)}{U(s)} = \frac{3s-1}{s^2+3s+2} = \frac{N(s)}{D(s)}$

$N(s) = 0 \quad \Rightarrow \quad 3s-1=0$

**Como solucion nos da un numero complejo el cual es el sigiente:**

$s = \frac{1}{3}$

**Una vez hallado el resultado este deberemos graficarlo en el plano cartesiano, este se representara con un circulo de la sigiente forma** 

[![image.png](https://i.postimg.cc/jjbjvR8X/image.png)](https://postimg.cc/YvdkCBBG)

## Polos en una funcion de transferencia
En el caso de los polos lo que deberemos hacer es igualar a cero el denomidador de la funcion de transferencia para hallar "S" estos valores tambien puden ser reales o complejos esto con la facilidad de poderlos graficar en el plano cartesiano

### ¿Por qué son importantes los polos?
Los polos determinan el comportamiento dinámico del sistema:

-Si los polos están en el semiplano izquierdo del plano complejo (tienen parte real negativa), el sistema es estable.

-Si uno o más polos están en el semiplano derecho (parte real positiva), el sistema es inestable.

-Si hay polos en el eje imaginario (parte real cero), el sistema puede ser marginalmente estable o inestable, dependiendo del caso.

#### 💡Ejemplo

$G(s) = \frac{Y(s)}{U(s)} = \frac{3s - 1}{s^2 + 3s + 2} = \frac{N(s)}{D(s)}$

$D(s) = 0$

$s^2 + 3s + 2 = 0$

$(s + 1)(s + 2) = 0$

$s = -1$

$s = -2$

**La ubucacion de los polos es muy similar a la de los zeros, solo que en este caso tendremos que demarcarlos con una X en el plano carteciano como se muestra en la siguiente imagen:**

[![image.png](https://i.postimg.cc/BvGtxqDQ/image.png)](https://postimg.cc/LJNHSFNr)

## Ubicacion General de los polos 
[![image.png](https://i.postimg.cc/jSXNBvwH/image.png)](https://postimg.cc/4YYm961y)

### Polos complejos conjugados
**Representados como un par de “X” simétricas respecto al eje real.**

Tienen la forma:

$s = \sigma \pm j\omega$

**donde:**

- 𝜎 es la parte real (negativa en sistemas estables).

- 𝜔 es la frecuencia imaginaria.

**Característica:** generan una respuesta oscilatoria amortiguada.

### Polos reales diferentes
Ubicados sobre el eje real (horizontal), pero en posiciones distintas.

**Tienen la forma:**

$s = s_1, \quad s = s_2 \quad \text{con} \quad s_1 \ne s_2, \quad s_1, s_2 \in \mathbb{R}$

**Característica:** producen una respuesta compuesta por dos exponentes reales negativos (si el sistema es estable).

### Polos reales iguales (repetidos)
Ubicados sobre el eje real en el mismo punto.

**Tienen la forma:**

$$s = s_0 \quad \text{con multiplicidad} > 1$$

**Característica:** generan una respuesta del tipo $t^n e^{s_0 t}$ , más lenta que polos reales simples.

## Teorema del valor final 
El Teorema del Valor Final es una herramienta en el análisis de sistemas dinámicos (especialmente en el dominio de Laplace) que permite encontrar el valor al que tiende una función en el tiempo cuando t→∞, usando su transformada de Laplace.

$$\lim_{t \to \infty} f(t) = \lim_{s \to 0} s F(s)$$

#### 💡Ejemplo 

$G(s) = \frac{Y(s)}{U(s)} = \frac{4}{5s + 1}$

$Y(s) = \frac{4 \ast U(s)}{5s + 1}$

**Si la entrada es un escalón:**

$Y(s) = \frac{\frac{4}{s}}{5s + 1}$

**Teorema del valor final:**

$\lim_{s \to 0} sY(s) = \lim_{s \to 0} s \cdot \frac{\frac{4}{s}}{5s + 1}$

$\lim_{s \to 0} \frac{4}{5s+1} = 4$

## Entradas de prueba de un sistema 
>🔑En este caso la solución de una ecuación diferencial depende de la entrada, la respuesta de un sistema también.Es muy difícil conocer las señales que están ocurriendo en un sistema, ya que depende de muchos factores como ruido, tipo de señales, ambiente, entre otros, además, el sistema de control debe diseñarse para que funcione ante cualquier señal.
En control, se utilizan diferentes tipos de señales de prueba para evaluar el desempeño de un sistema.

### Entrada escalon 
Un cambio abrupto en la entrada desde cero a un valor constante A en t=0, Evalúa la respuesta transitoria y el error en estado estacionario de un sistema (ej: tiempo de asentamiento, sobrepico).

Expresión matemática:

$$\mathcal{L}(u(t)) = \frac{A}{s}$$

### Entrada Rampa 
Una señal que aumenta linealmente con el tiempo, Analiza la capacidad del sistema para seguir señales que cambian continuamente (ej: sistemas de seguimiento como radares o motores).

Expresión matemática:

$$\mathcal{L}\{x(t)\} = \frac{A}{s^2}$$

### Entrada Parabola
Una señal que varía cuadráticamente con el tiempo, Estudia sistemas que requieren alta precisión para aceleraciones (ej: cohetes, satélites).

Expresión matemática:

$$\mathcal{L}\{r(t)\} = \frac{A}{s^3}$$
