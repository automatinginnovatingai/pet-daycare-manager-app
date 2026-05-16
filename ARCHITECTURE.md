# PET DAYCARE MANAGER – ARCHITECTURE DOCUMENTATION
==================================================

Overview
--------
The Pet Daycare Manager is a modular, scalable, and role‑secured application designed for
boarding/daycare operations. The architecture follows a clean separation of concerns:

• UI Layer (Tkinter Frames)  
• Manager/Service Layer (Business Logic)  
• Engine Layer (Calculations, Scheduling, Forecasting)  
• Database Layer (SQL Server + migrations)  
• Utilities Layer (PDF, images, file handling, logging)  
• RBAC + Session Layer (roles, plans, permissions)

This document describes the structure, responsibilities, and interactions of each module.

--------------------------------------------------
1. CORE APPLICATION LAYER
--------------------------------------------------
These files initialize the application, manage routing, and control frame switching.

• main.py  
  Entry point of the application.

• app_controller.py  
  Central controller that manages UI frames and navigation.

• router.py  
  Defines routing rules and maps UI frames to controller actions.

--------------------------------------------------
2. UI FRAMEWORK LAYER
--------------------------------------------------
Reusable UI components and layout helpers.

• ui_main_window.py  
  Main Tkinter window wrapper.

• ui_navigation.py  
  Navigation helpers and shared UI patterns.

• ui_settings.py  
  Application settings UI (admin‑only).

--------------------------------------------------
3. USER & ROLE MANAGEMENT
--------------------------------------------------
Handles authentication, session state, RBAC, and staff management.

• staff_manager_ui.py  
  Add/edit/archive staff accounts.

• add_staff_ui.py  
  UI for creating new staff members.

• staff_ui.py  
  Staff listing and management.

• session_context.py  
  Stores session data (user, company, plan, role).

• centralized_rbac.py  
  Feature‑level permission enforcement.

Roles:
- Global Admin  
- Staff  
- Kennel Tech

Plans:
- Basic  
- Pro  
- Enterprise

--------------------------------------------------
4. SHARED FEATURE MODULES
--------------------------------------------------
Reusable modules across the entire system.

• pets_ui.py  
  Pet profiles, medical notes, owner linking.

• owners_ui.py  
  Owner profiles and contact information.

• vaccinations_ui.py  
  CRUD + analytics for vaccinations.

• vaccination_alerts_ui.py  
  Color‑coded alerts for upcoming, recent, and overdue vaccinations.

• vaccination_forecast_ui.py  
  Forecast per‑pet vaccination schedule.

• vaccination_schedule_engine.py  
  Calculates next‑due dates and vaccination status.

• vaccinations_manager.py  
  CRUD operations for vaccinations.

• reminders_ui.py  
  Task reminders and notifications.

• reports_ui.py  
  PDF reports, charts, analytics.

• marketing_kit_ui.py (optional)  
  Templates for promotional materials.

--------------------------------------------------
5. BOARDING/DAYCARE MODULES
--------------------------------------------------
Core operational modules for daycare/boarding workflows.

• reservation_manager.py  
  Create, modify, and manage reservations.

• checkin_manager.py  
  Intake workflow for pets arriving at the facility.

• checkout_manager.py  
  Release workflow with billing integration.

• kennel_manager.py  
  Assign pets to kennels and track occupancy.

• daily_logs_manager.py  
  Daily activity logs (feeding, medication, playtime, notes).

• feeding_manager.py  
  Feeding schedule and logs.

• medication_manager.py  
  Medication tracking and dosage logs.

• playtime_manager.py  
  Playtime sessions and enrichment logs.

• incident_report_manager.py  
  Behavioral or medical incident reporting.

• billing_manager.py  
  Charges, invoices, and payment tracking.

• rate_plan_manager.py  
  Pricing rules for services.

• capacity_manager.py  
  Facility capacity tracking and kennel availability.

• pet_profile_ui.py  
  Detailed pet profile view.

• owner_manager.py  
  Owner CRUD operations.

--------------------------------------------------
6. DATABASE LAYER
--------------------------------------------------
Handles all database connectivity and schema management.

• db_connection.py  
  Centralized SQL Server connection handler.

• database_initializer.py  
  Creates initial tables and seeds data.

• database_migrations.py  
  Schema updates and versioning.

All managers use parameterized SQL and company_id isolation.

--------------------------------------------------
7. UTILITIES LAYER
--------------------------------------------------
Shared tools used across modules.

• validators.py  
  Input validation helpers.

• formatters.py  
  Date, currency, and text formatting.

• file_manager.py  
  Directory creation, file handling.

• pdf_generator.py  
  PDF creation with text blocks and images.

• image_processor.py  
  Image resizing and optimization.

• export_import.py  
  CSV/JSON import/export utilities.

• logger.py  
  Application logging.

--------------------------------------------------
8. ASSETS
--------------------------------------------------
Static resources used by the UI.

• /assets/icons/*  
• /assets/images/*  
• /assets/templates/*

--------------------------------------------------
9. UI FLOW
--------------------------------------------------
Dashboard →  
    Pets  
    Owners  
    Reservations  
        • Create Reservation  
        • Modify Reservation  
    Check‑In  
    Check‑Out  
    Kennel Assignments  
    Daily Logs  
        • Feeding  
        • Medication  
        • Playtime  
        • Notes  
    Incident Reports  
    Billing & Invoices  
    Reports  
    Staff Management (Global Admin only)  
    Settings (Global Admin only)

--------------------------------------------------
10. ARCHITECTURAL PRINCIPLES
--------------------------------------------------

• Separation of Concerns  
  UI → Manager → Engine → DB

• No SQL in UI  
  All database operations live in manager modules.

• Centralized RBAC  
  All feature access controlled by centralized_rbac.py.

• Company Isolation  
  Every query includes company_id from session_context.

• Modular UI  
  Each feature is a standalone Tkinter Frame.

• PDF‑First Reporting  
  All reports exportable via pdf_generator.py.

• Analytics Support  
  Matplotlib charts integrated into UI and PDFs.

--------------------------------------------------
11. EXTENSIBILITY
--------------------------------------------------
The system supports:

• Adding new modules without modifying core files  
• Custom pricing models  
• Additional staff roles  
• New report types  
• External API integrations (future)

--------------------------------------------------
12. SUPPORT
--------------------------------------------------
automatinginnovatingai@outlook.com

Thank you for using the Pet Daycare Manager!
