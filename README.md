# Cerebr贸Nico v1.0.49 - IDE de Desarrollo Aut贸nomo con IA

<div align="center">
  
![Cerebr贸Nico](https://raw.githubusercontent.com/cerebrocn-afk/Cerebr-Nico-V1.0.49/main/web-cerebronico-v1.97.3/assets/logo.png)
  
**馃殌 IDE de alto rendimiento para ingenier铆a de software aut贸noma**
  
**Combina inferencia local (Ollama) con aceleraci贸n en la nube (Gemini, OpenRouter)**

  Prueba demo en servidor (https://cerebronico-v1-0-49.ai.studio)
  
[![Version](https://img.shields.io/badge/v1.0.49-blue)](https://github.com/cerebrocn-afk/Cerebr-Nico-V1.0.49/releases)
[![License](https://img.shields.io/badge/License-Proprietary-red)](https://github.com/cerebrocn-afk/Cerebr-Nico-V1.0.49/blob/main/LICENSE)
[![Node.js](https://img.shields.io/badge/node.js-18+-green)](https://nodejs.org/)
[![Python](https://img.shields.io/badge/python-3.8+-yellow)](https://www.python.org/)

</div>

---

## 馃搵 Tabla de Contenidos

- [驴Qu茅 es Cerebr贸Nico?](#-qu茅-es-cerebr贸nico)
- [Caracter铆sticas Principales](#-caracter铆sticas-principales)
- [Arquitectura del Sistema](#-arquitectura-del-sistema)
- [Requisitos](#-requisitos)
- [Instalaci贸n y Arranque](#-instalaci贸n-y-arranque)
- [Proveedores de IA Soportados](#-proveedores-de-ia-soportados)
- [Memoria H铆brida (Opcional)](#-memoria-h铆brida-opcional)
- [Creador Web Integrado](#-creador-web-integrado)
- [Autonom铆a del Sistema](#-autonom铆a-del-sistema)
- [Tests y Verificaci贸n](#-tests-y-verificaci贸n)
- [Documentaci贸n](#-documentaci贸n)
- [Reconocimientos](#-reconocimientos)
- [Contribuir](#-contribuir)
- [Licencia](#-licencia)

---

## 馃 驴Qu茅 es Cerebr贸Nico?

Cerebr贸Nico es un entorno integrado de desarrollo (IDE) revolucionario que combina **inferencia local** con **aceleraci贸n en la nube** y **ejecuci贸n autom谩tica** del c贸digo generado. No es simplemente un chat con IA: es un sistema completo que escribe archivos, levanta previsualizaciones aisladas y controla procesos del sistema.

### 馃幆 Diferenciadores Clave

1. **Lo que el modelo olvida, lo completa el sistema**
   - An谩lisis autom谩tico de dependencias
   - Generaci贸n de manifiestos y documentos de entrada
   - Instalaci贸n precisa solo de lo necesario

2. **Previsualizaci贸n sin instalaci贸n costosa**
   - Servido directo para proyectos simples
   - Empaquetamiento 煤nico para proyectos complejos
   - Arranque inteligente seg煤n el tipo de proyecto

3. **Robustez y desacoplamiento**
   - Cuatro capas independientes por puerto
   - Fallos aislados que no afectan al sistema completo
   - Reportes detallados de errores

---

## 鉁?Caracter铆sticas Principales

### 馃敡 Desarrollo Aut贸nomo
- **Ejecuci贸n de c贸digo** en tiempo real
- **Previsualizaci贸n aislada** de proyectos web
- **Control de procesos** del sistema
- **An谩lisis de dependencias** autom谩tico

### 馃 Proveedores de IA M煤ltiples
- **Ollama** (local, sin costo)
- **Gemini** (Google)
- **OpenRouter** (varios modelos)
- **Proveedores personalizados** (OpenAI-compatible)

### 馃 Memoria H铆brida
- **Recordar entre sesiones** sin contexto limitado
- **Aprendizaje continuo** con retroalimentaci贸n
- **Skills bajo demanda** (67 habilidades integradas)
- **Exportaci贸n/Importaci贸n** de conocimiento

### 馃寪 Creador Web Integrado
- **27 herramientas** para creaci贸n de sitios web
- **Sin frameworks** (HTML+CSS+JS puro)
- **Auditor铆a autom谩tica** (accesibilidad, rendimiento, SEO)
- **PWA y SEO** listo para producci贸n

### 馃洝锔?Seguridad y Robustez
- **Validaci贸n continua** de c贸digo
- **Manejo de errores** detallado
- **Control de acceso** con tokens
- **Aislamiento de procesos**

---

## 馃彈锔?Arquitectura del Sistema

```
鈹屸攢鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹?   鈹屸攢鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹?   鈹屸攢鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹?鈹?  Frontend      鈹?   鈹?  Previsualizador鈹?   鈹?  Puente Python  鈹?鈹?  (Vite/React)  鈹傗梽鈹€鈹€鈻衡攤    (:3500)      鈹傗梽鈹€鈹€鈻衡攤    (:5000)      鈹?鈹斺攢鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹?   鈹斺攢鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹?   鈹斺攢鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹?         鈹?                      鈹?                      鈹?         鈻?                      鈻?                      鈻?鈹屸攢鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹?   鈹屸攢鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹?   鈹屸攢鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹?鈹?  API Server    鈹?   鈹?  Sandbox       鈹?   鈹?  MCP Servers   鈹?鈹?  (:3000)       鈹?   鈹?  Proyectos     鈹?   鈹?  Web, etc.     鈹?鈹斺攢鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹?   鈹斺攢鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹?   鈹斺攢鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹?         鈹?         鈻?鈹屸攢鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹?   鈹屸攢鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹?   鈹屸攢鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹?鈹?  Motor de IA   鈹?   鈹?  Ollama Local  鈹?   鈹?  Servicios      鈹?鈹?  (Gemini, etc) 鈹?   鈹?  (:11434)      鈹?   鈹?  Externos      鈹?鈹斺攢鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹?   鈹斺攢鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹?   鈹斺攢鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹?```

### 馃摗 Puertos del Sistema

| Puerto | Servicio | Descripci贸n |
|--------|----------|-------------|
| 3000 | Frontend + API | UI Vite/React + backend Express |
| 3500 | Previsualizador | Sandbox de proyectos web |
| 5000 | Puente Python | Control de sistema + MCP |
| 11434 | Ollama | Inferencia local (opcional) |
| 5100 | Memoria H铆brida | Sistema de persistencia (opcional) |
| 5102 | Creador Web | Generador de sitios (opcional) |

---

## 馃摝 Requisitos

### Sistema
- **Node.js 18+** (LTS recomendado)
- **Python 3.8+** (opcional, para memoria y creador web)
- **Ollama** (opcional, para inferencia local)

### Memoria Recomendada
- **M铆nimo:** 8GB RAM
- **Recomendado:** 16GB RAM
- **脫ptimo:** 32GB RAM (para modelos grandes)

### Espacio en Disco
- **M铆nimo:** 2GB
- **Recomendado:** 5GB (con modelos locales)

---

## 馃殌 Instalaci贸n y Arranque

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

El servidor estar谩 disponible en: **http://127.0.0.1:3000**

### 4. (Opcional) Instalar Ollama para inferencia local

```bash
# Descargar Ollama: https://ollama.ai/
# Arrancar Ollama
ollama serve
```

### Variables de Entorno

| Variable | Default | Descripci贸n |
|----------|---------|-------------|
| `PORT` | `3000` | Puerto del servidor principal |
| `HOST` | `127.0.0.1` | Direcci贸n de bind |
| `OLLAMA_HOST` | `http://127.0.0.1:11434` | URL de Ollama |
| `GEMINI_API_KEY` | 鈥?| API key de Gemini |
| `OPENROUTER_API_KEY` | 鈥?| API key de OpenRouter |
| `ACCESS_TOKEN` | 鈥?| Token de acceso para sandbox |
| `PROJECT_DIR` | `./.proyectos` | Directorio de proyectos |

---

## 馃 Proveedores de IA Soportados

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

## 馃 Memoria H铆brida (Opcional)

La capa de memoria permite a Cerebr贸Nico recordar y aprender entre sesiones.

### Activar Memoria H铆brida

```bash
# Windows
npm run memoria

# Linux/macOS
npm run memoria:linux
```

### Caracter铆sticas de la Memoria
- **19 herramientas** integradas
- **Modo espejo** (sin dependencias externas)
- **Modo biomim茅tico** (con Hindsight SDK)
- **Skills bajo demanda** (67 habilidades)
- **Exportaci贸n/Importaci贸n** de conocimiento

### Herramientas Disponibles
- `memory_estado` - Estado del sistema
- `memory_recall` - B煤squeda de recuerdos
- `memory_reflect` - S铆ntesis y reflexi贸n
- `memory_guardar_aprendizaje` - Guardar lecciones
- `memory_ingest` - Ingesta de documentos
- `memory_exportar` - Exportar memoria
- Y muchas m谩s...

---

## 馃寪 Creador Web Integrado

### Activar el Creador Web

```bash
# Windows
npm run creador

# Linux/macOS
npm run creador:linux
```

### 27 Herramientas Disponibles

#### Creaci贸n
- `crear_sitio` - Sitios web modernos
- `crear_sitio_multipagina` - Multi-p谩gina con navegaci贸n
- `crear_pagina` - P谩ginas adicionales
- `crear_bloque` - Bloques espec铆ficos
- `crear_pwa` - Progressive Web Apps
- `crear_og_image` - Open Graph images

#### Auditor铆a
- `auditar_pagina` - An谩lisis completo
- `auditar_sitio` - Auditor铆a multi-p谩gina
- `auditar_contraste` - Contraste WCAG

#### Mejora
- `mejorar_pagina` - Correcciones autom谩ticas
- `mejorar_hasta_estable` - Bucle de mejora

#### Componentes
- `componente_modo_oscuro` - Tema oscuro
- `componente_consentimiento` - Cookies GDPR
- `formulario_destino` - Formularios funcionales

#### Medici贸n
- `preflight_rendimiento` - An谩lisis de rendimiento

#### Entrega
- `exportar_sitio_zip` - Paquete listo para producci贸n
- `desplegar_carpeta` - Despliegue local
- `verificar_despliegue` - Verificaci贸n hash

---

## 馃洝锔?Autonom铆a del Sistema

Cerebr贸Nico est谩 dise帽ado para funcionar con m铆nima intervenci贸n humana.

### 1. Autodiagn贸stico de Puertos
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

### Caracter铆sticas de Autonom铆a
- **Detecci贸n autom谩tica** de puertos ocupados
- **Reinicio inteligente** de servicios ca铆dos
- **Instalaci贸n autom谩tica** de dependencias
- **Bloqueo de reinicios** sobre c贸digo roto
- **Logging detallado** de todas las acciones

---

## 馃И Tests y Verificaci贸n

### Tests End-to-End
```bash
# Ejecutar todos los tests
python3 tests/comprehensive_e2e_test.py
```

### Validaci贸n del Sistema
```bash
# Validar todo el proyecto
npm run validar
```

### Tests Disponibles
- **8 tests** completos
- **4 proveedores** de IA
- **3 m茅todos** de verificaci贸n
- **Tests de regresi贸n** para bugs conocidos

---

## 馃摎 Documentaci贸n

### Documentaci贸n Principal
- [`CHANGELOG.md`](CHANGELOG.md) - Historial de cambios
- [`HOJA_DE_RUTA_PERFECCION.md`](HOJA_DE_RUTA_PERFECCION.md) - Hoja de ruta
- [`manual-motor/manual-completo.md`](manual-motor/manual-completo.md) - Manual del motor
- [`SKILLS.md`](SKILLS.md) - Habilidades disponibles

### Documentaci贸n T茅cnica
- [`SUPERFICIE_RUTAS.md`](SUPERFICIE_RUTAS.md) - API del servidor
- [`documentacion/audits/AUDITS_MAESTRO.md`](documentacion/audits/AUDITS_MAESTRO.md) - Auditor铆as
- [`documentacion/ANALISIS_BUNDLE_TOP_REPOS_v1.17.0.md`](documentacion/ANALISIS_BUNDLE_TOP_REPOS_v1.17.0.md) - An谩lisis ecosistema

### Gu铆as R谩pidas
- [`LEEME-PRIMERO.txt`](LEEME-PRIMERO.txt) - Arranque r谩pido
- [`ACTIVAR-SKILLS-OAUTH.md`](ACTIVAR-SKILLS-OAUTH.md) - Skills OAuth
- [`CEREBRONICO-GITHUB.md`](CEREBRONICO-GITHUB.md) - Gu铆a GitHub

---

## 馃弳 Reconocimientos

Cerebr贸Nico no ser铆a posible sin las siguientes herramientas:

- **[Z.ai](https://z.ai)** - Acceso a GLM-4.5-Flash (gratis)
- **[Google AI Studio](https://aistudio.google.com)** - Modelado y afinaci贸n de prompts
- **[GitHub](https://github.com)** - Colaboraci贸n y versionado

> Reconocimiento especial a los desarrolladores de estas plataformas que han democratizado el acceso a la IA avanzada.

---

## 馃 Contribuir

### C贸mo Contribuir
1. Fork del proyecto
2. Crear rama de feature (`git checkout -b feature/AmazingFeature`)
3. Commit de cambios (`git commit -m 'Add some AmazingFeature'`)
4. Push a la rama (`git push origin feature/AmazingFeature`)
5. Abrir un Pull Request

### Normas de Contribuci贸n
- C贸digo limpio y documentado
- Tests para nuevas funcionalidades
- Actualizaci贸n de documentaci贸n
- Respeto al c贸digo existente

---

## 馃搫 Licencia

**Autor y propietario:** Mario Nicolas Quintero Marin  
**Copyright 漏 2026 Mario Nicolas Quintero Marin.**  
**Todos los derechos reservados.**

Este software es propiedad intelectual de Mario Nicolas Quintero Marin. Queda prohibida cualquier reproducci贸n, distribuci贸n o modificaci贸n sin autorizaci贸n expresa por escrito del autor.

---

## 馃摓 Contacto

**Mario  Quintero**  
[Perfil GitHub](https://github.com/cerebrocn-afk)  
[Email Principal](mailto:cerebrocn@gmail.com)

---

<div align="center">
  
![Cerebr贸Nico](https://raw.githubusercontent.com/cerebrocn-afk/Cerebr-Nico-V1.0.49/main/web-cerebronico-v1.97.3/assets/logo.png)
  
**Cerebr贸Nico - Donde la IA se encuentra con la ingenier铆a pr谩ctica**
  
</div>
