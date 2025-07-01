# 🏟️ ProyectoDataStreaming - Plataforma de Inicio

¡Bienvenid@ a `ProyectoDataStreaming`!  
Este repositorio es tu punto de partida para explorar, colaborar y desplegar soluciones de análisis en tiempo real sobre Azure de forma completamente automatizada.

---

![Imagen Representativa del Proyecto](/imagenes/DSA.png)

---

## 👥 Colaboradores

| Foto | Nombre | Rol |
|------|--------|-----|
| ![Foto de perfil de Javi](https://avatars.githubusercontent.com/u/207551147?v=4) | **Javier Martínez García** | 🛠️ Owner |
| ![Foto de perfil de Antonio](https://avatars.githubusercontent.com/u/usuario2?v=4) | **Antonio Jesús Robles Ruíz** | 👥 Colaborador |
| ![Foto de perfil de Lucía](https://avatars.githubusercontent.com/u/usuario3?v=4) | **Lucía Nieto Reus** | 👥 Colaboradora |

---

## 🎯 Objetivo del Proyecto

El propósito de este proyecto es construir una arquitectura completa de **procesamiento de datos en streaming** sobre servicios de **Azure**, con un enfoque especial en la **automatización** mediante **CI/CD con GitHub Actions**. Este entorno facilitará el despliegue y monitoreo continuo de componentes que simulan y analizan eventos en tiempo real de un partido de fútbol.

---

## 🏗️ Arquitectura General

El ecosistema se organiza en múltiples repositorios dentro de la organización `ProyectoDataStreaming`:

### 🔧 `infra`
- Encargado del despliegue de servicios en la nube de **Azure** (EventHub, Azure Container Registry, Azure Container Instances, etc).
- Automatización del aprovisionamiento mediante workflows.

### 🐳 `docker`
- Contiene los **Dockerfiles** que generan imágenes responsables de simular eventos de un partido de fútbol en tiempo real.
- Estas imágenes son registradas en **Azure Container Registry** y luego ejecutadas como contenedores en **Azure Container Instances**.
- Generan eventos hacia **EventHub** en tiempo real.

### 📓 `databricks`
- Repositorio que contiene la sincronización del entorno de trabajo en **Azure Databricks**.
- Incluye notebooks y scripts para procesar los eventos entrantes desde EventHub.
- Permite análisis en streaming de los datos recibidos.

---

## 🔁 CI/CD: Automatización Total

Todo el proceso, desde la construcción de imágenes Docker hasta el despliegue de infraestructura, está orquestado a través de **GitHub Actions**.  
Esto garantiza:
- **Despliegue automático y reproducible**
- **Reducción de errores humanos**
- **Optimización de costos**
- **Trazabilidad completa de los cambios**

---

## ⚽ Datos de Entrada: Fútbol en Tiempo Real

- Los datos simulados representan las **posiciones de jugadores y pelota** en un partido de fútbol.
- Se generan desde un script en Python ejecutado dentro de un contenedor Docker.
- Los eventos se envían a **Azure EventHub**, donde son capturados y procesados por Databricks.

Disponemos de dos archivos CSV como fuente original:
- `home_team.csv` → Posiciones del equipo local
- `away_team.csv` → Posiciones del equipo visitante

Cada archivo contiene información que se transmite en tiempo real simulando un partido en vivo.

---

## 🧭 Próximos Pasos

- Definición de herramienta de visualización en tiempo real (Power BI, Grafana, etc.)
- Optimización de performance en los pipelines de eventos
- Implementación de alertas y monitoreo automático

