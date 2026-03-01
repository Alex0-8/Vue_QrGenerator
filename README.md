[English Version](#english)

# 📱 Text to QR – Generador de códigos QR

<div align="center">
  <a href="https://vuejs.org/"><img src="https://img.shields.io/badge/Vue-4FC08D?logo=vue.js&logoColor=white&style=flat-square" alt="Vue 3" /></a>
  <a href="https://www.javascript.com/"><img src="https://img.shields.io/badge/JavaScript-yellow?logo=javascript&logoColor=black&style=flat-square" alt="JavaScript" /></a>
  <a href="https://www.npmjs.com/package/qrcode"><img src="https://img.shields.io/badge/qrcode-lib-blue?logo=npm&logoColor=white&style=flat-square" alt="qrcode" /></a>
  <a href="https://alex0-8.github.io/Vue_QrGenerator/"><img src="https://img.shields.io/badge/Live%20Demo-brightgreen?logo=vercel&logoColor=white&style=flat-square" alt="Live demo" /></a>
</div>

---

**Text to QR** fue mi primer proyecto con **Vue 3**. La app permite escribir o pegar texto y genera un código QR en tiempo real usando la librería **qrcode**. Ideal para aprender reactividad y manipulación de canvas en Vue.

🔗 **Demo en vivo** → [Vue QrGenerator/](https://alex0-8.github.io/Vue_QrGenerator/)

---

## ✨ Características principales

- Generación instantánea de QR conforme se tipean caracteres
- Opción para limpiar el campo o pegar desde portapapeles
- Código QR dibujado en `<canvas>` con colores personalizados
- Librería ligera (`qrcode`) sin dependencias pesadas
- Estilos básicos en CSS con diseño centrado y responsivo
- Proyecto inicial con Vue CLI

---

## 🛠️ Stack Tecnológico

| Categoría          | Tecnología / Herramienta                          | Notas                                      |
|--------------------|---------------------------------------------------|--------------------------------------------|
| Framework          | Vue 3                                            | Composición básica con `data`, `watch`     |
| Lenguaje           | JavaScript                                       | Estructura de componentes `.vue`           |
| QR Generation      | qrcode                                           | Genera el código en `<canvas>`             |
| Gestión de clipboard | Navigator Clipboard API                        | Pegar texto directamente                   |
| Build & Deploy     | Vue CLI + gh-pages                               | Publicación en GitHub Pages                |

---

## 🔥 Retos enfrentados y cómo los resolví

| Reto                                          | Solución aplicada                                                                 | Impacto / Aprendizaje                              |
|-----------------------------------------------|-----------------------------------------------------------------------------------|----------------------------------------------------|
| Reactividad del texto                         | Uso de `watch` para invocar generación en cada cambio                          | QR siempre actualizado al vuelo                    |
| Dibujar en canvas desde componente Vue        | Referencia con `ref` y llamada a `QRCode.toCanvas`                             | Entendí cómo interactuar con elementos DOM nativos  |
| Acceso al portapapeles                       | Uso de API `navigator.clipboard.readText()` con manejo de errores              | Mejor UX al permitir pegar contenido                |
| Primer proyecto en Vue                        | Configuración inicial de Vue CLI y adaptación a sintaxis de Single File Component | Buen punto de partida para futuras apps            |

---

## 🚀 Cómo empezar

### 1. ¿Qué necesito tener instalado?

- **Node.js** 14+   
  → [Descargar](https://nodejs.org/)

### 2. Pasos para ejecutar localmente

```bash
git clone https://github.com/Alex0-8/Vue_QrGenerator.git
cd text_to_qr
npm install
npm run serve
```

→ Abre http://localhost:8080 (o el puerto que indique Vue CLI).

Comandos útiles

```bash
  npm run serve       # Inicia el servidor de desarrollo
  npm run build       # Genera la versión para producción
  npm run lint        # Corrige problemas de estilo (ESLint)
```

---

# 📄 Licencia
Siéntete libre de usar, modificar y aprender de este proyecto.
Última actualización: 1 de Marzo de 2026
¡Gracias por probar Text to QR!

---

## English

# 📱 Text to QR – QR Code Generator

<div align="center">
  <a href="https://vuejs.org/"><img src="https://img.shields.io/badge/Vue-4FC08D?logo=vue.js&logoColor=white&style=flat-square" alt="Vue 3" /></a>
  <a href="https://www.javascript.com/"><img src="https://img.shields.io/badge/JavaScript-yellow?logo=javascript&logoColor=black&style=flat-square" alt="JavaScript" /></a>
  <a href="https://www.npmjs.com/package/qrcode"><img src="https://img.shields.io/badge/qrcode-lib-blue?logo=npm&logoColor=white&style=flat-square" alt="qrcode" /></a>
  <a href="https://alex0-8.github.io/Vue_QrGenerator/"><img src="https://img.shields.io/badge/Live%20Demo-brightgreen?logo=vercel&logoColor=white&style=flat-square" alt="Live demo" /></a>
</div>

---

**Text to QR** was my first Vue 3 project. The app allows typing or pasting text and generates a QR code in real time using the **qrcode** library. Great for learning reactivity and canvas manipulation in Vue.

🔗 **Live demo** → [Vue QrGenerator/](https://alex0-8.github.io/Vue_QrGenerator/)

---

## ✨ Key Features

- Live QR generation as characters are typed
- Buttons to clear input or paste from clipboard
- Canvas-rendered QR with custom colors
- Lightweight dependency (`qrcode`) with no heavy frameworks
- Simple CSS styles and centered, responsive layout
- Starter project with Vue CLI

---

## 🛠️ Tech Stack

| Category           | Technology / Tool                          | Notes                                      |
|--------------------|---------------------------------------------|--------------------------------------------|
| Framework          | Vue 3                                       | Basic composition with `data` and `watch`  |
| Language           | JavaScript                                  | Single File Components `.vue`              |
| QR Generation      | qrcode                                      | Renders to `<canvas>`                      |
| Clipboard         | Navigator Clipboard API                     | Enables paste feature                      |
| Build & Deploy     | Vue CLI + gh-pages                          | Hosted on GitHub Pages                     |

---

## 🔥 Challenges Faced and Solutions

| Challenge                                   | Applied Solution                                                       | Impact / Learning                             |
|---------------------------------------------|------------------------------------------------------------------------|-----------------------------------------------|
| Making text reactive                         | Used `watch` to run generator on each change                          | QR always up to date                           |
| Drawing to canvas from Vue component         | Refs plus `QRCode.toCanvas` call                                        | Learned DOM interaction                        |
| Clipboard access                             | Implemented `navigator.clipboard.readText()` with error handling      | Easier UX with paste                            |
| First Vue project                            | Setup with Vue CLI; adapted to SFC syntax                              | Solid starting point for future Vue apps       |

---

## 🚀 Getting Started (for beginners)

### 1. Prerequisites

- **Node.js** 14+   
  → [Download](https://nodejs.org/)

### 2. Local setup

```bash
git clone https://github.com/Alex0-8/Vue_QrGenerator.git
cd text_to_qr
npm install
npm run serve
```

→ Visit localhost port shown by CLI.

Useful commands

```bash
  npm run serve       # Start dev server
  npm run build       # Build for production
  npm run lint        # Lint & fix
```

---

# 📄 License
Feel free to use, modify and learn from this project.
Last update: March 1, 2026
Thank you for trying Text to QR!
