# Deployment Guide

## Prerequisites

- Node.js 18.x or later
- npm 8.x or later
- Vercel CLI
- Supabase account
- GitHub account

## Environment Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/personal-task-manager.git
   cd personal-task-manager
   ```

2. Install dependencies:
   ```bash
   # Install root dependencies
   npm install

   # Install frontend dependencies
   cd frontend && npm install

   # Install backend dependencies
   cd backend && npm install
   ```

3. Set up environment variables:
   ```bash
   # Frontend
   cp frontend/.env.example frontend/.env

   # Backend
   cp backend/.env.example backend/.env
   ```

## Supabase Setup

1. Create a new Supabase project
2. Set up the following tables:
   - users
   - tasks
   - categories
   - tags
3. Configure authentication providers
4. Set up storage buckets
5. Generate API keys

## Vercel Setup

1. Install Vercel CLI:
   ```bash
   npm install -g vercel
   ```

2. Login to Vercel:
   ```bash
   vercel login
   ```

3. Link your project:
   ```bash
   vercel link
   ```

4. Set up environment variables in Vercel dashboard:
   - Frontend variables
   - Backend variables
   - Supabase credentials

## Deployment

### Manual Deployment

1. Deploy frontend:
   ```bash
   cd frontend
   vercel --prod
   ```

2. Deploy backend:
   ```bash
   cd backend
   vercel --prod
   ```

### Automated Deployment

The project uses GitHub Actions for CI/CD. Push to the main branch to trigger automatic deployment:

```bash
git push origin main
```

## Monitoring

1. Set up error tracking:
   - Configure error monitoring in Vercel
   - Set up logging

2. Set up performance monitoring:
   - Configure Vercel Analytics
   - Set up performance monitoring

## Backup and Recovery

1. Database backups:
   - Configure Supabase backups
   - Set up automated backup schedule

2. Environment backups:
   - Export environment variables
   - Store securely

## Scaling

1. Monitor resource usage
2. Adjust Vercel plan as needed
3. Optimize database queries
4. Implement caching strategies

## Security

1. Enable HTTPS
2. Configure CORS
3. Set up rate limiting
4. Implement security headers
5. Regular security audits

## Maintenance

1. Regular updates:
   ```bash
   npm update
   ```

2. Dependency audits:
   ```bash
   npm audit
   ```

3. Performance optimization
4. Security patches
5. Database maintenance

## Troubleshooting

Common issues and solutions:

1. Deployment failures:
   - Check environment variables
   - Verify build logs
   - Check dependency versions

2. Database connection issues:
   - Verify Supabase credentials
   - Check network connectivity
   - Verify database permissions

3. Authentication problems:
   - Check JWT configuration
   - Verify Supabase auth setup
   - Check CORS settings 