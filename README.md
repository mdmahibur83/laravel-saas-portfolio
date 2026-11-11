# Laravel SaaS Portfolio

### Multi-Tenant SaaS Architecture with Laravel, React, TypeScript & Inertia.js

A portfolio project demonstrating how I design and structure modern SaaS applications using **Laravel, PHP, React, TypeScript, Inertia.js, MySQL, authentication, role-based access control, multi-tenant data separation, dashboards, and production-oriented architecture**.

This repository is designed as a public technical portfolio project and does not contain private customer data, production credentials, API keys, or proprietary source code from commercial systems.

---

## 🚀 Project Overview

The goal of this project is to demonstrate the architecture of a scalable SaaS platform where:

- Users can create accounts
- One user can manage multiple business profiles
- Each business can have its own website
- Businesses can connect custom domains and subdomains
- Admins can manage platform users and settings
- Customers and administrators have separate dashboards
- Data access is protected through authorization policies
- Business data is isolated between users
- The platform can be extended with billing, email, APIs, and automation

---

# 🛠 Technology Stack

## Backend

- PHP
- Laravel
- Laravel Authentication
- Laravel Policies
- REST API Architecture
- Form Request Validation
- Service Layer Architecture
- Eloquent ORM
- Laravel Migrations
- Role-Based Access Control

## Frontend

- React
- TypeScript
- Inertia.js
- JavaScript
- HTML5
- CSS
- Responsive UI
- Component-Based Architecture

## Database

- MySQL
- SQLite for local development
- Relational Data Modeling
- Database Migrations
- Foreign Keys
- Soft Deletes
- Data Validation

## Infrastructure

- Ubuntu Linux
- Nginx
- PHP-FPM
- Composer
- Node.js
- npm
- SSL / HTTPS
- DNS Management
- VPS Deployment

---

# ✨ Core Features

## 👤 Authentication

- User registration
- User login
- Secure authentication
- Password management
- Session handling
- Protected routes

---

## 🏢 Multi-Business Management

A single user account can manage multiple business profiles.

Each business can contain:

- Business name
- Registration information
- Address
- Contact information
- Industry information
- Branding details
- Website information
- Domain information

Users can:

- Create a business
- View a business
- Edit a business
- Archive or safely delete a business
- Manage associated website information

---

## 🌐 Website Management

Each business can have its own website configuration.

Planned architecture supports:

- Business website creation
- Website status
- Website branding
- Website pages
- SEO settings
- Custom hostname
- Primary domain selection
- Preview environment

---

## 🔗 Custom Domain Management

The architecture supports customer-owned:

- Apex domains
- Subdomains
- DNS verification
- Domain ownership verification
- Primary hostname management
- SSL deployment workflows

Example:

```text
example.com
www.example.com
portal.example.com
```

---

## 👨‍💼 Admin Panel

Administrative features include:

- Dashboard
- User management
- Platform settings
- Branding settings
- SEO settings
- Audit logs
- Account status management
- Role management

---

## 👨‍💻 Customer Dashboard

Customer-facing features include:

- Dashboard overview
- Business management
- Website management
- Domain management
- Profile management
- Security settings

---

# 🔐 Authorization & Security

Security is an important part of the architecture.

The project demonstrates concepts including:

- Authentication
- Authorization policies
- Role-based access control
- User ownership validation
- Tenant data isolation
- Protected admin routes
- Request validation
- Secure database relationships
- Soft deletion
- Audit logging

---

# 🧱 Application Architecture

Example architecture:

```text
app/
├── Http/
│   ├── Controllers/
│   ├── Middleware/
│   └── Requests/
│
├── Models/
│
├── Policies/
│
├── Services/
│
└── Providers/

database/
├── migrations/
├── seeders/
└── factories/

resources/
└── js/
    ├── components/
    ├── layouts/
    ├── pages/
    └── types/

routes/
├── web.php
└── api.php

tests/
├── Feature/
└── Unit/
```

---

# 🗄 Example Data Relationships

```text
User
 │
 ├── BusinessProfile
 │      │
 │      ├── Website
 │      │      │
 │      │      ├── Domain
 │      │      └── WebsitePage
 │      │
 │      └── BusinessSettings
 │
 └── UserSettings
```

This structure allows one user to manage multiple businesses while keeping business data properly separated.

---

# 🔄 Example SaaS Workflow

```text
User Registration
        ↓
Create Business Profile
        ↓
Configure Business Information
        ↓
Create Website
        ↓
Configure Branding & SEO
        ↓
Connect Domain
        ↓
Verify Domain
        ↓
Publish Website
```

---

# 🧩 Architecture Principles

I focus on the following principles when designing SaaS applications:

### Separation of Concerns

Controllers should remain lightweight while business logic is moved into dedicated service classes.

### Secure Authorization

Every sensitive action should verify that the authenticated user has permission to access the requested resource.

### Data Isolation

Users should never be able to access another customer's business or website data.

### Maintainable Code

Application features should be separated into clear models, services, policies, requests, and frontend components.

### Safe Production Changes

New features should be implemented without unnecessarily breaking existing functionality.

---

# 🧪 Testing Strategy

The architecture is designed to support:

- Authentication tests
- Authorization tests
- Business ownership tests
- CRUD feature tests
- Domain management tests
- Validation tests
- Admin access tests
- Tenant isolation tests

Example:

```text
tests/
├── Feature/
│   ├── AuthenticationTest.php
│   ├── BusinessProfileTest.php
│   ├── DomainManagementTest.php
│   ├── AdminAccessTest.php
│   └── TenantIsolationTest.php
│
└── Unit/
```

---

# 🌍 Deployment Architecture

Example production architecture:

```text
Internet
   │
   ▼
Nginx
   │
   ▼
Laravel Application
   │
   ├── React / Inertia Frontend
   │
   ├── PHP-FPM
   │
   └── MySQL
```

Production environments can also include:

- HTTPS / SSL
- Queue workers
- Background jobs
- Scheduled tasks
- Log monitoring
- Backup systems
- Domain routing

---

# 🔧 Local Development

Typical local setup:

```bash
git clone https://github.com/mdmahibur83/laravel-saas-portfolio.git

cd laravel-saas-portfolio

composer install

npm install

cp .env.example .env

php artisan key:generate
```

Configure the database inside `.env`.

Then run:

```bash
php artisan migrate

npm run dev

php artisan serve
```

---

# 🔒 Environment Security

Sensitive information should never be committed to GitHub.

Files such as:

```text
.env
.env.production
private keys
API credentials
database passwords
customer information
```

must remain private.

The repository should only contain:

```text
.env.example
```

with example configuration values.

---

# 📌 Portfolio Purpose

This repository is intended to demonstrate my practical understanding of:

- Laravel application architecture
- SaaS development
- Backend development
- React + TypeScript integration
- Multi-tenant systems
- Authentication
- Authorization
- Database design
- API-ready architecture
- Server deployment
- Business application development

---

# 🚧 Project Status

This repository is being developed as a public portfolio implementation.

Planned additions include:

- Authentication implementation
- Business CRUD
- Website management
- Domain management
- Authorization policies
- Admin dashboard
- Customer dashboard
- Feature tests
- REST API examples
- Deployment documentation

---

# 👨‍💻 Developer

**Mohammad Mahibur Rahman Bigoy**

Full-Stack & Backend Software Developer

### Main Technologies

`Laravel` `PHP` `React` `TypeScript` `Inertia.js` `MySQL` `SQLite` `REST APIs` `Linux` `Nginx`

### Areas of Interest

- SaaS Engineering
- Backend Development
- Full-Stack Development
- Business Automation
- API Integration
- AI Automation
- Multi-Tenant Systems
- Cloud & VPS Deployment

---

# 📫 Contact

**Email:** mdmahibur83@gmail.com

**GitHub:**  
https://github.com/mdmahibur83

**Location:**  
Sylhet, Bangladesh

---

# 🌍 Career

I am currently open to opportunities in:

- Software Development
- Backend Development
- Full-Stack Development
- PHP / Laravel Development
- SaaS Engineering
- Web Application Development

I am particularly interested in software engineering opportunities in **Ireland**.

---

## ⭐ Project Goal

The purpose of this project is simple:

> Build clean, secure, maintainable SaaS architecture while demonstrating practical full-stack software engineering skills.
