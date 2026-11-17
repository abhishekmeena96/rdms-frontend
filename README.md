# RDMS

### Enterprise Document Management Application

RDMS is an enterprise document management application built by extending the open-source [Alfresco Content Application (ACA)](https://github.com/Alfresco/alfresco-content-app).

It provides document management, metadata handling, collaboration, and workflow-based review and approval capabilities. The frontend was extended with custom Angular components and integrations to support RDMS-specific requirements.

## Features

- **Document Management** – Browse, view and manage documents using the Alfresco platform.
- **Document Details** – Custom document detail page combining document viewing with related information and actions.
- **Properties Management** – Custom metadata interface with General, Classification, Lifecycle, Technical and Audit sections.
- **Comments** – Add, view, reply to, edit and delete document comments.
- **Version History** – View document versions with a customized presentation.
- **Workflow Management** – Start document review and approval workflows and assign users.
- **Task Management** – View assigned documents and complete review or approval tasks through My Tasks.
- **Workflow Status** – Track document status, including Pending, Approved and Rejected.
- **Generate Cover Page** – Trigger cover-page generation through a backend API.
- **Authentication** – Choose between Basic and Keycloak-based login.
- **Navigation** – Customized sidebar navigation with folder tree support.

## Technology Stack

| Category | Technologies |
|---|---|
| Frontend | Angular 17, TypeScript |
| UI | Angular Material |
| Application Foundation | Alfresco ACA, ADF |
| State Management | NgRx |
| Reactive Programming | RxJS |
| Configuration | JSON-based ACA Extensions |
| API Integration | REST APIs, Angular Services |
| Document Repository | Alfresco Content Services |
| Workflow Engine | Camunda |
| Authentication | Basic Authentication, Keycloak |

## Architecture

RDMS extends the existing ACA application by combining reusable Alfresco components with custom Angular functionality.

```text
                 RDMS Frontend
                   Angular 17
                       |
          +------------+------------+
          |                         |
      ACA / ADF              Custom RDMS
      Components             Components
      Services               Dialogs
      Extensions             Features
          |                         |
          +------------+------------+
                       |
              Services / NgRx / RxJS
                       |
                    REST APIs
                       |
          +------------+------------+
          |                         |
    Alfresco Content          Custom Backend
       Services                    APIs
                                      |
                                   Camunda
```

Keycloak is used as an authentication option for the frontend.

## My Contribution

My primary responsibility was **frontend development and customization using Angular 17 and Alfresco ACA**.

### Developed
- Custom Document Detail Page.
- Document Actions Panel.
- Properties V2 dialog and supporting components.
- Document comments functionality.
- Workflow status interface.
- My Tasks component.
- Workflow and task completion dialogs.
- Basic and Keycloak login interfaces.

### Customized and Integrated
- Reused the existing Alfresco document viewer.
- Customized the presentation of existing version history functionality.
- Customized sidebar navigation and folder tree.
- Integrated document actions using `app.extensions.json` and `AppExtensionService`.
- Integrated frontend functionality with Alfresco and team-developed REST APIs.
- Connected the Generate Cover Page action to its backend API.

Backend development, Camunda workflow implementation and Keycloak infrastructure were handled by other team members.

## Project Scope

This repository serves as a project portfolio and documentation reference. It describes RDMS, its features, architecture, technologies and my individual frontend contributions.

It does not contain the complete RDMS application source code or backend implementation.

## References

- [Alfresco Content Application (ACA)](https://github.com/Alfresco/alfresco-content-app)
- [Alfresco Application Development Framework (ADF)](https://github.com/Alfresco/alfresco-ng2-components)
- [Alfresco API Explorer](https://api-explorer.alfresco.com/api-explorer/)
