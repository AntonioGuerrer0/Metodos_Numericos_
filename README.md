<h1 align="center">Problemario de Métodos Numéricos</h1>

<h3>Realizado por:</h3>

<ul>
    <li>Jose Antonio Guerrero Lazcano</li>
</ul>

<hr>

<h1 id="indice" align="center">ÍNDICE</h1>

<ul>

<li><a href="#competencia-asignatura">Competencia de la Asignatura</a></li>

<li>
<a href="#errores-numericos"> TEMA 1: Errores Numéricos</a>

<ul>
<li><a href="#error-redondeo">Error de redondeo</a></li>
<li><a href="#perdida-precision">Pérdida de precisión</a></li>
<li><a href="#comparacion-directa">Comparación directa</a></li>
<li><a href="#cancelacion-resta">Cancelación de resta</a></li>
<li><a href="#desbordamiento">Desbordamiento</a></li>
<li><a href="#conversion-estrecha">Conversión estrecha</a></li>
<li><a href="#error-absoluto">Error absoluto</a></li>
<li><a href="#error-relativo">Error relativo</a></li>
</ul>

</li>

<li>
<a href="#sistemas-ecuaciones"> TEMA 2: Sistemas de Ecuaciones</a>

<ul>
<li><a href="#eliminacion-gaussiana">Eliminación Gaussiana</a></li>
<li><a href="#gauss-jordan">Gauss-Jordan</a></li>
<li><a href="#gauss-seidel">Gauss-Seidel</a></li>
<li><a href="#jacobi">Método de Jacobi</a></li>
</ul>

</li>

<li>
<a href="#metodos-integracion">TEMA 3: Métodos de Integración</a>

<ul>
<li><a href="#trapecio">Método del Trapecio</a></li>
<li><a href="#simpson13">Método de Simpson 1/3</a></li>
<li><a href="#simpson38">Método de Simpson 3/8</a></li>
<li><a href="#cuadratura-gaussiana">Método de la Cuadratura Gaussiana</a></li>
</ul>

</li>

<li>
<a href="#interpolacion"> TEMA 4: Interpolación</a>

<ul>
<li><a href="#interpolacion-lineal">Interpolación Lineal</a></li>
<li><a href="#interpolacion-cuadratica">Interpolación Cuadrática</a></li>
<li><a href="#lagrange">Interpolación Lagrange</a></li>
<li><a href="#newton">Interpolación de Newton</a></li>
</ul>

</li>

<li>
<a href="#ecuaciones-diferenciales"> TEMA 5: Ecuaciones Diferenciales</a>

<ul>
<li><a href="#euler">Euler</a></li>
<li><a href="#runge-kutta">Runge-Kutta</a></li>
<li><a href="#taylor">Taylor</a></li>
</ul>

</li>

</ul>

<hr>

<h2 id="competencia-asignatura" align="center">
Competencia de la Asignatura
</h2>

<p>
Aplica los métodos numéricos para resolver problemas científicos y de ingeniería utilizando la computadora.
</p>


<hr>


<p align="right">
<a href="#indice">⬆ Volver al índice</a>
</p>

<hr>

<h1 id="errores-numericos" align="center">
Errores Numéricos
</h1>

<h2 id="error-redondeo" align="center">
1. Error de redondeo
</h2>

<h3>¿Qué es?</h3>

<p>
El error de redondeo ocurre cuando un número decimal no puede representarse exactamente dentro de la memoria de la computadora, por lo que el sistema realiza una aproximación. Este tipo de error es muy común en métodos numéricos debido a que las computadoras trabajan con una cantidad limitada de cifras significativas.
</p>

<p>
Por ejemplo:
</p>

<pre>
0.1 + 0.2 != 0.3
</pre>

<p>
Esto sucede porque algunos números decimales no pueden almacenarse de manera exacta en formato binario.
</p>

<hr>

<h3>Fórmulas</h3>

<h4>Error absoluto</h4>

<pre>
Ea = |Valor real - Valor aproximado|
</pre>

<h4>Error relativo</h4>

<pre>
Er = |Valor real - Valor aproximado| / |Valor real|
</pre>

<h4>Error porcentual</h4>

<pre>
Ep = Er × 100
</pre>

<hr>

<h3>Ventajas</h3>

<ul>
<li>Permite realizar cálculos rápidos en computadoras.</li>
<li>Facilita el manejo de números muy grandes o muy pequeños.</li>
<li>Reduce el consumo de memoria.</li>
<li>Hace posible la implementación de métodos numéricos complejos.</li>
</ul>

<hr>

<h3>Desventajas</h3>

<ul>
<li>Puede generar resultados inexactos.</li>
<li>Los errores pueden acumularse durante múltiples operaciones.</li>
<li>En cálculos científicos puede afectar significativamente la precisión.</li>
<li>Puede provocar diferencias entre resultados teóricos y computacionales.</li>
</ul>

<hr>

<h3>¿En qué ramas de la ingeniería se utiliza?</h3>

<ul>
<li><b>Ingeniería en Sistemas Computacionales:</b> Desarrollo de software científico, simulación numérica e inteligencia artificial.</li>
<li><b>Ingeniería Civil:</b> Cálculo estructural y análisis de deformaciones.</li>
<li><b>Ingeniería Mecánica:</b> Simulación de movimiento y fuerzas.</li>
<li><b>Ingeniería Electrónica:</b> Procesamiento digital de señales y sistemas embebidos.</li>
<li><b>Ingeniería Industrial:</b> Modelado matemático y optimización.</li>
</ul>

<hr>
<h3>Pseudocódigo</h3>

<pre>
Inicio

    Definir a = 0.1
    Definir b = 0.2

    resultado = a + b

    Mostrar "Resultado: " + resultado

    Si resultado == 0.3 Entonces

        Mostrar "Es igual a 0.3"

    Sino

        Mostrar "No es exactamente igual a 0.3"

    FinSi

Fin
</pre>

<h3>Ejemplo en Java</h3>

```java
public class ErrorRedondeo {

    public static void main(String[] args) {

        double a = 0.1;
        double b = 0.2;

        double resultado = a + b;

        System.out.println("Resultado: " + resultado);

        if(resultado == 0.3){
            System.out.println("Es igual a 0.3");
        } else {
            System.out.println("No es exactamente igual a 0.3");
        }
    }
}
```
<h2> compilacion del codigo </h2>

<img width="457" height="177" alt="Captura de pantalla 2026-05-26 113252" src="https://github.com/user-attachments/assets/6aa0da87-7d8b-4c09-86bd-8fc9355e54d0" />

<p align="right">
<a href="#indice">⬆ Volver al índice</a>
</p>

<hr>

<h2 id="perdida-precision" align="center">
2. Pérdida de precisión
</h2>

<h3>¿Qué es?</h3>

<p>
La pérdida de precisión ocurre cuando una computadora no puede representar todos los dígitos exactos de un número durante una operación matemática. Esto provoca que algunas cifras significativas se pierdan o se modifiquen, generando resultados aproximados.
</p>

<p>
Este problema es muy común en métodos numéricos, especialmente cuando se realizan operaciones con números muy grandes, muy pequeños o con muchos decimales.
</p>

<p>
Por ejemplo:
</p>

<pre>
1000000000.0 + 0.0000001
</pre>

<p>
La computadora puede ignorar el número pequeño debido a la limitada precisión del tipo de dato.
</p>

<hr>

<h3>Fórmulas</h3>

<h4>Error absoluto</h4>

<pre>
Ea = |Valor real - Valor aproximado|
</pre>

<h4>Error relativo</h4>

<pre>
Er = |Valor real - Valor aproximado| / |Valor real|
</pre>

<h4>Error porcentual</h4>

<pre>
Ep = Er × 100
</pre>

<hr>

<h3>Ventajas</h3>

<ul>
<li>Permite realizar cálculos complejos rápidamente.</li>
<li>Reduce el tiempo de procesamiento en computadoras.</li>
<li>Facilita el manejo de grandes cantidades de datos.</li>
<li>Hace posible el uso de simulaciones numéricas.</li>
</ul>

<hr>

<h3>Desventajas</h3>

<ul>
<li>Puede producir resultados inexactos.</li>
<li>Se pierden cifras significativas durante operaciones matemáticas.</li>
<li>Los errores pueden acumularse en cálculos repetitivos.</li>
<li>Puede afectar la precisión en cálculos científicos e ingenieriles.</li>
</ul>

<hr>

<h3>¿En qué ramas de la ingeniería se utiliza?</h3>

<ul>

<li><b>Ingeniería en Sistemas Computacionales:</b> Desarrollo de software científico y simulaciones.</li>

<li><b>Ingeniería Electrónica:</b> Procesamiento digital de señales y sistemas embebidos.</li>

<li><b>Ingeniería Civil:</b> Modelos matemáticos y cálculos estructurales.</li>

<li><b>Ingeniería Mecánica:</b> Simulación de fuerzas y movimientos.</li>

<li><b>Ingeniería Industrial:</b> Optimización y análisis estadístico.</li>

</ul>

<hr>

<h3>Pseudocódigo</h3>

<pre>
Inicio

    Definir numeroGrande = 1000000000.0
    Definir numeroPequeno = 0.0000001

    resultado = numeroGrande + numeroPequeno

    Mostrar "Resultado: " + resultado

Fin
</pre>

<h3>Ejemplo en Java</h3>

```java
public class PerdidaPrecision {

    public static void main(String[] args) {

        double numeroGrande = 1000000000.0;
        double numeroPequeno = 0.0000001;

        double resultado = numeroGrande + numeroPequeno;

        System.out.println("Resultado: " + resultado);
    }
}
```
<h3> compilación del codigo </h3>

<img width="502" height="181" alt="Captura de pantalla 2026-05-26 113924" src="https://github.com/user-attachments/assets/0f7ae3b5-ad0f-4190-8afa-f6e936376129" />

<p align="right">
<a href="#indice">⬆ Volver al índice</a>
</p>
<hr>

<h2 id="comparacion-directa" align="center">
3. Comparación directa
</h2>

<h3>¿Qué es?</h3>

<p>
La comparación directa es un problema numérico que ocurre cuando se comparan números decimales utilizando el operador de igualdad <b>==</b>. Debido a los errores de representación y redondeo en las computadoras, dos números que aparentemente deberían ser iguales pueden tener pequeñas diferencias internas.
</p>

<p>
Esto provoca que una comparación directa falle aunque los valores matemáticamente sean equivalentes.
</p>

<p>
Por ejemplo:
</p>

<pre>
0.1 + 0.2 == 0.3
</pre>

<p>
El resultado será falso debido a la representación binaria de los números decimales.
</p>

<hr>

<h3>Fórmulas</h3>

<h4>Comparación con tolerancia</h4>

<pre>
|a - b| &lt; ε
</pre>

<p>
Donde:
</p>

<ul>
<li><b>a</b> = valor calculado</li>
<li><b>b</b> = valor esperado</li>
<li><b>ε</b> = tolerancia permitida</li>
</ul>

<h4>Error absoluto</h4>

<pre>
Ea = |Valor real - Valor aproximado|
</pre>

<h4>Error relativo</h4>

<pre>
Er = |Valor real - Valor aproximado| / |Valor real|
</pre>

<hr>

<h3>Ventajas</h3>

<ul>
<li>Permite validar resultados numéricos.</li>
<li>Facilita la toma de decisiones en programas.</li>
<li>Ayuda a verificar condiciones lógicas.</li>
<li>Es sencilla de implementar.</li>
</ul>

<hr>

<h3>Desventajas</h3>

<ul>
<li>Las comparaciones exactas pueden fallar con números decimales.</li>
<li>Puede generar errores lógicos en programas.</li>
<li>Los resultados dependen de la precisión del tipo de dato.</li>
<li>En cálculos científicos puede producir decisiones incorrectas.</li>
</ul>

<hr>

<h3>¿En qué ramas de la ingeniería se utiliza?</h3>

<ul>

<li><b>Ingeniería en Sistemas Computacionales:</b> Desarrollo de software, simulaciones y algoritmos numéricos.</li>

<li><b>Ingeniería Electrónica:</b> Procesamiento de señales digitales y sistemas de control.</li>

<li><b>Ingeniería Mecánica:</b> Simulaciones físicas y cálculos computacionales.</li>

<li><b>Ingeniería Civil:</b> Verificación de modelos matemáticos y análisis estructural.</li>

<li><b>Ingeniería Industrial:</b> Sistemas de optimización y análisis estadístico.</li>

</ul>

<hr>
<h3>Pseudocódigo</h3>

<pre>
Inicio

    Definir a = 0.1 + 0.2
    Definir b = 0.3

    Mostrar "Valor de a: " + a
    Mostrar "Valor de b: " + b

    Si a == b Entonces

        Mostrar "Son iguales"

    Sino

        Mostrar "No son exactamente iguales"

    FinSi

    // Comparación usando tolerancia

    Definir epsilon = 0.000001

    Si valorAbsoluto(a - b) < epsilon Entonces

        Mostrar "Son aproximadamente iguales"

    FinSi

Fin
</pre>

<h3>Ejemplo en Java</h3>

```java
public class ComparacionDirecta {

    public static void main(String[] args) {

        double a = 0.1 + 0.2;
        double b = 0.3;

        System.out.println("Valor de a: " + a);
        System.out.println("Valor de b: " + b);

        if(a == b){
            System.out.println("Son iguales");
        } else {
            System.out.println("No son exactamente iguales");
        }

        // Comparación correcta usando tolerancia
        double epsilon = 0.000001;

        if(Math.abs(a - b) < epsilon){
            System.out.println("Son aproximadamente iguales");
        }
    }
}
```
<h3>Compilación de codigo</h3>
<img width="382" height="163" alt="Captura de pantalla 2026-05-26 114217" src="https://github.com/user-attachments/assets/bb2d071b-4964-4e76-a681-4014bb6a592f" />


<p align="right">
<a href="#indice">⬆ Volver al índice</a>
</p>
<hr>

<h2 id="cancelacion-resta" align="center">
4. Cancelación de resta
</h2>

<h3>¿Qué es?</h3>

<p>
La cancelación de resta es un problema numérico que ocurre cuando se restan dos números muy cercanos entre sí. Debido a que ambos valores son casi iguales, gran parte de sus cifras significativas se cancelan, provocando una pérdida importante de precisión en el resultado.
</p>

<p>
Este error es muy común en métodos numéricos y cálculos científicos donde se trabajan diferencias pequeñas entre valores grandes o similares.
</p>

<p>
Por ejemplo:
</p>

<pre>
1000.0001 - 1000.0000
</pre>

<p>
Aunque el resultado esperado es pequeño, la computadora puede perder precisión durante la operación.
</p>

<hr>

<h3>Fórmulas</h3>

<h4>Cancelación de resta</h4>

<pre>
Resultado = a - b
</pre>

<p>
Cuando:
</p>

<pre>
a ≈ b
</pre>

<p>
la precisión disminuye considerablemente.
</p>

<h4>Error absoluto</h4>

<pre>
Ea = |Valor real - Valor aproximado|
</pre>

<h4>Error relativo</h4>

<pre>
Er = |Valor real - Valor aproximado| / |Valor real|
</pre>

<hr>

<h3>Ventajas</h3>

<ul>
<li>Permite calcular diferencias entre valores.</li>
<li>Es una operación fundamental en métodos numéricos.</li>
<li>Se utiliza en simulaciones y modelos matemáticos.</li>
<li>Facilita cálculos científicos complejos.</li>
</ul>

<hr>

<h3>Desventajas</h3>

<ul>
<li>Puede provocar pérdida de cifras significativas.</li>
<li>Reduce la precisión de los resultados.</li>
<li>Los errores pueden propagarse en operaciones posteriores.</li>
<li>Afecta cálculos científicos y de ingeniería.</li>
</ul>

<hr>

<h3>¿En qué ramas de la ingeniería se utiliza?</h3>

<ul>

<li><b>Ingeniería en Sistemas Computacionales:</b> Algoritmos numéricos y simulaciones computacionales.</li>

<li><b>Ingeniería Electrónica:</b> Procesamiento digital de señales.</li>

<li><b>Ingeniería Mecánica:</b> Simulación de movimiento y fuerzas.</li>

<li><b>Ingeniería Civil:</b> Cálculos estructurales y análisis matemático.</li>

<li><b>Ingeniería Industrial:</b> Modelado matemático y optimización.</li>

</ul>

<hr>
<h3>Pseudocódigo</h3>

<pre>
Inicio

    Definir a = 1000.0001
    Definir b = 1000.0000

    resultado = a - b

    Mostrar "Resultado de la resta: " + resultado

Fin
</pre>
<h3>Ejemplo en Java</h3>

```java
public class CancelacionResta {

    public static void main(String[] args) {

        double a = 1000.0001;
        double b = 1000.0000;

        double resultado = a - b;

        System.out.println("Resultado de la resta: " + resultado);
    }
}
```
<h3>Compilación de codigo</h3>
<img width="535" height="242" alt="Captura de pantalla 2026-05-26 114258" src="https://github.com/user-attachments/assets/da1fb25f-84ce-4a5d-9af1-5f955785d7e4" />

<p align="right">
<a href="#indice">⬆ Volver al índice</a>
</p>
<hr>

<h2 id="desbordamiento" align="center">
5. Desbordamiento
</h2>

<h3>¿Qué es?</h3>

<p>
El desbordamiento ocurre cuando un cálculo produce un número mayor o menor que el rango máximo que puede almacenar un tipo de dato en la computadora. Cuando esto sucede, el resultado puede volverse incorrecto, infinito o incluso provocar errores en el programa.
</p>

<p>
Este problema es muy común en operaciones matemáticas con números extremadamente grandes o pequeños.
</p>

<p>
Por ejemplo:
</p>

<pre>
Integer.MAX_VALUE + 1
</pre>

<p>
El resultado excede la capacidad máxima del tipo entero y provoca un desbordamiento.
</p>

<hr>

<h3>Fórmulas</h3>

<h4>Condición de desbordamiento</h4>

<pre>
Resultado > Valor máximo permitido
</pre>

<p>
o
</p>

<pre>
Resultado < Valor mínimo permitido
</pre>

<h4>Error absoluto</h4>

<pre>
Ea = |Valor real - Valor aproximado|
</pre>

<h4>Error relativo</h4>

<pre>
Er = |Valor real - Valor aproximado| / |Valor real|
</pre>

<hr>

<h3>Ventajas</h3>

<ul>
<li>Permite detectar límites de almacenamiento en memoria.</li>
<li>Ayuda a optimizar el uso de tipos de datos.</li>
<li>Facilita el control de errores numéricos.</li>
<li>Es útil para validar operaciones matemáticas.</li>
</ul>

<hr>

<h3>Desventajas</h3>

<ul>
<li>Produce resultados incorrectos.</li>
<li>Puede provocar fallos en programas.</li>
<li>Genera pérdida de información numérica.</li>
<li>Afecta cálculos científicos y financieros.</li>
</ul>

<hr>

<h3>¿En qué ramas de la ingeniería se utiliza?</h3>

<ul>

<li><b>Ingeniería en Sistemas Computacionales:</b> Programación, manejo de memoria y algoritmos.</li>

<li><b>Ingeniería Electrónica:</b> Sistemas embebidos y procesamiento digital.</li>

<li><b>Ingeniería Mecánica:</b> Simulación de cálculos físicos complejos.</li>

<li><b>Ingeniería Industrial:</b> Análisis de datos y optimización.</li>

<li><b>Ingeniería Civil:</b> Modelos matemáticos y simulaciones estructurales.</li>

</ul>

<hr>
<h3>Pseudocódigo</h3>

<pre>
Inicio

    Definir numeroMaximo = valorMáximoEntero

    Mostrar "Valor máximo del entero: " + numeroMaximo

    resultado = numeroMaximo + 1

    Mostrar "Resultado después del desbordamiento: " + resultado

Fin
</pre>

<h3>Ejemplo en Java</h3>

```java
public class Desbordamiento {

    public static void main(String[] args) {

        int numeroMaximo = Integer.MAX_VALUE;

        System.out.println("Valor máximo del entero: " + numeroMaximo);

        int resultado = numeroMaximo + 1;

        System.out.println("Resultado después del desbordamiento: " + resultado);
    }
}
```
<h3>Compilación de codigo</h3>
<img width="566" height="190" alt="Captura de pantalla 2026-05-26 114700" src="https://github.com/user-attachments/assets/e444b0a6-2d3f-4a88-9bb9-3411d0c96fb7" />


<p align="right">
<a href="#indice">⬆ Volver al índice</a>
</p>
<hr>

<h2 id="conversion-estrecha" align="center">
6. Conversión estrecha
</h2>

<h3>¿Qué es?</h3>

<p>
La conversión estrecha ocurre cuando un dato de un tipo numérico grande se convierte a otro tipo con menor capacidad de almacenamiento. Durante esta conversión pueden perderse datos, decimales o incluso cambiar completamente el valor original.
</p>

<p>
Este problema es muy común en programación y métodos numéricos cuando se convierten valores de tipo <b>double</b> a <b>int</b>, o de <b>long</b> a <b>short</b>.
</p>

<p>
Por ejemplo:
</p>

<pre>
double numero = 9.99;
int valor = (int) numero;
</pre>

<p>
El valor decimal se pierde durante la conversión.
</p>

<hr>

<h3>Fórmulas</h3>

<h4>Conversión estrecha</h4>

<pre>
TipoPequeño = (TipoPequeño) TipoGrande
</pre>

<h4>Error absoluto</h4>

<pre>
Ea = |Valor real - Valor aproximado|
</pre>

<h4>Error relativo</h4>

<pre>
Er = |Valor real - Valor aproximado| / |Valor real|
</pre>

<hr>

<h3>Ventajas</h3>

<ul>
<li>Reduce el consumo de memoria.</li>
<li>Facilita la compatibilidad entre tipos de datos.</li>
<li>Puede mejorar el rendimiento en algunos sistemas.</li>
<li>Permite adaptar datos a ciertos algoritmos.</li>
</ul>

<hr>

<h3>Desventajas</h3>

<ul>
<li>Puede provocar pérdida de información.</li>
<li>Los valores decimales pueden eliminarse.</li>
<li>Puede generar errores numéricos.</li>
<li>En cálculos científicos afecta la precisión.</li>
</ul>

<hr>

<h3>¿En qué ramas de la ingeniería se utiliza?</h3>

<ul>

<li><b>Ingeniería en Sistemas Computacionales:</b> Programación, bases de datos y algoritmos.</li>

<li><b>Ingeniería Electrónica:</b> Sistemas embebidos y microcontroladores.</li>

<li><b>Ingeniería Industrial:</b> Procesamiento de datos y automatización.</li>

<li><b>Ingeniería Mecánica:</b> Simulación computacional y cálculos numéricos.</li>

<li><b>Ingeniería Civil:</b> Modelado matemático y software de simulación.</li>

</ul>

<hr>
<h3>Pseudocódigo</h3>

<pre>
Inicio

    Definir numeroDecimal = 9.99

    numeroEntero = convertirEntero(numeroDecimal)

    Mostrar "Número decimal: " + numeroDecimal

    Mostrar "Número entero: " + numeroEntero

Fin
</pre>
<h3>Ejemplo en Java</h3>

```java
public class ConversionEstrecha {

    public static void main(String[] args) {

        double numeroDecimal = 9.99;

        int numeroEntero = (int) numeroDecimal;

        System.out.println("Número decimal: " + numeroDecimal);

        System.out.println("Número entero: " + numeroEntero);
    }
}
```
<h3>Compilación de codigo</h3>
<img width="455" height="223" alt="Captura de pantalla 2026-05-26 115027" src="https://github.com/user-attachments/assets/c81d88b4-dbce-47ee-9170-9ac2a46a333c" />


<p align="right">
<a href="#indice">⬆ Volver al índice</a>
</p>
<hr>

<h2 id="error-absoluto" align="center">
7. Error absoluto
</h2>

<h3>¿Qué es?</h3>

<p>
El error absoluto es la diferencia entre el valor real de una cantidad y el valor aproximado obtenido mediante cálculos o métodos numéricos. Este tipo de error permite medir qué tan lejos está un resultado calculado respecto al valor verdadero.
</p>

<p>
Es uno de los errores más utilizados en métodos numéricos, análisis matemático y cálculos científicos.
</p>

<p>
Por ejemplo:
</p>

<pre>
Valor real = 3.1416
Valor aproximado = 3.14
</pre>

<p>
El error absoluto indica la diferencia exacta entre ambos valores.
</p>

<hr>

<h3>Fórmulas</h3>

<h4>Error absoluto</h4>

<pre>
Ea = |Valor real - Valor aproximado|
</pre>

<h4>Ejemplo matemático</h4>

<pre>
Ea = |3.1416 - 3.14|

Ea = 0.0016
</pre>

<hr>

<h3>Ventajas</h3>

<ul>
<li>Es fácil de calcular e interpretar.</li>
<li>Permite medir la precisión de un resultado.</li>
<li>Ayuda a comparar métodos numéricos.</li>
<li>Se utiliza ampliamente en cálculos científicos.</li>
</ul>

<hr>

<h3>Desventajas</h3>

<ul>
<li>No indica qué tan grande es el error respecto al valor real.</li>
<li>Puede ser engañoso con números muy grandes o muy pequeños.</li>
<li>No expresa el error en porcentaje.</li>
<li>Depende de la escala de los datos.</li>
</ul>

<hr>

<h3>¿En qué ramas de la ingeniería se utiliza?</h3>

<ul>

<li><b>Ingeniería en Sistemas Computacionales:</b> Validación de algoritmos y simulaciones.</li>

<li><b>Ingeniería Civil:</b> Análisis estructural y cálculos matemáticos.</li>

<li><b>Ingeniería Mecánica:</b> Simulación de fuerzas y movimiento.</li>

<li><b>Ingeniería Electrónica:</b> Procesamiento de señales y mediciones.</li>

<li><b>Ingeniería Industrial:</b> Control de calidad y análisis estadístico.</li>

</ul>

<hr>

<h3>Ejemplo en Java</h3>

```java
public class ErrorAbsoluto {

    public static void main(String[] args) {

        double valorReal = 3.1416;
        double valorAproximado = 3.14;

        double errorAbsoluto;

        errorAbsoluto = Math.abs(valorReal - valorAproximado);

        System.out.println("Valor real: " + valorReal);
        System.out.println("Valor aproximado: " + valorAproximado);
        System.out.println("Error absoluto: " + errorAbsoluto);
    }
}
```
<p align="right">
<a href="#indice">⬆ Volver al índice</a>
</p>
<hr>

<h2 id="error-relativo" align="center">
8. Error relativo
</h2>

<h3>¿Qué es?</h3>

<p>
El error relativo es una medida que indica qué tan grande es el error absoluto en relación con el valor real. Este tipo de error permite conocer la magnitud del error proporcionalmente al tamaño del dato original.
</p>

<p>
En métodos numéricos y cálculos científicos, el error relativo es muy importante porque ayuda a evaluar la precisión de una aproximación independientemente de la escala de los valores.
</p>

<p>
Por ejemplo:
</p>

<pre>
Valor real = 50
Valor aproximado = 49
</pre>

<p>
Aunque la diferencia es pequeña, el error relativo permite saber qué tan significativo es el error respecto al valor verdadero.
</p>

<hr>

<h3>Fórmulas</h3>

<h4>Error relativo</h4>

<pre>
Er = |Valor real - Valor aproximado| / |Valor real|
</pre>

<h4>Error porcentual</h4>

<pre>
Ep = Er × 100
</pre>

<h4>Ejemplo matemático</h4>

<pre>
Er = |50 - 49| / 50

Er = 1 / 50

Er = 0.02
</pre>

<hr>

<h3>Ventajas</h3>

<ul>
<li>Permite medir la precisión proporcional de un cálculo.</li>
<li>Facilita la comparación entre diferentes resultados.</li>
<li>Es ampliamente utilizado en métodos numéricos.</li>
<li>Ayuda a evaluar la calidad de aproximaciones matemáticas.</li>
</ul>

<hr>

<h3>Desventajas</h3>

<ul>
<li>No puede calcularse cuando el valor real es cero.</li>
<li>Puede generar valores muy grandes con números pequeños.</li>
<li>Depende directamente de la exactitud del valor real.</li>
<li>Puede ser más difícil de interpretar que el error absoluto.</li>
</ul>

<hr>

<h3>¿En qué ramas de la ingeniería se utiliza?</h3>

<ul>

<li><b>Ingeniería en Sistemas Computacionales:</b> Evaluación de algoritmos numéricos y simulaciones.</li>

<li><b>Ingeniería Civil:</b> Análisis estructural y cálculos de precisión.</li>

<li><b>Ingeniería Mecánica:</b> Simulación matemática y análisis físico.</li>

<li><b>Ingeniería Electrónica:</b> Procesamiento de señales y mediciones.</li>

<li><b>Ingeniería Industrial:</b> Control estadístico y optimización.</li>

</ul>

<hr>

<h3>Ejemplo en Java</h3>

```java
public class ErrorRelativo {

    public static void main(String[] args) {

        double valorReal = 50;
        double valorAproximado = 49;

        double errorRelativo;

        errorRelativo = Math.abs(valorReal - valorAproximado) / valorReal;

        System.out.println("Valor real: " + valorReal);
        System.out.println("Valor aproximado: " + valorAproximado);
        System.out.println("Error relativo: " + errorRelativo);

        double errorPorcentual = errorRelativo * 100;

        System.out.println("Error porcentual: " + errorPorcentual + "%");
    }
}
```
<p align="right">
<a href="#indice">⬆ Volver al índice</a>
</p>
<hr>

<h2 id="eliminacion-gaussiana" align="center">
1. Eliminación Gaussiana
</h2>

<h3>¿Qué es?</h3>

<p>
La Eliminación Gaussiana es un método numérico utilizado para resolver sistemas de ecuaciones lineales. Su objetivo es transformar una matriz aumentada en una matriz triangular superior mediante operaciones elementales entre filas.
</p>

<p>
Después de convertir la matriz en forma escalonada, se utiliza el proceso de sustitución hacia atrás para encontrar el valor de las incógnitas.
</p>

<p>
Este método es ampliamente utilizado en álgebra lineal, programación científica y simulaciones matemáticas.
</p>

<hr>

<h3>Fórmulas</h3>

<h4>Sistema de ecuaciones lineales</h4>

<pre>
a11x1 + a12x2 + a13x3 = b1
a21x1 + a22x2 + a23x3 = b2
a31x1 + a32x2 + a33x3 = b3
</pre>

<h4>Factor de eliminación</h4>

<pre>
Factor = aji / aii
</pre>

<h4>Actualización de filas</h4>

<pre>
Fila_j = Fila_j - (Factor × Fila_i)
</pre>

<hr>

<h3>Ventajas</h3>

<ul>
<li>Permite resolver sistemas de ecuaciones lineales de manera ordenada.</li>
<li>Es un método exacto en muchos casos.</li>
<li>Puede implementarse fácilmente en programación.</li>
<li>Es útil para matrices grandes.</li>
</ul>

<hr>

<h3>Desventajas</h3>

<ul>
<li>Puede presentar errores de redondeo.</li>
<li>Consume muchos recursos en matrices muy grandes.</li>
<li>Puede fallar si existen divisiones entre cero.</li>
<li>La precisión depende del tipo de dato utilizado.</li>
</ul>

<hr>

<h3>¿En qué ramas de la ingeniería se utiliza?</h3>

<ul>

<li><b>Ingeniería en Sistemas Computacionales:</b> Desarrollo de algoritmos matemáticos y simulaciones.</li>

<li><b>Ingeniería Civil:</b> Análisis estructural y cálculo de fuerzas.</li>

<li><b>Ingeniería Mecánica:</b> Sistemas dinámicos y simulaciones físicas.</li>

<li><b>Ingeniería Electrónica:</b> Resolución de circuitos eléctricos.</li>

<li><b>Ingeniería Industrial:</b> Optimización y modelos matemáticos.</li>

</ul>

<hr>

<h3>Ejemplo en Java</h3>

```java
public class EliminacionGaussiana {

    public static void main(String[] args) {

        int n = 3;

        double[][] matriz = {
            {2, -1, 1, 8},
            {-3, -1, 2, -11},
            {-2, 1, 2, -3}
        };

        // Eliminación Gaussiana
        for (int i = 0; i < n; i++) {

            for (int j = i + 1; j < n; j++) {

                double factor = matriz[j][i] / matriz[i][i];

                for (int k = i; k < n + 1; k++) {

                    matriz[j][k] =
                    matriz[j][k] - factor * matriz[i][k];
                }
            }
        }

        // Sustitución hacia atrás
        double[] resultado = new double[n];

        for (int i = n - 1; i >= 0; i--) {

            resultado[i] = matriz[i][n];

            for (int j = i + 1; j < n; j++) {

                resultado[i] =
                resultado[i] - matriz[i][j] * resultado[j];
            }

            resultado[i] =
            resultado[i] / matriz[i][i];
        }

        // Mostrar resultados
        for (int i = 0; i < n; i++) {

            System.out.println("x" + (i + 1)
            + " = " + resultado[i]);
        }
    }
}
```
<p align="right">
<a href="#indice">⬆ Volver al índice</a>
</p>
<hr>

<h2 id="gauss-jordan" align="center">
2. Gauss-Jordan
</h2>

<h3>¿Qué es?</h3>

<p>
El método de Gauss-Jordan es una técnica numérica utilizada para resolver sistemas de ecuaciones lineales. Es una extensión de la Eliminación Gaussiana, pero en este método la matriz se transforma completamente hasta obtener una matriz identidad.
</p>

<p>
A diferencia de la Eliminación Gaussiana, el método de Gauss-Jordan elimina tanto los elementos debajo como encima del pivote, permitiendo obtener directamente los valores de las incógnitas sin necesidad de realizar sustitución hacia atrás.
</p>

<p>
Este método es ampliamente utilizado en álgebra lineal, programación científica y análisis matemático.
</p>

<hr>

<h3>Fórmulas</h3>

<h4>Sistema de ecuaciones lineales</h4>

<pre>
a11x1 + a12x2 + a13x3 = b1
a21x1 + a22x2 + a23x3 = b2
a31x1 + a32x2 + a33x3 = b3
</pre>

<h4>Normalización del pivote</h4>

<pre>
Fila_i = Fila_i / Pivote
</pre>

<h4>Eliminación de elementos</h4>

<pre>
Fila_j = Fila_j - (Factor × Fila_i)
</pre>

<hr>

<h3>Ventajas</h3>

<ul>
<li>Obtiene directamente las soluciones del sistema.</li>
<li>No requiere sustitución hacia atrás.</li>
<li>Es útil para calcular matrices inversas.</li>
<li>Puede implementarse fácilmente en programación.</li>
</ul>

<hr>

<h3>Desventajas</h3>

<ul>
<li>Consume más operaciones que la Eliminación Gaussiana.</li>
<li>Puede presentar errores de redondeo.</li>
<li>Es menos eficiente para matrices muy grandes.</li>
<li>Puede fallar si existen pivotes iguales a cero.</li>
</ul>

<hr>

<h3>¿En qué ramas de la ingeniería se utiliza?</h3>

<ul>

<li><b>Ingeniería en Sistemas Computacionales:</b> Algoritmos matemáticos y simulaciones.</li>

<li><b>Ingeniería Civil:</b> Cálculo estructural y análisis de fuerzas.</li>

<li><b>Ingeniería Mecánica:</b> Sistemas dinámicos y simulaciones físicas.</li>

<li><b>Ingeniería Electrónica:</b> Resolución de circuitos eléctricos.</li>

<li><b>Ingeniería Industrial:</b> Modelos matemáticos y optimización.</li>

</ul>

<hr>

<h3>Ejemplo en Java</h3>

```java
public class GaussJordan {

    public static void main(String[] args) {

        double[][] matriz = {
            {2, 1, -1, 8},
            {-3, -1, 2, -11},
            {-2, 1, 2, -3}
        };

        int filas = matriz.length;
        int columnas = matriz[0].length;

        for (int i = 0; i < filas; i++) {

            double pivote = matriz[i][i];

            // Convertir pivote en 1
            for (int j = 0; j < columnas; j++) {

                matriz[i][j] =
                matriz[i][j] / pivote;
            }

            // Hacer ceros en las demás filas
            for (int j = 0; j < filas; j++) {

                if (i != j) {

                    double factor = matriz[j][i];

                    for (int k = 0; k < columnas; k++) {

                        matriz[j][k] =
                        matriz[j][k] -
                        factor * matriz[i][k];
                    }
                }
            }
        }

        // Mostrar resultados
        System.out.println("Resultados:");

        for (int i = 0; i < filas; i++) {

            System.out.println("x" + (i + 1)
            + " = " + matriz[i][columnas - 1]);
        }
    }
}
```
<p align="right">
<a href="#indice">⬆ Volver al índice</a>
</p>
<hr>

<h2 id="gauss-seidel" align="center">
3. Gauss-Seidel
</h2>

<h3>¿Qué es?</h3>

<p>
El método de Gauss-Seidel es un método numérico iterativo utilizado para resolver sistemas de ecuaciones lineales. A diferencia de métodos directos como Eliminación Gaussiana o Gauss-Jordan, este método obtiene soluciones aproximadas mediante iteraciones sucesivas.
</p>

<p>
En cada iteración, los valores calculados se actualizan inmediatamente y se reutilizan en los siguientes cálculos, lo que generalmente permite una convergencia más rápida.
</p>

<p>
Este método es ampliamente utilizado en simulaciones numéricas, análisis matemático y programación científica.
</p>

<hr>

<h3>Fórmulas</h3>

<h4>Fórmula general de Gauss-Seidel</h4>

<pre>
xi(k+1) = (1 / aii)
[ bi - Σ(aij * xj) ]
</pre>

<p>
Donde:
</p>

<ul>
<li><b>aii</b> = elemento diagonal principal</li>
<li><b>bi</b> = término independiente</li>
<li><b>xj</b> = valores aproximados de las variables</li>
<li><b>k</b> = número de iteración</li>
</ul>

<h4>Criterio de error</h4>

<pre>
Error = |Valor nuevo - Valor anterior|
</pre>

<hr>

<h3>Ventajas</h3>

<ul>
<li>Requiere menos memoria que métodos directos.</li>
<li>Es eficiente para matrices grandes.</li>
<li>Puede converger rápidamente en ciertos sistemas.</li>
<li>Es sencillo de implementar en programación.</li>
</ul>

<hr>

<h3>Desventajas</h3>

<ul>
<li>No siempre converge.</li>
<li>Depende de una buena aproximación inicial.</li>
<li>Puede acumular errores numéricos.</li>
<li>La convergencia depende de la matriz del sistema.</li>
</ul>

<hr>

<h3>¿En qué ramas de la ingeniería se utiliza?</h3>

<ul>

<li><b>Ingeniería en Sistemas Computacionales:</b> Simulaciones numéricas y algoritmos matemáticos.</li>

<li><b>Ingeniería Civil:</b> Análisis estructural y resolución de sistemas grandes.</li>

<li><b>Ingeniería Mecánica:</b> Simulación de movimiento y dinámica.</li>

<li><b>Ingeniería Electrónica:</b> Análisis de circuitos eléctricos.</li>

<li><b>Ingeniería Industrial:</b> Optimización y modelado matemático.</li>

</ul>

<hr>

<h3>Ejemplo en Java</h3>

```java
public class GaussSeidel {

    public static void main(String[] args) {

        double[][] A = {
            {4, 1, 2},
            {3, 5, 1},
            {1, 1, 3}
        };

        double[] b = {4, 7, 3};

        double[] x = {0, 0, 0};

        int iteraciones = 10;

        for (int k = 0; k < iteraciones; k++) {

            x[0] = (b[0] - A[0][1] * x[1]
                    - A[0][2] * x[2]) / A[0][0];

            x[1] = (b[1] - A[1][0] * x[0]
                    - A[1][2] * x[2]) / A[1][1];

            x[2] = (b[2] - A[2][0] * x[0]
                    - A[2][1] * x[1]) / A[2][2];
        }

        System.out.println("Resultados:");

        for (int i = 0; i < x.length; i++) {

            System.out.println("x" + (i + 1)
            + " = " + x[i]);
        }
    }
}
```
<p align="right">
<a href="#indice">⬆ Volver al índice</a>
</p>
<hr>

<h2 id="jacobi" align="center">
4. Método de Jacobi
</h2>

<h3>¿Qué es?</h3>

<p>
El método de Jacobi es un método iterativo utilizado para resolver sistemas de ecuaciones lineales. Este método consiste en despejar cada variable de las ecuaciones del sistema y calcular nuevas aproximaciones utilizando únicamente los valores obtenidos en la iteración anterior.
</p>

<p>
Es ampliamente utilizado en métodos numéricos debido a que permite resolver sistemas grandes de ecuaciones de manera sencilla y organizada.
</p>

<p>
El método continúa realizando iteraciones hasta que el error entre una iteración y otra sea suficientemente pequeño.
</p>

<hr>

<h3>Fórmulas</h3>

<h4>Forma general del método de Jacobi</h4>

<pre>
x₁(k+1) = (b₁ - a₁₂x₂(k) - a₁₃x₃(k) - ... - a₁nxn(k)) / a₁₁

x₂(k+1) = (b₂ - a₂₁x₁(k) - a₂₃x₃(k) - ... - a₂nxn(k)) / a₂₂

...

xn(k+1) = (bn - an₁x₁(k) - an₂x₂(k) - ... - an(n-1)x(n-1)(k)) / ann
</pre>

<h4>Error aproximado</h4>

<pre>
Ea = |Valor actual - Valor anterior|
</pre>

<hr>

<h3>Ventajas</h3>

<ul>
<li>Es fácil de implementar.</li>
<li>Permite resolver sistemas grandes de ecuaciones.</li>
<li>Puede aplicarse en programación paralela.</li>
<li>No requiere transformar completamente la matriz.</li>
<li>Es útil para matrices diagonalmente dominantes.</li>
</ul>

<hr>

<h3>Desventajas</h3>

<ul>
<li>Puede tardar muchas iteraciones en converger.</li>
<li>No siempre garantiza convergencia.</li>
<li>Es menos rápido que otros métodos iterativos como Gauss-Seidel.</li>
<li>Depende mucho de los valores iniciales.</li>
<li>Puede generar errores acumulativos.</li>
</ul>

<hr>

<h3>¿En qué ramas de la ingeniería se utiliza?</h3>

<ul>

<li>
<b>Ingeniería en Sistemas Computacionales:</b>
Resolución de sistemas matemáticos y simulaciones numéricas.
</li>

<li>
<b>Ingeniería Civil:</b>
Análisis estructural y cálculo de cargas.
</li>

<li>
<b>Ingeniería Mecánica:</b>
Modelado de sistemas físicos y transferencia de calor.
</li>

<li>
<b>Ingeniería Electrónica:</b>
Análisis de circuitos eléctricos.
</li>

<li>
<b>Ingeniería Industrial:</b>
Optimización de procesos y modelos matemáticos.
</li>

</ul>

<hr>

<h3>Ejemplo en Java</h3>

```java
public class Jacobi {

    public static final double EPSILON = 0.0001;
    public static final int MAX_ITERACIONES = 100;

    public static void main(String[] args) {

        double[][] A = {
            {10, -1, 2},
            {-1, 11, -1},
            {2, -1, 10}
        };

        double[] B = {6, 25, -11};

        double[] X = metodoJacobi(A, B);

        System.out.println("Resultados:");

        for(int i = 0; i < X.length; i++) {
            System.out.println("x" + (i + 1) + " = " + X[i]);
        }
    }

    public static double[] metodoJacobi(double[][] A, double[] B) {

        int n = B.length;

        double[] X = new double[n];
        double[] nuevoX = new double[n];

        int iteracion = 0;
        boolean convergencia = false;

        while(!convergencia && iteracion < MAX_ITERACIONES) {

            for(int i = 0; i < n; i++) {

                double suma = B[i];

                for(int j = 0; j < n; j++) {

                    if(i != j) {
                        suma -= A[i][j] * X[j];
                    }
                }

                nuevoX[i] = suma / A[i][i];
            }

            double errorMaximo = 0;

            for(int i = 0; i < n; i++) {

                double error = Math.abs(nuevoX[i] - X[i]);

                if(error > errorMaximo) {
                    errorMaximo = error;
                }

                X[i] = nuevoX[i];
            }

            if(errorMaximo < EPSILON) {
                convergencia = true;
            }

            iteracion++;
        }

        return X;
    }
}
```
<p align="right">
<a href="#indice">⬆ Volver al índice</a>
</p>
<hr>

<h2 id="trapecio" align="center">
1. Método del Trapecio
</h2>

<h3>¿Qué es?</h3>

<p>
El Método del Trapecio es un método numérico utilizado para aproximar el valor de una integral definida. Este método consiste en dividir el área bajo una curva en pequeños trapecios y calcular el área de cada uno para obtener una aproximación del área total.
</p>

<p>
A diferencia de otros métodos más simples, como la suma de rectángulos, el Método del Trapecio ofrece una mejor aproximación debido a que considera la inclinación de la función entre dos puntos consecutivos.
</p>

<p>
Es uno de los métodos más utilizados en integración numérica por su facilidad de implementación y buena precisión en funciones continuas.
</p>

<hr>

<h3>Fórmulas</h3>

<h4>Fórmula del Método del Trapecio Simple</h4>

<pre>
∫ f(x) dx ≈ (b - a) / 2 * [f(a) + f(b)]
</pre>

<h4>Fórmula del Método del Trapecio Compuesto</h4>

<pre>
∫ f(x) dx ≈ h/2 * [f(x0) + 2f(x1) + 2f(x2) + ... + 2f(xn-1) + f(xn)]
</pre>

<h4>Donde:</h4>

<ul>
<li><b>a:</b> límite inferior.</li>
<li><b>b:</b> límite superior.</li>
<li><b>h:</b> tamaño del subintervalo.</li>
<li><b>f(x):</b> función a integrar.</li>
<li><b>n:</b> número de segmentos.</li>
</ul>

<hr>

<h3>Ventajas</h3>

<ul>
<li>Es fácil de entender e implementar.</li>
<li>Proporciona una mejor aproximación que el método rectangular.</li>
<li>Puede utilizarse en funciones continuas y suaves.</li>
<li>Reduce el error utilizando más subdivisiones.</li>
<li>Es útil para cálculos científicos y de ingeniería.</li>
</ul>

<hr>

<h3>Desventajas</h3>

<ul>
<li>Puede generar errores en funciones muy curvas.</li>
<li>Es menos preciso que métodos como Simpson.</li>
<li>Requiere más subdivisiones para mejorar la precisión.</li>
<li>La aproximación depende del tamaño del intervalo.</li>
<li>Puede acumular errores numéricos.</li>
</ul>

<hr>

<h3>¿En qué ramas de la ingeniería se utiliza?</h3>

<ul>

<li>
<b>Ingeniería en Sistemas Computacionales:</b>
Desarrollo de software científico y simulaciones numéricas.
</li>

<li>
<b>Ingeniería Civil:</b>
Cálculo de áreas, volúmenes y análisis estructural.
</li>

<li>
<b>Ingeniería Mecánica:</b>
Cálculo de trabajo, energía y transferencia de calor.
</li>

<li>
<b>Ingeniería Electrónica:</b>
Análisis de señales y procesamiento digital.
</li>

<li>
<b>Ingeniería Industrial:</b>
Modelado matemático y optimización de procesos.
</li>

</ul>

<hr>

<h3>Ejemplo en Java</h3>

```java
public class MetodoTrapecio {

    public static double funcion(double x) {
        return Math.pow(x, 2);
    }

    public static void main(String[] args) {

        double a = 0;
        double b = 4;
        int n = 4;

        double h = (b - a) / n;

        double suma = funcion(a) + funcion(b);

        for(int i = 1; i < n; i++) {

            double x = a + i * h;

            suma += 2 * funcion(x);
        }

        double resultado = (h / 2) * suma;

        System.out.println("Resultado aproximado: " + resultado);
    }
}
```
<p align="right">
<a href="#indice">⬆ Volver al índice</a>
</p>
<hr>

<h2 id="simpson13" align="center">
2. Método de Simpson 1/3
</h2>

<h3>¿Qué es?</h3>

<p>
El Método de Simpson 1/3 es un método numérico utilizado para aproximar integrales definidas. Este método mejora la precisión del Método del Trapecio utilizando parábolas para aproximar la curva de la función en lugar de líneas rectas.
</p>

<p>
El método divide el intervalo en segmentos pares y utiliza polinomios de segundo grado para calcular una aproximación más precisa del área bajo la curva.
</p>

<p>
Es ampliamente utilizado en métodos numéricos debido a su buena precisión y facilidad de implementación.
</p>

<hr>

<h3>Fórmulas</h3>

<h4>Fórmula del Método de Simpson 1/3</h4>

<pre>
∫ f(x) dx ≈ h/3 * [f(x0) + 4f(x1) + 2f(x2) + 4f(x3) + ... + f(xn)]
</pre>

<h4>Donde:</h4>

<ul>
<li><b>h:</b> tamaño del intervalo.</li>
<li><b>a:</b> límite inferior.</li>
<li><b>b:</b> límite superior.</li>
<li><b>n:</b> número de segmentos (debe ser par).</li>
<li><b>f(x):</b> función a integrar.</li>
</ul>

<h4>Cálculo del tamaño de intervalo</h4>

<pre>
h = (b - a) / n
</pre>

<hr>

<h3>Ventajas</h3>

<ul>
<li>Mayor precisión que el Método del Trapecio.</li>
<li>Reduce significativamente el error numérico.</li>
<li>Es eficiente para funciones suaves.</li>
<li>Fácil de implementar en programación.</li>
<li>Muy utilizado en cálculos científicos.</li>
</ul>

<hr>

<h3>Desventajas</h3>

<ul>
<li>El número de intervalos debe ser par.</li>
<li>Puede ser menos eficiente en funciones irregulares.</li>
<li>Requiere más operaciones matemáticas.</li>
<li>No es ideal para funciones discontinuas.</li>
<li>Puede acumular errores de redondeo.</li>
</ul>

<hr>

<h3>¿En qué ramas de la ingeniería se utiliza?</h3>

<ul>

<li>
<b>Ingeniería en Sistemas Computacionales:</b>
Simulación matemática y software científico.
</li>

<li>
<b>Ingeniería Civil:</b>
Cálculo de áreas y análisis estructural.
</li>

<li>
<b>Ingeniería Mecánica:</b>
Análisis de energía y dinámica de sistemas.
</li>

<li>
<b>Ingeniería Electrónica:</b>
Procesamiento de señales y análisis numérico.
</li>

<li>
<b>Ingeniería Industrial:</b>
Optimización y modelado de procesos.
</li>

</ul>

<hr>

<h3>Ejemplo en Java</h3>

```java
public class SimpsonUnoTercio {

    public static double funcion(double x) {
        return Math.pow(x, 2);
    }

    public static void main(String[] args) {

        double a = 0;
        double b = 4;
        int n = 4;

        double h = (b - a) / n;

        double suma = funcion(a) + funcion(b);

        for(int i = 1; i < n; i++) {

            double x = a + i * h;

            if(i % 2 == 0) {
                suma += 2 * funcion(x);
            } else {
                suma += 4 * funcion(x);
            }
        }

        double resultado = (h / 3) * suma;

        System.out.println("Resultado aproximado: " + resultado);
    }
}
```
<p align="right">
<a href="#indice">⬆ Volver al índice</a>
</p>
<hr>

<h2 id="simpson38" align="center">
3. Método de Simpson 3/8
</h2>

<h3>¿Qué es?</h3>

<p>
El Método de Simpson 3/8 es un método numérico utilizado para aproximar integrales definidas. Este método es una extensión del Método de Simpson 1/3 y utiliza polinomios cúbicos para aproximar el comportamiento de una función.
</p>

<p>
El método divide el intervalo en múltiples segmentos y utiliza grupos de tres subintervalos para calcular una aproximación más precisa del área bajo la curva.
</p>

<p>
Es especialmente útil cuando el número de intervalos es múltiplo de tres y se requiere una mayor precisión en los cálculos numéricos.
</p>

<hr>

<h3>Fórmulas</h3>

<h4>Fórmula del Método de Simpson 3/8</h4>

<pre>
∫ f(x) dx ≈ 3h/8 * [f(x0) + 3f(x1) + 3f(x2) + 2f(x3)
+ 3f(x4) + 3f(x5) + 2f(x6) + ... + f(xn)]
</pre>

<h4>Donde:</h4>

<ul>
<li><b>h:</b> tamaño del intervalo.</li>
<li><b>a:</b> límite inferior.</li>
<li><b>b:</b> límite superior.</li>
<li><b>n:</b> número de intervalos (debe ser múltiplo de 3).</li>
<li><b>f(x):</b> función a integrar.</li>
</ul>

<h4>Cálculo del tamaño de intervalo</h4>

<pre>
h = (b - a) / n
</pre>

<hr>

<h3>Ventajas</h3>

<ul>
<li>Ofrece una mayor precisión que el Método del Trapecio.</li>
<li>Permite aproximaciones eficientes en funciones suaves.</li>
<li>Utiliza polinomios cúbicos para mejorar resultados.</li>
<li>Reduce el error numérico.</li>
<li>Es útil en cálculos científicos y de ingeniería.</li>
</ul>

<hr>

<h3>Desventajas</h3>

<ul>
<li>El número de intervalos debe ser múltiplo de 3.</li>
<li>Requiere más operaciones matemáticas.</li>
<li>Puede ser complejo para funciones discontinuas.</li>
<li>Consume más tiempo de cálculo que métodos simples.</li>
<li>Puede acumular errores de redondeo.</li>
</ul>

<hr>

<h3>¿En qué ramas de la ingeniería se utiliza?</h3>

<ul>

<li>
<b>Ingeniería en Sistemas Computacionales:</b>
Simulación matemática y desarrollo de software científico.
</li>

<li>
<b>Ingeniería Civil:</b>
Cálculo de áreas, volúmenes y análisis estructural.
</li>

<li>
<b>Ingeniería Mecánica:</b>
Análisis de energía y transferencia de calor.
</li>

<li>
<b>Ingeniería Electrónica:</b>
Procesamiento digital de señales y análisis numérico.
</li>

<li>
<b>Ingeniería Industrial:</b>
Optimización y modelado de procesos industriales.
</li>

</ul>

<hr>

<h3>Ejemplo en Java</h3>

```java
public class SimpsonTresOctavos {

    public static double funcion(double x) {
        return Math.pow(x, 2);
    }

    public static void main(String[] args) {

        double a = 0;
        double b = 3;
        int n = 3;

        double h = (b - a) / n;

        double suma = funcion(a) + funcion(b);

        for(int i = 1; i < n; i++) {

            double x = a + i * h;

            if(i % 3 == 0) {
                suma += 2 * funcion(x);
            } else {
                suma += 3 * funcion(x);
            }
        }

        double resultado = (3 * h / 8) * suma;

        System.out.println("Resultado aproximado: " + resultado);
    }
}
```
<p align="right">
<a href="#indice">⬆ Volver al índice</a>
</p>
<hr>

<h2 id="cuadratura-gaussiana" align="center">
4. Método de la Cuadratura Gaussiana
</h2>

<h3>¿Qué es?</h3>

<p>
El Método de la Cuadratura Gaussiana es un método numérico utilizado para aproximar integrales definidas con una alta precisión. A diferencia de otros métodos de integración, este utiliza puntos específicos llamados nodos y valores llamados pesos para obtener resultados más exactos utilizando menos evaluaciones de la función.
</p>

<p>
La Cuadratura Gaussiana se basa en polinomios ortogonales y permite integrar exactamente ciertos polinomios de grado elevado.
</p>

<p>
Es uno de los métodos más precisos y eficientes en integración numérica y es ampliamente utilizado en aplicaciones científicas e ingenieriles.
</p>

<hr>

<h3>Fórmulas</h3>

<h4>Fórmula general de Cuadratura Gaussiana</h4>

<pre>
∫ f(x) dx ≈ Σ [wi * f(xi)]
</pre>

<h4>Donde:</h4>

<ul>
<li><b>wi:</b> pesos de integración.</li>
<li><b>xi:</b> nodos o puntos de evaluación.</li>
<li><b>f(x):</b> función a integrar.</li>
</ul>

<h4>Transformación de intervalo</h4>

<pre>
x = ((b - a) / 2) * t + ((b + a) / 2)
</pre>

<hr>

<h3>Ventajas</h3>

<ul>
<li>Ofrece una gran precisión con pocos puntos.</li>
<li>Reduce el error numérico.</li>
<li>Es más eficiente que otros métodos de integración.</li>
<li>Funciona muy bien en funciones suaves.</li>
<li>Muy utilizada en cálculos científicos avanzados.</li>
</ul>

<hr>

<h3>Desventajas</h3>

<ul>
<li>Es más compleja de implementar.</li>
<li>Requiere el uso de nodos y pesos especiales.</li>
<li>Puede ser difícil de entender para principiantes.</li>
<li>No siempre es adecuada para funciones discontinuas.</li>
<li>Consume más procesamiento en ciertos casos.</li>
</ul>

<hr>

<h3>¿En qué ramas de la ingeniería se utiliza?</h3>

<ul>

<li>
<b>Ingeniería en Sistemas Computacionales:</b>
Desarrollo de simulaciones científicas y análisis numérico.
</li>

<li>
<b>Ingeniería Civil:</b>
Análisis estructural y cálculo de áreas complejas.
</li>

<li>
<b>Ingeniería Mecánica:</b>
Transferencia de calor y análisis dinámico.
</li>

<li>
<b>Ingeniería Electrónica:</b>
Procesamiento de señales y sistemas digitales.
</li>

<li>
<b>Ingeniería Industrial:</b>
Optimización matemática y modelado de sistemas.
</li>

</ul>

<hr>

<h3>Ejemplo en Java</h3>

```java
public class CuadraturaGaussiana {

    public static double funcion(double x) {
        return Math.pow(x, 2);
    }

    public static void main(String[] args) {

        double[] nodos = {-0.5773502692, 0.5773502692};
        double[] pesos = {1.0, 1.0};

        double a = 0;
        double b = 3;

        double suma = 0;

        for(int i = 0; i < nodos.length; i++) {

            double x = ((b - a) / 2) * nodos[i] + ((b + a) / 2);

            suma += pesos[i] * funcion(x);
        }

        double resultado = ((b - a) / 2) * suma;

        System.out.println("Resultado aproximado: " + resultado);
    }
}
```
<p align="right">
<a href="#indice">⬆ Volver al índice</a>
</p>
<hr>

<h2 id="interpolacion-lineal" align="center">
1. Interpolación Lineal
</h2>

<h3>¿Qué es?</h3>

<p>
La interpolación lineal es un método numérico utilizado para estimar valores desconocidos dentro de un intervalo utilizando dos puntos conocidos. Este método supone que entre ambos puntos existe una línea recta.
</p>

<p>
Es una de las técnicas de interpolación más simples y utilizadas debido a su facilidad de implementación y rapidez de cálculo.
</p>

<p>
La interpolación lineal permite aproximar valores intermedios cuando no se dispone de todos los datos exactos de una función.
</p>

<hr>

<h3>Fórmulas</h3>

<h4>Fórmula de Interpolación Lineal</h4>

<pre>
f(x) = f(x0) + ((x - x0) / (x1 - x0)) * (f(x1) - f(x0))
</pre>

<h4>Donde:</h4>

<ul>
<li><b>x0 y x1:</b> puntos conocidos.</li>
<li><b>f(x0) y f(x1):</b> valores conocidos de la función.</li>
<li><b>x:</b> valor a interpolar.</li>
<li><b>f(x):</b> valor aproximado.</li>
</ul>

<hr>

<h3>Ventajas</h3>

<ul>
<li>Es fácil de entender e implementar.</li>
<li>Requiere pocos cálculos matemáticos.</li>
<li>Es rápida para obtener aproximaciones.</li>
<li>Funciona bien con datos cercanos.</li>
<li>Es útil en aplicaciones simples de ingeniería.</li>
</ul>

<hr>

<h3>Desventajas</h3>

<ul>
<li>Puede generar errores en funciones curvas.</li>
<li>Solo utiliza dos puntos para aproximar.</li>
<li>No es adecuada para datos complejos.</li>
<li>La precisión disminuye en intervalos grandes.</li>
<li>No representa correctamente comportamientos no lineales.</li>
</ul>

<hr>

<h3>¿En qué ramas de la ingeniería se utiliza?</h3>

<ul>

<li>
<b>Ingeniería en Sistemas Computacionales:</b>
Procesamiento de datos y simulaciones numéricas.
</li>

<li>
<b>Ingeniería Civil:</b>
Estimación de valores estructurales y topográficos.
</li>

<li>
<b>Ingeniería Mecánica:</b>
Análisis de movimiento y datos experimentales.
</li>

<li>
<b>Ingeniería Electrónica:</b>
Procesamiento digital de señales.
</li>

<li>
<b>Ingeniería Industrial:</b>
Análisis estadístico y optimización de procesos.
</li>

</ul>

<hr>

<h3>Ejemplo en Java</h3>

```java
public class InterpolacionLineal {

    public static double interpolar(
            double x0,
            double y0,
            double x1,
            double y1,
            double x) {

        return y0 + ((x - x0) / (x1 - x0)) * (y1 - y0);
    }

    public static void main(String[] args) {

        double x0 = 2;
        double y0 = 4;

        double x1 = 6;
        double y1 = 10;

        double x = 4;

        double resultado = interpolar(x0, y0, x1, y1, x);

        System.out.println("Valor interpolado: " + resultado);
    }
}
```
<p align="right">
<a href="#indice">⬆ Volver al índice</a>
</p>
<hr>

<h2 id="interpolacion-cuadratica" align="center">
2. Interpolación Cuadrática
</h2>

<h3>¿Qué es?</h3>

<p>
La interpolación cuadrática es un método numérico utilizado para aproximar valores desconocidos mediante una función polinómica de segundo grado. A diferencia de la interpolación lineal, este método utiliza tres puntos conocidos para construir una parábola que pase por dichos puntos.
</p>

<p>
La interpolación cuadrática proporciona una mejor aproximación cuando los datos presentan curvaturas o cambios no lineales.
</p>

<p>
Es ampliamente utilizada en análisis numérico y simulaciones matemáticas debido a su mayor precisión respecto a métodos lineales.
</p>

<hr>

<h3>Fórmulas</h3>

<h4>Polinomio cuadrático general</h4>

<pre>
P(x) = ax² + bx + c
</pre>

<h4>Forma de interpolación cuadrática</h4>

<pre>
P(x) = y0L0(x) + y1L1(x) + y2L2(x)
</pre>

<h4>Donde:</h4>

<ul>
<li><b>x0, x1, x2:</b> puntos conocidos.</li>
<li><b>y0, y1, y2:</b> valores conocidos de la función.</li>
<li><b>P(x):</b> valor interpolado.</li>
<li><b>L(x):</b> polinomios de interpolación.</li>
</ul>

<hr>

<h3>Ventajas</h3>

<ul>
<li>Mayor precisión que la interpolación lineal.</li>
<li>Representa mejor funciones curvas.</li>
<li>Permite aproximaciones más suaves.</li>
<li>Es útil para análisis matemáticos complejos.</li>
<li>Reduce errores en ciertos cálculos numéricos.</li>
</ul>

<hr>

<h3>Desventajas</h3>

<ul>
<li>Requiere más cálculos matemáticos.</li>
<li>Necesita al menos tres puntos conocidos.</li>
<li>Puede presentar oscilaciones en algunos casos.</li>
<li>Es más compleja de implementar.</li>
<li>No siempre mejora la precisión en grandes intervalos.</li>
</ul>

<hr>

<h3>¿En qué ramas de la ingeniería se utiliza?</h3>

<ul>

<li>
<b>Ingeniería en Sistemas Computacionales:</b>
Simulación matemática y procesamiento numérico.
</li>

<li>
<b>Ingeniería Civil:</b>
Modelado de estructuras y análisis topográfico.
</li>

<li>
<b>Ingeniería Mecánica:</b>
Análisis de trayectorias y movimiento.
</li>

<li>
<b>Ingeniería Electrónica:</b>
Procesamiento y análisis de señales.
</li>

<li>
<b>Ingeniería Industrial:</b>
Optimización de datos y análisis estadístico.
</li>

</ul>

<hr>

<h3>Ejemplo en Java</h3>

```java
public class InterpolacionCuadratica {

    public static double interpolar(
            double x0, double y0,
            double x1, double y1,
            double x2, double y2,
            double x) {

        double L0 = ((x - x1) * (x - x2)) /
                    ((x0 - x1) * (x0 - x2));

        double L1 = ((x - x0) * (x - x2)) /
                    ((x1 - x0) * (x1 - x2));

        double L2 = ((x - x0) * (x - x1)) /
                    ((x2 - x0) * (x2 - x1));

        return (y0 * L0) + (y1 * L1) + (y2 * L2);
    }

    public static void main(String[] args) {

        double x0 = 1;
        double y0 = 1;

        double x1 = 2;
        double y1 = 4;

        double x2 = 3;
        double y2 = 9;

        double x = 2.5;

        double resultado = interpolar(
                x0, y0,
                x1, y1,
                x2, y2,
                x);

        System.out.println("Valor interpolado: " + resultado);
    }
}
```
<p align="right">
<a href="#indice">⬆ Volver al índice</a>
</p>
<hr>

<h2 id="lagrange" align="center">
3. Interpolación Lagrange
</h2>

<h3>¿Qué es?</h3>

<p>
La interpolación de Lagrange es un método numérico utilizado para encontrar un polinomio que pase exactamente por un conjunto de puntos conocidos. Este método construye un polinomio de interpolación utilizando combinaciones de polinomios base llamados polinomios de Lagrange.
</p>

<p>
La interpolación de Lagrange es muy utilizada cuando se necesita aproximar funciones a partir de datos discretos sin resolver sistemas de ecuaciones.
</p>

<p>
Permite obtener una función polinómica capaz de estimar valores intermedios con buena precisión.
</p>

<hr>

<h3>Fórmulas</h3>

<h4>Fórmula general de Lagrange</h4>

<pre>
P(x) = Σ [ yi * Li(x) ]
</pre>

<h4>Polinomio base de Lagrange</h4>

<pre>
Li(x) = Π [(x - xj) / (xi - xj)]
</pre>

<h4>Donde:</h4>

<ul>
<li><b>P(x):</b> polinomio interpolador.</li>
<li><b>Li(x):</b> polinomio base.</li>
<li><b>xi, yi:</b> puntos conocidos.</li>
<li><b>x:</b> valor a interpolar.</li>
</ul>

<hr>

<h3>Ventajas</h3>

<ul>
<li>No requiere resolver sistemas de ecuaciones.</li>
<li>Permite interpolar múltiples puntos.</li>
<li>Ofrece buena precisión en funciones suaves.</li>
<li>Es útil en análisis numérico.</li>
<li>Puede implementarse fácilmente en programación.</li>
</ul>

<hr>

<h3>Desventajas</h3>

<ul>
<li>El polinomio puede volverse muy grande.</li>
<li>Puede presentar oscilaciones con muchos puntos.</li>
<li>Consume más tiempo de cálculo.</li>
<li>Es menos eficiente para grandes conjuntos de datos.</li>
<li>Los errores aumentan en intervalos amplios.</li>
</ul>

<hr>

<h3>¿En qué ramas de la ingeniería se utiliza?</h3>

<ul>

<li>
<b>Ingeniería en Sistemas Computacionales:</b>
Procesamiento numérico y simulaciones matemáticas.
</li>

<li>
<b>Ingeniería Civil:</b>
Análisis estructural y representación de datos.
</li>

<li>
<b>Ingeniería Mecánica:</b>
Modelado de trayectorias y sistemas físicos.
</li>

<li>
<b>Ingeniería Electrónica:</b>
Procesamiento digital de señales.
</li>

<li>
<b>Ingeniería Industrial:</b>
Análisis estadístico y optimización matemática.
</li>

</ul>

<hr>

<h3>Ejemplo en Java</h3>

```java
public class InterpolacionLagrange {

    public static double lagrange(
            double[] x,
            double[] y,
            double valorX) {

        double resultado = 0;

        for(int i = 0; i < x.length; i++) {

            double termino = y[i];

            for(int j = 0; j < x.length; j++) {

                if(i != j) {

                    termino *= (valorX - x[j]) /
                               (x[i] - x[j]);
                }
            }

            resultado += termino;
        }

        return resultado;
    }

    public static void main(String[] args) {

        double[] x = {1, 2, 3};
        double[] y = {1, 4, 9};

        double valorX = 2.5;

        double resultado = lagrange(x, y, valorX);

        System.out.println("Valor interpolado: " + resultado);
    }
}
```
<p align="right">
<a href="#indice">⬆ Volver al índice</a>
</p>
<hr>

<h2 id="newton" align="center">
4. Interpolación de Newton
</h2>

<h3>¿Qué es?</h3>

<p>
La interpolación de Newton es un método numérico utilizado para construir un polinomio que pase por un conjunto de puntos conocidos. Este método utiliza diferencias divididas para generar el polinomio interpolador de manera eficiente.
</p>

<p>
A diferencia de otros métodos de interpolación, la interpolación de Newton facilita agregar nuevos puntos sin necesidad de recalcular completamente el polinomio.
</p>

<p>
Es ampliamente utilizada en análisis numérico debido a su eficiencia y facilidad de implementación computacional.
</p>

<hr>

<h3>Fórmulas</h3>

<h4>Polinomio de Newton</h4>

<pre>
P(x) = f(x0)
+ (x - x0)f[x0,x1]
+ (x - x0)(x - x1)f[x0,x1,x2]
+ ...
</pre>

<h4>Diferencia dividida</h4>

<pre>
f[xi,xj] = (f(xj) - f(xi)) / (xj - xi)
</pre>

<h4>Donde:</h4>

<ul>
<li><b>P(x):</b> polinomio interpolador.</li>
<li><b>f[xi,xj]:</b> diferencia dividida.</li>
<li><b>x0, x1, x2:</b> puntos conocidos.</li>
<li><b>x:</b> valor a interpolar.</li>
</ul>

<hr>

<h3>Ventajas</h3>

<ul>
<li>Permite agregar nuevos puntos fácilmente.</li>
<li>Es eficiente computacionalmente.</li>
<li>Reduce cálculos repetitivos.</li>
<li>Ofrece buena precisión en aproximaciones.</li>
<li>Es muy utilizada en programación numérica.</li>
</ul>

<hr>

<h3>Desventajas</h3>

<ul>
<li>Puede presentar errores en muchos puntos.</li>
<li>El polinomio puede crecer demasiado.</li>
<li>Es sensible a errores de redondeo.</li>
<li>Puede generar oscilaciones.</li>
<li>Es más compleja que la interpolación lineal.</li>
</ul>

<hr>

<h3>¿En qué ramas de la ingeniería se utiliza?</h3>

<ul>

<li>
<b>Ingeniería en Sistemas Computacionales:</b>
Simulación numérica y desarrollo de software científico.
</li>

<li>
<b>Ingeniería Civil:</b>
Análisis de datos estructurales y topográficos.
</li>

<li>
<b>Ingeniería Mecánica:</b>
Modelado de sistemas físicos y trayectorias.
</li>

<li>
<b>Ingeniería Electrónica:</b>
Procesamiento digital de señales.
</li>

<li>
<b>Ingeniería Industrial:</b>
Análisis matemático y optimización de procesos.
</li>

</ul>

<hr>

<h3>Ejemplo en Java</h3>

```java
public class InterpolacionNewton {

    public static double calcularNewton(
            double[] x,
            double[] y,
            double valorX) {

        int n = x.length;

        double[][] diferencias = new double[n][n];

        for(int i = 0; i < n; i++) {
            diferencias[i][0] = y[i];
        }

        for(int j = 1; j < n; j++) {

            for(int i = 0; i < n - j; i++) {

                diferencias[i][j] =
                    (diferencias[i + 1][j - 1] -
                     diferencias[i][j - 1]) /
                    (x[i + j] - x[i]);
            }
        }

        double resultado = diferencias[0][0];

        for(int i = 1; i < n; i++) {

            double termino = diferencias[0][i];

            for(int j = 0; j < i; j++) {
                termino *= (valorX - x[j]);
            }

            resultado += termino;
        }

        return resultado;
    }

    public static void main(String[] args) {

        double[] x = {1, 2, 3};
        double[] y = {1, 4, 9};

        double valorX = 2.5;

        double resultado =
            calcularNewton(x, y, valorX);

        System.out.println(
            "Valor interpolado: " + resultado);
    }
}
```
<p align="right">
<a href="#indice">⬆ Volver al índice</a>
</p>
<hr>

<h2 id="euler" align="center">
1. Método de Euler
</h2>

<h3>¿Qué es?</h3>

<p>
El método de Euler es uno de los métodos numéricos más sencillos para resolver ecuaciones diferenciales ordinarias (EDO). Su funcionamiento consiste en aproximar el valor de una función utilizando la pendiente de la recta tangente en un punto conocido.
</p>

<p>
Este método parte de una condición inicial y calcula valores aproximados de la solución avanzando paso a paso mediante incrementos pequeños.
</p>

<p>
Es ampliamente utilizado en métodos numéricos debido a su simplicidad y facilidad de implementación en programación.
</p>

<hr>

<h3>Fórmulas</h3>

<h4>Fórmula general del método de Euler</h4>

<pre>
y(n+1) = y(n) + h * f(xn, yn)
</pre>

<h4>Donde:</h4>

<ul>
<li><b>y(n+1):</b> Valor aproximado siguiente.</li>
<li><b>y(n):</b> Valor actual.</li>
<li><b>h:</b> Tamaño del paso.</li>
<li><b>f(xn, yn):</b> Función derivada de la ecuación diferencial.</li>
</ul>

<hr>

<h3>Ventajas</h3>

<ul>
<li>Es fácil de entender e implementar.</li>
<li>Requiere pocos cálculos matemáticos.</li>
<li>Ideal para introducir el estudio de ecuaciones diferenciales numéricas.</li>
<li>Permite aproximar soluciones rápidamente.</li>
</ul>

<hr>

<h3>Desventajas</h3>

<ul>
<li>Puede generar errores grandes si el tamaño del paso es muy grande.</li>
<li>No es muy preciso comparado con otros métodos avanzados.</li>
<li>Los errores se acumulan en cada iteración.</li>
<li>Puede volverse inestable en algunos problemas.</li>
</ul>

<hr>

<h3>¿En qué ramas de la ingeniería se utiliza?</h3>

<ul>
<li><b>Ingeniería en Sistemas Computacionales:</b> Simulación matemática y modelado computacional.</li>
<li><b>Ingeniería Mecánica:</b> Simulación de movimiento y dinámica.</li>
<li><b>Ingeniería Civil:</b> Modelado de estructuras y vibraciones.</li>
<li><b>Ingeniería Electrónica:</b> Análisis de circuitos y señales.</li>
<li><b>Ingeniería Industrial:</b> Procesos de optimización y simulación.</li>
</ul>

<hr>

<h3>Ejemplo en Java</h3>

```java
public class MetodoEuler {

    // Función diferencial dy/dx = x + y
    public static double f(double x, double y) {
        return x + y;
    }

    public static void main(String[] args) {

        double x0 = 0;
        double y0 = 1;

        double h = 0.1;

        int pasos = 10;

        double x = x0;
        double y = y0;

        System.out.println("x\t y");

        for(int i = 0; i < pasos; i++) {

            System.out.println(x + "\t" + y);

            y = y + h * f(x, y);

            x = x + h;
        }
    }
}
```

<h1>ANIMACION DEL METODO EULER</h1>


https://github.com/user-attachments/assets/56f0d751-5512-4172-890e-dd05b3998abe


<p align="right">
<a href="#indice">⬆ Volver al índice</a>
</p>
<hr>

<h2 id="runge-kutta" align="center">
2. Método de Runge-Kutta
</h2>

<h3>¿Qué es?</h3>

<p>
El método de Runge-Kutta es un método numérico utilizado para resolver ecuaciones diferenciales ordinarias (EDO). Este método mejora considerablemente la precisión del método de Euler al calcular varias pendientes intermedias dentro de cada paso.
</p>

<p>
El método más utilizado es el de cuarto orden, conocido como RK4, debido a que ofrece un excelente equilibrio entre precisión y eficiencia computacional.
</p>

<p>
Runge-Kutta es ampliamente utilizado en simulaciones científicas, físicas e ingenieriles donde se requiere una aproximación numérica confiable.
</p>

<hr>

<h3>Fórmulas</h3>

<h4>Fórmulas del método Runge-Kutta de cuarto orden (RK4)</h4>

<pre>
k1 = h * f(xn, yn)

k2 = h * f(xn + h/2, yn + k1/2)

k3 = h * f(xn + h/2, yn + k2/2)

k4 = h * f(xn + h, yn + k3)

y(n+1) = yn + (1/6)(k1 + 2k2 + 2k3 + k4)
</pre>

<h4>Donde:</h4>

<ul>
<li><b>h:</b> Tamaño del paso.</li>
<li><b>f(xn, yn):</b> Función diferencial.</li>
<li><b>k1, k2, k3, k4:</b> Pendientes intermedias.</li>
<li><b>y(n+1):</b> Aproximación siguiente.</li>
</ul>

<hr>

<h3>Ventajas</h3>

<ul>
<li>Alta precisión en comparación con Euler.</li>
<li>Reduce considerablemente el error numérico.</li>
<li>Es estable para muchos problemas matemáticos.</li>
<li>No requiere derivadas de orden superior.</li>
</ul>

<hr>

<h3>Desventajas</h3>

<ul>
<li>Requiere más operaciones matemáticas.</li>
<li>Consume más tiempo computacional.</li>
<li>Puede ser complejo para principiantes.</li>
<li>En problemas muy grandes puede aumentar el costo computacional.</li>
</ul>

<hr>

<h3>¿En qué ramas de la ingeniería se utiliza?</h3>

<ul>
<li><b>Ingeniería en Sistemas Computacionales:</b> Simulaciones numéricas y modelado matemático.</li>
<li><b>Ingeniería Mecánica:</b> Simulación de sistemas dinámicos y movimiento.</li>
<li><b>Ingeniería Electrónica:</b> Análisis de circuitos y señales.</li>
<li><b>Ingeniería Aeroespacial:</b> Simulación de trayectorias y dinámica de vuelo.</li>
<li><b>Ingeniería Civil:</b> Modelado estructural y vibraciones.</li>
</ul>

<hr>

<h3>Ejemplo en Java</h3>

```java
public class RungeKutta {

    // Ecuación diferencial dy/dx = x + y
    public static double f(double x, double y) {
        return x + y;
    }

    public static void main(String[] args) {

        double x = 0;
        double y = 1;

        double h = 0.1;

        int pasos = 10;

        System.out.println("x\t y");

        for(int i = 0; i < pasos; i++) {

            System.out.println(x + "\t" + y);

            double k1 = h * f(x, y);

            double k2 = h * f(x + h/2, y + k1/2);

            double k3 = h * f(x + h/2, y + k2/2);

            double k4 = h * f(x + h, y + k3);

            y = y + (k1 + 2*k2 + 2*k3 + k4) / 6;

            x = x + h;
        }
    }
}
```
<p align="right">
<a href="#indice">⬆ Volver al índice</a>
</p>
<hr>

<h2 id="taylor" align="center">
3. Método de Taylor
</h2>

<h3>¿Qué es?</h3>

<p>
El método de Taylor es un método numérico utilizado para resolver ecuaciones diferenciales ordinarias mediante el uso de series de Taylor. Este método aproxima la solución de una función utilizando derivadas sucesivas evaluadas en un punto conocido.
</p>

<p>
La idea principal consiste en expandir la función en forma de serie y utilizar esa expansión para calcular valores aproximados de la solución.
</p>

<p>
El método de Taylor puede ofrecer resultados muy precisos cuando se utilizan suficientes términos de la serie.
</p>

<hr>

<h3>Fórmulas</h3>

<h4>Serie de Taylor</h4>

<pre>
f(x+h) = f(x) + h*f'(x) + (h²/2!)*f''(x)
       + (h³/3!)*f'''(x) + ...
</pre>

<h4>Fórmula del método de Taylor para EDO</h4>

<pre>
y(n+1) = yn + h*y' + (h²/2!)*y'' + (h³/3!)*y'''
</pre>

<h4>Donde:</h4>

<ul>
<li><b>h:</b> Tamaño del paso.</li>
<li><b>y':</b> Primera derivada.</li>
<li><b>y'':</b> Segunda derivada.</li>
<li><b>y''':</b> Tercera derivada.</li>
<li><b>y(n+1):</b> Aproximación siguiente.</li>
</ul>

<hr>

<h3>Ventajas</h3>

<ul>
<li>Ofrece alta precisión numérica.</li>
<li>Reduce el error de aproximación.</li>
<li>Permite mejores resultados que Euler en muchos casos.</li>
<li>Es útil para análisis matemáticos avanzados.</li>
</ul>

<hr>

<h3>Desventajas</h3>

<ul>
<li>Requiere calcular derivadas de orden superior.</li>
<li>Puede volverse complejo matemáticamente.</li>
<li>Consume más tiempo computacional.</li>
<li>No siempre es práctico para funciones complicadas.</li>
</ul>

<hr>

<h3>¿En qué ramas de la ingeniería se utiliza?</h3>

<ul>
<li><b>Ingeniería en Sistemas Computacionales:</b> Simulación matemática y algoritmos numéricos.</li>
<li><b>Ingeniería Mecánica:</b> Modelado de sistemas dinámicos.</li>
<li><b>Ingeniería Electrónica:</b> Procesamiento de señales y control automático.</li>
<li><b>Ingeniería Aeroespacial:</b> Simulación de trayectorias y dinámica.</li>
<li><b>Ingeniería Física:</b> Resolución de modelos matemáticos complejos.</li>
</ul>

<hr>

<h3>Ejemplo en Java</h3>

```java
public class MetodoTaylor {

    // Primera derivada
    public static double dydx(double x, double y) {
        return x + y;
    }

    // Segunda derivada
    public static double d2ydx2(double x, double y) {
        return 1 + dydx(x, y);
    }

    public static void main(String[] args) {

        double x = 0;
        double y = 1;

        double h = 0.1;

        int pasos = 10;

        System.out.println("x\t y");

        for(int i = 0; i < pasos; i++) {

            System.out.println(x + "\t" + y);

            y = y + h * dydx(x, y)
                    + (Math.pow(h, 2) / 2) * d2ydx2(x, y);

            x = x + h;
        }
    }
}
```
<p align="right">
<a href="#indice">⬆ Volver al índice</a>
</p>
