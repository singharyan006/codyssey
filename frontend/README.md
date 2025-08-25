# Codyssey Frontend

React/TypeScript application with Monaco Editor for code editing and result visualization.

## Tech Stack

- React + TypeScript
- Monaco Editor (VS Code-like code editor)
- Material UI (or Shadcn) for UI components
- React Query for API state management
- Recharts for visualization

## Key Components

- `EditorPane` - Monaco editor and file tree for multi-file uploads
- `ResultsPane` - Score gauge and tabbed results display
- `IssueList` - Display of static analysis findings
- `AiCard` - AI mentor advice and patch previews
- `FacultyDashboard` - Class metrics and export features

## Getting Started

1. Install dependencies:
   ```
   npm install
   ```

2. Start development server:
   ```
   npm run dev
   ```

3. Build for production:
   ```
   npm run build
   ```

## API Integration

The frontend communicates with the backend API for:

- Submission of code for analysis
- Retrieval of analysis results
- Application of suggested patches

See the API documentation in the `/docs` directory for endpoint details.
