# Proyecto de Antenas - Monitoreo en Tiempo Real

Este proyecto permite la visualización en tiempo real de datos recibidos por un módulo LoRa (SX1276) conectado a Arduino mediante un servidor Node.js.

## Estructura

- `/public/index.html`: Interfaz web
- `dataGatheringJS.js`: Servidor Node.js que usa SerialPort y Socket.IO
- `package.json`: Dependencias del proyecto

## Requisitos

- Node.js v16.20.2
- npm v8.x
- Arduino conectado por USB (COM4)

## Instrucciones

```bash
npm install
npm start
```

Abre `http://localhost:8080` o despliega con [Render](https://render.com).
