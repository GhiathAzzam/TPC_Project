# Manufacturing Management System - Use Case Diagram Documentation

## Overview
This use case diagram represents a comprehensive manufacturing management system built with Laravel. The system manages the complete manufacturing workflow from raw materials to finished products, including financial tracking and reporting.

**✨ Visual Improvements:**
- **Color-coded packages** for easy identification of functional areas
- **Logical grouping** of related use cases into themed packages
- **Emoji icons** for quick visual reference
- **Optimized layout** with directional arrows for better flow
- **Enhanced styling** with rounded corners and improved spacing

## System Actors

### 1. Admin 👑 (Light Orange)
- **Role**: System administrator with full access
- **Responsibilities**: Complete system oversight, user management, and all operational functions
- **Access Level**: Full access to all system features
- **Visual Position**: Top-left with connections to all packages

### 2. Accountant 💼 (Light Green)
- **Role**: Financial operations manager
- **Responsibilities**: Managing expenses, sales, production settings, and financial reporting
- **Access Level**: Limited to financial operations and reporting
- **Visual Position**: Bottom-left with focus on financial packages

### 3. Warehouse Keeper 📦 (Light Pink)
- **Role**: Inventory and production manager
- **Responsibilities**: Managing raw materials, products, batches, and production processes
- **Access Level**: Limited to inventory and production operations
- **Visual Position**: Bottom-right with focus on inventory/production packages

### 4. System ⚙️ (Light Purple)
- **Role**: Automated system processes
- **Responsibilities**: Activity logging, notifications, and automated report generation
- **Visual Position**: Right side connected to system operations

## Use Case Packages (Color-Coded)

### 1. 👤 User & Authentication (Light Blue)
- **UC1: Register Users** - Create new user accounts with appropriate roles
- **UC5: Login/Logout** - Authenticate users into the system
- **UC7: Update Profile** - Allow users to modify their personal information
- **UC2: Manage User Accounts** - Edit user information and permissions
- **UC3: Change User Activation** - Enable/disable user accounts
- **UC4: View Activity Logs** - Monitor all user activities and system changes (Admin only)

### 2. 📦 Inventory Management (Light Green)
- **UC8: Manage Raw Materials** - Add, edit, delete raw materials
- **UC9: Manage Raw Material Batches** - Track material batches with quantities and dates
- **UC11: Search Materials** - Find materials by name, category, or other criteria
- **UC10: Track Damaged Materials** - Record and manage damaged/waste materials

### 3. 🏭 Production Management (Light Orange)
- **UC12: Manage Products** - Add, edit, delete product definitions
- **UC13: Manage Product Batches** - Track production batches and inventory
- **UC14: Define Product Materials (BOM)** - Set up Bill of Materials for products
- **UC15: Convert Materials to Products** - Process raw materials into finished products
- **UC16: Update Product Prices** - Adjust product pricing based on costs

### 4. 💰 Financial Operations (Light Pink)
- **UC17: Manage Expenses** - Record and track business expenses
- **UC18: Manage Expense Categories** - Organize expenses by category
- **UC19: Record Product Sales** - Track product sales and revenue
- **UC20: Manage Production Settings** - Configure production parameters and costs

### 5. 📊 Reporting & Analytics (Light Purple)
- **UC21: Generate Profit/Loss Reports** - Calculate and display profit/loss analysis
- **UC22: Generate Product Summary Reports** - Create detailed product performance reports
- **UC23: View Monthly Sales** - Display sales data organized by month
- **UC24: Refresh Reports** - Update existing reports with current data

### 6. 🔔 Notifications (Light Gray)
- **UC25: View Notifications** - Display system notifications to users
- **UC26: Mark Notifications as Read** - Update notification status

### 7. ⚙️ System Operations (Light Gray)
- **UC27: Log Activities** - Automatically record all user actions
- **UC28: Send Notifications** - Generate and deliver system notifications
- **UC29: Generate Reports** - Automated report generation and calculations

## Visual Layout Improvements

### Enhanced Organization
- **Logical Flow**: Packages are arranged in a logical workflow from user management to system operations
- **Color Coding**: Each package has a distinct color theme for easy identification
- **Directional Arrows**: Clear directional indicators showing the flow between actors and use cases
- **Grouped Functionality**: Related use cases are grouped together for better understanding

### Improved Readability
- **Emoji Icons**: Each package has a relevant emoji for quick visual identification
- **Actor Colors**: Different colored actors to distinguish roles clearly
- **Rounded Corners**: Softer visual appearance with rounded corner styling
- **Better Spacing**: Optimized spacing between elements for cleaner presentation

### Connection Clarity
- **Directional Relationships**: Arrows show clear directional flow (up, down, right)
- **Relationship Types**: Different line styles for include, extend, and trigger relationships
- **Visual Hierarchy**: Important relationships are emphasized through positioning

## Key Relationships

### Include Relationships
- **Material/Product Search**: Both inventory and production management include search functionality
- **Sales Integration**: Product sales automatically trigger profit/loss and product summary reports
- **Activity Logging**: All major operations include automatic activity logging
- **Report Generation**: Automated report generation is included in financial reporting

### Extend Relationships
- **Report Refresh**: Extending product summary reports with refresh capability
- **Notification Management**: Extending notification viewing with read functionality
- **Price Updates**: Extending product management with price update capability

### Trigger Relationships
- **Activity → Notification**: Activity logging triggers notification generation

## Role-Based Access Control

### Admin Access (Full System)
- **Complete Control**: Access to all packages and use cases
- **User Management**: Exclusive access to user administration functions
- **System Monitoring**: Unique access to activity logs and system oversight

### Accountant Access (Financial Focus)
- **Financial Operations**: Full access to expense and sales management
- **Reporting**: Complete reporting and analytics capabilities
- **Limited System Access**: Basic authentication and notification functions

### Warehouse Keeper Access (Operations Focus)
- **Inventory Control**: Full access to raw material and inventory management
- **Production Management**: Complete production and BOM management
- **Limited System Access**: Basic authentication and notification functions

## System Features

### Security Features
- **Role-Based Access Control**: Middleware-enforced permissions by user role
- **Activity Logging**: Comprehensive audit trail for all system actions
- **User Activation Control**: Admin ability to enable/disable user accounts

### Business Logic
- **Automated Calculations**: Real-time profit/loss calculations based on sales and expenses
- **Material Conversion Tracking**: Complete workflow from raw materials to finished products
- **Batch Management**: Detailed tracking of material and product batches
- **Damage Control**: Systematic tracking of waste and damaged materials

### Reporting Features
- **Monthly Analytics**: Comprehensive monthly sales and production analysis
- **Performance Summaries**: Detailed product performance reports
- **Financial Statements**: Automated profit/loss statement generation
- **Real-time Updates**: Live report refresh capabilities

## Technical Implementation Notes

### Authentication & Security
- **Laravel Sanctum**: Token-based API authentication
- **Middleware Protection**: Role-based route protection
- **Status Validation**: User activation status checking

### Database Architecture
- **Eloquent ORM**: Laravel's object-relational mapping
- **Relationship Modeling**: Complex relationships between entities
- **Polymorphic Logging**: Flexible activity logging system

### API Design
- **RESTful Architecture**: Standard HTTP methods and status codes
- **Search Capabilities**: Full-text search across multiple entities
- **Batch Operations**: Efficient bulk operations for performance

## Usage Scenarios

### Daily Operations Workflow
1. **Morning Check**: Warehouse keeper reviews inventory levels and pending orders
2. **Material Receipt**: Log new raw material batches and update inventory
3. **Production Planning**: Review BOMs and plan material conversion
4. **Quality Control**: Track any damaged materials during production
5. **Sales Recording**: Accountant logs daily sales and updates financial records

### Financial Management Workflow
1. **Expense Tracking**: Daily logging of operational expenses by category
2. **Sales Analysis**: Regular review of sales performance and trends
3. **Report Generation**: Weekly/monthly profit/loss analysis
4. **Cost Optimization**: Adjust production settings based on financial performance

### Administrative Workflow
1. **User Management**: Monitor user activities and manage accounts
2. **System Monitoring**: Review activity logs for security and performance
3. **Access Control**: Adjust user permissions and activation status
4. **System Maintenance**: Oversee overall system health and performance

## Visual Benefits

### Improved User Experience
- **Quick Recognition**: Color coding and icons enable faster navigation
- **Logical Flow**: Natural workflow representation from left to right
- **Clear Hierarchy**: Visual emphasis on important relationships and processes

### Better Communication
- **Stakeholder Clarity**: Easier for non-technical stakeholders to understand
- **Development Guide**: Clear visual guide for development teams
- **Training Material**: Effective tool for user training and onboarding

This optimized use case diagram provides a comprehensive yet visually clear representation of the manufacturing management system, making it easier for stakeholders to understand the system's capabilities and user interactions.