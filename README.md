# Servidor de WebSockets
Este es un breve README para configurar y ejecutar un servidor de WebSockets utilizando Node.js.

## Requisitos
Node.js instalado en tu sistema.

## Instalación

1.Clona este repositorio en tu máquina local:
````bash
git clone <URL_del_repositorio>
````

2. Navega hasta el directorio del repositorio:
````bash
cd <nombre_del_directorio>
````

3.Instala las dependencias:
````bash
npm install
````
## Uso

Ejecuta el servidor:
````bash
npm run dev
````

El servidor estará ahora escuchando en el puerto especificado (por defecto es 5000).

## Ejemplo de Cliente
javascript
````bash
const socket = new WebSocket('ws://localhost:3000');

// Evento cuando la conexión se establece
socket.addEventListener('open', function (event) {
    console.log('Conexión establecida');
    // Envía un mensaje al servidor
    socket.send('Hola servidor!');
});

// Evento para recibir mensajes del servidor
socket.addEventListener('message', function (event) {
    console.log('Mensaje del servidor:', event.data);
});

// Evento cuando se cierra la conexión
socket.addEventListener('close', function (event) {
    console.log('Conexión cerrada');
});
````

## Contribución
¡Siéntete libre de contribuir abriendo issues o enviando pull requests!

## Autor
Norbory

## Licencia
Este proyecto está bajo la Licencia.
