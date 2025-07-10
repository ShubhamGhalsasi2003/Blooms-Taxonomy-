# 🎓 Bloom’s Taxonomy Question Classifier

This desktop app lets teachers and students type (or paste) a list of questions and instantly see which Bloom’s‑Taxonomy level each question targets.  
The program also saves every entry to an Excel sheet on the user’s desktop for later analysis.

---

## 📌 What the App Does

| Action | Result |
| ------ | ------ |
| **Login** as *Student* or *Teacher* | Simple credential check (`student/password`, `teacher/password`) |
| **Enter questions** separated by commas | App scans each question for Bloom‑keywords |
| **Click “Show Descriptions”** | Displays the cognitive level (Remember, Understand, Apply, Analyze, Evaluate, Create) for every question |
| **Excel export** | Automatically appends the questions and their levels to `questions.xlsx` on the desktop |

---

## 🧰 Tech Stack

- **Python 3** + **Tkinter** – GUI windows  
- **openpyxl** – writes the Excel file  
- **Standard library** only for everything else (no external DB)

---

## 🗂 Folder / File Layout

```
bloom_classifier/
├── bloom_app.py          # (main code shown below)
└── README.md
```

---

## 🚀 How to Run

```bash
# 1. Clone or download
git clone https://github.com/<your‑handle>/bloom-classifier.git
cd bloom-classifier

# 2. (Optional) create virtual env
python -m venv venv
source venv/bin/activate   # Windows: venv\Scripts\activate

# 3. Install openpyxl (Tkinter is bundled with Python)
pip install openpyxl

# 4. Launch the app
python bloom_app.py
```

Login with:
- **Student** → `student` / `password`
- **Teacher** → `teacher` / `password`

---

## 🧠 How It Works (Logic Flow)

1. **Login Window** decides which role (no DB, just hard‑coded strings).
2. After success, the **BloomGUI** window appears.
3. User enters questions → program splits them by comma.
4. Each question is converted to lowercase and matched against keyword lists for the six Bloom levels.
5. The identified level (or “Unknown”) is displayed in the GUI.
6. The same data are appended to `questions.xlsx` on the user’s desktop:
   - Column A = serial number  
   - Column B = original question  
   - Column C = Bloom level

---

## ✏️ Customize the Keyword Lists

Inside `BloomGUI.__init__` you’ll find `self.levels_keywords`.  
Add or remove verbs to fine‑tune detection—for example:

```python
"Analyze": ["analyze", "compare", "categorize", "differentiate", "dissect"]
```

---

## 📈 Possible Improvements

- Hash‑based login or integration with a real user database
- Better NLP (e.g., spaCy) instead of simple keyword matching
- Export CSV or PDF reports
- Dark/light theme toggle in Tkinter
- Mac/Linux Desktop path detection (currently uses Windows `%USERPROFILE%`)

---

## 👨‍💻 Author

Shubham Ghalsasi • Final‑year B.Tech (Cloud Computing) • MIT‑ADT University  
📫 ghalsasishubham@gmail.com

---

> **Note**  
> This tool is a proof‑of‑concept for classroom use. Accuracy depends on the keyword lists and may need tweaking for real exams.
