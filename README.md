 Resume Screening & Job Application Web App

This project contains two parts:

1. **A Flask-based Job Application Form** where candidates can submit their information and upload a resume.
2. **A Resume Screening Script** that reads resumes and scores them based on similarity to a given job description using TF-IDF and cosine similarity.



 Project Files

* **app.py** – Flask application for handling form submissions and resume uploads
* **form.html** – Bootstrap-based front-end form
* **screen_resume.py** – Script for automated resume reading, scoring, and ranking
* **uploads/** – Folder where uploaded resumes are saved (auto-created)


 Features

 Web Application (Flask)

* User-friendly job application form
* Validates all fields
* Accepts **PDF**, **DOC**, **DOCX** resumes (max 30 MB)
* Secure file upload using `werkzeug`
* Flash messages for success or errors
* Clean Bootstrap UI

 Resume Screening Script

* Reads `.pdf` and `.docx` files
* Extracts text using **python-docx** and **PyPDF2**
* Uses **TF-IDF Vectorization**
* Calculates **cosine similarity** between resume and job description
* Sorts resumes by highest match score
* Saves results to **results.csv**



 Tech Stack

* **Python**
* **Flask**
* **Bootstrap 5**
* **python-docx**
* **PyPDF2**
* **scikit-learn**


 Installation

 Clone the repository

```
git clone <your-repository-url>
cd <repository-folder>
```

 Create a virtual environment

```
python -m venv venv
```

Activate:

* Windows: `venv\Scripts\activate`
* macOS/Linux: `source venv/bin/activate`

 Install dependencies

```
pip install flask python-docx PyPDF2 scikit-learn
```

---

 Running the Flask App

```
python app.py
```

The app will run at:

```
http://127.0.0.1:5000/
```

Uploaded resumes appear in the **uploads/** folder.

---

## ▶ Running the Resume Screening Script

Place all resumes to evaluate inside:

```
resumes/
```

Edit the job description in `screen_resume.py` if needed, then run:

```
python screen_resume.py
```

This will:

* Print ranked results in the terminal
* Generate **results.csv** with scores

---

 Example Output

```
Resume Ranking Based on Job Description Match:

resume1.pdf --> Score: 0.7512
resume2.docx --> Score: 0.5034
resume3.pdf --> Score: 0.4301
```

---

 Future Enhancements

* Admin dashboard to view applications
* NLP-based resume parsing
* Database integration
* Custom job description upload
* Support for more file types

---

 License

This project is open-source. You may use, modify, or distribute it as needed.
