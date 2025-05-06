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

 -Node.js/Express backend

- MongoDB

- AWS S3 (file storage)

- Auth service (JWT)

- API gateway (optional)


# Database Schema Diagram (ERD or NoSQL Model)
Purpose: Visualize collections, fields, and relationships.

Include collections like:

- Users

- Documents

- DocumentVersions

- AuditLogs

- Notifications

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

Upload → Draft → Review → Approved → Archived
        ↓         ↓         ↓
    Rejected   Needs Edit   Expired
    
Include decision points like who can approve, when notifications are sent, etc.



