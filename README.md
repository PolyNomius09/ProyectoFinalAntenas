# Proyecto de Antenas - Monitoreo en Tiempo Real

Este proyecto permite la visualización en tiempo real de datos recibidos por un módulo LoRa (SX1276) conectado a Arduino mediante un servidor Node.js.

## 📦 Estructura del Proyecto

- `/public/index.html`: Interfaz web (cliente)
- `dataGatheringJS.js`: Servidor Node.js que usa SerialPort y Socket.IO
- `package.json`: Manejo de dependencias con npm
- `Procfile`: Para despliegue en Render
- `.gitignore`: Exclusiones para Git

---

## 🔧 Requisitos

### 🖥️ Software necesario

| Software     | Versión recomendada | Enlace de descarga |
|--------------|---------------------|---------------------|
| Node.js      | v16.20.2            | [Descargar](https://nodejs.org/download/release/v16.20.2/) |
| npm          | v8.x (incluido con Node.js) | Incluido |
| Python       | 3.9.x (solo para pruebas opcionales) | [python.org](https://www.python.org/downloads/release/python-390/) |
| Arduino IDE  | Última versión       | [arduino.cc](https://www.arduino.cc/en/software) |

---

## 📥 Instalación del Proyecto

1. Clona este repositorio o descomprime el ZIP.

2. Abre una terminal y navega al directorio del proyecto:

```bash
cd proyecto-antenas
```

3. Instala las dependencias:

```bash
npm install
```

Esto instalará:
- `express`
- `serialport`
- `socket.io`

4. Ejecuta el servidor:

```bash
npm start
```

Abre tu navegador en:  
👉 `http://localhost:8080`

---

## 🌐 Despliegue en Línea (Render)

1. Sube este proyecto a GitHub.
2. Ve a [https://render.com](https://render.com)
3. Crea un nuevo Web Service:
   - Selecciona tu repositorio
   - Puerto: `8080`
   - Start command: `node dataGatheringJS.js`
4. Render generará una URL pública como:
   ```
   https://proyecto-antenas.onrender.com
   ```

---

## 🛰️ Cómo Funciona

1. Arduino envía datos por USB (COM4)
2. Node.js los recibe vía `serialport`
3. El servidor emite datos al navegador vía `socket.io`
4. El cliente HTML muestra los datos y gráficos en tiempo real

---

## 📋 Notas

- Asegúrate de que tu Arduino esté conectado al **puerto COM4** o cambia la configuración en `dataGatheringJS.js`.
- Usa `Chart.js` y `Bootstrap` incluidos en el HTML para visualización y estilo.
- Usa el script Python (`dataGathering.py`) solo si deseas pruebas rápidas del puerto serial.

