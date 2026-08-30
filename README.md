# Joel Pasapera

**Data-oriented Python developer — quantitative analysis & trading systems.**

I turn data into decisions: statistical models, trading strategies, and analysis pipelines, with a focus on keeping the number-crunching fast. Based in Peru 🇵🇪, working in quantitative and algorithmic trading.

development philosophy: 

1. Development of high-performance algorithms (including building from scratch if the system requires it) 
2. "No uploads. No servers. No tracking" (whenever possible)
3. Preference for low-level implementations when performance and reliability are critical.

---


#### 🔗 Find me

[Portfolio](https://joelpasapera.github.io/) · [ORCID](https://orcid.org/0000-0003-3023-2147) · [MQL5](https://www.mql5.com/en/users/joel_pasapera)

---

<div align="center">

  <h1>Joel Pasapera</h1>
  <h3>Systems Architecture, High-Performance Computing & Software Engineering</h3>

  <p>
    <img src="https://img.shields.io/badge/Rust-000000?style=for-the-badge&logo=rust&logoColor=white" />
    <img src="https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=cplusplus&logoColor=white" />
    <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" />
    <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" />
    <img src="https://img.shields.io/badge/Kotlin-7F52FF?style=for-the-badge&logo=kotlin&logoColor=white" />
    <img src="https://img.shields.io/badge/Swift-F05138?style=for-the-badge&logo=swift&logoColor=white" />
  </p>

</div>

---

## 🛠️ Technology Stack & Operational Strategy

### ⚡ Systems & High-Performance Backend

* **Rust** *(Default Core)*
  * **Use Cases:** Greenfield native cores, security-sensitive cryptography (`RustCrypto`, `ring`), cross-platform logic shared across Android/iOS/Desktop via `UniFFI`, zero-data-race concurrent systems, high-reliability backends (`Axum`, `Actix`), high-performance CLI tools, and WebAssembly.
  * **When to choose:** Building from scratch for long-term maintainability where memory safety and performance are non-negotiable.

* **C++** *(Ecosystem-Driven)*
  * **Use Cases:** Real-time game/graphics engines (Unreal, custom), audio/video processing and codecs, computer vision (`OpenCV`), heavy numerical computing (`Eigen`, `BLAS`/`MKL`, `CUDA`), embedded systems, and legacy codebase integrations.
  * **When to choose:** When target ecosystems require official C++ drivers or absolute low-level hardware control.

> **Backend Decision Protocol:**
> 1. **Standard I/O-bound API:** Python / FastAPI.
> 2. **High-Demand Systems:** Rust by default.
> 3. **Rule:** All high-performance code targets Rust; C++ is introduced strictly when forced by specific library dependencies.

---

### 🌐 Frontend & Native UIs

* **The Web Triad (JavaScript, HTML, CSS)**
  * **Use Cases:** Web applications, interactive dashboards, SaaS frontends, and PWAs.
  * **When to choose:** When rapid iteration, universal distribution, and zero-installation access via the browser are required.

* **Kotlin (Jetpack Compose)**
  * **Use Cases:** Native Android UIs, notifications, navigation, and Android SDK integration.
  * **Architecture:** Kotlin handles the UI layer; heavy lifting runs on the underlying Rust core via `UniFFI`.

* **Swift (SwiftUI)**
  * **Use Cases:** Native iOS UIs, Apple ecosystem integration, and declarative interfaces.
  * **Architecture:** Swift handles the UI layer, consuming the exact same shared Rust core via `UniFFI` bindings.

> **UI Decision Protocol:**
> * **Mobile App Store distribution:** Native Kotlin / Swift frontends + Single shared Rust core.
> * **Universal browser reach:** Web Triad / PWA.

---

### 🐍 Prototyping & Data Science

* **Python**
  * **Use Cases:** Data science, ML/AI exploration, vectorized mathematical modeling (`NumPy`, `SciPy`, `Polars`), web automation, web scraping, rapid REST APIs (`FastAPI`), and algorithmic prototyping before compiling to Rust or C++.
  * **When to choose:** When development speed outweighs execution latency, or when validating ideas against data.

---

<div align="center">

*Engineered for performance, safety, and architectural clarity.*

</div>
