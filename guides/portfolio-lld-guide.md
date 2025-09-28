# Portfolio Project Low-Level Design (LLD) Guide

## Purpose
This guide details the component structure, data flows, schemas, and reusable elements for both the UI (Frontend Application) and API (Spring Boot) layers of the Candidate's portfolio project. It is written to be framework-agnostic, enabling future migration between UI frameworks (e.g., Angular, React).

## UI (Frontend Application) Structure

- **Workspace Layout:**
  - Use a workspace with:
    - `portfolio-app`: Main application project (feature-based folder structure)
    - `portfolio-ui-lib`: Library for reusable components (e.g., tables, cards, templates)
- **Feature-Based Structure:**
  - Organize features as `/projects`, `/about`, `/resume`, etc., within the app.
  - Shared and core modules for generic services and components.
- **Styling:**
  - Use a themeable, utility-first CSS approach (e.g., CSS variables, Tailwind, Material Design), not tied to a specific framework.
  - Leverage a component library for UI consistency (e.g., Material UI, Chakra UI, or Angular Material if using Angular).
- **State Management:**
  - Use service-based state management (e.g., Angular services, React context/hooks, or equivalent) for any shared state; no external state management library required for this project.

## API (Spring Boot) Structure

- **Workspace Layout:**
  - `portfolio-api`: Main application module.
  - Plan for a future reusable library module (e.g., for generic utilities or services, to be externalized as a JAR).
- **Module Organization:**
  - Service module for controllers and business logic.
  - Core module for core entities and shared logic.

## Data Flow

- **Phase 1:** Frontend app fetches data from static JSON files in the `assets` or `public` folder.
- **Phase 2:** Replace JSON calls with REST API endpoints as backend is developed.

## Data Schemas (Sample)

- **Project:**
  ```json
  {
    "id": "string",
    "title": "string",
    "description": "string",
    "techStack": ["string"],
    "link": "string",
    "year": "number"
  }
  ```
- **About:**
  ```json
  {
    "name": "string",
    "summary": "string",
    "skills": ["string"],
    "aspirations": "string"
  }
  ```
- **Resume:**
  ```json
  {
    "education": [
      {
        "degree": "string",
        "institution": "string",
        "year": "number"
      }
    ],
    "experience": [
      {
        "role": "string",
        "company": "string",
        "duration": "string",
        "details": ["string"]
      }
    ]
  }
  ```

## UML Diagrams

- Use Mermaid markdown for any UML diagrams in documentation or design discussions.
- Example component relationship diagram:

  ```mermaid
  classDiagram
      PortfolioApp --> ProjectsFeature
      PortfolioApp --> AboutFeature
      PortfolioApp --> ResumeFeature
      PortfolioApp --> PortfolioUiLib
      PortfolioUiLib <|-- TableComponent
      PortfolioUiLib <|-- CardComponent
  ```

## Testing

- Unit tests should be written for critical components and services.
- UI: Use Angular's built-in testing utilities (Jasmine/Karma).
- API: Use JUnit/TestNG for service and controller tests.
- Focus on testing data flows, component rendering, and API responses.

## Additional Notes

- LLD should focus on data flows, data objects, component/module structure, and relationships.
- Keep the design modular to allow for future extraction of reusable libraries or modules.
- Use recruiter-friendly keywords in UI content and documentation.