# Blog CMS

A full-stack blog content management system with a Spring Boot REST API, a Vue website and admin dashboard, and a Uni-app H5/WeChat Mini Program client.

## Languages

- **Backend:** Java 21
- **Frontend and cross-platform client:** JavaScript, Vue single-file components, HTML and CSS
- **Data and tooling:** SQL, Python, PowerShell and shell scripts

## Development Environment

| Component | Requirement / Stack |
| --- | --- |
| Java | JDK 21 |
| Backend | Spring Boot 3.5.16, Spring Security, JdbcTemplate |
| Build tools | Maven 3.9+, Node.js 22+, npm |
| Web frontend | Vue 3.5.44, Vue Router 4, Vite 7.3.7 |
| Cross-platform client | Uni-app with a separate Vue/Vite dependency tree |
| Local database | Persistent H2 database |
| Production database | MySQL 8+ |
| Production environment | Linux, Java 21, Nginx, systemd and HTTPS |

Use the lockfile in each application directory. Keep the Uni-app vendor patches and build helpers included in the source archive.

## Features

- Article and page management with drafts, publishing and archiving
- Categories, tags, search, comments and media uploads
- Role-based admin access, session authentication and CSRF protection
- Editable homepage carousel advertisements
- SEO-friendly category routes such as `/category/1`, with legacy URL redirects
- Responsive layouts and light/dark themes
- H5 and WeChat Mini Program source code; WeChat platform configuration is required separately

## Source Code and Documentation

- [Complete source archive](ittext-cms-source-2026-10-24.zip)
- [SHA-256 checksum](ittext-cms-source-2026-10-24.zip.sha256)
- [Development Guide (Chinese)](开发手册.md)
- [Deployment Guide (Chinese)](部署手册.md)

Download and extract the ZIP, then open the `ittext-cms` directory. The archive includes the backend, web application, Uni-app client, dependency lockfiles, vendor patches, design assets and project documentation. This repository currently stores the project as a source archive rather than an expanded Git source tree.

## Quick Start

From the extracted project root, run the backend:

```sh
mvn -f backend/pom.xml spring-boot:run
```

In another terminal:

```sh
cd web
npm ci
npm run dev
```

The default website is at `http://localhost:5173` and the backend API is at `http://127.0.0.1:8080`. Configure production secrets through server-side environment variables.

## Delivery Scope

The archive excludes databases, article exports, uploaded business attachments, credentials, private keys, local toolchains, `node_modules` and build outputs. A fresh installation does not contain production articles; restore authorized data backups separately. The ZIP includes a per-file SHA-256 manifest.

No project-wide open-source license has been selected. Third-party license notices remain with the bundled dependencies and assets.
