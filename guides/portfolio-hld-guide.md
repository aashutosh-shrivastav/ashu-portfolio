
# Portfolio Project High-Level Design (HLD) Guide

## Purpose
This guide outlines the high-level architecture and design principles for the Candidate's portfolio project, ensuring scalability, maintainability, and a modern user experience. It is written to be framework-agnostic, enabling future migration between UI frameworks (e.g., Angular, React).

- **Monorepo Structure:** Both Frontend Application and API reside in a single repository for easier management and atomic commits.
- **Current Framework Choices:**
	- UI: Angular (latest version)
	- API: Spring Boot (latest version)
- **Frontend Application:**
	- Modular, component-based, and feature-oriented structure.
	- Technology-agnostic: can be implemented in Angular, React, or other frameworks.
	- Minimalistic, responsive design.
	- Reusable component library (tables, cards, templates) as a separate package or library.
	- Styling should use a themeable, utility-first approach (e.g., CSS variables, Tailwind, Material Design), not tied to a specific framework.
- **Backend:** Spring Boot (latest version), RESTful API, PostgreSQL (to be integrated in later phases).
- **Data Flow (Phase 1):** Frontend fetches data from static JSON files in the assets/public folder, simulating API responses.
- **Data Flow (Phase 2):** Replace JSON file calls with real API endpoints as backend is developed.

## API Contracts & Data Schemas
- Clearly define all API endpoints and data schemas in a shared documentation (OpenAPI/Swagger or Markdown), so any UI can consume them.

## Key Modules/Components
- **Landing Page:** Brief intro, call-to-action, and navigation.
- **About:** Professional summary, skills, and aspirations.
- **Projects:** List of projects with summary and tech stack.
- **Resume:** Downloadable PDF generated at runtime.
- **Contact:** Social links and mail button.
- **Blog (Future):** Section for technical articles and insights.

## Security & Extensibility
- Minimal user data collected; no authentication in initial phase.
- Plan for role-based access (admin/user) in later phases.
- Modular code structure for easy feature addition and maintenance.

## Scalability & Performance
- Use lazy loading/code splitting as supported by the chosen UI framework.
- Optimized asset loading and modularization.
- Backend designed for stateless REST APIs and easy scaling.

## DevOps & Deployment
- Use Docker for containerization (optional in early phase).
- CI/CD pipeline with GitHub Actions or similar.
- Deploy frontend and backend separately or together as needed.

## Best Practices
- Follow framework-agnostic coding standards and best practices.
- Write unit tests for critical components and services (Jest recommended for UI).
- Use recruiter-friendly keywords in UI content.
- Keep design and codebase minimal, clean, and professional.