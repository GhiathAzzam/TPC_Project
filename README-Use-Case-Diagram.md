# Use Case Diagram for Manufacturing Management System

## Generated Files

This directory contains the following files related to the use case diagram:

1. **`use-case-diagram.puml`** - PlantUML source file for the use case diagram
2. **`Manufacturing Management System - Use Case Diagram.png`** - Generated PNG image of the use case diagram
3. **`use-case-diagram-documentation.md`** - Comprehensive documentation explaining the diagram

## How to Use

### Viewing the Diagram
The generated PNG image (`Manufacturing Management System - Use Case Diagram.png`) can be viewed in any image viewer or web browser.

### Modifying the Diagram
If you need to modify the diagram:

1. Edit the `use-case-diagram.puml` file
2. Regenerate the diagram using:
   ```bash
   java -jar plantuml.jar use-case-diagram.puml
   ```

### Understanding the Diagram
Please refer to `use-case-diagram-documentation.md` for a detailed explanation of:
- System actors and their roles
- Use case descriptions
- Access control permissions
- System relationships and workflows

## System Overview

This use case diagram represents a comprehensive **Manufacturing Management System** with the following key features:

### Main User Roles
- **Admin**: Full system access and user management
- **Accountant**: Financial operations and reporting
- **Warehouse Keeper**: Inventory and production management

### Core Functionality
- **User Management**: User registration, account management, activity tracking
- **Authentication**: Secure login/logout system
- **Material Management**: Raw material tracking, batch management, damage tracking
- **Product Management**: Product definition, batch tracking, BOM (Bill of Materials)
- **Financial Management**: Expense tracking, sales recording, production settings
- **Reporting**: Profit/loss analysis, product summaries, monthly reports
- **Notifications**: System notifications and alerts

### Key Features
- Role-based access control (RBAC)
- Comprehensive audit trail through activity logging
- Automated report generation
- Real-time inventory tracking
- Production cost analysis
- Waste/damage tracking

## Technical Details

### Built With
- **Backend**: Laravel PHP Framework
- **Authentication**: Laravel Sanctum (API tokens)
- **Database**: MySQL/PostgreSQL (Laravel Eloquent ORM)
- **API**: RESTful API design

### Architecture
- **MVC Pattern**: Model-View-Controller architecture
- **Middleware**: Role-based access control
- **API-First**: Designed for mobile and web clients
- **Scalable**: Modular design for easy extension

## Next Steps

After reviewing the use case diagram, you might want to:

1. **System Design**: Create sequence diagrams for key workflows
2. **Database Design**: Design entity relationship diagrams
3. **API Documentation**: Document all API endpoints
4. **User Interface**: Design mockups for different user roles
5. **Testing Strategy**: Plan test cases based on use cases

## Dependencies

To regenerate the diagram, you need:
- Java Runtime Environment (JRE) 8+
- PlantUML JAR file (download from https://plantuml.com/download)
- Graphviz (for diagram rendering)

### Installing Dependencies (Ubuntu/Debian)
```bash
sudo apt update
sudo apt install -y graphviz default-jre
```

### Installing Dependencies (macOS)
```bash
brew install graphviz
brew install openjdk
```

### Installing Dependencies (Windows)
1. Install Java JRE from Oracle or OpenJDK
2. Install Graphviz from https://graphviz.org/download/
3. Add both to your system PATH

## Contact & Support

For questions about the system design or modifications to the diagram, please refer to the project documentation or contact the development team.

---

*This use case diagram was generated automatically by analyzing the Laravel project structure and API endpoints.*