# Codyssey AI Service

Python FastAPI service for intelligent code analysis and suggestion generation.

## Tech Stack

- Python 3.10+
- FastAPI for REST API
- Pydantic for data validation
- Optional integrations:
  - CodeT5-small / StarCoder-base for text generation
  - sentence-transformers for retrieval
  - LLM API integration (optional premium path)

## Key Features

- Two-stage analysis:
  1. Signal extraction from static analysis results
  2. Suggestion generation based on code patterns
- Structured output format for suggestions
- Educational context for identified issues
- Optional patch generation

## Getting Started

1. Set up a Python virtual environment:
   ```
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

2. Install dependencies:
   ```
   pip install -r requirements.txt
   ```

3. Run the service:
   ```
   uvicorn app.main:app --reload
   ```

## API Endpoints

- `POST /analyze` - Process code and static analysis results to generate mentoring suggestions

See the API documentation in the `/docs` directory for complete details.

## AI Approach

The service uses a dual-path strategy:

1. **Free Path (Offline)**
   - Heuristics + small models for text generation
   - Template-guided refactor hints for common smells
   - Retrieval from curated knowledge base

2. **Premium Path (Optional)**
   - Integration with hosted LLM APIs for higher-quality advice
