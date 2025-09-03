# Edu-App (FastAPI Project)

This is a simple FastAPI application that serves an HTML page using Jinja2 templates and displays system information.

# Edu-App (FastAPI Project)

This project is a **web application built with FastAPI**.  
It shows **system information** (like OS, CPU, version, etc.) inside a webpage by using **Jinja2 templates**.

Think of it like this:
- `main.py` → starts the FastAPI server (like the brain of the app).
- `system_info.py` → collects system details.
- `templates/index.html` → defines how the web page looks.
- `requirements.txt` → lists the Python packages the app needs.

---

## ✨ What happens when you run the app?

1. You start the server with **Uvicorn** (a super fast ASGI server).
2. The server waits for requests on [http://127.0.0.1:8000](http://127.0.0.1:8000).
3. When you open that URL in your browser:
   - FastAPI calls `get_system_info()` from `system_info.py`.
   - That function returns system details in a Python dictionary.
   - The dictionary is converted into JSON text (pretty formatted).
   - The `index.html` template is loaded and filled with this JSON.
   - Finally, the webpage displays your system information.

---

'''## 📂 Project Structure

Edu-App/
│── main.py # FastAPI entry point
│── system_info.py # Function to fetch system information
│── templates/
│ └── index.html # HTML template
│── requirements.txt # Python dependencies

## 🛠️ Installation

### 1. Clone the repository
```bash
git clone https://github.com/ajithapamula/Edu-App.git
cd Edu-App
