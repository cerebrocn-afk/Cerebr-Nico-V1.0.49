# CerebróNico v1.0.49 - IDE de Desarrollo Autónomo con IA

<div align="center">
  
![CerebróNico](https://raw.githubusercontent.com/cerebrocn-afk/Cerebr-Nico-V1.0.49/main/web-cerebronico-v1.97.3/assets/logo.png)
  
**🚀 IDE de alto rendimiento para ingeniería de software autónoma**
  
**Combina inferencia local (Ollama) con aceleración en la nube (Gemini, OpenRouter)**
  
[![Version](https://img.shields.io/badge/v1.0.49-blue)](https://github.com/cerebrocn-afk/Cerebr-Nico-V1.0.49/releases)
[![License](https://img.shields.io/badge/License-Proprietary-red)](https://github.com/cerebrocn-afk/Cerebr-Nico-V1.0.49/blob/main/LICENSE)
[![Node.js](https://img.shields.io/badge/node.js-18+-green)](https://nodejs.org/)
[![Python](https://img.shields.io/badge/python-3.8+-yellow)](https://www.python.org/)

</div>

---

## 📋 Tabla de Contenidos

- [¿Qué es CerebróNico?](#-qué-es-cerebrónico)
- [Características Principales](#-características-principales)
- [Arquitectura del Sistema](#-arquitectura-del-sistema)
- [Requisitos](#-requisitos)
- [Instalación y Arranque](#-instalación-y-arranque)
- [Proveedores de IA Soportados](#-proveedores-de-ia-soportados)
- [Memoria Híbrida (Opcional)](#-memoria-híbrida-opcional)
- [Creador Web Integrado](#-creador-web-integrado)
- [Autonomía del Sistema](#-autonomía-del-sistema)
- [Tests y Verificación](#-tests-y-verificación)
- [Documentación](#-documentación)
- [Reconocimientos](#-reconocimientos)
- [Contribuir](#-contribuir)
- [Licencia](#-licencia)

---

## 🧠 ¿Qué es CerebróNico?

CerebróNico es un entorno integrado de desarrollo (IDE) revolucionario que combina **inferencia local** con **aceleración en la nube** y **ejecución automática** del código generado. No es simplemente un chat con IA: es un sistema completo que escribe archivos, levanta previsualizaciones aisladas y controla procesos del sistema.

### 🎯 Diferenciadores Clave

1. **Lo que el modelo olvida, lo completa el sistema**
   - Análisis automático de dependencias
   - Generación de manifiestos y documentos de entrada
   - Instalación precisa solo de lo necesario

2. **Previsualización sin instalación costosa**
   - Servido directo para proyectos simples
   - Empaquetamiento único para proyectos complejos
   - Arranque inteligente según el tipo de proyecto

3. **Robustez y desacoplamiento**
   - Cuatro capas independientes por puerto
   - Fallos aislados que no afectan al sistema completo
   - Reportes detallados de errores

---

## ✨ Características Principales

### 🔧 Desarrollo Autónomo
- **Ejecución de código** en tiempo real
- **Previsualización aislada** de proyectos web
- **Control de procesos** del sistema
- **Análisis de dependencias** automático

### 🤖 Proveedores de IA Múltiples
- **Ollama** (local, sin costo)
- **Gemini** (Google)
- **OpenRouter** (varios modelos)
- **Proveedores personalizados** (OpenAI-compatible)

### 🧠 Memoria Híbrida
- **Recordar entre sesiones** sin contexto limitado
- **Aprendizaje continuo** con retroalimentación
- **Skills bajo demanda** (67 habilidades integradas)
- **Exportación/Importación** de conocimiento

### 🌐 Creador Web Integrado
- **27 herramientas** para creación de sitios web
- **Sin frameworks** (HTML+CSS+JS puro)
- **Auditoría automática** (accesibilidad, rendimiento, SEO)
- **PWA y SEO** listo para producción

### 🛡️ Seguridad y Robustez
- **Validación continua** de código
- **Manejo de errores** detallado
- **Control de acceso** con tokens
- **Aislamiento de procesos**

---

## 🏗️ Arquitectura del Sistema

```
┌─────────────────┐    ┌─────────────────┐    ┌─────────────────┐
│   Frontend      │    │   Previsualizador│    │   Puente Python  │
│   (Vite/React)  │◄──►│    (:3500)      │◄──►│    (:5000)      │
└─────────────────┘    └─────────────────┘    └─────────────────┘
         │                       │                       │
         ▼                       ▼                       ▼
┌─────────────────┐    ┌─────────────────┐    ┌─────────────────┐
│   API Server    │    │   Sandbox       │    │   MCP Servers   │
│   (:3000)       │    │   Proyectos     │    │   Web, etc.     │
└─────────────────┘    └─────────────────┘    └─────────────────┘
         │
         ▼
┌─────────────────┐    ┌─────────────────┐    ┌─────────────────┐
│   Motor de IA   │    │   Ollama Local  │    │   Servicios      │
│   (Gemini, etc) │    │   (:11434)      │    │   Externos      │
└─────────────────┘    └─────────────────┘    └─────────────────┘
```

### 📡 Puertos del Sistema

| Puerto | Servicio | Descripción |
|--------|----------|-------------|
| 3000 | Frontend + API | UI Vite/React + backend Express |
| 3500 | Previsualizador | Sandbox de proyectos web |
| 5000 | Puente Python | Control de sistema + MCP |
| 11434 | Ollama | Inferencia local (opcional) |
| 5100 | Memoria Híbrida | Sistema de persistencia (opcional) |
| 5102 | Creador Web | Generador de sitios (opcional) |

---

## 📦 Requisitos

### Sistema
- **Node.js 18+** (LTS recomendado)
- **Python 3.8+** (opcional, para memoria y creador web)
- **Ollama** (opcional, para inferencia local)

### Memoria Recomendada
- **Mínimo:** 8GB RAM
- **Recomendado:** 16GB RAM
- **Óptimo:** 32GB RAM (para modelos grandes)

### Espacio en Disco
- **Mínimo:** 2GB
- **Recomendado:** 5GB (con modelos locales)

---

## 🚀 Instalación y Arranque

### 1. Clonar el Repositorio

```bash
git clone https://github.com/cerebrocn-afk/Cerebr-Nico-V1.0.49.git
cd Cerebr-Nico-V1.0.49
```

### 2. Instalar Dependencias

```bash
npm install
```

### 3. Arrancar el Sistema

```bash
npm run dev
```

El servidor estará disponible en: **http://127.0.0.1:3000**

### 4. (Opcional) Instalar Ollama para inferencia local

```bash
# Descargar Ollama: https://ollama.ai/
# Arrancar Ollama
ollama serve
```

### Variables de Entorno

| Variable | Default | Descripción |
|----------|---------|-------------|
| `PORT` | `3000` | Puerto del servidor principal |
| `HOST` | `127.0.0.1` | Dirección de bind |
| `OLLAMA_HOST` | `http://127.0.0.1:11434` | URL de Ollama |
| `GEMINI_API_KEY` | — | API key de Gemini |
| `OPENROUTER_API_KEY` | — | API key de OpenRouter |
| `ACCESS_TOKEN` | — | Token de acceso para sandbox |
| `PROJECT_DIR` | `./.proyectos` | Directorio de proyectos |

---

## 🤖 Proveedores de IA Soportados

### 1. Ollama (Local)
```bash
# Requiere Ollama instalado y corriendo
curl -sN -X POST http://127.0.0.1:3000/api/ai/stream \
  -H "Content-Type: application/json" \
  -d '{"prompt":"Hola","provider":"ollama","model":"qwen2.5:7b"}'
```

### 2. Gemini (Google)
```bash
# Requiere API key de Gemini
curl -sN -X POST http://127.0.0.1:3000/api/ai/stream \
  -H "Content-Type: application/json" \
  -d '{"prompt":"Hola","provider":"gemini","model":"gemini-1.5-flash"}'
```

### 3. OpenRouter
```bash
# Requiere API key de OpenRouter
curl -sN -X POST http://127.0.0.1:3000/api/ai/stream \
  -H "Content-Type: application/json" \
  -d '{"prompt":"Hola","provider":"openrouter","model":"openai/gpt-3.5-turbo"}'
```

### 4. Proveedores Personalizados
Cualquier endpoint compatible con OpenAI API.

---

## 🧠 Memoria Híbrida (Opcional)

La capa de memoria permite a CerebróNico recordar y aprender entre sesiones.

### Activar Memoria Híbrida

```bash
# Windows
npm run memoria

# Linux/macOS
npm run memoria:linux
```

### Características de la Memoria
- **19 herramientas** integradas
- **Modo espejo** (sin dependencias externas)
- **Modo biomimético** (con Hindsight SDK)
- **Skills bajo demanda** (67 habilidades)
- **Exportación/Importación** de conocimiento

### Herramientas Disponibles
- `memory_estado` - Estado del sistema
- `memory_recall` - Búsqueda de recuerdos
- `memory_reflect` - Síntesis y reflexión
- `memory_guardar_aprendizaje` - Guardar lecciones
- `memory_ingest` - Ingesta de documentos
- `memory_exportar` - Exportar memoria
- Y muchas más...

---

## 🌐 Creador Web Integrado

### Activar el Creador Web

```bash
# Windows
npm run creador

# Linux/macOS
npm run creador:linux
```

### 27 Herramientas Disponibles

#### Creación
- `crear_sitio` - Sitios web modernos
- `crear_sitio_multipagina` - Multi-página con navegación
- `crear_pagina` - Páginas adicionales
- `crear_bloque` - Bloques específicos
- `crear_pwa` - Progressive Web Apps
- `crear_og_image` - Open Graph images

#### Auditoría
- `auditar_pagina` - Análisis completo
- `auditar_sitio` - Auditoría multi-página
- `auditar_contraste` - Contraste WCAG

#### Mejora
- `mejorar_pagina` - Correcciones automáticas
- `mejorar_hasta_estable` - Bucle de mejora

#### Componentes
- `componente_modo_oscuro` - Tema oscuro
- `componente_consentimiento` - Cookies GDPR
- `formulario_destino` - Formularios funcionales

#### Medición
- `preflight_rendimiento` - Análisis de rendimiento

#### Entrega
- `exportar_sitio_zip` - Paquete listo para producción
- `desplegar_carpeta` - Despliegue local
- `verificar_despliegue` - Verificación hash

---

## 🛡️ Autonomía del Sistema

CerebróNico está diseñado para funcionar con mínima intervención humana.

### 1. Autodiagnóstico de Puertos
```bash
python autonomia.py puertos [--matar]
```

### 2. Gestor de Dependencias Python
```bash
python autonomia.py deps [--auto]
```

### 3. Watchdog Externo
```bash
npm run vigilar
```

### Características de Autonomía
- **Detección automática** de puertos ocupados
- **Reinicio inteligente** de servicios caídos
- **Instalación automática** de dependencias
- **Bloqueo de reinicios** sobre código roto
- **Logging detallado** de todas las acciones

---

## 🧪 Tests y Verificación

### Tests End-to-End
```bash
# Ejecutar todos los tests
python3 tests/comprehensive_e2e_test.py
```

### Validación del Sistema
```bash
# Validar todo el proyecto
npm run validar
```

### Tests Disponibles
- **8 tests** completos
- **4 proveedores** de IA
- **3 métodos** de verificación
- **Tests de regresión** para bugs conocidos

---

## 📚 Documentación

### Documentación Principal
- [`CHANGELOG.md`](CHANGELOG.md) - Historial de cambios
- [`HOJA_DE_RUTA_PERFECCION.md`](HOJA_DE_RUTA_PERFECCION.md) - Hoja de ruta
- [`manual-motor/manual-completo.md`](manual-motor/manual-completo.md) - Manual del motor
- [`SKILLS.md`](SKILLS.md) - Habilidades disponibles

### Documentación Técnica
- [`SUPERFICIE_RUTAS.md`](SUPERFICIE_RUTAS.md) - API del servidor
- [`documentacion/audits/AUDITS_MAESTRO.md`](documentacion/audits/AUDITS_MAESTRO.md) - Auditorías
- [`documentacion/ANALISIS_BUNDLE_TOP_REPOS_v1.17.0.md`](documentacion/ANALISIS_BUNDLE_TOP_REPOS_v1.17.0.md) - Análisis ecosistema

### Guías Rápidas
- [`LEEME-PRIMERO.txt`](LEEME-PRIMERO.txt) - Arranque rápido
- [`ACTIVAR-SKILLS-OAUTH.md`](ACTIVAR-SKILLS-OAUTH.md) - Skills OAuth
- [`CEREBRONICO-GITHUB.md`](CEREBRONICO-GITHUB.md) - Guía GitHub

---

## 🏆 Reconocimientos

CerebróNico no sería posible sin las siguientes herramientas:

- **[Z.ai](https://z.ai)** - Acceso a GLM-4.5-Flash (gratis)
- **[Google AI Studio](https://aistudio.google.com)** - Modelado y afinación de prompts
- **[GitHub](https://github.com)** - Colaboración y versionado

> Reconocimiento especial a los desarrolladores de estas plataformas que han democratizado el acceso a la IA avanzada.

---

## 🤝 Contribuir

### Cómo Contribuir
1. Fork del proyecto
2. Crear rama de feature (`git checkout -b feature/AmazingFeature`)
3. Commit de cambios (`git commit -m 'Add some AmazingFeature'`)
4. Push a la rama (`git push origin feature/AmazingFeature`)
5. Abrir un Pull Request

### Normas de Contribución
- Código limpio y documentado
- Tests para nuevas funcionalidades
- Actualización de documentación
- Respeto al código existente

---

## 📄 Licencia

**Autor y propietario:** Mario Nicolas Quintero Marin  
**Copyright © 2026 Mario Nicolas Quintero Marin.**  
**Todos los derechos reservados.**

Este software es propiedad intelectual de Mario Nicolas Quintero Marin. Queda prohibida cualquier reproducción, distribución o modificación sin autorización expresa por escrito del autor.

---

## 📞 Contacto

**Mario Nicolas Quintero Marin**  
[Perfil GitHub](https://github.com/cerebrocn-afk)  
[Email](mailto:mario.nicolas.quintero.marin@gmail.com)  
[Email Principal](mailto:cerebrocn@gmail.com)

---

<div align="center">
  
![CerebróNico](https://raw.githubusercontent.com/cerebrocn-afk/Cerebr-Nico-V1.0.49/main/web-cerebronico-v1.97.3/assets/logo.png)
  
**CerebróNico - Donde la IA se encuentra con la ingeniería práctica**
  
</div>