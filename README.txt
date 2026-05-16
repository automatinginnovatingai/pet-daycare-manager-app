PET DAYCARE MANAGER – README
============================

Overview
--------
The Pet Daycare Manager is a complete, modern, and secure management system designed for
boarding and daycare facilities. It centralizes daily operations including pets, owners,
reservations, check‑ins, check‑outs, kennels, daily logs, feeding, medication, playtime,
incident reports, billing, vaccinations, reminders, staff management, and reporting.

The system is built for speed, clarity, and reliability, with a modular architecture that
supports clean UI separation, centralized RBAC, and scalable SQL Server database design.

Key Features
------------
• Pet & Owner Management  
  Maintain detailed pet profiles, medical notes, feeding instructions, and owner information.

• Reservations  
  Create, modify, and cancel daycare and boarding reservations with capacity safeguards.

• Check‑In / Check‑Out  
  Streamlined workflows for intake and release, including billing integration.

• Kennel Assignments  
  Assign pets to kennels, track occupancy, and prevent overbooking.

• Daily Logs  
  Record feeding, medication, playtime, enrichment, and behavior notes.

• Incident Reports  
  Log behavioral or medical incidents with full detail for internal records or client reports.

• Billing & Invoicing  
  Track charges, generate invoices, apply packages/credits, and manage payments.

• Vaccination Tracking  
  Log vaccinations, calculate next due dates, generate alerts, and produce health reports.

• Reminders & Notifications  
  Automated alerts for vaccinations, tasks, and due items.

• Reporting & Analytics  
  Generate PDF reports and view charts for operations, billing, and vaccinations.

• Staff Management  
  Add, edit, archive staff; enforce roles, permissions, and subscription limits.

• Role‑Based Access Control (RBAC)  
  Global Admin, Staff, and Kennel Tech roles with feature‑level permissions.

• Subscription Plan Enforcement  
  Basic, Pro, and Enterprise plans with automatic feature gating.

System Requirements
-------------------
• Windows 10 or later  
• 4–8 GB RAM  
• SQL Server Express or SQL Server Standard/Enterprise  
• Python 3.10+ (development mode only)  
• PDF viewer installed  
• Required Python packages listed in requirements.txt

Installation
------------
1. Install Python 3.10 or later (development mode only).  
2. Install dependencies:  
   pip install -r requirements.txt  
3. Run the database setup:  
   python run_database_setup.py  
4. Launch the application:  
   python main.py  

(End‑users installing the packaged `.exe` do not need Python.)

Directory Structure
-------------------
core/
    main.py
    app_controller.py
    router.py

ui_framework/
    ui_main_window.py
    ui_navigation.py
    ui_settings.py

user_management/
    staff_manager_ui.py
    add_staff_ui.py
    staff_ui.py
    session_context.py
    centralized_rbac.py

modules/
    pets_ui.py
    owners_ui.py
    reservation_manager.py
    checkin_manager.py
    checkout_manager.py
    kennel_manager.py
    daily_logs_manager.py
    feeding_manager.py
    medication_manager.py
    playtime_manager.py
    incident_report_manager.py
    billing_manager.py
    rate_plan_manager.py
    capacity_manager.py
    vaccinations_ui.py
    vaccination_alerts_ui.py
    vaccination_forecast_ui.py
    vaccination_schedule_engine.py
    vaccinations_manager.py
    reminders_ui.py
    reports_ui.py
    marketing_kit_ui.py (optional)

database/
    db_connection.py
    database_initializer.py
    database_migrations.py

tools/
    validators.py
    formatters.py
    file_manager.py
    pdf_generator.py
    image_processor.py
    export_import.py
    logger.py

assets/
    icons/
    images/
    templates/

docs/
    README.txt
    CHANGELOG.txt
    LICENSE.txt

build/
    requirements.txt
    build_config.json
    photo.ico

User Roles
----------
1. Global Admin  
   Full access to all modules and settings.

2. Staff  
   Operational access: pets, owners, reservations, check‑in/out, logs, billing.

3. Kennel Tech  
   Limited access: daily logs, feeding, medication, playtime, notes.

Navigation
----------
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

Support
-------
automatinginnovatingai@outlook.com

Thank you for using the Pet Daycare Manager!
