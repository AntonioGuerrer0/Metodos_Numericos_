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
<a href="#errores-numericos">Errores Numéricos</a>

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
<a href="#sistemas-ecuaciones">Sistemas de Ecuaciones</a>

<ul>
<li><a href="#eliminacion-gaussiana">Eliminación Gaussiana</a></li>
<li><a href="#gauss-jordan">Gauss-Jordan</a></li>
<li><a href="#gauss-seidel">Gauss-Seidel</a></li>
<li><a href="#jacobi">Método de Jacobi</a></li>
</ul>

</li>

<li>
<a href="#metodos-integracion">Métodos de Integración</a>

<ul>
<li><a href="#trapecio">Método del Trapecio</a></li>
<li><a href="#simpson13">Método de Simpson 1/3</a></li>
<li><a href="#simpson38">Método de Simpson 3/8</a></li>
<li><a href="#cuadratura-gaussiana">Método de la Cuadratura Gaussiana</a></li>
</ul>

</li>

<li>
<a href="#interpolacion">Interpolación</a>

<ul>
<li><a href="#interpolacion-lineal">Interpolación Lineal</a></li>
<li><a href="#interpolacion-cuadratica">Interpolación Cuadrática</a></li>
<li><a href="#lagrange">Interpolación Lagrange</a></li>
<li><a href="#newton">Interpolación de Newton</a></li>
</ul>

</li>

<li>
<a href="#ecuaciones-diferenciales">Ecuaciones Diferenciales</a>

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

<p align="right">
<a href="#indice">⬆ Volver al índice</a>
</p>

<hr>

<h2 id="perdida-precision" align="center">
2. Pérdida de precisión
</h2>

<p>
Aquí va tu contenido sobre Pérdida de precisión.
</p>

<p align="right">
<a href="#indice">⬆ Volver al índice</a>
</p>

<hr>

<h2 id="comparacion-directa" align="center">
3. Comparación directa
</h2>

<p>
Aquí va tu contenido sobre Comparación directa.
</p>

<p align="right">
<a href="#indice">⬆ Volver al índice</a>
</p>

<hr>

<h2 id="cancelacion-resta" align="center">
4. Cancelación de resta
</h2>

<p>
Aquí va tu contenido sobre Cancelación de resta.
</p>

<p align="right">
<a href="#indice">⬆ Volver al índice</a>
</p>

<hr>

<h2 id="desbordamiento" align="center">
5. Desbordamiento
</h2>

<p>
Aquí va tu contenido sobre Desbordamiento.
</p>

<p align="right">
<a href="#indice">⬆ Volver al índice</a>
</p>

<hr>

<h2 id="conversion-estrecha" align="center">
6. Conversión estrecha
</h2>

<p>
Aquí va tu contenido sobre Conversión estrecha.
</p>

<p align="right">
<a href="#indice">⬆ Volver al índice</a>
</p>

<hr>

<h2 id="error-absoluto" align="center">
7. Error absoluto
</h2>

<p>
Aquí va tu contenido sobre Error absoluto.
</p>

<p align="right">
<a href="#indice">⬆ Volver al índice</a>
</p>

<hr>

<h2 id="error-relativo" align="center">
8. Error relativo
</h2>

<p>
Aquí va tu contenido sobre Error relativo.
</p>

<p align="right">
<a href="#indice">⬆ Volver al índice</a>
</p>

<hr>

<h1 id="sistemas-ecuaciones" align="center">
Sistemas de Ecuaciones
</h1>

<h2 id="eliminacion-gaussiana" align="center">
1. Eliminación Gaussiana
</h2>

<p>
Aquí va tu contenido de Eliminación Gaussiana.
</p>

<p align="right">
<a href="#indice">⬆ Volver al índice</a>
</p>

<hr>

<h2 id="gauss-jordan" align="center">
2. Gauss-Jordan
</h2>

<p>
Aquí va tu contenido de Gauss-Jordan.
</p>

<p align="right">
<a href="#indice">⬆ Volver al índice</a>
</p>

<hr>

<h2 id="gauss-seidel" align="center">
3. Gauss-Seidel
</h2>

<p>
Aquí va tu contenido de Gauss-Seidel.
</p>

<p align="right">
<a href="#indice">⬆ Volver al índice</a>
</p>

<hr>

<h2 id="jacobi" align="center">
4. Método de Jacobi
</h2>

<p>
Aquí va tu contenido de Jacobi.
</p>

<p align="right">
<a href="#indice">⬆ Volver al índice</a>
</p>

<hr>

<h1 id="metodos-integracion" align="center">
Métodos de Integración
</h1>

<h2 id="trapecio" align="center">
Método del Trapecio
</h2>

<p>
Aquí va tu contenido del Método del Trapecio.
</p>

<p align="right">
<a href="#indice">⬆ Volver al índice</a>
</p>

<hr>

<h2 id="simpson13" align="center">
Método de Simpson 1/3
</h2>

<p>
Aquí va tu contenido del Método de Simpson 1/3.
</p>

<p align="right">
<a href="#indice">⬆ Volver al índice</a>
</p>

<hr>

<h2 id="simpson38" align="center">
Método de Simpson 3/8
</h2>

<p>
Aquí va tu contenido del Método de Simpson 3/8.
</p>

<p align="right">
<a href="#indice">⬆ Volver al índice</a>
</p>

<hr>

<h2 id="cuadratura-gaussiana" align="center">
Método de la Cuadratura Gaussiana
</h2>

<p>
Aquí va tu contenido de Cuadratura Gaussiana.
</p>

<p align="right">
<a href="#indice">⬆ Volver al índice</a>
</p>

<hr>

<h1 id="interpolacion" align="center">
Interpolación
</h1>

<h2 id="interpolacion-lineal" align="center">
1. Interpolación Lineal
</h2>

<p>
Aquí va tu contenido de Interpolación Lineal.
</p>

<p align="right">
<a href="#indice">⬆ Volver al índice</a>
</p>

<hr>

<h2 id="interpolacion-cuadratica" align="center">
2. Interpolación Cuadrática
</h2>

<p>
Aquí va tu contenido de Interpolación Cuadrática.
</p>

<p align="right">
<a href="#indice">⬆ Volver al índice</a>
</p>

<hr>

<h2 id="lagrange" align="center">
3. Interpolación Lagrange
</h2>

<p>
Aquí va tu contenido de Interpolación Lagrange.
</p>

<p align="right">
<a href="#indice">⬆ Volver al índice</a>
</p>

<hr>

<h2 id="newton" align="center">
4. Interpolación de Newton
</h2>

<p>
Aquí va tu contenido de Interpolación de Newton.
</p>

<p align="right">
<a href="#indice">⬆ Volver al índice</a>
</p>

<hr>

<h1 id="ecuaciones-diferenciales" align="center">
Ecuaciones Diferenciales
</h1>

<h2 id="euler" align="center">
1. Euler
</h2>

<p>
Aquí va tu contenido del método de Euler.
</p>

<p align="right">
<a href="#indice">⬆ Volver al índice</a>
</p>

<hr>

<h2 id="runge-kutta" align="center">
2. Runge-Kutta
</h2>

<p>
Aquí va tu contenido de Runge-Kutta.
</p>

<p align="right">
<a href="#indice">⬆ Volver al índice</a>
</p>

<hr>

<h2 id="taylor" align="center">
3. Taylor
</h2>

<p>
Aquí va tu contenido del método de Taylor.
</p>

<p align="right">
<a href="#indice">⬆ Volver al índice</a>
</p>

<hr>
