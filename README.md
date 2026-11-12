# OpenSeed

[![Angular](https://img.shields.io/badge/Angular-17%2B-DD0031?logo=angular&logoColor=white)](https://angular.dev/)
[![Node.js](https://img.shields.io/badge/Node.js-18%2B-339933?logo=nodedotjs&logoColor=white)](https://nodejs.org/)
[![Apache-2.0](https://img.shields.io/badge/Licencia-Apache--2.0-blue)](LICENSE)

[Español](#español) · [English](#english)

---

## Español

### Índice

- [Descripción](#descripción)
- [Demo](#demo)
- [Características](#características)
- [Stack tecnológico](#stack-tecnológico)
- [Estructura del proyecto](#estructura-del-proyecto)
- [Requisitos](#requisitos)
- [Instalación](#instalación)
- [Uso](#uso)
- [Créditos](#créditos)
- [Licencia](#licencia)

### Descripción

**OpenSeed** ayuda a encontrar *good first issues* en GitHub para dar el salto a contribuir en proyectos de código abierto. Filtra por lenguaje, categoría, licencia, propietario, estrellas, etiqueta o repositorio, y guarda los issues que te interesan para luego.

> Este repositorio es un **fork** del proyecto original de [Akhil P Vijayan](https://github.com/akhilpvijayan/openseed), publicado bajo Apache-2.0.

### Demo

- **Aplicación:** <https://openseed.web.app/>
- **Ficha en Product Hunt:** <https://www.producthunt.com/products/openseed>

### Características

- **Descubrir issues para principiantes** consultando la API de GitHub.
- **Filtros combinables**: lenguaje, categoría (web, móvil, machine learning…), licencia, propietario, forks, estrellas, etiqueta y repositorio.
- **Marcadores** guardados en `localStorage` para volver más tarde.
- **Tema claro y oscuro**.
- **Interfaz multiidioma**.
- **Servidor propio** que firma las peticiones a GitHub con un token, evitando los límites del cliente.

### Stack tecnológico

| Capa | Tecnología |
|---|---|
| Frontend | Angular, TypeScript, Angular Material, SCSS |
| Backend | Node.js + Express (`openseed-server`) |
| Datos | GitHub REST API |
| Despliegue | Firebase Hosting (cliente) y Vercel (servidor) |

### Estructura del proyecto

```text
Openseed/
├── openseed-client/          # Aplicación Angular
│   ├── src/app/              # Componentes, servicios y modelos
│   ├── src/environments/     # URL del backend
│   └── package.json
├── openseed-server/          # API intermedia en Node.js
│   ├── api/github.js         # Llamadas a la GitHub API
│   ├── server.js
│   └── vercel.json
├── LICENSE                   # Apache-2.0
└── README.md
```

### Requisitos

- **Node.js 18 o superior** y npm.
- Un **token de GitHub** con permisos de lectura pública (sin scopes especiales).

### Instalación

```bash
git clone https://github.com/alberto2005-coder/Openseed.git
cd Openseed/openseed-server
npm install
```

Crea un `.env` en `openseed-server`:

```bash
GITHUB_TOKEN=tu_token_de_github
GITHUB_API_URL=https://api.github.com
```

Después, el cliente:

```bash
cd ../openseed-client
npm install
```

Ajusta la URL del backend en `src/environments/environment.ts` si no usas `http://localhost:3000`.

### Uso

```bash
# terminal 1
cd openseed-server && node server.js

# terminal 2
cd openseed-client && ng serve
```

Abre <http://localhost:4200>.

- **Filtrar**: usa la barra lateral para acotar por lenguaje, categoría, licencia, propietario, forks, estrellas, etiqueta o repositorio.
- **Guardar**: marca issues para revisarlos luego.
- **Tema e idioma**: los conmutadores están en la esquina superior.

### Créditos

Proyecto original de **Akhil P Vijayan** y colaboradores. Este fork conserva su licencia y su estructura; los cambios propios se limitan a documentación y ajustes menores.

### Licencia

**Apache-2.0**, la misma del proyecto original: consulta [LICENSE](LICENSE). Permite uso comercial y modificaciones siempre que se conserve el aviso de copyright y se indique qué cambió.

---

## English

### Table of contents

- [Overview](#overview)
- [Demo](#demo)
- [Features](#features)
- [Tech stack](#tech-stack)
- [Project structure](#project-structure)
- [Requirements](#requirements)
- [Installation](#installation)
- [Usage](#usage)
- [Credits](#credits)
- [License](#license)

### Overview

**OpenSeed** helps you find *good first issues* on GitHub so you can start contributing to open source. Filter by language, category, license, owner, stars, label or repository, and bookmark the issues you want to come back to.

> This repository is a **fork** of the original project by [Akhil P Vijayan](https://github.com/akhilpvijayan/openseed), released under Apache-2.0.

### Demo

- **App:** <https://openseed.web.app/>
- **Product Hunt page:** <https://www.producthunt.com/products/openseed>

### Features

- **Beginner-friendly issue discovery** powered by the GitHub API.
- **Combinable filters**: language, category (web, mobile, machine learning…), license, owner, forks, stars, label and repository.
- **Bookmarks** stored in `localStorage`.
- **Light and dark themes**.
- **Multi-language interface**.
- **Own backend** that signs GitHub requests with a token, sidestepping client-side rate limits.

### Tech stack

| Layer | Technology |
|---|---|
| Frontend | Angular, TypeScript, Angular Material, SCSS |
| Backend | Node.js + Express (`openseed-server`) |
| Data | GitHub REST API |
| Deployment | Firebase Hosting (client) and Vercel (server) |

### Project structure

```text
Openseed/
├── openseed-client/          # Angular app
│   ├── src/app/              # Components, services and models
│   ├── src/environments/     # Backend URL
│   └── package.json
├── openseed-server/          # Node.js middleware API
│   ├── api/github.js         # GitHub API calls
│   ├── server.js
│   └── vercel.json
├── LICENSE                   # Apache-2.0
└── README.md
```

### Requirements

- **Node.js 18 or later** and npm.
- A **GitHub token** with public read access (no special scopes).

### Installation

```bash
git clone https://github.com/alberto2005-coder/Openseed.git
cd Openseed/openseed-server
npm install
```

Create a `.env` inside `openseed-server`:

```bash
GITHUB_TOKEN=your_github_token
GITHUB_API_URL=https://api.github.com
```

Then the client:

```bash
cd ../openseed-client
npm install
```

Point `src/environments/environment.ts` at your backend if it is not `http://localhost:3000`.

### Usage

```bash
# terminal 1
cd openseed-server && node server.js

# terminal 2
cd openseed-client && ng serve
```

Open <http://localhost:4200>.

- **Filter**: use the sidebar to narrow by language, category, license, owner, forks, stars, label or repository.
- **Bookmark**: save issues to review later.
- **Theme and language**: both toggles sit in the top corner.

### Credits

Original project by **Akhil P Vijayan** and contributors. This fork keeps its license and structure; its own changes are limited to documentation and minor adjustments.

### License

**Apache-2.0**, the same as the original project: see [LICENSE](LICENSE). It allows commercial use and modifications as long as the copyright notice is preserved and changes are stated.
