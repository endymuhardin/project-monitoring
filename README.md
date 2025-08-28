# Student Project Monitoring System

## Overview
A comprehensive web-based application for monitoring student software development projects in an integrated academic environment. This system supports the Integrated Project-Based Learning (PjBL) methodology, combining Project Management, Systems Analysis & Design, and Web Application Development into a single semester-long experience.

## System Requirements

### Academic Context
- **Target Institution**: STMIK Tazkia Information Systems Program
- **Learning Model**: Integrated Project-Based Learning (Hybrid Agile-Waterfall)
- **Duration**: One semester (16 weeks)
- **Team Structure**: Student teams of 3-5 members
- **Instructor Role**: Facilitator and mentor, not traditional lecturer

### Core Objectives
1. **Real-time Project Monitoring**: Track student progress across all project phases
2. **Deliverable Management**: Collect, review, and grade project submissions
3. **Collaborative Learning Support**: Facilitate team collaboration and communication
4. **Assessment Automation**: Implement comprehensive rubric-based grading
5. **Industry Alignment**: Mirror real-world software development practices

## Feature Specifications

### 1. User Management & Authentication

#### 1.1 User Roles
- **Students**: Team members working on projects
- **Instructors**: Faculty monitoring and grading projects
- **Administrators**: System managers with full access

#### 1.2 Authentication Features
- Secure login/logout system
- Role-based access control (RBAC)
- Password reset functionality
- Session management
- Multi-factor authentication (optional)

#### 1.3 Profile Management
- User profile creation and editing
- Academic information tracking
- Contact details management
- Avatar/photo upload

#### 1.4 Student Registration System - Google Workspace Integration

**Google for Education Single Sign-On (SSO):**
- **Mandatory Google Workspace Authentication**: All students must use their @stmik.tazkia.ac.id Google account
- **Active Session Requirement**: Registration only available with active Google sign-on session
- **OAuth 2.0 Integration**: Secure authentication using Google OAuth 2.0 with Spring Security
- **Domain Restriction**: Only @stmik.tazkia.ac.id domain accounts are permitted
- **Automatic Profile Population**: Student information pulled from Google Workspace directory

**Registration Security Features:**
- **Domain Validation**: Automatic verification of stmik.tazkia.ac.id email domain
- **Session Management**: Active Google session monitoring and timeout handling
- **Multi-factor Authentication**: Leverages Google's 2FA if enabled on student accounts
- **Account Linking Prevention**: One Google account per student, no duplicate registrations
- **Audit Trail**: Complete logging of authentication and registration activities

### 2. Group Registration & Formation System

#### 2.1 Google-Authenticated Group Registration Process

**Google SSO Pre-Registration Phase:**
- **Google Authentication Required**: Students must sign in using @stmik.tazkia.ac.id credentials
- **Automatic Profile Import**: Google Workspace profile data automatically imported (name, email, photo)
- **Course Enrollment Verification**: Integration with Google Classroom or manual course assignment
- **Academic Information Validation**: Student ID and program verification against institutional records

**Google-Integrated Group Formation Workflow:**
- **Authenticated Group Creation**: Only Google-authenticated students can create groups
- **Google Contacts Integration**: Group discovery using Google Workspace directory
- **Email-Based Invitations**: Native integration with Gmail for group invitations
- **Google Calendar Integration**: Automatic team meeting scheduling capabilities
- **Google Drive Workspace**: Automatic creation of shared Google Drive folder for each group

**Enhanced Group Registration Requirements:**
- **Google Account Verification**: All group members must have verified @stmik.tazkia.ac.id accounts
- **Team Size Validation**: Enforce 2-3 member limit with Google account verification
- **Course Section Matching**: Automatic verification through Google Classroom integration
- **Google Workspace Collaboration**: Shared Google Drive, Calendar, and Meet access
- **Unified Communication**: Integration with Google Chat for team coordination

#### 2.2 Group Management Features
- **Member Role Assignment**: Designation of group leader and specialized roles
- **Group Modification Window**: Time-limited period for membership changes
- **Conflict Resolution**: Built-in tools for handling group formation disputes
- **Instructor Oversight**: Faculty approval workflow for group registrations
- **Emergency Dissolution**: Administrative tools for handling group breakdown

#### 2.3 Registration Analytics
- **Formation Progress Tracking**: Monitor group formation completion rates
- **Skill Balance Analysis**: Automatic assessment of team skill diversity
- **Registration Timeline**: Visual progress tracking for course enrollment
- **Notification System**: Automated reminders for registration deadlines
- **Wait List Management**: Queue system for students without groups

### 3. Project Assessment & Monitoring Module

#### 3.1 Project Assignment & Setup
- **Course Project Assignment**: Automatic assignment of course projects to registered groups
- **Project Brief Distribution**: Standardized project requirements and specifications
- **Group-Project Mapping**: Linking registered groups to assigned projects
- **Project Categories**: Classification by complexity, domain, or learning objectives
- **Initial Documentation Requirements**: Baseline documentation templates and requirements

#### 3.2 Progress Monitoring
- **Phase-Based Tracking**: Monitor student progress through 5 defined project phases
- **Milestone Verification**: Validation of phase completion and deliverable submission
- **Progress Dashboard**: Visual representation of each group's advancement
- **Timeline Adherence**: Tracking adherence to academic calendar deadlines

#### 3.3 Academic Calendar Integration
- **Semester Schedule Sync**: Integration with institutional academic calendar
- **Deadline Management**: Automated tracking of submission deadlines
- **Phase Transition Alerts**: Notifications for phase progression deadlines
- **Holiday and Break Considerations**: Adjustment for non-working academic periods

### 4. Phase-Based Project Tracking

#### 4.1 Phase 1: Initiation & Planning (Weeks 1-4)
**Deliverables Management:**
- Project Charter upload and review
- Business case documentation
- Work Breakdown Structure validation
- Project plan approval workflow

**Monitoring Features:**
- Bi-weekly progress check-ins
- Instructor feedback system
- Peer review mechanisms
- Risk assessment tools

#### 3.2 Phase 2: Systems Analysis & Design (Weeks 5-8)
**Deliverables Management:**
- Requirements documentation (functional/non-functional)
- Use Case Diagram creation and validation
- Data Flow Diagram (DFD) or UML model submission
- Entity Relationship Diagram (ERD) verification
- UI/UX mockup review system

**Analysis Tools:**
- Requirement traceability matrix
- Design consistency checker
- Model validation tools
- Stakeholder feedback collection

#### 3.3 Phase 3: Development & Implementation (Weeks 9-12)
**Code Management Integration:**
- Git repository connection (GitHub/GitLab)
- Automated code quality analysis
- Commit history tracking
- Branch management monitoring
- Pull request workflow integration

**Development Monitoring:**
- Source code metrics dashboard
- Code review assignment and tracking
- Testing progress monitoring
- Documentation completeness checks

#### 3.4 Phase 4: Testing & Validation (Weeks 13-14)
**Testing Management:**
- Test case documentation system
- Test execution tracking
- Bug reporting and tracking
- Compatibility testing results
- Performance metrics collection

**Quality Assurance:**
- Automated testing integration
- Code coverage analysis
- Security vulnerability scanning
- Performance benchmarking

#### 3.5 Phase 5: Project Closure (Weeks 15-16)
**Final Deliverables:**
- Comprehensive project report generation
- Presentation scheduling system
- Application demonstration platform
- Project retrospective tools
- Knowledge transfer documentation

### 4. Git Repository Integration

#### 4.1 Version Control Monitoring
- **Repository Setup Guidance**: Step-by-step repository creation tutorials
- **Branch Strategy Enforcement**: Automated branch policy validation
- **Commit Quality Assessment**: Commit message analysis and scoring
- **Collaboration Metrics**: Team collaboration effectiveness measurement

#### 4.2 Code Quality Management
- **Folder Structure Validation**: Automated project structure compliance checking
- **Documentation Standards**: README.md quality assessment
- **Code Review Integration**: Automated assignment of code reviewers
- **Merge Request Workflow**: Structured merge request approval process

#### 4.3 Repository Analytics
- **Contribution Analysis**: Individual and team contribution metrics
- **Activity Timeline**: Visual representation of development activity
- **File Change Tracking**: Detailed change history analysis
- **Repository Health Score**: Overall repository quality assessment

### 5. Comprehensive Submission & Grading System

#### 5.1 Multi-Course Grading Architecture
**Individual Course Assessment (Each 100%):**
- **Project Management Course**: Separate grading track with dedicated rubrics
- **Systems Analysis & Design Course**: Independent assessment framework  
- **Web Development Course**: Standalone evaluation criteria
- **Integrated Learning Outcomes**: Cross-course competency validation

#### 5.2 CMMI Dev 3.0 Integrated Assessment Framework

**CMMI Dev 3.0 Compliance Overview:**
The assessment framework incorporates CMMI Dev 3.0 process areas across the four Category Areas:
- **Doing**: Production and delivery of high-quality solutions
- **Managing**: Planning and workforce management capabilities  
- **Enabling**: Analysis, decision-making, and stakeholder communication
- **Improving**: Process development and organizational performance enhancement

**Project Management Assessment (100% Total) - CMMI Dev 3.0 Aligned:**

- **CMMI Managing Category - Project Planning & Control (45%)**:
  - **Project Charter & Business Case (15%)**:
    - CMMI Project Planning practices: Stakeholder identification and engagement
    - Work breakdown structure aligned with CMMI estimation practices
    - Risk identification and mitigation strategy documentation
    
  - **Work Planning & Scheduling (20%)**:
    - CMMI-compliant project plan with defined processes and procedures
    - Resource allocation and capacity planning following CMMI practices
    - Schedule management with milestone tracking and progress measurement
    
  - **Project Monitoring & Control (10%)**:
    - CMMI Measurement and Analysis practices implementation
    - Progress tracking against planned objectives and commitments
    - Corrective action planning and execution documentation

- **CMMI Enabling Category - Process & Quality Management (35%)**:
  - **Requirements Management Implementation (15%)**:
    - CMMI Requirements Management (RDM) practice area compliance
    - Requirements traceability and change management documentation
    - Stakeholder requirements validation and verification processes
    
  - **Configuration Management (10%)**:
    - Version control strategy and implementation using Git
    - Change control processes and audit trails
    - Baseline establishment and maintenance practices
    
  - **Final Project Documentation (10%)**:
    - Comprehensive project report covering full CMMI lifecycle
    - Process performance analysis and improvement recommendations
    - Lessons learned and organizational knowledge transfer

- **CMMI Improving Category - Organizational Capability (20%)**:
  - **Team Collaboration & Communication (10%)**:
    - CMMI-aligned team formation and role definition
    - Communication management and stakeholder engagement
    - Conflict resolution and team performance optimization
    
  - **Professional Presentation & Knowledge Transfer (10%)**:
    - Process-focused project presentation delivery
    - Demonstration of CMMI practice area understanding
    - Organizational learning and capability improvement recommendations

**Systems Analysis & Design Assessment (100% Total) - CMMI Dev 3.0 Aligned:**

- **CMMI Doing Category - Requirements Development & Analysis (50%)**:
  - **Requirements Elicitation & Documentation (25%)**:
    - CMMI Requirements Development (RD) practice area compliance
    - Stakeholder needs analysis and requirements gathering techniques
    - Business process modeling aligned with CMMI practices
    - Requirements validation and verification methodologies
    
  - **Requirements Management & Traceability (25%)**:
    - CMMI Requirements Management (RDM) implementation
    - Bidirectional requirements traceability matrix
    - Change request management and impact analysis
    - Requirements baseline establishment and maintenance

- **CMMI Doing Category - Technical Solution Development (40%)**:
  - **System Architecture & Design (20%)**:
    - CMMI Technical Solution practice area alignment
    - Entity Relationship Diagram (ERD) design following normalization principles
    - Data Flow Diagram (DFD) or UML modeling with CMMI-compliant documentation
    - System architecture decisions documentation and rationale
    
  - **Interface Design & Integration Planning (20%)**:
    - User Interface (UI/UX) design with usability and accessibility considerations
    - System integration planning and interface specifications
    - CMMI Product Integration practice area elements
    - Design verification and validation planning

- **CMMI Enabling Category - Decision Analysis & Technical Review (10%)**:
  - **Design Defense & Technical Communication (5%)**:
    - CMMI Decision Analysis and Resolution practices
    - Ability to explain and defend technical design decisions
    - Alternative solution analysis and selection criteria documentation
    
  - **Peer Review & Quality Assurance (5%)**:
    - CMMI Verification practice area implementation
    - Technical peer review participation and feedback incorporation
    - Design quality metrics and improvement recommendations

**Web Development Assessment (100% Total):**
- **Source Code Quality (40%)**:
  - Code structure, readability, and maintainability
  - Adherence to coding best practices and standards
  - Technical documentation and inline comments
  
- **Application Functionality & Testing (40%)**:
  - Feature completeness against requirements (25%)
  - System testing documentation and bug reports (15%)
  - Cross-browser compatibility and performance
  
- **Technical Demonstration & Repository Management (20%)**:
  - Live application demonstration and feature walkthrough (10%)
  - Git repository organization and commit quality (10%)

#### 5.3 CMMI Dev 3.0 Maturity Level Assessment
**CMMI Dev 3.0 Six-Level Maturity Framework Integration:**
The system evaluates student projects against CMMI Dev 3.0's expanded maturity levels:

- **Level 0 - Incomplete**: Processes are incomplete, unprepared, or unknown
- **Level 1 - Initial**: Processes are unpredictable and reactive
- **Level 2 - Managed**: Processes are planned, performed, measured, and controlled at project level
- **Level 3 - Defined**: Processes are well characterized and understood across the organization
- **Level 4 - Quantitatively Managed**: Processes are controlled using statistical and quantitative techniques
- **Level 5 - Optimizing**: Processes are continuously improved through innovation and technology adoption

**CMMI Process Area Compliance Tracking:**
- **Managing Category Areas**: Project Planning, Project Monitoring & Control, Requirements Management
- **Doing Category Areas**: Requirements Development, Technical Solution, Product Integration, Verification
- **Enabling Category Areas**: Measurement & Analysis, Decision Analysis & Resolution, Configuration Management
- **Improving Category Areas**: Organizational Process Definition, Organizational Process Focus, Organizational Training

#### 5.4 4-Point Rubric Scale Implementation
**Scoring Criteria (1-4 Scale):**
- **4 - Exemplary**: Exceeds all expectations, demonstrates innovation and deep understanding
- **3 - Proficient**: Meets all requirements with good quality and proper execution  
- **2 - Developing**: Meets most requirements but shows areas needing improvement
- **1 - Inadequate**: Below standard, major deficiencies in execution or understanding

#### 5.4 Advanced Submission Management with CMMI Dev 3.0 Compliance

**CMMI-Aligned Phase-Based Deliverable Tracking:**
- **CMMI Process Area Milestone Calendar**: Automated tracking aligned with CMMI practice areas
- **Process Area Compliance Validation**: Automatic checking against CMMI-specific requirements
- **CMMI Artifact Repository Integration**: Version control with CMMI work product templates
- **Maturity Level Assessment**: Automated evaluation against CMMI 3.0 six-level framework

**CMMI Work Product Submission Support:**
- **CMMI-Compliant Document Templates**: Pre-structured templates for CMMI work products
- **Requirements Traceability Matrix**: Bidirectional traceability tracking and validation
- **Process Performance Data**: Integration with measurement and analysis requirements
- **CMMI Audit Trail Documentation**: Complete process execution evidence collection

**CMMI Process Area Specific Validations:**
- **Project Planning (PP)**: Work breakdown structure, effort estimation, and schedule validation
- **Requirements Management (RDM)**: Requirements change impact analysis and approval workflows
- **Requirements Development (RD)**: Stakeholder needs analysis and requirements validation documentation  
- **Technical Solution (TS)**: Design alternatives analysis and selection rationale documentation
- **Measurement and Analysis (MA)**: Process performance measurement data and analysis reports

#### 5.5 CMMI-Enhanced Automated Assessment Features

**CMMI Process Area Compliance Analysis:**
- **CMMI Generic Practices Validation**: Automated checking of commitment, ability, and verification practices
- **Process Performance Measurement**: Statistical analysis of process execution effectiveness
- **CMMI Work Product Quality Assessment**: Automated evaluation against CMMI work product criteria
- **Organizational Maturity Scoring**: Assessment against CMMI 3.0 six-level maturity framework

**CMMI Category Area Specific Analysis:**
- **Managing Category Assessment**:
  - Project planning adherence to CMMI estimation and scheduling practices
  - Monitoring and control activities validation against planned objectives
  - Resource management and capacity planning effectiveness measurement
  
- **Doing Category Assessment**:
  - Requirements development completeness and stakeholder validation
  - Technical solution alternatives analysis and decision documentation
  - Product integration and verification activities compliance
  
- **Enabling Category Assessment**:
  - Decision analysis and resolution process implementation
  - Configuration management practices and audit trail maintenance
  - Measurement and analysis data collection and statistical analysis

**Advanced CMMI Traceability Checking:**
- **Bidirectional Requirements Traceability**: Automated validation of requirements-to-design-to-code links
- **CMMI Verification Compliance**: Ensure peer reviews and testing align with CMMI verification practices
- **Process Asset Integration**: Validation of organizational process asset usage and improvement

#### 5.6 CMMI-Enhanced Instructor Grading Interface

**CMMI Process Area Assessment Dashboard:**
- **CMMI Maturity Level Visualization**: Real-time assessment against six-level CMMI framework
- **Process Area Compliance Tracking**: Individual and team performance across CMMI categories
- **CMMI Work Product Evaluation**: Specialized assessment tools for CMMI-specific deliverables
- **Organizational Capability Analytics**: Trends and patterns in process improvement capabilities

**CMMI-Specific Review Features:**
- **Process Area Compliance Scoring**: Specialized rubrics for each CMMI process area
- **Generic Practice Assessment**: Evaluation of commitment, ability, activities, and verification practices
- **CMMI Appraisal Preparation**: Tools for mock CMMI appraisal exercises and feedback
- **Process Performance Analysis**: Statistical analysis tools for measurement and analysis practice area

**CMMI Category Area Grading Tools:**
- **Managing Category Interface**: Specialized tools for project planning and monitoring assessment
- **Doing Category Interface**: Focused evaluation tools for requirements, technical solution, and verification
- **Enabling Category Interface**: Assessment tools for decision analysis, configuration management, and measurement
- **Improving Category Interface**: Organizational process focus and definition evaluation capabilities

#### 5.7 Grade Calculation & Reporting
**Weighted Grade Computation:**
- **Individual Course Grades**: Separate final grades for each of the three courses
- **Integrated Learning Assessment**: Additional scoring for cross-course competencies
- **Team vs Individual Contributions**: Balanced assessment of collaborative and individual work
- **Grade Export Integration**: Direct connection to institutional LMS/SIS systems

**Detailed Performance Analytics:**
- **Phase-by-Phase Progress Tracking**: Visual representation of student improvement
- **Competency Heat Maps**: Identification of strength and weakness areas
- **Comparative Performance Analysis**: Peer comparison and class average benchmarking
- **Predictive Success Indicators**: Early warning system for at-risk students

### 6. Communication & Collaboration

#### 6.1 Team Communication
- **Integrated Messaging System**: Real-time team communication
- **Discussion Forums**: Project-specific discussion boards
- **Announcement System**: Instructor-to-student communication
- **Video Conferencing Integration**: Embedded meeting tools

#### 6.2 Feedback Management
- **Continuous Feedback Loop**: Regular feedback collection and distribution
- **Anonymous Feedback Options**: Safe feedback sharing mechanisms
- **Feedback Analytics**: Sentiment analysis and trend tracking
- **Response Tracking**: Feedback acknowledgment and action tracking

#### 6.3 Conflict Resolution
- **Issue Reporting System**: Team conflict reporting tools
- **Mediation Tools**: Instructor-mediated conflict resolution
- **Team Dynamics Assessment**: Regular team health check surveys
- **Intervention Alerts**: Automated alerts for team performance issues

### 7. Monitoring & Analytics Dashboard

#### 7.1 Student Progress Dashboard
- **Individual Progress Tracking**: Personal progress visualization
- **Team Performance Metrics**: Collective team achievement indicators
- **Phase Completion Status**: Visual phase completion tracking
- **Upcoming Deadlines**: Personalized deadline calendar

#### 7.2 Instructor Dashboard
- **Multi-Team Overview**: Simultaneous monitoring of all teams
- **Risk Identification**: Early warning system for at-risk projects
- **Workload Distribution**: Fair assessment workload management
- **Performance Comparison**: Cross-team performance analysis

#### 7.3 Administrative Analytics
- **System Usage Statistics**: Platform utilization metrics
- **Academic Performance Trends**: Longitudinal performance analysis
- **Resource Utilization**: Infrastructure usage optimization
- **User Satisfaction Metrics**: Platform effectiveness measurement

### 8. Learning Management Integration

#### 8.1 Academic Calendar Synchronization
- **Semester Schedule Integration**: Automatic academic calendar import
- **Holiday and Break Management**: Non-working day consideration
- **Exam Period Adjustments**: Assessment schedule coordination
- **Academic Year Rollover**: Seamless transition between semesters

#### 8.2 Grade Book Integration
- **Automated Grade Export**: Direct integration with institutional LMS
- **Transcript Generation**: Official academic record creation
- **Grade Distribution Analysis**: Statistical grade analysis tools
- **Academic Integrity Monitoring**: Plagiarism and collaboration tracking

### 9. Reporting & Documentation

#### 9.1 Progress Reports
- **Weekly Progress Reports**: Automated progress summary generation
- **Phase Completion Reports**: Detailed phase assessment documentation
- **Team Performance Reports**: Comprehensive team evaluation summaries
- **Individual Assessment Reports**: Personal performance documentation

#### 9.2 Portfolio Generation
- **Digital Portfolio Creation**: Automated student portfolio generation
- **Project Showcase Platform**: Public project demonstration space
- **Achievement Certification**: Automated certificate generation
- **Industry Readiness Reports**: Employment preparation assessment

### 10. Technical Infrastructure

#### 10.1 System Architecture
- **Web-based Application**: Cross-platform accessibility
- **Responsive Design**: Mobile and tablet compatibility
- **Cloud-hosted Solution**: Scalable infrastructure deployment
- **API-first Architecture**: Integration-ready system design

#### 10.2 Technology Stack
**Backend Framework:**
- Java 21 - Latest LTS version with modern language features
- Maven - Dependency management and build automation
- Spring Boot 3.5 - Enterprise-grade application framework
- Spring Security with OAuth 2.0 - Google Workspace authentication integration
- Spring Data JPA - Data access layer abstraction
- Spring Web MVC - RESTful web services

**Authentication & Security:**
- Google OAuth 2.0 Client - Spring Boot native integration for Google authentication
- Google Workspace Directory API - User profile and organizational data access
- Domain Validation - @stmik.tazkia.ac.id domain restriction enforcement
- JWT Token Management - Secure session handling with Google-issued tokens
- CSRF Protection - Cross-site request forgery prevention with OAuth state parameters

**Frontend & Templates:**
- Thymeleaf with Layout Dialect - Server-side templating engine
- Tailwind CSS (latest) - Utility-first CSS framework for modern responsive design
- Alpine.js - Lightweight JavaScript framework for progressive enhancement
- Chart.js - Data visualization and analytics charts

**Database:**
- PostgreSQL - Primary relational database
- HikariCP - High-performance connection pooling
- Flyway - Database migration management

**Testing Stack:**
- TestContainers - Integration testing with containerized dependencies
- Playwright - End-to-end testing framework
- JUnit 5 - Unit testing framework
- Mockito - Mocking framework for unit tests
- AssertJ - Fluent assertion library

**Integration APIs:**
- GitHub/GitLab REST API - Repository management
- Google Calendar API - Academic scheduling integration
- Spring Boot Actuator - Application monitoring and health checks

#### 10.3 Security Requirements
- **Data Encryption**: End-to-end data protection
- **Secure Authentication**: Multi-factor authentication support
- **Access Control**: Granular permission management
- **Audit Logging**: Comprehensive activity tracking
- **GDPR Compliance**: Privacy regulation adherence

### 11. Deployment & Maintenance

#### 11.1 Deployment Strategy
- **Docker Containerization**: Multi-stage Dockerfile with OpenJDK 21 base image
- **Maven Build Pipeline**: Automated JAR packaging and dependency resolution
- **Spring Boot Profiles**: Environment-specific configuration management
- **Database Migrations**: Flyway-managed schema versioning
- **Backup and Recovery**: PostgreSQL automated backup strategies

#### 11.2 Monitoring & Maintenance
- **Spring Boot Actuator**: Built-in health checks and metrics endpoints
- **Micrometer Integration**: Application metrics collection
- **Logback Configuration**: Structured logging with configurable levels
- **TestContainers CI**: Automated integration testing in build pipeline
- **Playwright E2E Testing**: Continuous user workflow validation

## Implementation Roadmap

### Phase 1: Foundation (Months 1-2)
- **Spring Boot Application Setup**: Maven project structure with Spring Boot 3.5
- **Database Schema**: PostgreSQL database with Flyway migrations
- **User Authentication**: Spring Security with role-based access control
- **Student Registration System**: Individual account creation and group formation
- **Group Registration Workflow**: 2-3 person group validation and enrollment
- **Basic Entity Models**: JPA entities for users, groups, and projects
- **Thymeleaf Layout**: Base template structure with Layout Dialect
- **TestContainers Setup**: Integration test infrastructure

### Phase 2: Core Features (Months 3-4)
- **Project Management Controllers**: Spring MVC controllers for project CRUD operations
- **Phase Tracking Services**: Business logic for 5-phase project workflow
- **File Upload System**: Deliverable submission with Spring Boot file handling
- **Assessment Framework**: JPA entities and services for rubric-based grading
- **Git Integration**: REST client for GitHub/GitLab API integration
- **Playwright E2E Tests**: Critical user journey automation

### Phase 3: Advanced Features (Months 5-6)
- **Analytics Dashboard**: Thymeleaf templates with Chart.js visualizations
- **Advanced Rubrics**: Complex assessment logic with Spring Data JPA
- **RESTful APIs**: Spring Web MVC REST endpoints for external integrations
- **Responsive Design**: Tailwind CSS utility classes for mobile-first optimization
- **Performance Optimization**: Database query tuning and caching strategies

### Phase 4: Testing & Deployment (Months 7-8)
- **Comprehensive Test Suite**: Full JUnit 5, Mockito, and TestContainers coverage
- **Docker Containerization**: Multi-stage Dockerfile with Maven build
- **Spring Profiles Configuration**: Production-ready application properties
- **Performance Testing**: Load testing with realistic academic workloads
- **Documentation**: JavaDoc and user documentation completion

### 10.3 Google Workspace OAuth 2.0 Configuration

**Required Maven Dependencies:**
```xml
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-oauth2-client</artifactId>
</dependency>
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-security</artifactId>
</dependency>
```

**Application Properties Configuration:**
```yaml
spring:
  security:
    oauth2:
      client:
        registration:
          google:
            client-id: ${GOOGLE_CLIENT_ID}
            client-secret: ${GOOGLE_CLIENT_SECRET}
            scope:
              - openid
              - profile
              - email
              - https://www.googleapis.com/auth/admin.directory.user.readonly
            redirect-uri: "{baseUrl}/login/oauth2/code/{registrationId}"
        provider:
          google:
            authorization-uri: https://accounts.google.com/o/oauth2/v2/auth
            token-uri: https://oauth2.googleapis.com/token
            user-info-uri: https://www.googleapis.com/oauth2/v3/userinfo
            user-name-attribute: sub

# Custom domain validation
app:
  security:
    allowed-domain: stmik.tazkia.ac.id
    redirect-after-login: /dashboard
    session-timeout: 3600
```

**Spring Security Configuration Requirements:**
- **Domain Validation Filter**: Custom filter to validate @stmik.tazkia.ac.id email domain
- **OAuth 2.0 Success Handler**: Custom handler to populate user profile from Google Workspace
- **Session Management**: Configure session timeout and concurrent session control
- **CSRF Protection**: Enable CSRF protection with OAuth 2.0 state parameter validation
- **Access Control**: Role-based access control with student/instructor roles

**Google Workspace API Integration:**
- **Directory API Setup**: Service account configuration for accessing organizational data
- **User Profile Enrichment**: Automatic population of student information from directory
- **Group Management**: Integration with Google Groups for team organization
- **Calendar Integration**: Optional calendar integration for project milestone tracking

## Success Metrics

### Academic Outcomes
- **Student Engagement**: 90%+ active participation rate
- **Project Completion**: 95%+ successful project completion rate
- **Learning Objectives**: 85%+ achievement of integrated learning goals
- **Industry Readiness**: 80%+ positive employer feedback on graduates

### System Performance
- **System Uptime**: 99.5%+ availability
- **Response Time**: <2 seconds for standard operations
- **User Satisfaction**: 4.5/5.0+ user rating
- **Data Accuracy**: 99.9%+ data integrity maintenance

### Institutional Benefits
- **Faculty Efficiency**: 40%+ reduction in manual grading time
- **Administrative Overhead**: 50%+ reduction in project monitoring effort
- **Quality Assurance**: 30%+ improvement in assessment consistency
- **Student Outcomes**: 25%+ improvement in employment placement rates

## Conclusion

This Student Project Monitoring System represents a comprehensive solution for implementing integrated project-based learning in higher education. By combining modern software development practices with academic rigor, the system enables institutions to deliver industry-relevant education while maintaining high academic standards.

The system's design reflects the real-world software development lifecycle, providing students with authentic learning experiences while giving instructors powerful tools for monitoring, assessment, and guidance. Through its comprehensive feature set and robust technical architecture, this platform can transform how project-based learning is delivered and assessed in academic environments.