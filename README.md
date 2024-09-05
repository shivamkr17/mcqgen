# MCQ Generator

This project is a Multiple Choice Question (MCQ) Generator that uses the **Google Generative AI** model (Gemini Pro) to create quizzes from text input or a PDF file. The application allows customization of the number of questions, subject, and difficulty level. The generated quizzes are analyzed for complexity, adjusted as needed, and can be downloaded as a PDF file.

## Features

- **Generate MCQs from Text or PDF**: Input text directly or upload a PDF file to generate multiple-choice questions.
- **Customizable Quiz Settings**: Set the number of questions, the subject of the quiz, and the difficulty level.
- **AI-Powered Quiz Generation and Evaluation**: Leverages the Gemini Pro model to generate high-quality MCQs and evaluate their complexity.
- **PDF Export**: Generated quizzes are downloadable as a well-formatted PDF file with both questions and answers.

## Technologies Used

- **Python**
- **Streamlit**: For building the web interface.
- **LangChain**: To build LLM-powered chains for generating and evaluating the quiz.
- **Google Generative AI (Gemini Pro)**: For generating MCQs and evaluating their complexity.
- **FPDF**: For generating PDFs with questions and answers.
- **PyPDF2**: For extracting text from uploaded PDF files.
- **dotenv**: For managing environment variables securely.


