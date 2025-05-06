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

# A. User Layer (Frontend)
- Technology: React.js + Tailwind CSS

- Purpose:

    - Provides a responsive interface for document uploads, searches, and workflow management.

    - Communicates with the backend via RESTful APIs.

- Key Features:

    - Role-based UI rendering (e.g., Admins see approval buttons, Users see upload forms).

    - Real-time notifications (using WebSockets or polling).
 
  
# B. Backend Layer (Business Logic)
- Technology: Node.js + Express.js
- Core Modules:
    - JWT Authentication
        - Validates user roles (Admin/Auditor/User) using tokens.
        - Secures API endpoints (e.g., only Admins can approve documents).
    - Document Workflow Engine
        - Manages version control (e.g., v1.0 → v2.0).
        - Enforces approval workflows (e.g., Auditor sign-off before publishing).
    - Audit Trail Logger
        - Tracks all actions (who edited what and when).
        - Stores logs in MongoDB for compliance audits.
    - Search Service
        - Full-text search with filters (e.g.,Show all expired HACCP certificates").
    - Notification Service
        - Sends alerts for expiring documents/pending approvals (email/in-app).

# C. Data Layer
- Mongodb:
    - Stores structured data: User profiles, document metadata, audit logs.
    - Relationships:
        - Users → Documents (One-to-Many: A user owns many documents).
        - Documents → DocumentVersions (One-to-Many: A document has multiple versions).
- AWS S3:
    - Stores files (PDFs, images) with versioning enabled.
    - Each DocumentVersion points to an S3 file path.


![System Architecture](https://github.com/andresga11/Smart_Docs-/blob/main/SmartDocs_System_Architecture.drawio.png)


# Database Schema Diagram (ERD or NoSQL Model)
Purpose: Visualize collections, fields, and relationships.

Include collections like:

- Users
    - Stores user details with role-based access control (Admin, Auditor, User).
    - Linked to DOCUMENTS (owner) and AUDIT_LOGS (actions).
      
- Documents
    - Tracks metadata (title, category, expiry date).
    - References USERS._id for ownership and approval.

- DocumentVersions
    - Manages version history with S3 file paths, approval status, and change notes.
    - Linked to DOCUMENTS (parent) and USERS (uploader/approver).

- AuditLogs
    - Logs all user actions (timestamps, IPs) for compliance.
    - References USERS, DOCUMENTS, and DOCUMENT_VERSIONS.
      
- Notifications
    - Alerts for approvals/expiries, marked as read/unread.

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



