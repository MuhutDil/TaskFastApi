# TaskFastApi

A lightweight, modern to-do application built with **FastAPI** and **HTMX**. This project demonstrates how to create dynamic, interactive web applications without heavy JavaScript frameworks.

## 🚀 Features

- ✅ Create new tasks
- ✅ Mark tasks as complete/incomplete
- ✅ Inline task editing (click to edit)
- ✅ Delete tasks
- ✅ Real-time UI updates with HTMX
- ✅ Clean, responsive UI with Tailwind CSS
- ✅ No database required (in-memory storage)

## 🛠️ Tech Stack

- **Backend**: FastAPI (Python)
- **Frontend**: HTMX + Alpine.js for interactivity
- **Styling**: Tailwind CSS
- **Storage**: In-memory (Python list)

## 📦 Installation

### Prerequisites
- Python 3.8+
- pip

### Setup

1. Clone the repository:
```bash
git clone <repository-url>
cd TaskFastApi
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Run the application:
```bash
uvicorn main:app --reload
```

4. Open your browser and navigate to:
```
http://localhost:8000
```

## 📖 How It Works

### Backend (FastAPI)
- `main.py` contains all API endpoints
- Tasks are stored in a simple Python list (in-memory)
- Each task has: `id`, `title`, and `completed` status
- Endpoints return HTML fragments for HTMX to swap into the DOM

### Frontend (HTMX)
- **HTMX** handles AJAX requests and DOM updates
- **Alpine.js** provides minimal client-side state management
- **Tailwind CSS** styles the interface
- No build step required - everything works with plain HTML

### Key Endpoints

| Endpoint | Method | Description |
|----------|--------|-------------|
| `/` | GET | Main page with task list |
| `/tasks` | POST | Create a new task |
| `/tasks/{id}/toggle` | POST | Toggle task completion status |
| `/tasks/{id}/edit` | POST | Update task title |
| `/tasks/{id}/delete` | POST | Delete a task |

## 🎯 Usage

1. **Add a Task**: Type in the input field and press Enter or click "Add"
2. **Complete a Task**: Click the checkbox next to any task
3. **Edit a Task**: Click on the task text to edit it inline
4. **Delete a Task**: Click the delete button (🗑️) on any task

## 📁 Project Structure

```
TaskFastApi/
├── main.py          # FastAPI application and routes
├── templates/       # HTML templates
│   └── index.html   # Main template with HTMX
├── requirements.txt # Python dependencies
└── README.md        # This file
```

## 🧪 Learning Objectives

This project is designed to teach:
- FastAPI basics and routing
- HTMX for dynamic web interactions
- Server-side rendering patterns
- Modern alternatives to JavaScript-heavy SPAs
- RESTful API design principles

## 📄 License

This is a training project based on an article [TestDriven.io](https://testdriven.io/blog/fastapi-htmx/).
