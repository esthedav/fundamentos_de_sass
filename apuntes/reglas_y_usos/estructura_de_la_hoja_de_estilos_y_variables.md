# Estructura de la hoja de estilos y variables

---

## Top-level statements

Solo se pueden utilizar en la parte superior de una hoja de estilos

* Imports
* Definición de un `Mixin`
* Definición de una `Función`
* Módulos

---

## Universal statements

* Variables, estructuras de control y las reglas: `@error, @warn y @debug`
* **Declaraciones CSS:** Reglas de estilo, At-rules y Mixins.

---

## Tipos de variables

Se declaran utilizando el símbolo `$` de la siguiente manera:

```scss
$primary-color: blue;
$secondary-color: green;
$tertiary-color: purple;
```

### CSS variables VS Sass variables

| CSS variables | Sass variables |
| ------------- | -------------- |
| Pueden tener diferentes valores para distintos elementos | Tienen un valor único correspondiente a un elemento |
| Son declarativas | Son imperativas |

---

## Shadowing



