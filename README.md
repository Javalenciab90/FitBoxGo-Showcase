# 🇪🇸 FitBoxGo: Optimiza tu Fuerza con Precisión

**FitBoxGo** es la herramienta definitiva para atletas que buscan eliminar las conjeturas en su entrenamiento de fuerza. Diseñada para centralizar tu progreso, la app automatiza los cálculos más complejos del gimnasio para que tú solo te enfoques en levantar.

---

### 🚀 Funcionalidades Principales

* **Gestión Inteligente de RM (1RM):** Calcula tu Repetición Máxima de forma precisa basada en tus levantamientos actuales.
* **Cálculo Automático de Porcentajes:** Obtén instantáneamente las cargas exactas para tus series de aproximación, hipertrofia o fuerza máxima.
* **Calculadora de Discos Bidireccional (Kg/Lb):** La app te indica exactamente qué discos colocar en la barra. Compatible con **Kilogramos** y **Libras**, adaptándose a cualquier equipamiento.
* **Sincronización en Tiempo Real:** Gracias a su arquitectura Cloud, tus récords se sincronizan instantáneamente entre dispositivos Android e iOS.

> **FitBoxGo. Activa tu mejor versión.**

---

### 🎥 Demo: Sincronización en Tiempo Real

<p align="center">
  <video src="assets/video/demo_sync.mp4" width="800" autoplay loop muted>
  </video>
</p>

**¿Qué estás viendo en esta demo?**
Observa la interoperabilidad entre un **iPhone (Light Mode)** y un emulador de **Android (Dark Mode)**. Al registrar un levantamiento, se muestra la sincronización con la base de datos en ambas pantallas sin latencia. La lógica compartida calcula automáticamente los porcentajes y la distribución de discos de forma instantánea.

#### **Guía de Usuario (Onboarding Contextual)**
Para garantizar una curva de aprendizaje mínima, la primera vez que un atleta accede a la **Calculadora de Discos**, se activa un sistema de **Onboarding Dinámico**:
* **Diálogos de Guía:** Se presentan componentes visuales no interactivos que resaltan las secciones clave de la pantalla.
* **Flujo Paso a Paso:** Al marcar como "Entendido", el usuario realiza la acción e inmediatamente el sistema guía al usuario hacia la siguiente acción, asegurando que comprenda cómo interactuar con los cálculos de RM y la distribución de discos antes de su primer levantamiento.

---

### 🛠️ Arquitectura y Stack Tecnológico

Para garantizar que **FitBoxGo** sea escalable y robusta, he implementado una arquitectura de vanguardia que separa la lógica de negocio de la interfaz de usuario.

#### **Arquitectura MVI (Model-View-Intent)**
Patrón elegido para gestionar el estado de forma predecible:
* **Estado Único:** La interfaz siempre refleja una única fuente de verdad.
* **Flujo Unidireccional:** Facilita el seguimiento de acciones y la depuración del flujo de datos.

---

### 🏗️ Estructura Multi-modular

La aplicación utiliza una arquitectura modularizada para maximizar la reutilización y el mantenimiento:

* **`:domain` (El Corazón):** Lógica de negocio pura y algoritmos de cálculo (RM, discos). 100% Kotlin nativo.
* **`:data`:** Gestión de datos. Incluye `:service` (Firebase Cloud) y `:local` (Persistencia).
* **`:features`:** Módulos independientes por funcionalidad (Login, Dashboard, Records).
* **`:presentation`:** Lógica de vista reactiva bajo el patrón MVI.
* **`:design-system`:** Librería visual propia en **Compose Multiplatform** para consistencia total.
* **`:navigation`:** Gestión de flujo desacoplada entre pantallas.
* **`:di`:** Inyección de dependencias centralizada con **Koin**.
* **`:app-android` / `:app-ios`:** Puntos de entrada nativos de cada plataforma.

---

### 🛠️ Tecnologías Clave

* **Compose Multiplatform (CMP):** UI 100% compartida con rendimiento nativo en Android e iOS.
* **Soporte Nativo de Temas:** Detección dinámica de **Dark Mode / Light Mode** mediante el `:design-system`.
* **Kotlin Multiplatform (KMP):** Lógica de negocio y modelos compartidos.
* **Firebase Ecosystem:** Authentication (Google Login) y Cloud Firestore (Real-time DB).
* **Koin:** DI ligera optimizada para proyectos multiplataforma.
* **Corrutinas y Flow:** Motor de reactividad asíncrona para una interfaz fluida.

> *"Gracias a CMP, el sistema de diseño mantiene el comportamiento táctil y el rendimiento nativo de cada sistema operativo."*

---

### 🚀 Hoja de Ruta (Roadmap)

* [ ] **📚 Biblioteca de WODs Clásicos:** Registro de marcas en entrenamientos icónicos (Fran, Amanda, etc.).
* [ ] **🧘 Sección de Movilidad:** Guía visual de rutinas pre-entrenamiento.
* [ ] **📊 Historial y Gráficos:** Análisis dinámico de la progresión de fuerza.

---

### 🚀 Disponibilidad

Actualmente en etapas finales de pruebas y proceso de aprobación oficial.

| Plataforma | Estado |
| :---: | :---: |
| [![App Store](https://img.shields.io/badge/App_Store-Coming_Soon-007AFF?style=for-the-badge&logo=apple&logoColor=white)](#) | 🍏 En revisión por Apple. |
| [![Google Play](https://img.shields.io/badge/Google_Play-Coming_Soon-34A853?style=for-the-badge&logo=google-play&logoColor=white)](#) | 🤖 En revisión por Google. |

---

### ⚖️ Legal & Copyright
Este repositorio es un **Showcase Técnico**. El código fuente, diseño y activos visuales de **FitBoxGo** son propiedad intelectual de **Jaime Valencia**. Queda prohibida la reproducción, distribución o uso total/parcial del material expuesto sin autorización previa.

*© 2026 FitBoxGo. Todos los derechos reservados.*

---

### 📩 Contacto

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](TU_LINK_DE_LINKEDIN)
[![Instagram](https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white)](TU_LINK_DE_INSTAGRAM)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:TU_CORREO@EMAIL.COM)

**Jaime Valencia** *Mobile Software Developer | Especialista en Android & Compose Multiplatform*
