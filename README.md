![Python](https://img.shields.io/badge/Tool-Python-blue)  
![Gui](https://img.shields.io/badge/Gui-Tinker-blue) 
![File export](https://img.shields.io/badge/FileExport-openpyxl-blue) 
![Completed](https://img.shields.io/badge/Status-Completed-success)



# 🎓 Bloom’s Taxonomy Question Classifier
**"Bloom’s Taxonomy-Based Question Classification"** uses **NLP** and **WordNet** to categorize questions by cognitive level, enhancing educational assessments.

<img width="293" height="172" alt="image" src="https://github.com/user-attachments/assets/65cc4b25-1fd4-43d2-a074-820b897d16b6" />

*six levels of Bloom’s Taxonomy** (Remember, Understand, Apply, Analyze, Evaluate, Create).
---

## 📌 Features

* 🔑 **Login system** with two roles:

  * Student → `student` / `password`
  * Teacher → `teacher` / `password`
* 📝 Enter multiple questions separated by commas
* 🧠 Automatic classification into Bloom’s levels using keyword matching
* 📊 Entering Question Mannulay 
* 🖥️ Easy-to-use Tkinter GUI

---

## 🧰 Tech Stack

| Component   | Technology                       |
| ----------- | -------------------------------- |
| Language    | Python 3                         |
| GUI         | Tkinter                          |
| File Export | openpyxl                         |

---

## 🗂 Project Structure

```
bloom_classifier/
├── bloom_app.py      # Main Python application
└── README.md         # Project documentation
```

---

## 🚀 How to Run

Vs code 

Login with:

* **Student** → `student` / `password`
* **Teacher** → `teacher` / `password`

---
## ScreenShots 
<img width="496" height="277" alt="image" src="https://github.com/user-attachments/assets/e14c1f69-edd7-4952-8b39-4ad4aa0b6ae0" />
<img width="746" height="782" alt="image" src="https://github.com/user-attachments/assets/fc84223d-b7c4-4541-bc43-b7328308b9ab" />




## 🧠 How It Works

1. **Login screen** checks role (hardcoded usernames/passwords).
2. After login, the **BloomGUI** opens.
3. User enters questions → app splits them by commas.
4. Each question is matched against keyword lists for Bloom’s levels.
5. Classified results are shown in the GUI.
6. The same data is appended to an Excel file (`questions.xlsx`) on the desktop:

   * Column A → Serial number
   * Column B → Question text
   * Column C → Bloom’s level

---


## 📈 Future Enhancements

* ✅ Stronger login system (hashed passwords or DB)
* ✅ Advanced NLP with **spaCy** or **transformers** instead of simple keyword matching
* ✅ Export to CSV/PDF for reports

---

## 👨‍💻 Author

**Shubham Ghalsasi**
Final Year B.Tech – Cloud Computing
MIT ADT University
📫 [ghalsasishubham@gmail.com](mailto:ghalsasishubham@gmail.com)

