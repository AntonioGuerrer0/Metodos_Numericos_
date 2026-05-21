# Metodos_Numericos_
Problemario de Métodos Numéricos

Realizado por:
<li>José Antonio Guerrero Lazcano</li>
<li>Gabriela Hernández Juárez</li>

# Sobre la materia

<h2 align = "center">
<font size = "+6">
<a name="Competencia_de_la_Asignatura">Competencia de la asignatura</a>
</font>
</h2>

Aplica los métodos numéricos para resolver problemas científicos y de ingeniería utilizando la computadora.

<h2 align = "center">
<font size = "+6">
<a name="Significado_Metodos_Numericos">Significado de Métodos Numéricos</a>
</font>
</h2>

Técnicas matemáticas que se utilizan para formular problemas de manera que puedan resolverse mediante operaciones aritméticas.

---

<h2 align = "center">
<font color = "darkorange" size = "+6" font face = "bauhaus 93">
Índice
</font>
</h2>

<header>
<font color = "red" size="+1" font face = "aharoni">

<nav class="navegacion">

<ul class="Indice">

<li><a href="#Competencia_de_la_Asignatura">Competencia de la Asignatura</a></li>

<li><a href="#Significado_Metodos_Numericos">Significado de Métodos Numéricos</a></li>

<li><a href="#TEMA1">TEMA 1 - Errores en Métodos Numéricos</a></li>

<li><a href="#Competencia_Tema1">Competencia del Tema 1</a></li>

<ul class="subindice">

<li><a href="#redondeo">Error de redondeo</a></li>

<li><a href="#precision">Pérdida de precisión</a></li>

<li><a href="#comparacion">Comparación directa</a></li>

<li><a href="#cancelacion">Cancelación de resta</a></li>

<li><a href="#desbordamiento">Desbordamiento</a></li>

<li><a href="#conversion">Conversión estrecha</a></li>

<li><a href="#absoluto">Error absoluto</a></li>

<li><a href="#relativo">Error relativo</a></li>

</ul>

</ul>

</nav>

</font>
</header>

---

<h1 align = "center">
<font font face = "bauhaus 93">
<a name="TEMA1">TEMA 1</a>
</font>
</h1>

<h2 align = "center">
<font size = "+6">
<a name="Competencia_Tema1">Competencia del tema</a>
</font>
</h2>

Aplica los métodos numéricos con el objeto de solucionar ecuaciones mediante los métodos de intervalo e interpolación apoyada de un lenguaje de programación.

---

<h1 align = "center">
<font font face = "bauhaus 93">
ERRORES
</font>
</h1>

---

<h2 align = "center">
<font font face = "forte">
<a name="redondeo">1. Error de redondeo</a>
</font>
</h2>

<h3>¿Qué es?</h3>

El error de redondeo ocurre cuando un número tiene demasiados decimales y la computadora debe aproximarlo a una cantidad limitada de cifras.

<h3>Fórmula</h3>

Error = Valor real - Valor aproximado

<h3>¿Dónde se utiliza?</h3>

<ul>
<li>Cálculos científicos</li>
<li>Simulaciones numéricas</li>
<li>Operaciones financieras</li>
<li>Programación matemática</li>
</ul>

<h3>Errores básicos que pueden ocurrir</h3>

<ul>
<li>Pérdida de exactitud en operaciones repetitivas</li>
<li>Diferencias mínimas entre resultados esperados</li>
<li>Acumulación de errores</li>
</ul>

<h3>Ventajas</h3>

<ul>
<li>Reduce espacio de almacenamiento</li>
<li>Hace más rápidos los cálculos</li>
</ul>

<h3>Desventajas</h3>

<ul>
<li>Disminuye la precisión</li>
<li>Puede alterar resultados importantes</li>
</ul>

<h3><b><i>Ejemplo en código Java</i></b></h3>

```java
public class Redondeo {

    public static void main(String[] args) {

        double numero = 10.0 / 3.0;

        System.out.println("Número original: " + numero);

        double redondeado = Math.round(numero * 100.0) / 100.0;

        System.out.println("Número redondeado: " + redondeado);
    }
}
