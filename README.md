# Sistema de Ajedrez Inteligente - STM32F429 (Dual Core)
Diseño, montaje y programación de un tablero de ajedrez inteligente capaz de detectar el posicionamiento y movimiento de las piezas de forma autónoma. El sistema combina detección magnética, identificación por radiofrecuencia (NFC) y sensores de proximidad para crear un ecosistema de ajedrez interactivo. Además, integra una densa matriz de sensores con un sistema de iluminación dinámica para guiar al usuario durante la partida.

### 🔧 Hardware e Interfaces
- ***Protocolo SPI*** Control de la cadena de LEDs direccionables (APA102) integrados en el tablero para proporcionar retroalimentación visual de movimientos y estados y escaneo e identificación de piezas mediante tags NFC y lector RFID (RC522)
- ***Protocolo I2C:*** Gestión de una red de 64 sensores de efecto Hall (A1104) mediante el uso de expansores de GPIO (PCF8575) para el escaneo de la matriz de casillas. También se utiliza para la comunicación con el sensor de vuelo (VL6180X) que gestiona el cambio de turno.
- ***Protocolo UART/USART:*** Implementación del enlace de comunicación serie para la sincronización de datos y estados lógicos entre las dos tarjetas STM32F429ZI.

### 🏗️ Arquitectura de Software
- ***Sistema Operativo:*** Implementación de RTOS para la gestión de hilos prioritarios, garantizando una respuesta inmediata en el escaneo de la matriz y la detección de proximidad.
- ***Programación:*** Desarrollo modular en C, optimizado para el manejo de buses de comunicación y la gestión de estados del juego.
- ***Lógica de Detección:*** Programación modular en C que procesa los cambios de estado magnético y los valida mediante la identidad de la pieza detectada por NFC.

### 🚀 Funcionalidades Clave
- ***Identificación Automática:*** El sensor externo reconoce automáticamente qué pieza (rey, dama, peón) se debe colocar en cada casilla antes de comenzar o retomar una partida, gracias a la tecnología NFC.
- ***Gestión de Turnos por Gestos:*** Cambio de turno inteligente detectado mediante el sensor de vuelo (ToF) al finalizar un movimiento.
- ***Guiado Visual:*** Sistema de iluminación LED que indica casillas de origen, destino y posibles errores en la partida.

### 🛠️ Herramientas y Tecnología
- ***Sensores Especializados:*** RC522 (NFC), VL6180X (ToF).
- ***Microcontroladores:*** Dos (2) STM32F429 (NUCLEO-144).
- ***Técnicas de Laboratorio:*** Diseño y montaje electrónico, soldadura de precisión y validación de protocolos con instrumentación de laboratorio.

### 👥 Colaboradores
Proyecto académico desarrollado por Raúl Torres, Fabián Castro, Gonzalo Taravillo y Yuanze Li.
