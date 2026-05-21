<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/iapex-org/.github/main/profile/banner-dark.svg">
    <img alt="IAPEX" src="https://raw.githubusercontent.com/iapex-org/.github/main/profile/banner-light.svg" width="100%">
  </picture>
</p>

<h1 align="center">🆔 IAPEX — Hybrid AI Ecosystem for Patient Identification</h1>

<p align="center">
  <em>Bridging the gap between unidentified hospital patients and searching families</em>
</p>

<p align="center">
  <a href="https://github.com/iapex-org/web-app"><img src="https://img.shields.io/badge/Web_Portal-Angular_19-DD0031?logo=angular&logoColor=white" alt="Web Portal"></a>
  <a href="https://github.com/iapex-org/mobile-app"><img src="https://img.shields.io/badge/Mobile_App-React_18_+_Ionic_8-4584FF?logo=ionic&logoColor=white" alt="Mobile App"></a>
  <a href="https://github.com/iapex-org/core-api"><img src="https://img.shields.io/badge/Core_API-Spring_Boot_3-6DB33F?logo=springboot&logoColor=white" alt="Core API"></a>
  <a href="https://virtual.cuautitlan.unam.mx/intar/wp-content/uploads/sites/19/2025/12/166-A-Hybrid-Artificial-Intelligent-System-for-Missing-JORGE-CHRISTIAN-SERRANO-PUERTOS.pdf"><img src="https://img.shields.io/badge/Paper-Research_Pdf-4285F4?logo=googlescholar" alt="Research Paper"></a>
</p>

<p align="center">
  <a href="README.md">🇬🇧 English</a> · <a href="README.es.md">🇪🇸 Español</a>
</p>

---

## 🎯 The Challenge

Hospitals rely on isolated, manual protocols to register unidentified patients ("John Does"), creating a critical data disconnect with families who search blindly in morgues and ERs. IAPEX solves this by providing a **privacy-focused ecosystem** connecting institutional data with public queries through a secure biometric matching core, reducing identification time from **days to seconds**.

## 🏗 Architecture

```
┌─────────────────────────────────────────────────┐
│                 Mobile App (Family)              │
│          React + Ionic + Capacitor               │
└───────────────────────┬─────────────────────────┘
                        │ HTTPS / JWT
┌───────────────────────▼─────────────────────────┐
│              Core API (Spring Boot)              │
│     PostgreSQL + MongoDB + JWT Auth + RBAC       │
└────┬──────────────────────┬─────────────────────┘
     │                      │
     ▼                      ▼
┌──────────────┐  ┌──────────────────┐
│  Web Portal  │  │  AI Search       │
│  (Instit.)   │  │  Engine          │
│  Angular 19  │  │  (Neural Core)   │
│  Bootstrap   │  │  FastAPI + dlib  │
└──────────────┘  └──────────────────┘
```

## 📦 Repositories

| Repository | Purpose | Stack | Status |
|------------|---------|-------|--------|
| [web-app](https://github.com/iapex-org/web-app) | Institutional web portal for medical staff | Angular 19, Bootstrap, TypeScript | ✅ Active |
| [mobile-app](https://github.com/iapex-org/mobile-app) | Mobile app for family search | React 18, Ionic 8, Capacitor | ✅ Active |
| [core-api](https://github.com/iapex-org/core-api) | REST API: auth, patients, institutions | Spring Boot 3, PostgreSQL, MongoDB | ✅ Active |
| [neural-core](https://github.com/iapex-org/neural-core) | AI engine: facial + text hybrid search | FastAPI, dlib, scikit-learn | 🚧 Coming soon |

## 🧠 How It Works

1. **Hospitals** register unidentified patients via the **Web Portal** — capturing morphological traits, photographs, and medical data under strict RBAC
2. **Families** search via the **Mobile App** — uploading photos and descriptions of missing loved ones
3. The **Neural Core** fuses FaceNet embeddings (Euclidean distance) with text filters (Levenshtein, Jaro-Winkler) to rank candidates, significantly reducing false positives
4. Matches are displayed with similarity scores — patient privacy is protected until verified by institution staff

## 🔬 Research

Published paper: *"A Hybrid Artificial Intelligent System for the Identification of Missing Persons in Health Institutions"* — [Read the full paper](https://virtual.cuautitlan.unam.mx/intar/wp-content/uploads/sites/19/2025/12/166-A-Hybrid-Artificial-Intelligent-System-for-Missing-JORGE-CHRISTIAN-SERRANO-PUERTOS.pdf)

## 🛡 Privacy & Security

- End-to-end JWT authentication
- Role-Based Access Control (RBAC)
- Patient data anonymized until verified match
- Encrypted media storage

## 🤝 Contributing

We follow a strict PR-based workflow. Check each repository's `CONTRIBUTING.md` for guidelines. All contributions must adhere to our [Code of Conduct](https://github.com/iapex-org/.github/blob/main/CODE_OF_CONDUCT.md).

---

<p align="center">
  <sub>Built with ❤️ by the IAPEX team · 2025</sub>
</p>
