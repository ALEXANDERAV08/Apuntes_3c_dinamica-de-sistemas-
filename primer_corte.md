### nestor alexander avila rojas 
# 1 Función de transferencia 14/05/2025
Una función de transferencia es una herramienta matemática que se utiliza en ingeniería y control de sistemas para describir la relación entre la entrada y la salida de un sistema dinámico lineal, en el dominio de Laplace.

$$G(s) = \frac{Y(s)}{U(s)}$$

**Donde:**

- $G(s)$ es la función de transferencia

- $Y(s)$ es la transformada de Laplace de la salida

- $U(s)$ es la transformada de Laplace de la entrada

La función de transferencia representa cómo un sistema responde a una entrada en términos de sus componentes dinámicos (como integradores, derivadores, y constantes de ganancia). Incluye el comportamiento transitorio y en estado estacionario.
#### 💡ejemplo 
**Para un sistema masa-resorte-amortiguador:**

$m\ddot{x} + b\dot{x} + kx = F(t)$

**Aplicando Transformada de Laplace (condiciones iniciales nulas):**

$ms^2X(s) + bsX(s) + kX(s) = F(s) \Rightarrow G(s) = \frac{X(s)}{F(s)} = \frac{1}{ms^2 + bs + k}$

### 1.1 Clasificaciones 
Las funciones de transferencia se pueden expresar de diferentes maneras, esto dependera de su denominador y numerador, teniendo tres casos particulares los cuales son 

[![image.png](https://i.postimg.cc/CKXqw3Jn/image.png)](https://postimg.cc/GBP2QSWb)

**Teniendo esto en cuenta podremos analizar varios ejemplos como los sigientes** 

$s^2 + 1 \quad \text{(impropia)}$

$2 \quad \text{(bipropia)}$

$\frac{1}{s + 1} \quad \text{(Estrictamente propia)}$

$\frac{s^2 - 1}{s + 1} \quad \text{(impropia)}$

$\frac{s - 1}{s + 1} \quad \text{(bipropia)}$

## 2 Zeros en una funcion de transferencia 
Para la solucion de los zeros debemos igualar el numerador a 0 para obter los valores de (S), si de casualidad el numerador se hace 0 toda la funcion de transferencia se vuelve 0 de ahi el nombre, la solucion de (S) pueden ser numeros reales o complejos esto con el fin de ubicarlos en el plano cartesiano 

$G(s) = \frac{Y(s)}{U(s)} = \frac{3s-1}{s^2+3s+2} = \frac{N(s)}{D(s)}$

$N(s) = 0 \quad \Rightarrow \quad 3s-1=0$

**Como solucion nos da un numero complejo el cual es el sigiente:**

$s = \frac{1}{3}$

**Una vez hallado el resultado este deberemos graficarlo en el plano cartesiano, este se representara con un circulo de la sigiente forma** 

[![image.png](https://i.postimg.cc/jjbjvR8X/image.png)](https://postimg.cc/YvdkCBBG)

## 2.1 Polos en una funcion de transferencia
>🔑En el caso de los polos lo que deberemos hacer es igualar a cero el denomidador de la funcion de transferencia para hallar "S" estos valores tambien puden ser reales o complejos esto con la facilidad de poderlos graficar en el plano cartesiano

### ¿Por qué son importantes los polos?
Los polos determinan el comportamiento dinámico del sistema:

- Si los polos están en el semiplano izquierdo del plano complejo (tienen parte real negativa), el sistema es estable.

- Si uno o más polos están en el semiplano derecho (parte real positiva), el sistema es inestable.

- Si hay polos en el eje imaginario (parte real cero), el sistema puede ser marginalmente estable o inestable, dependiendo del caso.

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

## 3 Teorema del valor final 
>🔑El Teorema del Valor Final es una herramienta en el análisis de sistemas dinámicos (especialmente en el dominio de Laplace) que permite encontrar el valor al que tiende una función en el tiempo cuando t→∞, usando su transformada de Laplace.

$\lim_{t \to \infty} f(t) = \lim_{s \to 0} s F(s)$

#### 💡Ejemplo 

$G(s) = \frac{Y(s)}{U(s)} = \frac{4}{5s + 1}$

$Y(s) = \frac{4 \ast U(s)}{5s + 1}$

**Si la entrada es un escalón:**

$Y(s) = \frac{\frac{4}{s}}{5s + 1}$

**Teorema del valor final:**

$\lim_{s \to 0} sY(s) = \lim_{s \to 0} s \cdot \frac{\frac{4}{s}}{5s + 1}$

$\lim_{s \to 0} \frac{4}{5s+1} = 4$

## 4 Entradas de prueba de un sistema 
>🔑En este caso la solución de una ecuación diferencial depende de la entrada, la respuesta de un sistema también.Es muy difícil conocer las señales que están ocurriendo en un sistema, ya que depende de muchos factores como ruido, tipo de señales, ambiente, entre otros, además, el sistema de control debe diseñarse para que funcione ante cualquier señal.
En control, se utilizan diferentes tipos de señales de prueba para evaluar el desempeño de un sistema.

### 4.1 Entrada escalon 
>🔑Un cambio abrupto en la entrada desde cero a un valor constante A en t=0, Evalúa la respuesta transitoria y el error en estado estacionario de un sistema (ej: tiempo de asentamiento, sobrepico).

**Expresión matemática:**

$\mathcal{L}(u(t)) = \frac{A}{s}$

### 4.2 Entrada Rampa 
>🔑Una señal que aumenta linealmente con el tiempo, Analiza la capacidad del sistema para seguir señales que cambian continuamente (ej: sistemas de seguimiento como radares o motores).

**Expresión matemática:**

$\mathcal{L}\{x(t)\} = \frac{A}{s^2}$

### 4.3 Entrada Parabola
>🔑Una señal que varía cuadráticamente con el tiempo, Estudia sistemas que requieren alta precisión para aceleraciones (ej: cohetes, satélites).

**Expresión matemática:**

$\mathcal{L}\{r(t)\} = \frac{A}{s^3}$

## 5 📚Ejercicios

#### 📚 Ejercicio 1

**Dada:**

$G(s) = \frac{s+3}{s^2 + 6s + 9}$

### Paso 1: Encontrar los ceros

* Tomamos el numerador: $s + 3 = 0 \Rightarrow s = -3$

### Paso 2: Encontrar los polos

* Factorizamos el denominador:

$s^2 + 6s + 9 = (s + 3)^2 \Rightarrow s = -3 \text{ (polo doble)}$

✅ Resultado:

* Cero en $s = -3$
* Polo doble en $s = -3$

#### 📚 Ejercicio 2

**Dada:**

$G(s) = \frac{s^2 + 4}{s(s+1)(s+2)}$

### Paso 1: Ceros

* Resolver $s^2 + 4 = 0 \Rightarrow s = \pm 2j$

### Paso 2: Polos

* Denominador factorizado nos da:

$s = 0, -1, -2$

✅ Resultado:

* Ceros en $s = \pm 2j$
* Polos en $s = 0, -1, -2$

#### 📚 Ejercicio 3

**Dado:**

$Y(s) = \frac{10}{s(s+5)}$

### Paso 1: Verificar estabilidad

* Polos en $s = 0$ y $s = -5$. Sistema marginalmente estable (polo en el origen es aceptable).

### Paso 2: Aplicar el teorema

$\lim_{t \to \infty} y(t) = \lim_{s \to 0} s Y(s) = \lim_{s \to 0} \frac{10s}{s(s+5)} = \frac{10}{5} = 2$

✅ Valor final: $y(\infty) = 2$
