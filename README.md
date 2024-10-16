# AI English Tutor with RAG (Powered by Groq)

This repository contains an AI-based English teaching application that utilizes Retrieval-Augmented Generation (RAG) to generate engaging and personalized lessons on various topics. The system leverages **Groq's large language models** and **Sentence Transformers** to retrieve relevant information from a custom-built knowledge base and dynamically create lessons based on user queries. The app is built using **Streamlit** for an easy-to-use web interface.

### Key Features
- **Knowledge Base Creation**: Add content to the knowledge base by uploading PDFs or manually entering text. The content is indexed using the Sentence Transformer model `all-MiniLM-L6-v2` and stored using FAISS for efficient retrieval.
- **Retrieval-Augmented Generation (RAG)**: The system retrieves relevant content from the knowledge base and generates lessons on requested topics using Groq's large language models (e.g., `mixtral-8x7b-32768`).
- **PDF Output**: Generated lessons can be saved as PDF files for offline use, offering a convenient way to retain and share the content.
- **Topic-Based Learning**: Users can enter a topic, and the system will create an engaging lesson by combining retrieved knowledge and AI-generated content.

### Prerequisites
- Python 3.8+
- Required Python libraries:
  - `streamlit`
  - `fpdf`
  - `faiss`
  - `PyPDF2`
  - `sentence-transformers`
  - `groq`
  - `python-dotenv`

### How to Use

1. **Setup Environment**: Clone the repository and install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```

2. **Set Up API Key**: Create a `.env` file in the root directory and add your Groq API key:
    ```env
    api_key=your_groq_api_key
    ```

3. **Run the Application**: Start the Streamlit app by running:
    ```bash
    streamlit run app.py
    ```

4. **Add Content**: 
   - Upload a PDF file or manually enter text to populate the knowledge base.
   - Once added, the content will be indexed for future retrieval.

5. **Generate Lessons**: Enter an English topic and let the AI generate a tailored lesson. You can also save the lesson as a PDF for later use.

### Example Workflow
- Upload a PDF document to add relevant text to the knowledge base.
- Enter a topic, such as "Present Perfect Tense," and the system will retrieve relevant content and generate a lesson based on the stored knowledge and AI model.
- Save the lesson as a PDF for distribution or offline review.


Enjoy teaching and learning with the AI English Tutor!
