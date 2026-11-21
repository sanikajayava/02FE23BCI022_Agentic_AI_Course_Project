# Question Paper OBE Agent — Source Bundle

This folder contains the application source needed to run the Streamlit app,
including its agent, tool, runtime, memory, and skill modules.

## Run on Windows

Use Python 3.13, then run these commands from this folder:

```powershell
python -m venv .venv
& '.\.venv\Scripts\python.exe' -m pip install -r requirements.txt
& '.\.venv\Scripts\python.exe' .\setup_admin.py
& '.\.venv\Scripts\python.exe' -m streamlit run app.py
```

The setup script prompts for the initial administrator ID and password.
Sign in as Administrator, then create individual faculty accounts from
Faculty Management.

## Included project data

The bundle includes the question banks and four subject lesson plans needed
for the paper-generation workflow. See [data/README.md](data/README.md) for
the file list. The historical question-paper archive is not included.
Only publish these materials if you have permission to share them.

Scanned-PDF OCR also requires the Tesseract executable. The current source
expects it at `C:\Program Files\Tesseract-OCR\tesseract.exe`; update
`tools/pdf_reader_tool.py` if it is installed elsewhere.

The local faculty database is created at `data/faculty_users.db`. It is
ignored by Git and should not be uploaded.
