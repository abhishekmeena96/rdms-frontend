# RDMS – Frontend Features

## Overview

RDMS is an enterprise document management application built by customizing the open-source **Alfresco Content Application (ACA)**.

This document describes the frontend features I developed, customized, and integrated as part of the RDMS project using Angular 17 and the Alfresco ACA framework.

**Scope:** My contribution was focused on frontend development. Backend services, Camunda workflow engine implementation, and Keycloak infrastructure were handled by other team members.

---

## 1. Document Detail Page

Developed a custom `DocumentDetailPage` component to provide a detailed document management experience.

The page opens when a user selects a document from the document listing.

Key functionality:

- Displays document information and details.
- Provides access to document properties.
- Displays document comments.
- Shows document version history.
- Displays current workflow status.
- Provides access to available document actions.

The component brings important document-related information and operations together in one interface.

## 2. Properties Management

Developed and customized the frontend properties interface to organize and display document metadata.

The properties interface includes sections such as:

- **General** – General document information.
- **Classification** – Document classification details.
- **Lifecycle** – Document lifecycle information.
- **Technical** – Technical document metadata.
- **Audit** – Audit-related information.

Integrated the frontend with the existing application services and APIs for document property operations.

## 3. Document Comments

Implemented frontend functionality for managing document comments.

Key functionality:

- Add new comments.
- View existing comments.
- Reply to comments.
- Edit existing comments.
- Delete comments.

This provides users with a way to discuss and track information related to individual documents.

## 4. Document Version History

Customized the existing Alfresco version history presentation within the RDMS frontend.

Key functionality:

- Display document version numbers.
- View previous document versions.
- Download previous document versions.

The implementation builds on the existing Alfresco version history functionality rather than replacing its underlying backend capabilities.

## 5. Document Workflow Status

Developed the frontend workflow status interface to display the current status of a document.

Supported statuses include:

- Pending
- Approved
- Rejected

The interface displays workflow information received through the application's integration with the workflow services.

## 6. Workflow Management

Implemented frontend functionality for starting and assigning document workflows.

The application supports the following workflow types:

- Review
- Approval

Key functionality:

- Start a workflow from the document actions panel.
- Select the required workflow type.
- Search for users through the user management integration.
- Assign the workflow to another user.
- Integrate the frontend workflow experience with the existing backend services.

The workflow engine and backend workflow implementation are handled by the backend team. My contribution focused on the Angular frontend and its integration.

## 7. My Tasks and Task Completion

Developed the frontend My Tasks experience for working with assigned document tasks.

Key functionality:

- View assigned documents and tasks.
- Access review and approval tasks.
- Open the relevant task interface.
- Complete assigned workflow tasks through the frontend.

Also developed supporting workflow and task completion dialogs and integrated them with the available backend APIs.

## 8. Document Actions Panel

Customized the existing Alfresco ACA `DocumentActionsPanelComponent` to support RDMS-specific document operations.

The panel provides access to actions such as:

- Delete
- Copy
- Preview
- Start Workflow

Key contributions:

- Customized the existing ACA document actions panel.
- Added and configured RDMS-specific actions.
- Integrated the custom Start Workflow action.
- Reused existing ACA actions and services where applicable.
- Used ACA's extension and configuration mechanisms to integrate document actions.

## 9. Sidebar and Navigation Customization

Customized the existing ACA sidebar navigation to support RDMS navigation requirements.

Navigation sections include:

- My Home
- Trash
- Favorites
- Personal Files

Also developed a custom folder tree interface to display subfolders within the navigation experience.

The tree focuses on folder navigation rather than displaying individual files.

## 10. Authentication Integration

Developed separate frontend login interfaces for Basic authentication and Keycloak-based authentication.

Key contributions:

- Created a Basic login interface.
- Created a Keycloak login interface.
- Updated the frontend authentication approach from Basic authentication to an OAuth-based approach.
- Integrated the frontend with the existing Keycloak authentication infrastructure.

Keycloak server configuration and infrastructure were managed by the team.

## 11. Generate Cover Page

Integrated a frontend action for generating a document cover page.

Key functionality:

- Provides a user-accessible Generate Cover Page action.
- Triggers the corresponding backend API.
- Connects the frontend action with the existing backend functionality.

The cover page generation logic is handled by the backend service.

## 12. ACA Configuration and Customization

Customized the Alfresco Content Application using its existing extension and configuration mechanisms.

Key contributions:

- Worked with JSON-based ACA configuration.
- Configured and integrated document actions.
- Customized menus and navigation.
- Worked with form and field configurations.
- Integrated custom components and extensions.
- Used `app.extensions.json` and `AppExtensionService` for application extension integration.
- Reused existing ACA services and created or modified Angular services where required.

These customizations allowed RDMS-specific functionality to be integrated into the existing Alfresco application.

---

## Technical Areas

The frontend work involved the following technologies and concepts:

| Area | Technologies |
|---|---|
| Frontend Framework | Angular 17 |
| Programming Language | TypeScript |
| State Management | NgRx |
| Reactive Programming | RxJS |
| UI Components | Angular Material |
| Alfresco Framework | Alfresco ACA / ADF |
| Configuration | JSON-based ACA extensions |
| Integration | REST APIs and Angular services |
| Authentication Integration | Keycloak |
| Workflow Integration | Camunda |

## Contribution Summary

My work focused on extending and customizing the existing Alfresco ACA frontend to support RDMS-specific document management and workflow requirements.

The main areas of contribution included:

- Developing custom Angular components and dialogs.
- Customizing existing Alfresco ACA components.
- Implementing document comments and properties interfaces.
- Integrating document version history and workflow status.
- Developing workflow initiation and task management interfaces.
- Customizing document actions and sidebar navigation.
- Implementing frontend authentication integration.
- Working with NgRx, RxJS, Angular services, and JSON-based ACA extensions.
- Integrating frontend functionality with existing Alfresco and backend APIs.

**Project scope clarification:** This repository documents my frontend contribution to RDMS. It does not contain the complete RDMS application, backend implementation, Camunda workflow engine, or Keycloak infrastructure.
