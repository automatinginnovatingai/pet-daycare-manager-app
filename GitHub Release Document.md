# Pet Daycare Manager — Unified Desktop Edition
## Initial GitHub Release — Version 1.0.0

This release introduces the fully unified version of the Pet Daycare Manager App, combining
all daycare and boarding features, staff roles, and subscription plans into a single Windows
`.exe` application. The app uses a unified SQL Server–ready architecture, allowing facilities
of any size to deploy the system without maintaining multiple builds.

All subscription tiers (Basic, Pro, Enterprise) are included in one unified application,
with access determined by the user’s plan and role permissions.

---

## Included in This Release
- Basic Plan  
- Pro Plan  
- Enterprise Plan  
- Staff Add‑on  
- Kennel Tech Add‑on  
- Unified SQL Server–ready architecture  
- One installer, one app, one onboarding flow  

---

## Role‑Based Access Control (RBAC)

The Pet Daycare Manager includes a secure, centralized RBAC system designed for multi‑staff
daycare and boarding environments.

### Global Admin
Full system access. Can configure company‑wide settings, manage staff accounts, control
pricing, and access all modules.

### Staff
Operational access. Can manage pets, owners, reservations, check‑ins, check‑outs, daily logs,
billing, and reports depending on plan level.

### Kennel Tech
Hands‑on care role with limited access. Can record feeding, medication, playtime, and notes,
but cannot modify reservations, billing, or staff settings.

### Admin‑Only Registration
Only Global Admins can register new staff accounts. No self‑registration is allowed.

### Dynamic UI Permissions
Each screen automatically adapts to the user’s role and plan. Restricted modules are hidden
or blocked with clear access messages.

### Centralized Permission Enforcement
All role and feature checks are handled through a unified RBAC engine to ensure consistent,
professional‑grade security across every module.

### Multi‑Staff Support
Global Admins can add unlimited staff and kennel techs using the Staff Add‑on. Each user
receives their own secure login and role‑based access.

This RBAC system ensures secure, scalable, and compliant access control across the entire
Pet Daycare Manager platform.

---

## Plan Descriptions

### Basic Plan
Provides essential management features for small daycare or boarding operations.  
Includes core tools for pets, owners, reservations, check‑ins, check‑outs, and basic logs.  
Ideal for facilities needing a reliable, cost‑effective foundation.

---

### Pro Plan
Expands on the Basic plan with advanced operational tools.  
Designed for growing facilities that manage higher pet volume or require deeper tracking.  
Includes kennel assignments, daily logs (feeding, medication, playtime), and enhanced billing.

---

### Enterprise Plan
Unlocks the full capabilities of the system, including everything in Pro plus advanced
features and enterprise‑grade controls.  
Required for organizations with multiple administrators or complex operational needs.

Enterprise includes:
- Advanced reporting and analytics  
- Vaccination forecasting and alerts  
- Incident reporting  
- Capacity management  
- Priority support  
- Staff management with role assignment  
- Marketing kit templates  

---

### Staff Add‑on
Allows Global Admins to add additional Staff users.  
Each staff member receives their own secure login and operational access.  
Cannot function alone — requires an active Basic, Pro, or Enterprise plan.

---

### Kennel Tech Add‑on
Available for Pro and Enterprise customers.  
Provides limited‑access log‑entry functionality for kennel technicians.  
Cannot be used as a standalone license.

---

## License Activation
This application requires a valid license key to unlock full functionality.

- You will be prompted to enter your license key on first launch.  
- The app verifies your key securely through the licensing service.  
- If the license is invalid or revoked, access will be restricted.  
- Internet access is required for initial license validation.

After activation, the app operates fully offline.

---

## Database
The Pet Daycare Manager supports two database modes:

### SQL Express (Local Database — Recommended for 1–5 users)
- Automatically installed and configured by the installer  
- Ideal for individuals, small teams, and single‑machine setups  
- Fully offline and self‑contained  

### SQL Server (Remote or On‑Prem Server)
- Connect to an existing SQL Server instance  
- Supports multi‑user environments and IT‑managed deployments  
- Ideal for medium‑to‑large facilities with dedicated servers  

Both modes use the same unified application and feature set.

---

## Stability
This version is the current stable build and serves as the foundation for all future updates.
All modules have been tested for reliability, data integrity, and multi‑user consistency.
