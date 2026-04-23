# 📘 La Biblia del Desarrollo Web (Cheat Sheet Detallado)

Este documento es tu guía definitiva y detallada con todas las variaciones de código posibles para lo que hemos aprendido hasta el momento.

---

## Estructura de una Etiqueta y de una Página We

### 1.1 Etiquetas Básicas

- **Encabezados:** Jerarquía desde `<h1>` hasta `<h6>`.
  - _Regla:_ Solo un `<h1>` por documento para SEO.
- **Párrafos y Listas:**
  - `<p>Mi texto</p>`
  - Desordenada: `<ul><li>Elemento 1</li></ul>`
  - Ordenada: `<ol><li>Elemento 1</li></ol>`

### ⚡ Reto #1: "Tu Perfil de Desarrollador"

Como estamos yendo "paso a paso", vamos a crear tu primera estructura. No te preocupes por los colores todavía, solo por la estructura.

**Objetivo:** Crear una página simple con tu información personal.

- Un título principal con tu nombre.
- Un subtítulo que diga "Sobre mí".
- Un párrafo breve contando que estudias Ingeniería en Electrónica.
- Un subtítulo que diga "Mis herramientas favoritas".
- Una lista desordenada con 3 herramientas que uses (ej. Raspberry Pi, VS Code, Python).
- Una lista ordenada con tus 3 objetivos de este curso (ej. 1. Aprender Semántica, 2. Dominar Flexbox, 3. Subir mi web).

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>RETO #1</title>
  </head>
  <body>
    <h1>Arturo Knezevich</h1>
    <h2>Sobre mí</h2>
    <p>
      Hola soy estudiante de Ingeniera Electrónica y Automatización Industrial
      me apasiona la tecnlogía el uso de herramientas IA que permitan mejorar
      los sistemas productivos y la calidad de servicios de una empresa
    </p>
    <h2>Mis herramientas favoritas</h2>
    <ul>
      <li>Raspberry PI</li>
      <li>Antigravity</li>
      <li>Python</li>
      <li>Node-Red</li>
    </ul>
    <ol>
      <li>Aprender a programar un SCADA COMPLETO</li>
      <li>Aprender HTML & CSS</li>
      <li>Aprender JavaScript</li>
      <li>Aprender VUE.JS</li>
    </ol>
  </body>
</html>
```

### 🔗 Enlaces, 🖼️ Imágenes y Rutas

Estos elementos son los que hacen que una web sea "Hipertexto" (que puedas saltar de un lugar a otro).

- **Enlaces (`<a>`):**
  ```html
  <a href="https://google.com">Link normal</a>
  <a href="https://google.com" target="_blank">Abre nueva pestaña</a>
  <a href="mailto:correo@correo.com">Abre app de correo</a>
  <a href="tel:+123456789">Abre app de teclado numérico</a>
  <a href="#mi-id">Salta a otra sección de la página</a>
  ```
- **Imágenes (`<img>`):** Requiren `src` y `alt` siempre.
  ```html
  <!-- loading="lazy" retrasa la carga hasta hacer scroll -->
  <img src="foto.jpg" alt="Descripción para ciegos" loading="lazy" />
  ```
- **Rutas:**
  - **Ruta Absoluta:** Es la ruta completa de un archivo en internet. Se empieza con `https://` o `http://`.
  - **Ruta Relativa:** Es la ruta de un archivo con respecto al archivo actual. Se empieza con `./` o `../`.

### ⚡ Reto #2: "Conectando mi Perfil"

Vamos a evolucionar tu código anterior. Tu misión es añadir lo siguiente:

- **Imagen de perfil:** Añade una imagen después de tu nombre. Puedes usar una de internet (como una de un circuito o un logo de ingeniería) o una foto tuya si la tienes en la misma carpeta.
  - **Tip:** Si no tienes una, usa esta de prueba: `https://cdn-icons-png.flaticon.com/512/606/606200.png`

- **Enlace a LinkedIn o GitHub:** Debajo de tu párrafo "Sobre mí", añade un enlace que diga "Visita mi perfil profesional". Debe abrirse en una pestaña nueva.
- **Anclas internas** (Opcional - Nivel Pro): Haz que en tu lista de objetivos, la palabra "JavaScript" sea un enlace que lleve a la página oficial de MDN sobre JS: https://developer.mozilla.org/es/docs/Web/JavaScript.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>RETO #1</title>
  </head>
  <body>
    <h1>Arturo Knezevich</h1>
    <img src="https://cdn-icons-png.flaticon.com/512/606/606200.png" alt="" />
    <h2>Sobre mí</h2>
    <p>
      Hola soy estudiante de Ingeniera Electrónica y Automatización Industrial
      me apasiona la tecnlogía el uso de herramientas IA que permitan mejorar
      los sistemas productivos y la calidad de servicios de una empresa
    </p>
    <a href="https://ec.linkedin.com/" target="_blank"
      >Visita mi perfil profesional</a
    >
    <h2>Mis herramientas favoritas</h2>
    <ul>
      <li>Raspberry PI</li>
      <li>Antigravity</li>
      <li>Python</li>
      <li>Node-Red</li>
    </ul>
    <ol>
      <li>Aprender a programar un SCADA COMPLETO</li>
      <li>Aprender HTML & CSS</li>
      <li>
        Aprender
        <a
          href="https://developer.mozilla.org/es/docs/Web/JavaScript"
          target="_blank"
          >JavaScript</a
        >
      </li>
      <li>Aprender VUE.JS</li>
    </ol>
  </body>
</html>
```

### 📝 Formularios (El último paso de HTML Básico)

- **Cajas de texto (`<input>`):**
  ```html
  <input type="text" placeholder="Tu nombre" />
  <input type="password" placeholder="Tu contraseña" />
  <input type="email" placeholder="correo@ejemplo.com" />
  <input type="number" min="1" max="10" />
  ```
- **Caja grande y Menús Desplegables:**

  ```html
  <textarea rows="4" cols="50">Escribe un párrafo...</textarea>

  <select name="opciones">
    <option value="1">Opción 1</option>
    <option value="2">Opción 2</option>
  </select>
  ```

- **Agrupadores y Accesibilidad:**
  El `<label>` se asocia via `for` y `id`. Todo se envuelve en un `<fieldset>` con un `<legend>`.
  ```html
  <fieldset>
    <legend>Datos Personales</legend>
    <label for="nombre">Dime tu nombre</label>
    <input type="text" id="nombre" />
  </fieldset>
  ```

### ⚡Reto #3: "Interfaz de Control de Usuario"

Imagina que estás diseñando una pequeña interfaz para registrar una nueva máquina en tu sistema de automatización. Vamos a añadir un formulario al final de tu documento actual (debajo de la lista ordenada).

- Tu tarea es crear un formulario que contenga:
  - Un campo de texto para el "Nombre de la Máquina".
  - Un campo de número para la "Dirección IP" (o un ID numérico).
  - Un botón que diga "Registrar Equipo".

```html
<form>
  <label>Nombre de la máquina:</label>
  <input type="text" placeholder="Ej: Bomba 1" />

  <br />
  <button type="submit">Enviar</button>
</form>
```

### 1.4 HTML Semántico (Adiós a los Divs infinitos)

- `<header>`: Inicio de la página o de un artículo.
- `<nav>`: Bloque de enlaces de navegación (Menú principal).
- `<main>`: El contenido protagonista de la página, solo hay uno.
- `<article>`: Contenido que tiene sentido por sí mismo (Noticia de blog).
- `<section>`: Agrupador temático de contenido.
- `<footer>`: Pie de página.

---

## 🎨 Parte 2: CSS BÁSICO E INTERMEDIO (Estilos y Arquitectura)

### 🎨 CSS BÁSICO: Introducción y Selectores

CSS (Cascading Style Sheets) es lo que le da "estilo" a tu estructura. Si el HTML es el esqueleto de tu tablero de control, el CSS es la pintura, las luces y la forma de los botones.

El Selector, la Propiedad y el Valor
Para cambiar algo, necesitas esta estructura en tu archivo .css:

```css
selector {
  propiedad: valor;
}

h1 {
  color: blue;
  font-size: 24px;
}
```

### ⚡ Reto Final de hoy: "Primeros Colores"

Tu misión:
Añade un bloque de estilos que haga lo siguiente:

-   Que el cuerpo (body) tenga un color de fondo gris claro (puedes usar `background-color: lightgrey;`).
-   Que tu nombre (h1) sea de color azul marino (`navy`).
-   Que todos los subtítulos (h2) tengan una fuente diferente (usa `font-family: Arial;`).
-   Que el botón tenga el fondo verde y el texto blanco.

```html
<head>
    <style>
        body {
            background-color: #f0f0f0;
        }
        button {
            background-color: green;
            color: white;
        }
    </style>
</head>
```

### SOLUCIÓN

```css
body {
  background-color: lightgray;
}

h1 {
  color: navy;
}

h2 {
  font-family: Arial;
}

button {
  background-color: green;
  color: white;
}
```



### 2.1 El Modelo de Caja (Box Model) Detallado

Todo elemento es cuadrado.

- **Reset Universal:** Imprescindible en todo proyecto.
  ```css
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box; /* Previene que el padding modifique el tamaño real de la caja */
  }
  ```
- **Padding (Relleno Interior):**

  ```css
  /* Individuales */
  padding-top: 10px;
  padding-right: 20px;
  padding-bottom: 10px;
  padding-left: 20px;

  /* Shorthands (Atajos) */
  padding: 10px; /* Aplica a los 4 lados */
  padding: 10px 20px; /* Arriba/Abajo 10px, Derecha/Izquierda 20px */
  padding: 10px 20px 30px 40px; /* Arriba, Derecha, Abajo, Izquierda (Las agujas del reloj) */
  ```

- **Margin (Espaciado Exterior):** Funciona igual que padding (`margin-top`, etc).
  - _Truco de centrado:_ `margin: 0 auto;` centra cajas en medio de la pantalla.
- **Borders y Radius:**

  ```css
  /* Borde largo */
  border-width: 2px;
  border-style: solid; /* solid, dashed, dotted, double */
  border-color: red;

  /* Borde Atajo (El más usado) */
  border: 2px solid red;
  border-bottom: 5px dashed blue; /* Poner borde a un solo lado */

  /* Redondear esquinas */
  border-radius: 10px; /* 4 esquinas */
  border-radius: 50%; /* Crea un círculo perfecto si la caja es cuadrada */
  ```

### ⚡ Reto #4: "Dando forma a tu interfaz"

Vamos a aplicar esto a tu archivo de ayer. Abre tu styles.css y modifica tus reglas para que se vea profesional:
1. **Margen Global:**Agrega esto al principio para que todo use el modelo de caja correcto:
```css
* {
  box-sizing: border-box;
}
```

2. **El formulario:**Vamos a hacer que parezca una tarjeta de control real:
```css
form {
  background-color: white;
  padding: 20px;          /* Espacio interno */
  border: 2px solid navy; /* El borde */
  border-radius: 8px;     /* Bordes redondeados */
  margin-top: 20px;       /* Separarlo de la lista de arriba */
  width: 300px;           /* Ancho fijo */
}
```
3. **Inputs:**Haz que los campos de texto ocupen todo el ancho y tengan espacio para respirar:
```css
input {
  display: block;        /* Para que ocupen su propia línea */
  width: 100%;           /* Todo el ancho del formulario */
  margin-bottom: 15px;   /* Separación entre inputs */
  padding: 8px;
}
```






### 🎨 Fondos, Gradientes y Sombras

- **Fondos (`background`):**

  ```css
  background-color: #ff0000; /* HEX Puro */
  background-color: rgb(255, 0, 0); /* RGB Puro */
  background-color: rgba(
    255,
    0,
    0,
    0.5
  ); /* RGB con Opacidad (50% transparente) */

  /* Degradados Lineales */
  background-image: linear-gradient(to right, red, blue);
  ```

- **Sombras (`box-shadow`):**
  ```css
  /* EjeX EjeY Difuminado Propagación Color */
  box-shadow: 0px 4px 10px 2px rgba(0, 0, 0, 0.3);
  ```


### ⚡ Reto #5: "Efecto Industrial"

Vamos a aplicar esto a tu botón y a tu formulario para que parezca un panel de control moderno.

**Tu misión es actualizar estas dos reglas en tu CSS:**
1. **Botón con Gradiente:** Cambia el `background-color: green` por un gradiente que vaya de un verde oscuro a uno más claro.
```css
button {
  background: linear-gradient(135deg, #28a745, #5cd65c);
  border: none;
  padding: 10px 20px;
  border-radius: 5px;
  cursor: pointer; /* Cambia el ratón a una mano */
  transition: 0.3s; /* Para que el cambio sea suave */
}
```

2. **Formulario con Sombra:** Dale elevación a tu "tarjeta" de registro.
```css
form {
  /* Mantén lo anterior y agrega esto: */
  box-shadow: 0 10px 25px rgba(0, 0, 0, 0.2);
  border: none; /* Podemos quitar el borde navy si ya tenemos sombra */
}
```
3. **Efecto de Presión (Opcional):** Añade esto para que cuando pases el mouse sobre el botón, cambie un poco:

```css
button:hover {
  transform: scale(1.05); /* Se agranda un poquito */
  filter: brightness(1.1); /* Brilla más */
}
```


### 2.3 Selectores Compuestos y BEM

- **Selectores:**

  ```css
  p {
  } /* Etiqueta */
  .caja {
  } /* Clase */
  #unico {
  } /* ID */

  div p {
  } /* Descendiente: Todos los <p> dentro de cualquier <div> */
  div > p {
  } /* Hijo Directo: Solo los <p> que sean hijos INMEDIATOS del <div> */
  h1 + p {
  } /* Hermano adyacente: El <p> inmediatamente debajo del <h1> */
  ```

- **Metodología BEM (Bloque\_\_Elemento--Modificador):**
  Nomenclatura profesional para clases:
  ```html
  <button class="boton boton--rojo">
    <span class="boton__icono"></span>
    Texto
  </button>
  ```

### 2.4 Comportamiento de Diseño (`display` y Textos)

- **Display:**
  - `block`: Ocupan el 100% del ancho de la fila (ej. `<div>`).
  - `inline`: Fluyen como letras. NO respetan ancho, alto ni márgneres arriba/abajo (ej. `<span>`, `<a>`).
  - `inline-block`: Fluyen en línea, pero SÍ respetan ancho, alto y márgenes. Ideal para botones.
  - `none`: Desaparece de pantalla.
- **Trucos de Texto e Imágenes:**

  ```css
  /* Evitar desbordes de palabras gigantes */
  word-wrap: break-word;

  /* Truncar texto y agregar "..." */
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;

  /* Que las fotos no se aplasten si el width y height son fijos */
  object-fit: cover; /* Recorta preservando proporción */
  object-position: center; /* Enfoca el centro */
  ```


### Organización de Formularios: fieldset, legend y datalist
Cuando tienes muchos parámetros (por ejemplo, configuración de red, límites de alarma y datos del motor), no puedes poner todos los inputs sueltos. Necesitas agruparlos.

- **fieldset**: Crea un recuadro que agrupa elementos relacionados.
- **legend**: Es el título de ese recuadro.
- **datalist**: Es como un "autocompletado". El usuario puede escribir o elegir de una lista predefinida.

### Multimedia y Carga Eficiente (Lazy Loading)
Para tus proyectos de monitoreo:

- `<video>` y `<audio>`: Ya no necesitas plugins externos. Puedes embeber un stream de una cámara o una alerta sonora directamente.

- **Lazy Loading** (`loading="lazy"`): Es un atributo para imágenes y iframes. Le dice al navegador: "no cargues esta imagen hasta que el usuario haga scroll cerca de ella". Esto ahorra ancho de banda y hace tu web más rápida.

### Detalles y Resúmenes: <details> y <summary>

Esto es oro puro para interfaces de ingeniería. Te permite crear secciones que se despliegan y se contraen sin usar una sola línea de JavaScript.

**<details>**: Envuelve todo el contenido. Por defecto está cerrado.

**<summary>**: Debe ser la primera línea dentro del details. Es el título que se ve siempre.

```html
<details>
    <summary>Ver configuración avanzada del PLC</summary>
    <p>IP: 192.168.0.10 | Puerto: 502 (Modbus)</p>
</details>
```

### ⚡ Reto #6: "Formulario de Configuración Técnica"
Vamos a actualizar tu archivo index.html. Vamos a simular que este es el panel para configurar un nodo de Node-RED o un equipo en la planta.

**Tu misión es crear un nuevo formulario (o modificar el anterior) que incluya:**

- Un <fieldset> con un <legend> que diga "Parámetros del Sistema".

- Dentro, un <label> y un <input> con un <datalist> para que el usuario elija el "Protocolo de Comunicación" (opciones: MQTT, Modbus, OPC UA, HTTP).

- Usa la etiqueta <details> debajo del formulario para ocultar información técnica como "Manual de Usuario" o "Notas de mantenimiento".

- Añade una imagen de un componente electrónico (puedes usar la de ayer) pero esta vez agrégale el atributo loading="lazy".



**<details>** : Envuelve todo el contenido. Por defecto está cerrado.

**<summary>** : Debe ser la primera línea dentro del details. Es el título que se ve siempre.

```html
<details>
    <summary>Ver configuración avanzada del PLC</summary>
    <p>IP: 192.168.0.10 | Puerto: 502 (Modbus)</p>
</details>
```

### 🏁 Cierre de HTML Avanzado: Semántica y Accesibilidad

Como mencionaste al inicio que aún no dominabas la semántica, vamos a darle el toque final a tu código para que sea 100% profesional.

Actualmente, tu código tiene todos los elementos sueltos en el body. Un experto organiza su código usando contenedores que describen el contenido.

**Etiquetas de Estructura (Semántica):**

- `<header>`: Para tu nombre y foto (el encabezado de tu perfil).
- `<main>`: Para el contenido principal (Sobre mí, herramientas, objetivos y el formulario).
- `<section>`: Para agrupar cada bloque lógico (ej. una sección para el formulario de registro).
- `<footer>`: Para datos de contacto o derechos de autor al final.

Accesibilidad (A11y):
Añadir alt="Descripción" a las imágenes no es solo por si no cargan, es para que los lectores de pantalla le digan a una persona con discapacidad visual qué hay en la imagen.

### ⚡ Reto #7: "Refactorización Semántica"

Este es el último paso para graduarte de HTML. Vamos a envolver tu código actual en estas etiquetas.

Tu misión es reordenar tu código así:

- Envuelve tu nombre (h1) y tu imagen de perfil en un <header>.
- Envuelve todo lo demás (desde "Sobre mí" hasta el formulario) en un <main>.
- Dentro del <main>, coloca el formulario dentro de una <section>.
- Añade un <footer> al final de todo que diga: © 2026 - Arturo Knezevich | Ingeniería en Electrónica.
- Bonus: Asegúrate de que todas tus imágenes tengan un alt descriptivo (ej: alt="Icono de engranaje y tecnología").




### 2.5 Magias Vivas: Pseudoclases y Transiciones

- **Estado e Interactividad:**
  ```css
  a:hover { ... } /* Puntero encima */
  input:focus { outline: 2px solid blue; } /* Al hacer clic adentro */
  li:first-child { ... } /* El primero de la lista */
  ```
- **Animando Suavemente (`transition`):** Si a la clase `.boton` le metes color rojo en el `:hover`, el cambio es seco.
  ```css
  .boton {
    /* Propiedad, Duración, Ritmo */
    transition: background-color 0.3s ease;
    /* shortcut: transition: all 0.3s ease; */
  }
  ```

### 2.6 Ubicaciones y Layouts (`position`)

Propiedad crítica del CSS intermedio que saca a los elementos de su flujo natural:

- `position: static`: El estado normal y pasivo de todos.
- `position: relative`: Conserva su lugar en el flujo, pero te permite "moverlo" usando `top`, `bottom`, `left`, `right`. Además, encierra como "cárcel" a sus hijos absolutos.
- `position: absolute`: Flota desconectado del flujo real de la página. Se rige por el ancestro con posición relativa más cercano que tenga.
- `position: fixed`: Flota pegado a la pantalla. Nunca se mueve aunque hagas scroll.
- `position: sticky`: Es normal hasta que haces scroll, luego se pega al borde de la pantalla.
- `z-index: 100;`: Define el orden de las capas 3D. El número más alto está al frente de la pantalla.


### Metodología BEM (Block, Element, Modifier)
Para que tu código no sea un caos cuando crezca (como en tus proyectos de Power BI o Node-RED), usamos BEM. Es una forma de nombrar clases:

- **Block**: El componente (.card)
- **Element**: Parte del componente (.card__button)
- **Modifier**: Una versión diferente (.card__button--red)

### ⚡ Reto #8: "El Panel de Control Flotante"
Vamos a aplicar estos conceptos a tu perfil. Vamos a crear un "Badge" o insignia de estado que flote sobre tu formulario, simulando un indicador de "Sistema Online".

Tu misión en el CSS:

- **Prepara el padre**: Asegúrate de que tu form tenga `position: relative;`.
- **Crea el indicador**: Añade un pequeño div (o span) dentro de tu formulario en el HTML que diga "ONLINE".
- **Posiciónalo**:
```css
/* Clase usando BEM */
.form__status {
  position: absolute;
  top: -10px;
  right: -10px;
  background-color: #28a745;
  color: white;
  padding: 5px 10px;
  border-radius: 20px;
  font-size: 12px;
  font-weight: bold;
  box-shadow: 0 4px 6px rgba(0,0,0,0.1);
}
```

- **Sticky Footer**: Haz que tu footer sea sticky o fixed al fondo de la página.


### Pseudoclases: El estado de los elementos
- **Pseudoclases** son selectores especiales que identifican el estado de un elemento. Permiten aplicar estilos diferentes según la situación del usuario o del documento.
- **Principales Pseudoclases**:
  - **:hover**: Se activa cuando el puntero del mouse está sobre el elemento.
  - **:active**: Se activa cuando el elemento está siendo presionado (por ejemplo, un botón).
  - **:focus**: Se activa cuando el elemento recibe el foco (por ejemplo, un campo de formulario al hacer clic en él).
  - **:visited**: Se activa en los enlaces que ya han sido visitados por el usuario.
  - **:link**: Se activa en los enlaces que aún no han sido visitados.
  - **:first-child**: Selecciona el primer hijo de un elemento padre.
  - **:last-child**: Selecciona el último hijo de un elemento padre.
  - **:nth-child(n)**: Selecciona el n-ésimo hijo de un elemento padre.


### ⚡ Reto #9: "Interactividad de Tablero"
Vamos a hacer que tu interfaz responda al usuario como un SCADA real.

Tu misión en el CSS:

- Feedback de Escritura: Haz que cuando hagas clic en un input, el borde cambie de color y brille un poco.

```css
input:focus {
  outline: none;
  border: 2px solid #28a745;
  box-shadow: 0 0 8px rgba(40, 167, 69, 0.4);
}
```

- **Cebra en las Listas**: Vamos a darle un estilo diferente a los elementos pares de tu lista de herramientas para que sea más legible.

```css
li:nth-child(even) {
  color: navy;
  font-weight: bold;
}
```

- **Ajuste del Footer**: Tu footer tiene `position: sticky`. Para que funcione, el contenedor padre debe ser lo suficientemente largo para permitir el scroll. Por ahora, asegúrate de que el texto del footer esté centrado con `text-align: center;`.



### Introducción a Flexbox
- **Flexbox** es un sistema de layout bidimensional que permite distribuir y alinear elementos en un contenedor.
- **Propiedades del contenedor**:
  - `display: flex;`: Activa el modo flexbox.
  - `flex-direction: row;` | `row-reverse;` | `column;` | `column-reverse;`: Define la dirección de los elementos.
  - `justify-content: flex-start;` | `flex-end;` | `center;` | `space-between;` | `space-around;` | `space-evenly;`: Define la alineación en el eje principal.
  - `align-items: flex-start;` | `flex-end;` | `center;` | `stretch;` | `baseline;`: Define la alineación en el eje transversal.
  - `flex-wrap: nowrap;` | `wrap;` | `wrap-reverse;`: Define si los elementos se envuelven en varias líneas.
  - `gap: 10px;`: Define el espacio entre los elementos.

Conceptos Clave:
- **Flex Container**: El padre (donde pones display: flex).

- **Flex Items**: Los hijos directos que se alinearán.

- **Eje Principal (Main Axis)**: Por defecto es horizontal (filas).

- **Eje Cruzado (Cross Axis)**: Por defecto es vertical.

### Alineación en los Ejes
Aquí es donde ocurre la magia:

- **justify-content**: Alinea los hijos en el eje principal (horizontal por defecto).
  - **center**, **space-between** (espacio en medio), **space-around**.
- **align-items**: Alinea los hijos en el eje cruzado (vertical por defecto).
  - **center**, **flex-start**, **flex-end**.


### ⚡ Reto #10: "El Header Profesional"

Vamos a transformar tu encabezado. Actualmente, tu nombre y tu imagen están uno debajo del otro. Vamos a usar Flexbox para que se vean como una barra de navegación real, con el nombre a un lado y la foto al otro.

Tu misión en el CSS:

Convierte el Header en Flex:

```css
header {
  display: flex;
  justify-content: space-between; /* Empuja los elementos a los extremos */
  align-items: center;           /* Los centra verticalmente */
  background-color: navy;
  padding: 10px 40px;
  color: white;
  border-radius: 0 0 15px 15px;  /* Redondea solo las esquinas de abajo */
}
```

- Ajusta la imagen: Dale un tamaño pequeño para que quepa bien en la barra.

```css
header img {
  width: 50px;
  height: 50px;
  border-radius: 50%; /* La hace circular */
  border: 2px solid white;
}
```
Color del H1: Como el fondo del header ahora es azul (navy), asegúrate de que el h1 dentro del header sea blanco.