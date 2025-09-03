



### Complex Table Extraction from PDFs to CSV-JSON - AI Web Application

Automatically extract complex tables from your PDF documents and convert them into clean, ready-to-use CSV or JSON formats. Powered by advanced AI, this application streamlines the data extraction process and allows you to ask questions about the tables via an agent.

# 🚀 Key Features 

- **AI-Powered Extraction:** Processes complex PDF tables with high accuracy.
- **User-Friendly Interface:** Upload a PDF, select pages, and instantly download as CSV or JSON.
- **Smart Error Handling:** Delivers clean and reliable outputs.
- **Powerful Integrations:** Hugging Face models, gmft library, agentic AI, and vector database support.

# 🔧 Technology Stack

- **Backend:** Python (FastAPI), Hugging Face Transformers
- **Frontend:** React.js
- **PDF Processing:** gmft, PyPDF2
- **Database:** PostgreSQL
- **AI Features:** Custom NER and summarization models

# 🛠 Use Cases
- **Complex Table Extraction**

  Accurately handles nested headers, merged cells, and similar structures.
  Suitable for financial reports, academic studies, and official documents.
- **RAG (Retrieval-Augmented Generation) Integration**




## Installation

### 1️⃣ Clone the Repository

Run the following command in your terminal or command prompt to clone the repository to your local machine:
```bash
git clone https://github.com/klncgty/pdfXtractor.git
```

### 2️⃣ Install Python Dependencies

To install the required Python packages for the API, use the requirements.txt file located in the project’s root directory:
```bash
pip install -r requirements.txt
```

### 3️⃣ Run the API

The API code is located in the api folder. Navigate to the api folder in your terminal and start the FastAPI application:
```bash
cd ../api
uvicorn main:app --reload
```

### 4️⃣ Run the Frontend

The frontend code is located in the src folder. Navigate to the src folder in your terminal and run the following commands:
```bash
cd src
npm install
npm run dev
```

After running the command, you will see an output similar to this in your terminal:
```
➜  Local:   http://localhost:port/
```

click on terminal to visualize app [http://localhost:port/](http://localhost:port/) 


## ⚠️ Important Notes

- ** PDF uploading:**  
  Uploaded PDF files will be saved in the uploads folder in your local directory.
- ** Outputs:**  
Outputs generated from processed PDF files are saved in the outputs folder. Ensure this folder exists and has write permissions.
- ** CORS error:**  
If you encounter an error in the browser like this:
  ```
  Access to XMLHttpRequest at 'http://localhost:8000/upload' from origin 'http://localhost:5173' has been blocked by CORS policy
  ```

  You can solve erorr  adding this `allow_origins=["*"]`  to `api/main.py`  

  ```python
  from fastapi.middleware.cors import CORSMiddleware

  app.add_middleware(
      CORSMiddleware,
      allow_origins=["*"],  # Tüm domainlere izin verir
      allow_credentials=True,
      allow_methods=["*"],
      allow_headers=["*"],
  )
  ```

## 📌 Add.

- **Frontend and API Communication:**  
The frontend interacts with the API to upload and process PDF files. Ensure both are running simultaneously.
- **Development:**  
 ....


- **Models**  
   gmft: https://github.com/conjuncts/gmft and
  pandasai base model: https://arxiv.org/abs/2110.00061

---

If you encounter any issues, please report them via GitHub Issues.


