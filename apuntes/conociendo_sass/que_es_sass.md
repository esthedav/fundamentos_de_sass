# ¿Qué es SASS?

**SASS: Hojas de Estilo en Cascada con Sintaxis Mejorada**

### Introducción a SASS

SASS (Syntactically Awesome Stylesheets) es una extensión de CSS que permite escribir hojas de estilo de una manera más eficiente y estructurada. Aporta características adicionales que no están presentes en CSS tradicional, como variables, anidamiento, mixins, funciones y más. Estas funcionalidades facilitan la escritura y mantenimiento del código CSS, haciéndolo más modular y reutilizable.

### Variables

Las variables son uno de los pilares de SASS. Permiten almacenar valores que se pueden reutilizar a lo largo del código. Esto facilita la modificación y consistencia de estilos en un proyecto. Por ejemplo:

```scss
$color-primario: #3498db;
$fuente-principal: 'Roboto', sans-serif;

.elemento {
  color: $color-primario;
  font-family: $fuente-principal;
}
```

### Anidamiento

SASS permite anidar selectores, lo que ayuda a estructurar el código de manera más visual y jerárquica, evitando la repetición de nombres de selectores. Por ejemplo:

```scss
.nav {
  ul {
    list-style: none;
    padding: 0;

    li {
      display: inline-block;

      a {
        text-decoration: none;
        color: $color-primario;

        &:hover {
          color: darken($color-primario, 10%);
        }
      }
    }
  }
}
```

### Mixins

Los mixins son bloques de código reutilizables que pueden contener propiedades CSS. Se pueden parametrizar para adaptarse a diferentes situaciones. Por ejemplo:

```scss
@mixin bordes-redondeados($radio) {
  border-radius: $radio;
  -webkit-border-radius: $radio;
  -moz-border-radius: $radio;
}

.boton {
  @include bordes-redondeados(5px);
}
```

### Funciones

SASS incluye funciones que pueden realizar cálculos o manipular valores. Por ejemplo:

```scss
$base-font-size: 16px;

@function em($px, $base: $base-font-size) {
  @return ($px / $base) * 1em;
}

.texto-pequenio {
  font-size: em(12px);
}
```

### Importación y Partials

SASS permite dividir el código en archivos más pequeños y luego importarlos en un archivo principal. Estos archivos más pequeños se denominan "partials". Por ejemplo, si se tiene un archivo `_botones.scss` con estilos de botones:

```scss
// En _botones.scss
.boton {
  background-color: $color-primario;
  color: white;
  padding: 8px 16px;
}
```

Luego se pueden importar en el archivo principal:

```scss
// En archivo principal
@import 'botones';
```

### Directivas de Control

SASS ofrece directivas de control, como `@if`, `@for`, `@each` y `@while`, que permiten controlar el flujo de estilos de manera dinámica. Por ejemplo:

```scss
@for $i from 1 through 3 {
  .columna-#{$i} {
    width: 30% * $i;
  }
}
```

### Conclusiones

SASS es una herramienta poderosa que agrega funcionalidades avanzadas a la escritura de estilos CSS. Su uso puede mejorar significativamente la organización, mantenimiento y reutilización del código en proyectos web, facilitando la creación de hojas de estilo más eficientes y robustas.
