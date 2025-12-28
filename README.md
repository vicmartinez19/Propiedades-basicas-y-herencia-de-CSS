# Propiedades-basicas-de-CSS
Aprendiendo propiedades de CSS basicas y herencias
# Proyecto: Evolución de Estilos y Posicionamiento (Clase 3)

Este proyecto es una actualización de la página web básica anterior, enfocada en el control avanzado de CSS mediante herencia, especificidad y esquemas de posicionamiento.

## 🎯 Objetivos de esta entrega
* Implementar **herencia** de estilos globales.
* Integrar tipografías externas mediante **Google Fonts**.
* Aplicar posicionamiento avanzado: `sticky`, `relative` y `absolute`.
* Resolver conflictos de **especificidad** y cascada.

### 1. Implementación de Herencia y Cascada
En este proyecto, utilicé la herencia para gestionar la tipografía base de la página.

Decisión técnica: Apliqué font-family: 'Times New Roman' en el selector body. Esto permite que todos los elementos hijos, como las descripciones de las tarjetas y los textos de los botones, hereden automáticamente este estilo sin necesidad de repetirlo en cada clase.

Uso de fuentes externas: Incorporé la clase .gideon-roman-regular para el título principal. Aquí la cascada decidió que el estilo específico de la clase ganara sobre el estilo general del cuerpo.

### 2. Dominando la Especificidad
Para las tarjetas de perfil y de Google Play, utilicé selectores combinados.

Ejemplo: Al usar .card-perfil .descripcion, aseguré una mayor especificidad que un simple selector de etiqueta p. Esto garantiza que si en el futuro agrego más párrafos fuera de las tarjetas, no se vean afectados por los estilos exclusivos del perfil.

### 3. Esquemas de Posicionamiento
Siguiendo los objetivos del día, implementé tres tipos de posicionamiento para sacar los elementos del flujo natural:

position: fixed (Navegación): La clase .navbar-mejorado utiliza un posicionamiento fijo en el tope (top: 0). Gracias al z-index: 1000, la barra se mantiene siempre visible por encima de las tarjetas mientras el usuario hace scroll.

position: relative y absolute (Insignia de verificado): * Establecí .avatar-container como relative para crear un marco de referencia.

Posicioné la .badge-verificado como absolute con coordenadas bottom: 5px y right: 5px. Esto permitió "clavar" la insignia azul exactamente en la esquina de la foto de perfil sin desplazar el nombre del alumno hacia abajo.