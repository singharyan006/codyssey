# Codyssey Documentation

This directory contains design documents, API contracts, and other documentation for the Codyssey project.

## Contents

- `api-contracts/` - OpenAPI specifications for REST APIs
- `architecture/` - System architecture diagrams and decisions
- `database/` - Database schema and ERD
- `user-flow/` - User journey maps and wireframes

## API Contracts

### Backend API

- `POST /api/submissions`
  - Create a new code submission for analysis
  - Request: Java code files (text or zip)
  - Response: Submission ID and status

- `GET /api/submissions/{id}`
  - Get analysis results for a submission
  - Response: Full analysis results with issues, metrics, and suggestions

- `POST /api/analyze/sync`
  - Synchronous analysis for development/demo
  - Request: Java code files
  - Response: Immediate analysis results

### AI Service API

- `POST /analyze`
  - Generate mentoring suggestions based on code and static analysis
  - Request: Code snippets and top issues
  - Response: Structured suggestions with rationale and patches

## Database Schema

- `users` - User information and roles
- `submissions` - Code submissions and metadata
- `files` - Individual files within submissions
- `issues` - Static analysis findings
- `metrics` - Code quality metrics
- `suggestions` - AI-generated improvement suggestions
- `scores` - CQI and component scores

## Code Quality Index (CQI) Calculation

The CQI is calculated as a weighted average of four components:

1. **Style (25%)** - Based on Checkstyle violations per KLOC
2. **Complexity (25%)** - Based on cyclomatic complexity and nesting
3. **Maintainability (25%)** - Based on duplication, method length, and comments
4. **OOP Smells (25%)** - Based on class design and responsibility principles

Each component is normalized against thresholds and combined into a 0-100 score.
