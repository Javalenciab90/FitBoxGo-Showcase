# 🇨🇴 FitBoxGo: Optimiza la Fuerza con Precisión

**FitBoxGo** es la herramienta definitiva para atletas que buscan eliminar las conjeturas en el entrenamiento de fuerza. Diseñada para centralizar el progreso, la aplicación automatiza los cálculos más complejos del gimnasio para permitir un enfoque total en el levantamiento.

---

### 🚀 Funcionalidades Principales

* **Gestión Inteligente de RM (1RM):** Cálculo preciso de la Repetición Máxima basado en los levantamientos actuales.
* **Calculadora de Discos Dinámica:** Algoritmo avanzado que calcula la distribución exacta de discos basándose en el inventario real del usuario (configuración mediante *checkboxes*).
* **Calculadora de Discos Bidireccional (Kg/Lb):** Indicación exacta de los discos necesarios para la barra. Compatible con **Kilogramos** y **Libras**, adaptándose a cualquier equipamiento.
* **Firebase Remote Config:** Sistema de control remoto para forzar actualizaciones de versión y despliegue de configuraciones en tiempo real.
* **Benchmarks WOD:** Módulo de seguimiento de rendimiento para *Workouts of the Day* con categorización por niveles (**RX, Intermediate, Scaled**) y soporte para métricas de tiempo o repeticiones.
* **Sincronización Cloud:** Arquitectura basada en eventos con Firestore para una experiencia consistente entre Android e iOS.
> **FitBoxGo. Activa tu mejor versión.**

---
### 🎥 Demo: Recorrido de Funcionalidades

Para facilitar la visualización inmediata del flujo de usuario, comparto estos recorridos cortos integrados:

| Parte 1: RM y Calculadora | Parte 2: Sincronización y WODs |
| :---: | :---: |
| ![Demo Part 1](https://github.com/user-attachments/assets/2c213f51-27bb-4f7c-a700-ae9629814a4e) | ![Demo Part 2](https://github.com/user-attachments/assets/38d15b9e-7900-4500-aa5c-b0e49c01e876) |


### 🛠️ Arquitectura y Stack Tecnológico

#### **Arquitectura MVI (Model-View-Intent)**
Implementación de un flujo de datos unidireccional para garantizar una UI predecible y altamente testeable. [cite: 2]

* **Data Layer:** Contiene las implementaciones de los servicios de Firebase (Autenticación, Firestore/Storage, Remote Config)
* **Domain Layer:** Contiene la lógica del negocio, incluyendo el motor de cálculo de discos y las reglas de validación de los WODs.
* **Remote Config Integration:** Implementación de un servicio de escucha reactiva que compara versiones y dispara alertas de actualización mediante diálogos nativos.
* **Design System:** Librería modular en **Compose Multiplatform** que gestiona tanto el Onboarding Dinámico como la adaptabilidad de temas (Light/Dark Mode).

Para garantizar que **FitBoxGo** sea escalable y robusta, se ha implementado una arquitectura de vanguardia que separa la lógica de negocio de la interfaz de usuario.

---

### **Diagrama Clean Architecture**

<img width="1536" height="1024" alt="Diagram_clean_architecture" src="https://github.com/user-attachments/assets/790f771d-2b35-4023-a362-6deb5a9ae911" />

---


### 🏗️ Estructura Multi-modular

La aplicación utiliza una arquitectura modularizada para maximizar la reutilización y el mantenimiento:

* **`:domain` (El Corazón):** Lógica de negocio pura y algoritmos de cálculo (RM, discos). 100% Kotlin nativo.
* **`:data`:** Gestión de datos. Incluye `:service` (Firebase Cloud) y `:local` (Persistencia).
* **`:features`:** Módulos independientes por funcionalidad (Login, Dashboard, Records).
* **`:presentation`:** Lógica de vista reactiva bajo el patrón MVI.
* **`:design-system`:** Librería visual propia en **Compose Multiplatform** para consistencia total. Incluye el motor de Onboarding dinámico.
* **`:navigation`:** Gestión de flujo desacoplada entre pantallas.
* **`:di`:** Inyección de dependencias centralizada con **Koin**.
* **`:app-android` / `:app-ios`:** Puntos de entrada nativos de cada plataforma.

---

### 🛠️ Tecnologías Clave

* **Compose Multiplatform (CMP):** UI 100% compartida con rendimiento nativo en Android e iOS.
* **Soporte Nativo de Temas:** Detección dinámica de **Dark Mode / Light Mode** mediante el `:design-system`.
* **Kotlin Multiplatform (KMP):** Lógica de negocio y modelos compartidos.
* **Firebase Ecosystem:** Authentication (Google Login), Cloud Firestore (Real-time DB) y Remote Config.
* **Koin:** DI ligera optimizada para proyectos multiplataforma.
* **Corrutinas y Flow:** Motor de reactividad asíncrona para una interfaz fluida.

> *"Gracias a CMP, el sistema de diseño mantiene el comportamiento táctil y el rendimiento nativo de cada sistema operativo."*

---

### 🚀 Disponibilidad

**FitBoxGo** Enfocada en la comunidad de atletas fitness de **Colombia** 🇨🇴.

[![App Store](https://img.shields.io/badge/App_Store-Download-007AFF?style=for-the-badge&logo=apple&logoColor=white)](https://apps.apple.com/app/fitboxgo/id6761392693)

[![Google Play](https://img.shields.io/badge/Google_Play-Download-34A853?style=for-the-badge&logo=google-play&logoColor=white)](https://play.google.com/store/apps/details?id=org.javalenciab90.fitboxgo)

---

### ⚖️ Legal & Copyright
Este repositorio es un **Showcase Técnico**. El código fuente, diseño y activos visuales de **FitBoxGo** son propiedad intelectual de **Jaime Valencia**. Queda prohibida la reproducción, distribución o uso total/parcial del material expuesto sin autorización previa.

*© 2026 FitBoxGo. Todos los derechos reservados.*

---

### 📩 Contacto

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/javalenciab90)
[![Instagram](https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white)](https://www.instagram.com/javalenciab90)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:javalenciab90@gmail.com)

**Jaime Valencia** *Mobile Software Developer | Android & Compose Multiplatform*
