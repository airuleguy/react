# 🍔 Los class component

## Introducción

Utilizar la sintaxis de class es una de las formas más comunes de definir un componente React. Las class en javascript se introdujeron en ECMAScript 2015 con el objetivo de tener una sintaxis mucho más clara y simple para crear objetos y lidiar con la herencia.

Para crear un class component utilizaremos la herencia ya que extenderemos de una class llamada [Component que viene con react.](https://reactjs.org/docs/react-component.html)

Gracias a extender de esta clase podremos hacer cosas cómo manejar el state del componente, escuchar el ciclo de vida, etc. Cosas que vamos a ir viendo a lo largo del workshop.

## Creando un class component

Veamos un ejemplo básico de cómo sería un class component.

```javascript
import React, { Component } from 'react';

class MyComponent extends Component {
  render() {
    return (
      <div>Hello word</div>
    );
  }
}

export default MyComponent;
```

Cómo verás importamos Component para poder extenderlo. El método render de nuestro componente es el que va a dibujar en el HTML la UI. Siempre debe retornar algo\(react element, string, null, etc\).

### Leyendo propiedades

En secciones anteriores habíamos dicho que todo componente de react recibía una serie de props y retornaba un react element. Los class component también reciben props y devuelven un react element\(con el método render\).

Veamos un ejemplo de cómo leemos las props en un class component.

```javascript
import React, { Component } from 'react';
​
class MyComponent extends Component {
  render() {
    return (
      <div>{this.props.content}</div>
    );
  }
}
​
export default MyComponent;
```

Cómo verás, las props las tenemos dentro de **this**, es la única diferencia con el resto de los components.

### Ejecutando class methods

Es muy común que los eventos de los class components estén escritos en un método de la class, veamos un ejemplo:

```javascript
import React, { Component } from 'react';
​
class MyComponent extends Component {
  constructor() {
    this.execute = this.execute.bind(this);
  }
  
  execute(event) {
    console.log('click');
  }

  render() {
    return (
      <button onClick={this.execute}>
        Label
      </button>
    );
  }
}
​
export default MyComponent;
```

Cómo verás. la sintaxis es super limpia. Más adelante iremos viendo más características de este tipo de compenente, para aprender más [puedes ingresar aquí](https://reactjs.org/docs/react-component.html).

## Práctico

Llevemos esto a la práctica!

{% embed data="{\"url\":\"https://github.com/workshopsjsmvd/react/tree/master/practico/steps/class-components\",\"type\":\"link\",\"title\":\"workshopsjsmvd/react\",\"description\":\"react - Workshop sobre React\",\"icon\":{\"type\":\"icon\",\"url\":\"https://github.com/fluidicon.png\",\"aspectRatio\":0},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://avatars1.githubusercontent.com/u/38766393?s=400&v=4\",\"width\":240,\"height\":240,\"aspectRatio\":1}}" %}


