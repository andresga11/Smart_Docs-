# Smart_Docs
Develop a web-based Document Management System tailored for food safety and compliance, enabling users to upload, manage, and track documents with features like version control, approval workflows, and audit trails.

A web-based module designed to manage food safety and compliance documents. It enables uploading, versioning, approval, and tracking of SOPs, audit logs, certificates, and other regulatory documents. The system will support role-based access, searchable document libraries, and audit-ready logs.

# Project Objectives:
Implement a secure and scalable document management platform.

Ensure compliance with food safety standards (e.g., HACCP, FSMA).

Facilitate easy document retrieval and audit readiness.


# Tech Stack:
Frontend: React.js, Tailwind CSS <br>
Backend: Node.js, Express.js <br>
Database: MongoDB <br>
File Storage: AWS S3 (or local for dev) <br>
Authentication: JWT (JSON Web Token) <br>

# Scope:
User authentication and role-based access control.

Document upload, categorization, and storage.

Version control and document history tracking.

Approval workflows with digital signatures.

Audit trail logging user activities.

Search functionality with filters. 

Notifications: Reminders for document expiration and pending reviews.


# System Architecture Diagram
Purpose: Shows how all components (frontend, backend, DB, file storage, auth) interact.

Include:

- React frontend

- Node.js/Express backend

- MongoDB

- AWS S3 (file storage)

- Auth service (JWT)

- API gateway (optional)

![System Architecture](https://github.com/andresga11/Smart_Docs-/blob/main/SmartDocs_System_Architecture.drawio.png)


# Database Schema Diagram (ERD or NoSQL Model)
Purpose: Visualize collections, fields, and relationships.

Include collections like:

- Users

- Documents

- DocumentVersions

- AuditLogs

- Notifications

![Database Architecture](https://github.com/andresga11/Smart_Docs-/blob/main/sDocs_dbDiagram.drawio.png)

# UI Wireframes (Low-Fidelity or High-Fidelity)
Purpose: Map out user experience and navigation.

Pages to wireframe:

- Login/Register

- Dashboard

- Document Upload

- Document Viewer (with approval/version tabs)

- Admin Panel (user management + logs)

Tools: Figma, Balsamiq, or even simple pen-and-paper sketches.

# Workflow Diagram
Purpose: Show how document states change.

Example:

![Screenshot 2025-05-06 at 3 17 56 PM](https://github.com/user-attachments/assets/25764ce9-97af-4c10-8102-936059d5e6c7)

    
Include decision points like who can approve, when notifications are sent, etc.



