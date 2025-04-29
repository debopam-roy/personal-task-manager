# System Architecture

## Overview

The Personal Task Manager is a modern web application built with a microservices architecture. It consists of a React frontend, NestJS backend, and Supabase for data storage and authentication.

## Components

### Frontend (React + TypeScript + Vite)

- **Components**: Reusable UI components organized by feature
- **Pages**: Route-based components for different views
- **Services**: API communication layer
- **Store**: State management using Redux Toolkit
- **Hooks**: Custom React hooks for shared logic
- **Utils**: Helper functions and utilities

### Backend (NestJS)

- **Modules**: Feature-based organization
  - Auth: Authentication and authorization
  - Tasks: Task management
  - Users: User management
- **Services**: Business logic
- **Controllers**: API endpoints
- **DTOs**: Data transfer objects
- **Entities**: Database models

### Database (Supabase)

- **Tables**:
  - users
  - tasks
  - categories
  - tags
- **Relationships**: Properly defined foreign keys and constraints
- **Indexes**: Optimized for common queries

### Authentication (Supabase Auth)

- Email/password authentication
- Social login integration
- JWT-based session management
- Role-based access control

### Notifications

- **Email**: Using Resend
- **Slack**: Webhook integration
- **In-app**: Real-time notifications

## Data Flow

1. User interacts with React frontend
2. Frontend makes API calls to NestJS backend
3. Backend processes request and interacts with Supabase
4. Supabase handles data persistence and authentication
5. Backend sends response to frontend
6. Frontend updates UI based on response

## Security

- HTTPS everywhere
- JWT authentication
- Input validation
- Rate limiting
- CORS configuration
- Environment variable management

## Deployment

- Frontend: Vercel
- Backend: Vercel Serverless Functions
- Database: Supabase
- CI/CD: GitHub Actions

## Monitoring and Logging

- Error tracking
- Performance monitoring
- User analytics
- Server logs

## Scalability Considerations

- Horizontal scaling for backend
- CDN for static assets
- Database optimization
- Caching strategies 