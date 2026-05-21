
<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/iapex-org/.github/main/profile/banner-dark.svg">
    <img alt="IAPEX" src="https://raw.githubusercontent.com/iapex-org/.github/main/profile/banner-light.svg" width="100%">
  </picture>
</p>

<h1 align="center">🆔 IAPEX — Ecosistema Híbrido de IA para Identificación de Pacientes</h1>

<p align="center">
  <em>Cerrando la brecha entre pacientes no identificados en hospitales y familias que los buscan</em>
</p>

<p align="center">
  <a href="https://github.com/iapex-org/web-app"><img src="https://img.shields.io/badge/Portal_Web-Angular_19-DD0031?logo=angular&logoColor=white" alt="Portal Web"></a>
  <a href="https://github.com/iapex-org/mobile-app"><img src="https://img.shields.io/badge/App_M%C3%B3vil-React_18_+_Ionic_8-4584FF?logo=ionic&logoColor=white" alt="App Móvil"></a>
  <a href="https://github.com/iapex-org/core-api"><img src="https://img.shields.io/badge/Core_API-Spring_Boot_3-6DB33F?logo=springboot&logoColor=white" alt="Core API"></a>
  <a href="https://virtual.cuautitlan.unam.mx/intar/wp-content/uploads/sites/19/2025/12/166-A-Hybrid-Artificial-Intelligent-System-for-Missing-JORGE-CHRISTIAN-SERRANO-PUERTOS.pdf"><img src="https://img.shields.io/badge/Paper-Research_Pdf-4285F4?logo=googlescholar" alt="Paper"></a>
</p>

---

## 🎯 El Desafío

Los hospitales dependen de protocolos manuales y aislados para registrar pacientes no identificados, creando una desconexión crítica con las familias que buscan en morgues y salas de emergencia. IAPEX resuelve esto proporcionando un **ecosistema centrado en la privacidad** que conecta datos institucionales con consultas públicas a través de un núcleo de coincidencia biométrica segura, reduciendo el tiempo de identificación de **días a segundos**.

## 🏗 Arquitectura

```
┌─────────────────────────────────────────────────┐
│              App Móvil (Familia)                  │
│          React + Ionic + Capacitor               │
└───────────────────────┬─────────────────────────┘
                        │ HTTPS / JWT
┌───────────────────────▼─────────────────────────┐
│           Core API (Spring Boot)                  │
│     PostgreSQL + MongoDB + JWT Auth + RBAC       │
└────┬──────────────────────┬─────────────────────┘
     │                      │
     ▼                      ▼
┌──────────────┐  ┌──────────────────┐
│  Portal Web  │  │  Motor de IA     │
│  (Instit.)   │  │  (Neural Core)   │
│  Angular 19  │  │  FastAPI + dlib  │
│  Bootstrap   │  │  scikit-learn    │
└──────────────┘  └──────────────────┘
```

## 📦 Repositorios

| Repositorio | Propósito | Stack | Estado |
|-------------|-----------|-------|--------|
| [web-app](https://github.com/iapex-org/web-app) | Portal web institucional para personal médico | Angular 19, Bootstrap, TypeScript | ✅ Activo |
| [mobile-app](https://github.com/iapex-org/mobile-app) | App móvil para búsqueda familiar | React 18, Ionic 8, Capacitor | ✅ Activo |
| [core-api](https://github.com/iapex-org/core-api) | API REST: auth, pacientes, instituciones | Spring Boot 3, PostgreSQL, MongoDB | ✅ Activo |
| [neural-core](https://github.com/iapex-org/neural-core) | Motor IA: búsqueda híbrida facial + textual | FastAPI, dlib, scikit-learn | 🚧 Próximamente |

## 🧠 ¿Cómo funciona?

1. **Hospitales** registran pacientes no identificados vía el **Portal Web** — capturando rasgos morfológicos, fotografías y datos médicos bajo RBAC estricto
2. **Familias** buscan mediante la **App Móvil** — subiendo fotos y descripciones de sus seres queridos
3. El **Neural Core** fusiona embeddings de FaceNet (distancia euclidiana) con filtros de texto (Levenshtein, Jaro-Winkler) para clasificar candidatos, reduciendo significativamente los falsos positivos
4. Las coincidencias se muestran con puntajes de similitud — la privacidad del paciente se protege hasta que el personal institucional verifica

## 🔬 Investigación

Artículo publicado: *"A Hybrid Artificial Intelligent System for the Identification of Missing Persons in Health Institutions"* — [Leer el artículo completo](https://virtual.cuautitlan.unam.mx/intar/wp-content/uploads/sites/19/2025/12/166-A-Hybrid-Artificial-Intelligent-System-for-Missing-JORGE-CHRISTIAN-SERRANO-PUERTOS.pdf)

## 🛡 Privacidad y Seguridad

- Autenticación JWT de extremo a extremo
- Control de Acceso Basado en Roles (RBAC)
- Datos de pacientes anonimizados hasta coincidencia verificada
- Almacenamiento de medios encriptado

## 🤝 Contribuciones

Seguimos un flujo de trabajo estricto basado en PRs. Revisa el `CONTRIBUTING.md` de cada repositorio para lineamientos. Todas las contribuciones deben adherirse a nuestro [Código de Conducta](https://github.com/iapex-org/.github/blob/main/CODE_OF_CONDUCT.md).

---

<p align="center">
  <sub>Hecho con ❤️ por el equipo IAPEX · UNAM Cuautitlán · 2025</sub>
</p>
