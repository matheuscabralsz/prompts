# CLAUDE.md - Todo App

This file provides guidance to Claude Code when working with the Todo App project.

## Repository Purpose

A full-stack todo application with user authentication, built to demonstrate clean architecture and modern web development practices. Users can sign up, log in, and manage their personal todo lists with full CRUD operations.

## Project Structure

```
todo-app/
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   │   ├── auth/          # Login, Signup components
│   │   │   ├── todos/         # Todo list, item, form components
│   │   │   └── common/        # Shared UI components
│   │   ├── hooks/             # Custom React hooks
│   │   ├── services/          # API client functions
│   │   ├── utils/             # Helper functions
│   │   ├── types/             # TypeScript type definitions
│   │   └── App.tsx
│   ├── public/
│   └── package.json
├── backend/
│   ├── src/
│   │   ├── controllers/       # Route handlers
│   │   ├── models/            # Database models
│   │   ├── middleware/        # Express middleware
│   │   ├── routes/            # API routes
│   │   ├── utils/             # Helper functions
│   │   ├── config/            # Configuration
│   │   └── server.ts
│   └── package.json
└── docs/
    ├── initial-idea.md
    ├── planning.md
    └── PROGRESS.md
```

## Technology Stack

**Frontend**:
- React 18 with TypeScript
- React Router for client-side routing
- TailwindCSS for styling
- Axios for HTTP requests

**Backend**:
- Node.js with Express
- TypeScript
- PostgreSQL with pg library
- bcrypt for password hashing
- jsonwebtoken for JWT authentication

**Development Tools**:
- ESLint + Prettier
- Jest for testing
- ts-node for development

## Development Workflow

### Running the Application

**Frontend**:
```bash
cd frontend
npm install
npm run dev        # Development server on port 3000
npm run build      # Production build
npm run test       # Run tests
```

**Backend**:
```bash
cd backend
npm install
npm run dev        # Development server on port 5000
npm run build      # Compile TypeScript
npm run test       # Run tests
```

**Database**:
```bash
# Ensure PostgreSQL is running
psql -U postgres -c "CREATE DATABASE todoapp;"
```

### Testing Approach

- **Unit Tests**: Business logic, utilities, and individual functions
- **Integration Tests**: API endpoints with test database
- **Component Tests**: React components with React Testing Library
- **Coverage Target**: >80% for all modules

### Quality Gates

Before completing any phase:
1. All tests must pass (`npm test`)
2. Build must succeed (`npm run build`)
3. No ESLint errors (`npm run lint`)
4. No TypeScript errors (`tsc --noEmit`)

## Implementation Phases

Follow the phases defined in `docs/planning.md`:
1. **Phase 1**: Project setup and infrastructure
2. **Phase 2**: Authentication system
3. **Phase 3**: Todo CRUD backend
4. **Phase 4**: Todo UI components
5. **Phase 5**: Polish and testing

Track progress in `docs/PROGRESS.md`.

## Coding Conventions

### TypeScript
- Use strict mode
- Explicit return types for all functions
- Use interfaces for object shapes
- Prefer `type` for unions and primitives
- No `any` types - use `unknown` if needed

### React
- Functional components with hooks
- Props interfaces defined above component
- Custom hooks in `/hooks` directory
- Component file structure: imports → types → component → export

### API Design
- RESTful conventions
- HTTP status codes: 200 (OK), 201 (Created), 400 (Bad Request), 401 (Unauthorized), 404 (Not Found), 500 (Server Error)
- Consistent JSON response format:
  ```typescript
  { success: true, data: {...} }
  { success: false, error: "message" }
  ```

### Naming
- Components: PascalCase (`TodoList.tsx`)
- Files: camelCase (`authService.ts`)
- API routes: kebab-case (`/api/todos`)
- Constants: UPPER_SNAKE_CASE
- Variables/functions: camelCase

### Database
- Table names: plural snake_case (`users`, `todos`)
- Column names: snake_case
- Use migrations for schema changes
- Always use parameterized queries (prevent SQL injection)

## File Organization

### Frontend
- `/components/auth/`: Authentication-related components
- `/components/todos/`: Todo management components
- `/components/common/`: Reusable UI components (buttons, inputs, modals)
- `/services/`: API client functions, grouped by resource
- `/hooks/`: Custom React hooks (`useAuth`, `useTodos`)
- `/types/`: Shared TypeScript interfaces and types
- `/utils/`: Helper functions, validators, formatters

### Backend
- `/controllers/`: Route handlers (thin, delegate to services)
- `/models/`: Database models and queries
- `/middleware/`: Express middleware (auth, validation, error handling)
- `/routes/`: API route definitions
- `/utils/`: Helper functions, validators
- `/config/`: Configuration (database, JWT secret, etc.)

## Important Principles

1. **Security First**:
   - Never store passwords in plain text
   - Always validate and sanitize user input
   - Use parameterized queries to prevent SQL injection
   - Store JWT secret in environment variables
   - Implement rate limiting on auth endpoints

2. **User Isolation**:
   - Users can only access their own todos
   - All todo queries must filter by user ID
   - Verify token and user ownership in middleware

3. **Error Handling**:
   - Use try-catch blocks in async functions
   - Return meaningful error messages
   - Log errors server-side for debugging
   - Don't expose sensitive information in error responses

4. **Type Safety**:
   - Define interfaces for all API requests/responses
   - Type all component props
   - Use TypeScript's strict mode

5. **Testing**:
   - Write tests alongside features
   - Test happy paths and error cases
   - Mock external dependencies (database, APIs)
   - Use a separate test database

6. **Code Quality**:
   - Keep functions small and focused
   - Use meaningful variable names
   - Comment complex logic
   - Remove unused code and imports

## Common Tasks

### Adding a New Todo Field
1. Update Todo interface in `/backend/src/models/todo.ts`
2. Modify database schema and run migration
3. Update API validation middleware
4. Update frontend Todo type in `/frontend/src/types/`
5. Update TodoForm component
6. Add tests for new field

### Adding a New API Endpoint
1. Define route in `/backend/src/routes/`
2. Create controller function in `/backend/src/controllers/`
3. Add authentication middleware if needed
4. Write validation middleware
5. Add integration tests
6. Create frontend service function
7. Update components to use new endpoint

### Adding a New Component
1. Create component file in appropriate directory
2. Define Props interface
3. Implement component logic
4. Add to parent component
5. Write component tests
6. Update Storybook if using
