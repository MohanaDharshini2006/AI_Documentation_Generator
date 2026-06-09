# AI-Powered External Documentation Generator

Automatically converts source code into professional, business-friendly documentation using Google Gemini AI. Supports code paste, file uploads, Git repository analysis, industry-specific templates, Mermaid diagrams, and PDF export.


## Overview

Writing external documentation manually is slow and inconsistent. This tool automates the entire process — it reads your source code, understands what it does, and produces structured documentation tailored to your industry and audience (clients, stakeholders, or end users).

---

## Features

**Code Input Options**
- Paste source code directly into the editor
- Upload code files from your local machine
- Analyze a remote Git repository by URL

**AI Documentation Generation**
- Powered by Google Gemini 2.5 Flash
- Identifies your tech stack automatically
- Extracts and explains features in business-friendly language
- Generates structured documentation ready for external use

**Industry-Specific Templates**
- SaaS, FinTech, MedTech, and EduTech templates available
- Each template is tailored to domain-specific terminology and structure

**Diagrams & Visualizations**
- Generates Mermaid diagrams (architecture, workflows)
- Exports diagrams as PNG

**Export**
- Download as PDF
- Shareable documentation output

---

## Tech Stack

| Layer | Technology |
|---|---|
| Backend | Python, Flask |
| AI / NLP | Google Gemini 2.5 Flash |
| Frontend | HTML, CSS, JavaScript |
| Diagrams | Mermaid.js |
| PDF Generation | ReportLab |
| Utilities | Git processing, file upload handling, `.env` config |

---

## Project Structure

```
project/
├── app.py
├── templates/
│   ├── index.html
│   └── ...
├── static/
│   ├── css/
│   ├── js/
│   └── images/
├── uploads/
├── generated_docs/
├── .env.example
├── requirements.txt
└── README.md
```

---

## Installation

### Prerequisites

- Python 3.8+
- pip
- A Google Gemini API key ([get one here](https://aistudio.google.com/app/apikey))

### 1. Clone the repository

```bash
git clone https://github.com/your-username/ai-documentation-generator.git
cd ai-documentation-generator
```

### 2. Create a virtual environment

**Windows**
```bash
python -m venv venv
venv\Scripts\activate
```

**Linux / macOS**
```bash
python3 -m venv venv
source venv/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

---

## Configuration

Create a `.env` file in the project root (use `.env.example` as a template):

```env
GOOGLE_API_KEY=your_gemini_api_key_here
```

> **Important:** Never commit your `.env` file. It is already listed in `.gitignore`.

---

## Usage

Start the development server:

```bash
python app.py
```

Open your browser at `http://localhost:5000`.

### Option 1 — Paste code

1. Open the app and paste your source code into the editor.
2. Select an industry template (SaaS, FinTech, MedTech, or EduTech).
3. Click **Generate Documentation**.

### Option 2 — Upload a file

1. Click the upload button and select a code file from your machine.
2. Choose a documentation template.
3. Click **Generate Documentation**.

### Option 3 — Analyze a Git repository

1. Enter your repository URL in the Git input field.
2. Click **Analyze Repository**.
3. Once analysis is complete, click **Generate Documentation**.

---

## Workflow

```
Source Code / Repository
         │
         ▼
    Code Analysis
         │
         ▼
  Gemini AI Engine
         │
         ▼
  Template Selection
         │
         ▼
Documentation Generation
         │
         ▼
   PDF / Export Output
```

---

## Use Cases

**SaaS Applications** — Product documentation, feature descriptions, user guides

**FinTech Platforms** — Financial workflow documentation, user onboarding guides, compliance summaries

**MedTech Solutions** — Healthcare software documentation, functional workflow descriptions, end-user guides

**EduTech Products** — Learning platform documentation, student onboarding guides, feature explanations

---

## Security

- Store your API key in `.env` — never hardcode it in source files
- Add `.env` to `.gitignore` before your first commit
- Validate and sanitize all uploaded files before processing
- Set an upload size limit in your Flask configuration to prevent abuse

```python
app.config['MAX_CONTENT_LENGTH'] = 5 * 1024 * 1024  # 5 MB max upload
```

---

## Roadmap

- [ ] Multi-language documentation output
- [ ] Swagger / OpenAPI integration
- [ ] Interactive architecture diagrams
- [ ] Version-controlled documentation history
- [ ] Cloud deployment support (AWS / GCP / Azure)
- [ ] CI/CD pipeline integration
- [ ] Automated test generation

---

## License

This project is licensed under the [MIT License](LICENSE).

---

## Acknowledgements

- [Google Gemini API](https://ai.google.dev/)
- [Flask](https://flask.palletsprojects.com/)
- [Mermaid.js](https://mermaid.js.org/)
- [ReportLab](https://www.reportlab.com/)
