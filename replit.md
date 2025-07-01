# Digital Seva Kendra - Application Management System

## Overview
Digital Seva Kendra ("We Fill, You Focus on Success") is a full-stack web application designed to streamline educational and government service applications. The system provides a professional platform for users to submit various types of applications (university admissions, government jobs, exam registrations) with integrated document management, status tracking, and payment processing.

## System Architecture

### Frontend Architecture
- **Framework**: React 18 with TypeScript
- **Styling**: Tailwind CSS with custom CSS variables for theming
- **UI Components**: Radix UI primitives with custom shadcn/ui components
- **Routing**: Wouter for client-side routing
- **State Management**: TanStack Query (React Query) for server state
- **Form Handling**: React Hook Form with Zod validation
- **Build Tool**: Vite with custom configuration for monorepo structure

### Backend Architecture
- **Runtime**: Node.js with Express.js
- **Language**: TypeScript with ES modules
- **API Design**: RESTful endpoints with JSON responses
- **Middleware**: Custom logging, error handling, and request processing
- **Development**: Integrated Vite middleware for hot reloading

### Data Storage Solutions
- **Database**: PostgreSQL with Drizzle ORM
- **Connection**: Neon serverless database (@neondatabase/serverless)
- **Schema Management**: Drizzle Kit for migrations and schema updates
- **Fallback Storage**: In-memory storage implementation for development/testing

## Key Components

### Application Management
- Multi-step application form with validation
- Document upload functionality with file type and size validation
- Service type selection (university, government, exam)
- Pricing tiers (basic, premium, enterprise) with dynamic pricing
- Reference number generation for tracking

### User Interface
- Responsive design with mobile-first approach
- Professional branding with custom color scheme
- Component library built on Radix UI primitives
- Form components with real-time validation
- Toast notifications for user feedback

### Status Tracking
- Application status workflow (submitted → processing → verified → completed/rejected)
- Status history tracking with timestamps
- Public tracking interface via reference numbers
- Progress indicators and status badges

### Document Handling
- File upload with drag-and-drop support
- Multiple file format support (.pdf, .jpg, .jpeg, .png)
- File size validation (5MB limit)
- File preview and management

## Data Flow

### Application Submission Flow
1. User fills multi-step form with personal information
2. Document upload and validation
3. Service type and pricing selection
4. Form validation using Zod schemas
5. Applicant creation in database
6. Application creation with reference number
7. Success confirmation with tracking information

### Status Tracking Flow
1. User enters reference number
2. API lookup by reference number
3. Application data retrieval with applicant information
4. Status history display
5. Real-time status updates

### Contact Management
1. Contact form submission
2. Validation using shared schemas
3. Storage in contacts table
4. Confirmation notification

## External Dependencies

### Core Libraries
- **@neondatabase/serverless**: PostgreSQL database connection
- **drizzle-orm**: Type-safe database ORM
- **@tanstack/react-query**: Server state management
- **react-hook-form**: Form handling and validation
- **zod**: Schema validation
- **wouter**: Lightweight routing

### UI Libraries
- **@radix-ui/***: Accessible UI primitives
- **tailwindcss**: Utility-first CSS framework
- **class-variance-authority**: Component variant management
- **lucide-react**: Icon library

### Development Tools
- **vite**: Build tool and dev server
- **typescript**: Type safety
- **tsx**: TypeScript execution
- **esbuild**: Production bundling

## Deployment Strategy

### Build Process
- Frontend: Vite builds React app to `dist/public`
- Backend: esbuild bundles server code to `dist/index.js`
- Static assets served from build output

### Environment Configuration
- Development: Hot reloading with Vite middleware
- Production: Static file serving with Express
- Database: PostgreSQL connection via environment variables

### Scripts
- `dev`: Development server with hot reloading
- `build`: Production build for both frontend and backend
- `start`: Production server
- `db:push`: Database schema deployment

## Changelog
- July 01, 2025. Initial setup
- July 01, 2025. Updated branding from "EduGov" to "Digital Seva Kendra" with motto "We Fill, You Focus on Success"
- July 01, 2025. Enhanced navigation styling with highlighted Home and Track Application buttons

## User Preferences
Preferred communication style: Simple, everyday language.