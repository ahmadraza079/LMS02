# Learning Management System (LMS) - Replit Configuration

## Overview

This is a modern Learning Management System built for the Skill Development Center at the University of the Punjab. The system provides comprehensive course management, digital attendance tracking, and an administrative dashboard. It's designed as a full-stack TypeScript application with a React frontend and Express.js backend, featuring role-based authentication for students, faculty, and administrators.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
- **Framework**: React 18 with TypeScript using Vite for fast development and hot module replacement
- **UI Library**: Shadcn/ui component system built on Radix UI primitives for accessibility and consistent design
- **Styling**: Tailwind CSS with custom design tokens and CSS variables for comprehensive theming support
- **State Management**: TanStack Query (React Query) for server state management, caching, and synchronization
- **Routing**: Wouter for lightweight client-side routing with protected route functionality
- **Form Handling**: React Hook Form integrated with Zod validation for type-safe form management
- **Charts & Analytics**: Chart.js integration for attendance analytics and dashboard visualizations

### Backend Architecture
- **Framework**: Express.js with TypeScript for RESTful API development
- **Database ORM**: Drizzle ORM providing type-safe database operations with PostgreSQL
- **Authentication**: Session-based authentication with Passport.js supporting multiple login strategies
- **Session Storage**: PostgreSQL-backed session storage using connect-pg-simple for scalability
- **API Design**: RESTful endpoints with comprehensive error handling and request validation
- **Development Environment**: Hot reload integration with Vite middleware for seamless development

### Database Architecture
- **Primary Database**: PostgreSQL with Neon serverless configuration for cloud deployment
- **Schema Management**: Drizzle Kit for database migrations and schema version control
- **Core Entities**: Users, Courses, Enrollments, Materials, Announcements, Attendance, and Audit Logs
- **Data Validation**: Zod schemas providing runtime type checking and API request validation
- **Role System**: PostgreSQL enums defining user roles (STUDENT, TEACHER, ADMIN) and status types

### Authentication & Authorization
- **Authentication Strategy**: Multi-modal authentication supporting student CNIC-based login and staff credential login
- **Session Management**: Secure server-side sessions with PostgreSQL persistence and automatic cleanup
- **Role-Based Access Control**: Three-tier permission system with middleware-based route protection
- **Security Features**: HTTPS-only cookies, session rotation, CSRF protection, and secure password hashing
- **Registration Flow**: Separate registration processes for students and staff with appropriate validation

### Project Structure
- **Monorepo Organization**: Shared TypeScript schemas and types between client and server
- **Client Directory**: React application with organized component hierarchy and page structure
- **Server Directory**: Express API with modular route handlers and data access layer
- **Shared Directory**: Common type definitions, Zod validation schemas, and utility functions
- **Component Library**: Modular UI component system with consistent design patterns and accessibility

## External Dependencies

### Database & Storage
- **Neon Database**: Serverless PostgreSQL database with connection pooling
- **Drizzle ORM**: Type-safe database operations and query building
- **connect-pg-simple**: PostgreSQL session store for Express sessions

### Authentication & Security
- **Passport.js**: Authentication middleware supporting multiple strategies
- **bcrypt/scrypt**: Secure password hashing and verification
- **express-session**: Session management with secure configuration

### Frontend Libraries
- **Radix UI**: Accessible UI primitives for complex components
- **Tailwind CSS**: Utility-first CSS framework for responsive design
- **React Hook Form**: Performant form handling with minimal re-renders
- **TanStack Query**: Server state management and data fetching
- **Chart.js**: Data visualization for analytics and reporting
- **date-fns**: Date manipulation and formatting utilities

### Development Tools
- **Vite**: Fast build tool and development server
- **TypeScript**: Static type checking across the entire application
- **Zod**: Runtime type validation and schema definition
- **ESBuild**: Fast JavaScript bundler for production builds