# API Documentation

## GraphQL API

The Personal Task Manager uses GraphQL for its API. All endpoints are prefixed with `/graphql`.

## Authentication

All requests require a valid JWT token in the Authorization header:

```
Authorization: Bearer <token>
```

## Queries

### Get User Profile

```graphql
query GetUserProfile {
  me {
    id
    email
    name
    avatarUrl
    createdAt
    updatedAt
  }
}
```

### Get Tasks

```graphql
query GetTasks($filter: TaskFilterInput) {
  tasks(filter: $filter) {
    id
    title
    description
    status
    priority
    dueDate
    createdAt
    updatedAt
    category {
      id
      name
    }
    tags {
      id
      name
    }
  }
}
```

### Get Categories

```graphql
query GetCategories {
  categories {
    id
    name
    color
    taskCount
  }
}
```

## Mutations

### Create Task

```graphql
mutation CreateTask($input: CreateTaskInput!) {
  createTask(input: $input) {
    id
    title
    description
    status
    priority
    dueDate
    createdAt
    updatedAt
  }
}
```

### Update Task

```graphql
mutation UpdateTask($id: ID!, $input: UpdateTaskInput!) {
  updateTask(id: $id, input: $input) {
    id
    title
    description
    status
    priority
    dueDate
    updatedAt
  }
}
```

### Delete Task

```graphql
mutation DeleteTask($id: ID!) {
  deleteTask(id: $id) {
    success
  }
}
```

## Input Types

### TaskFilterInput

```graphql
input TaskFilterInput {
  status: TaskStatus
  priority: TaskPriority
  categoryId: ID
  tagIds: [ID!]
  dueDate: DateTime
  search: String
}
```

### CreateTaskInput

```graphql
input CreateTaskInput {
  title: String!
  description: String
  status: TaskStatus
  priority: TaskPriority
  dueDate: DateTime
  categoryId: ID
  tagIds: [ID!]
}
```

### UpdateTaskInput

```graphql
input UpdateTaskInput {
  title: String
  description: String
  status: TaskStatus
  priority: TaskPriority
  dueDate: DateTime
  categoryId: ID
  tagIds: [ID!]
}
```

## Enums

### TaskStatus

```graphql
enum TaskStatus {
  TODO
  IN_PROGRESS
  DONE
  ARCHIVED
}
```

### TaskPriority

```graphql
enum TaskPriority {
  LOW
  MEDIUM
  HIGH
  URGENT
}
```

## Error Handling

The API returns errors in the following format:

```json
{
  "errors": [
    {
      "message": "Error message",
      "extensions": {
        "code": "ERROR_CODE",
        "status": 400
      }
    }
  ]
}
```

Common error codes:
- `UNAUTHENTICATED`: Authentication required
- `FORBIDDEN`: Insufficient permissions
- `NOT_FOUND`: Resource not found
- `VALIDATION_ERROR`: Input validation failed
- `INTERNAL_SERVER_ERROR`: Server error 