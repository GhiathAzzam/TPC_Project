# Manufacturing Management System - Use Case Diagram Documentation

## Overview
This use case diagram represents a comprehensive manufacturing management system built with Laravel. The system manages the complete manufacturing workflow from raw materials to finished products, including financial tracking and reporting.

## System Actors

### 1. Admin
- **Role**: System administrator with full access
- **Responsibilities**: Complete system oversight, user management, and all operational functions
- **Access Level**: Full access to all system features

### 2. Accountant
- **Role**: Financial operations manager
- **Responsibilities**: Managing expenses, sales, production settings, and financial reporting
- **Access Level**: Limited to financial operations and reporting

### 3. Warehouse Keeper
- **Role**: Inventory and production manager
- **Responsibilities**: Managing raw materials, products, batches, and production processes
- **Access Level**: Limited to inventory and production operations

### 4. System
- **Role**: Automated system processes
- **Responsibilities**: Activity logging, notifications, and automated report generation

## Use Case Packages

### 1. User Management (Admin Only)
- **UC1: Register Users** - Create new user accounts with appropriate roles
- **UC2: Manage User Accounts** - Edit user information and permissions
- **UC3: Change User Activation** - Enable/disable user accounts
- **UC4: View Activity Logs** - Monitor all user activities and system changes

### 2. Authentication (All Users)
- **UC5: Login** - Authenticate users into the system
- **UC6: Logout** - End user session securely
- **UC7: Update Profile** - Allow users to modify their personal information

### 3. Material Management (Warehouse Keeper + Admin)
- **UC8: Manage Raw Materials** - Add, edit, delete raw materials
- **UC9: Manage Raw Material Batches** - Track material batches with quantities and dates
- **UC10: Track Damaged Materials** - Record and manage damaged/waste materials
- **UC11: Search Materials** - Find materials by name, category, or other criteria

### 4. Product Management (Warehouse Keeper + Admin)
- **UC12: Manage Products** - Add, edit, delete product definitions
- **UC13: Manage Product Batches** - Track production batches and inventory
- **UC14: Define Product Materials (BOM)** - Set up Bill of Materials for products
- **UC15: Convert Materials to Products** - Process raw materials into finished products
- **UC16: Update Product Prices** - Adjust product pricing based on costs

### 5. Financial Management (Accountant + Admin)
- **UC17: Manage Expenses** - Record and track business expenses
- **UC18: Manage Expense Categories** - Organize expenses by category
- **UC19: Record Product Sales** - Track product sales and revenue
- **UC20: Manage Production Settings** - Configure production parameters and costs

### 6. Reporting (All Users - View, Accountant/Admin - Generate)
- **UC21: Generate Profit/Loss Reports** - Calculate and display profit/loss analysis
- **UC22: Generate Product Summary Reports** - Create detailed product performance reports
- **UC23: View Monthly Sales** - Display sales data organized by month
- **UC24: Refresh Reports** - Update existing reports with current data

### 7. Notifications (All Users)
- **UC25: View Notifications** - Display system notifications to users
- **UC26: Mark Notifications as Read** - Update notification status

### 8. System Operations (Automated)
- **UC27: Log Activities** - Automatically record all user actions
- **UC28: Send Notifications** - Generate and deliver system notifications
- **UC29: Generate Reports** - Automated report generation and calculations

## Key Relationships

### Include Relationships
- Search functionality is included in material and product management
- Sales recording automatically triggers profit/loss and product summary report generation
- All major operations include activity logging
- Report generation is included in profit/loss and product summary reports

### Extend Relationships
- Report refreshing extends product summary reports
- Marking notifications as read extends viewing notifications
- Updating product prices extends product management

## Role-Based Access Control

### Admin Access
- Full system access including all user management functions
- Can perform all warehouse keeper and accountant functions
- Exclusive access to user management and activity logs

### Accountant Access
- Financial operations: expenses, sales, production settings
- Reporting: profit/loss, product summaries, monthly sales
- Basic profile management and notifications

### Warehouse Keeper Access
- Inventory management: raw materials, products, batches
- Production operations: material conversion, BOM definition
- Basic profile management and notifications

## System Features

### Security Features
- Role-based access control with middleware protection
- Activity logging for audit trails
- User activation/deactivation controls

### Business Logic
- Automated profit/loss calculations based on sales and expenses
- Material conversion tracking from raw materials to finished products
- Batch tracking for inventory management
- Damage tracking for waste management

### Reporting Features
- Monthly sales analysis
- Product performance summaries
- Profit/loss statements
- Real-time report refresh capabilities

## Technical Implementation Notes

### Authentication
- Uses Laravel Sanctum for API authentication
- Middleware-based role protection
- User activation status checking

### Database Structure
- Separate models for raw materials, products, batches, sales, expenses
- Relationship mapping between products and materials (BOM)
- Activity logging with polymorphic relationships

### API Design
- RESTful API endpoints with proper HTTP methods
- Search functionality across multiple entities
- Batch operations for efficiency

## Usage Scenarios

### Daily Operations
1. Warehouse keeper logs in and checks raw material inventory
2. Records new material batches received
3. Processes materials into products using defined BOMs
4. Tracks any damaged materials during production

### Financial Operations
1. Accountant records daily expenses by category
2. Logs product sales as they occur
3. Generates weekly/monthly profit/loss reports
4. Updates production settings based on cost analysis

### Administrative Tasks
1. Admin monitors system through activity logs
2. Manages user accounts and permissions
3. Oversees overall system health and performance
4. Handles user support and system maintenance

This use case diagram provides a comprehensive view of the manufacturing management system, showing how different user roles interact with various system functions to manage the complete manufacturing workflow from raw materials to sales and reporting.