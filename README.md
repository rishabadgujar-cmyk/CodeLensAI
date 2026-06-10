# AI Code Review Assistant (CodeLensAI)

AI Code Review Assistant is a full-stack application that analyzes source code and provides insights related to bugs, security issues, performance, complexity, and coding best practices.

Built using **FastAPI**, **React**, and integrated with **Specmatic** for contract-driven API testing.

---

## Features

- Upload source code files
- Automatic language detection
- AST-based static analysis
- Complexity analysis
- Code metrics analysis
- Bug detection
- Security issue detection
- Performance recommendations
- Best-practice suggestions
- AI-generated code review summary
- Contract-driven API testing using Specmatic

---

## Tech Stack

### Backend
- Python
- FastAPI
- Uvicorn

### Frontend
- React
- Vite

### Testing
- Specmatic
- OpenAPI

---

## Project Structure

```
ai-code-review-assistant/
│
├── backend/
│   ├── main.py
│   ├── routes.py
│   ├── ast_analyzer.py
│   ├── complexity_analyzer.py
│   ├── metrics_analyzer.py
│   ├── language_detector.py
│   └── requirements.txt
│
├── frontend/
│   ├── src/
│   ├── public/
│   └── package.json
│
├── specs/
│   ├── codelensai.yaml
│   └── openapi.json
│
└── README.md
```

---

## Installation

### Clone the repository

```bash
git clone <repository-url>
cd ai-code-review-assistant
```

---

## Backend Setup

Create a virtual environment:

```bash
python -m venv venv
```

Activate it:

### Windows

```bash
venv\Scripts\activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Run the backend:

```bash
python -m uvicorn main:app --reload
```

Server runs at:

```
http://127.0.0.1:8000
```

---

## Frontend Setup

Move into frontend:

```bash
cd frontend
```

Install dependencies:

```bash
npm install
```

Start the development server:

```bash
npm run dev
```

Frontend runs at:

```
http://localhost:5173
```

---

## API Endpoint

### Upload Source Code

**POST**

```
/upload
```

Accepts:

- multipart/form-data

Parameter:

| Name | Type |
|------|------|
| file | UploadFile |

Returns:

```json
{
  "filename": "example.py",
  "score": 85,
  "summary": "Code quality is acceptable but improvements are recommended.",
  "bugs": [],
  "security": [],
  "performance": [],
  "best_practices": [],
  "complexity": {},
  "metrics": {}
}
```

---

## Specmatic Integration

The project uses Specmatic and OpenAPI contracts to eliminate integration uncertainty.

Benefits:

- Contract-first API development
- Automatic request and response validation
- Consumer-driven contract testing
- Improved API reliability
- Better frontend-backend collaboration

---

## Future Improvements

- Support multiple programming languages
- AI-powered review suggestions using LLMs
- GitHub integration
- PDF report generation
- Authentication and user accounts
- Historical analysis dashboard

---

## Author

**Risha Badgujar**

LinkedIn:
https://www.linkedin.com/in/risha-badgujar

Hashnode:
https://rishatech.hashnode.dev

---

## License

This project is licensed under the MIT License.
