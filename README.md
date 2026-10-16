# Práctica 1: Juego del tenis

Proyecto de la asignatura **Sistemas Informáticos Industriales** (curso 2026-2027).

## Descripción

Juego de tenis para dos jugadores con en el mismo teclado, escrito en C++ con OpenGL y GLUT. En esta práctica se ha configurado el entorno de desarrollo en Linux (Git, CMake y Make) y se ha dado movimiento a las raquetas y a la esfera.

## Controles

- Raqueta izquierda: `w` (arriba) y `s` (abajo)
- Raqueta derecha: `o` (arriba) y `l` (abajo)

## Compilación y ejecución

    cd workspace
    mkdir build
    cd build
    cmake ..
    make
    ./tenis
    
## Práctica 2: comunicación con FIFO
- Nuevo programa `logger` que crea una tubería con nombre (`/tmp/FIFO_LOGGER`)
  y muestra por pantalla los mensajes que le envía el tenis.
- El tenis envía al logger, cada vez que se marca un punto, el jugador
  que lo ha marcado y el total de puntos que lleva.
- El juego termina cuando uno de los jugadores llega a 3 puntos, y el logger
  termina a la vez al detectar que se ha cerrado la tubería.

### Ejecución
1. En una terminal: `./logger` (siempre primero, porque crea la tubería).
2. En otra terminal: `./tenis`.

## Autora

Paula Verdejo Rodríguez
