from getpass import getpass
import os

# -----------------------------
# 1️⃣ GitHub info
GIT_USERNAME = "saymon800"
GIT_EMAIL = "kaaziisaymon58@gmail.com"
REPO_URL = "https://github.com/kazisaymon/Pdf-assistant.git"
PROJECT_PATH = "/content/ai-pdf-assistant"

# GitHub Personal Access Token
GIT_TOKEN = getpass("Enter your GitHub Personal Access Token: ")

# -----------------------------
# 2️⃣ Create Project Folder
os.makedirs(PROJECT_PATH, exist_ok=True)
print("Project folder created at:", PROJECT_PATH)

# -----------------------------
# 3️⃣ Create Files
# app.py
app_code = """
import streamlit as st

st.title("📄 AI PDF Assistant")
st.write("Modern AI PDF Assistant App placeholder")
"""
with open(os.path.join(PROJECT_PATH, "app.py"), "w") as f:
    f.write(app_code)

# requirements.txt
requirements = """
streamlit
pdfplumber
sentence-transformers
faiss-cpu
transformers
torch
numpy
pandas
scikit-learn
tqdm
pyngrok
reportlab
"""
with open(os.path.join(PROJECT_PATH, "requirements.txt"), "w") as f:
    f.write(requirements.strip())

# .gitignore
gitignore = """
__pycache__/
*.pyc
*.pkl
*.ipynb_checkpoints/
.env
"""
with open(os.path.join(PROJECT_PATH, ".gitignore"), "w") as f:
    f.write(gitignore.strip())

# Professional README.md
readme = """
#  AI PDF Assistant

A modern **Streamlit app** that allows you to interact with PDF documents efficiently.
Upload any PDF, generate summaries, ask questions, and download results as TXT or PDF.

---

##  Features

- **Upload PDFs:** Easily upload your documents.
- **Automatic Summaries:** Generate concise summaries instantly.
- **Interactive Q&A:** Ask questions about your PDF content.
- **Download Options:** Save summaries in TXT or PDF format.
- **Modern UI:** Clean interface with optional dark mode.

---

##  Installation

Clone the repository and install the dependencies:

```bash
git clone https://github.com/kazisaymon/Pdf-assistant.git
cd Pdf-assistant
pip install -r requirements.txt
