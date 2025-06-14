# 1. Diagramas de flujo de señales 
>🔑Los diagramas de flujo de señales son una herramienta gráfica utilizada en la dinámica de sistemas para representar las relaciones entre las 
variables de un sistema complejo. A diferencia de los diagramas de bloques, estos diagramas facilitan el cálculo de la función de transferencia 
total de un sistema, utilizando la fórmula de Mason.

Elementos clave de los diagramas de flujo de señales
Nodos: Representan las variables del sistema (entrada o salida) y se indican con un círculo etiquetado.

![image](https://github.com/user-attachments/assets/e223dfcf-a7e3-45eb-93f3-04abbc2fb09a)

Flechas: Indican la relación entre variables, incluyendo la función de transferencia asociada.

![image](https://github.com/user-attachments/assets/6701d779-d273-4312-b4d3-87e0b385b204)

## 2. Lazos y Trayectorias:
>🔑Camino directo: Conecta un nodo de entrada con uno de salida sin cruzar nodos repetidos.
Lazo cerrado: Camino que regresa al nodo inicial sin repetir otros nodos.
Fórmula de Mason
La fórmula de Mason permite calcular la función de transferencia total 

T(s) de un sistema complejo:

$$𝑇(𝑠)= \frac{∑PkΔk}{Δ}$$
​
​
 
**Donde:**
 - Pk: Ganancia de cada camino directo.
 - Δ: Determinante general del sistema.
 - Δk: Determinante que excluye los lazos que afectan al camino directo Pk.


![download](https://github.com/user-attachments/assets/bce56f20-e084-48c0-b485-efec54efce01)

![image](https://github.com/user-attachments/assets/79c56fc0-f263-456b-b67c-62ab68b8176f)

#### 💡Ejemplo:

**5. Utilice la fórmula de Mason para encontrar las siguientes funciones de transferencia en los diagramas siguientes:**

![image](https://github.com/user-attachments/assets/c3eeffcb-2b16-4ace-ada9-09323724e66f)

**Trayectorias (Forward Paths):** 2

* $P_1 = G_1 G_2 G_3$
* $P_2 = G_4 G_3$

**Lazos Cerrados (Loops):**

* $L_1 = -G_1 H_1$
* $L_2 = -G_4 G_3 H_3$
* $L_3 = -G_3 H_2$
* $L_4 = -G_1 G_2 G_3 H_3$

**Determinante ($\Delta$):**

$\Delta = 1 - (L_1 + L_2 + L_3 + L_4) + (L_1 L_3)$

**Cofactores:**

* $\Delta_1 = 1$
* $\Delta_2 = 1$

**Funciones de Transferencia:**

$\frac{Y_5}{Y_1} = \frac{1}{\Delta} \cdot (P_1 \Delta_1 + P_2 \Delta_2)$

This can also be written as:

$\frac{Y_5}{Y_1} = \frac{P_1 \Delta_1 + P_2 \Delta_2}{1 - (L_1 + L_2 + L_3 + L_4) + L_1 L_3}$

Desde mi perspectiva, los diagramas de flujo de señales son una mejora considerable frente a los diagramas de bloques 
en sistemas complejos. Su estructura ordenada y la sistematicidad de la fórmula de Mason reducen la probabilidad de errores 
al manejar sistemas con múltiples interacciones.

Lo que encuentro más interesante es cómo esta herramienta conecta conceptos visuales con cálculos formales. En mi experiencia,
resulta valiosa tanto para estudiantes como para profesionales que trabajan con modelos de control, permitiendo una comprensión 
más profunda y efectiva de los sistemas.

con el diagrama de flujo de señales es mas rapido llegar a la funcion de tranferencia unicamente se debe tenr en cuenta la 
identificacion de la trayectoria o trayectorias y aplicar bien la formula de mason
