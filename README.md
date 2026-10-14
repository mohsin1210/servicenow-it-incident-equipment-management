# ServiceNow IT Incident & Equipment Inventory Management

ServiceNow Administrator Portfolio Project

Developed by: Mohsin R

## Project Overview

This project demonstrates the configuration and administration of a custom IT incident management and equipment inventory solution in ServiceNow.

The application was developed in a ServiceNow Personal Developer Instance (PDI) using a fictional manufacturing environment, Apex Manufacturing, as the business scenario.

The objective was to build an incident tracking process, automate assignment based on incident categories, maintain equipment inventory records, and provide reporting for IT support activities.

The project uses custom tables rather than modifying the out-of-box Incident table.

## Business Requirements

The application was designed to address the following requirements:

- Provide a centralized location for recording internal IT incidents.
- Classify incidents into Hardware, Software, and Network categories.
- Automatically route new incidents to the appropriate support group.
- Maintain a separate inventory of IT equipment.
- Support bulk equipment data uploads using CSV files.
- Provide reports and dashboards for operational visibility.
- Configure forms, fields, and policies to support consistent data entry.

## 1. Application Configuration

Created custom tables for incident management and equipment inventory.

TD IT Incident

Configured the incident form with fields including:

- Caller
- Category and Subcategory
- Impact and Urgency
- Assignment Group
- Assigned To
- State

Configured form layouts, choice values, and UI Policies to support data entry and incident management.

TD Equipment Inventory

Created the custom table `u_td_equipment_inventory` to store equipment records.

Configured fields including:

- Asset Tag
- Equipment Type
- Manufacturer and Model
- Serial Number
- Status
- Assigned To
- Location
- Purchase Date
- Warranty Expiry
- Cost

## 2. Incident Assignment Automation

Created and activated a Flow Designer flow named TD IT Incident Assignment.

The flow executes when a new TD IT Incident record is created.

Based on the selected incident category, the flow evaluates conditions and updates the incident's Assignment Group.

| Incident Category | Assignment Group |
|---|---|
| Hardware | Hardware Support |
| Software | Software Support |
| Network | Network Support |

The flow was tested using new incident records to verify category-based assignment.

This configuration demonstrates record-triggered automation, conditional flow logic, and record updates.

## 3. Equipment Inventory Data Import

Configured the Import Set and Transform Map functionality to load equipment inventory records from a CSV file.

Implementation:

1. Prepared equipment records in CSV format.
2. Uploaded the file using ServiceNow's data import functionality.
3. Created the staging table `u_td_equipment_inventory_import`.
4. Configured the TD Equipment Inventory Transform map.
5. Mapped source fields to the target Equipment Inventory table.
6. Executed the transformation.
7. Reviewed the imported equipment records in the target table.

This exercise demonstrates practical experience with data sources, import sets, field mapping, and data transformation.

## 4. Reporting and Dashboard

Created a dashboard named TD IT & Equipment Dashboard.

Configured reporting to provide visibility into equipment and IT support information.

This component demonstrates ServiceNow's reporting and dashboard configuration capabilities.

## 5. Additional Administration

The project also involved working with several core ServiceNow administration features:

- Custom table and field configuration
- Form and list layouts
- Choice lists and dependent fields
- UI Policies
- User groups and assignment configuration
- Flow Designer
- Import Sets and Transform Maps
- Reports and Dashboards
- Knowledge Management
- Notifications

## 6. Testing and Validation

Performed functional testing throughout development.

| Test Scenario | Validation |
|---|---|
| Create TD IT Incident | Record creation and field configuration |
| Select incident category | Category and subcategory behavior |
| Create Hardware incident | Hardware assignment routing |
| Create Software incident | Software assignment routing |
| Create Network incident | Network assignment routing |
| Import equipment CSV | Import set and transformation execution |
| View equipment records | Imported records visible in target table |
| Open dashboard | Dashboard and report configuration |

## 7. Project Documentation

Detailed implementation screenshots and configuration evidence are provided in the project documentation.

The documentation covers the application setup, custom tables, incident assignment flow, equipment import process, and reporting configuration.

## 8. Skills Demonstrated

ServiceNow Administration: Custom tables, forms, lists, fields, UI Policies, groups, and application configuration.

Workflow Automation: Flow Designer triggers, conditional logic, and record updates.

Data Management: CSV imports, Import Sets, Transform Maps, and field mapping.

Reporting: ServiceNow reports and dashboards.

Testing: Functional testing and validation of application configurations.

## Project Environment

- Platform: ServiceNow
- Environment: Personal Developer Instance (PDI)
- Project Type: ServiceNow Administration
- Business Scenario: Apex Manufacturing (fictional)
- Development Approach: Custom application configuration

---

Author: Mohsin R

This is an independent portfolio project developed for hands-on ServiceNow administration practice. It is not a production deployment or an official ServiceNow implementation.
