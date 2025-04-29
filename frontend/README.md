# Personal Task Manager

A modern task management application built with React, TypeScript, and NestJS.

## Project Structure

```
personal-task-manager/
├── .github/                    # GitHub Actions workflows
│   ├── workflows/
│   │   ├── ci.yml             # Continuous Integration
│   │   ├── cd.yml             # Continuous Deployment
│   │   └── security.yml       # Security scanning
│   └── ISSUE_TEMPLATE/        # Issue templates
├── docs/                      # Project documentation
│   ├── architecture.md       # System architecture
│   ├── api.md               # API documentation
│   └── deployment.md        # Deployment guide
├── frontend/                 # React frontend
│   ├── public/              # Static assets
│   ├── src/
│   │   ├── assets/         # Images, fonts, etc.
│   │   ├── components/     # Reusable components
│   │   │   ├── common/    # Shared components
│   │   │   ├── layout/    # Layout components
│   │   │   └── features/  # Feature-specific components
│   │   ├── hooks/         # Custom React hooks
│   │   ├── pages/         # Page components
│   │   ├── services/      # API services
│   │   ├── store/         # State management
│   │   ├── types/         # TypeScript types
│   │   ├── utils/         # Utility functions
│   │   ├── App.tsx        # Main App component
│   │   └── main.tsx       # Entry point
│   ├── tests/             # Frontend tests
│   ├── .env.example       # Environment variables example
│   └── package.json       # Frontend dependencies
├── backend/                # NestJS backend
│   ├── src/
│   │   ├── auth/          # Authentication module
│   │   ├── tasks/         # Tasks module
│   │   ├── users/         # Users module
│   │   ├── common/        # Common utilities
│   │   ├── config/        # Configuration
│   │   └── main.ts        # Entry point
│   ├── tests/             # Backend tests
│   ├── .env.example       # Environment variables example
│   └── package.json       # Backend dependencies
├── scripts/               # Utility scripts
│   ├── setup.sh          # Project setup
│   └── deploy.sh         # Deployment scripts
├── .gitignore            # Git ignore rules
├── .prettierrc           # Prettier configuration
├── .prettierignore       # Prettier ignore rules
├── .eslintrc.js          # ESLint configuration
├── tsconfig.json         # TypeScript configuration
└── package.json          # Root package.json
```

## Getting Started

1. Clone the repository
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
4. Start development servers:
   ```bash
   # Start frontend
   cd frontend && npm run dev
   
   # Start backend
   cd backend && npm run start:dev
   ```

## Development Guidelines

- Follow the [Code of Conduct](CODE_OF_CONDUCT.md)
- Use [Conventional Commits](https://www.conventionalcommits.org/)
- Follow the [Contributing Guidelines](CONTRIBUTING.md)
- Maintain test coverage above 80%

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
