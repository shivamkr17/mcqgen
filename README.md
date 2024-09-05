## Libraries Used:
- os & dotenv: For managing environment variables, particularly to fetch the Google API key for Google Generative AI.
- json & base64: For handling JSON data (MCQs and quiz structure) and base64 encoding (for displaying the PDF).
- PyPDF2: To extract text from a PDF file uploaded by the user.
- FPDF: To create and format the PDF containing the MCQs.
- streamlit: To create the user interface.

## Template Strings:
- TEMPLATE1: A prompt template used to generate the quiz by interacting with Google Generative AI (Gemini model). It asks for a  certain number of MCQs based on a provided text, in a specific subject and tone.
- TEMPLATE2: A prompt template for evaluating the complexity and appropriateness of the generated quiz for a particular level (e.g., students).

## Response JSON Structure:
- The RESPONSE_JSON dictionary provides an example format for how the response from Google AI should look, containing questions, options, and correct answers.

## LangChain & AI Chain Setup:
- ChatGoogleGenerativeAI: Initializes the connection to Google’s Gemini AI using the API key.
- LLM Chains:
   - quiz_chain: Uses the TEMPLATE to generate the MCQ quiz based on the input text, subject, and tone.
   - review_chain: Uses TEMPLATE2 to evaluate the complexity of the generated quiz and adjust if necessary.
- SequentialChain: Chains the quiz_chain and review_chain together, meaning after generating the quiz, it will be immediately evaluated.

## Quiz Generation and PDF Creation:
- Response Parsing: The response from the AI is split and parsed into a JSON format.
- PDF Creation: The quiz is added to a PDF using the PDF class. Each question and its options are added, and an "Answers" section is appended with the correct answers.
- PDF Download: The generated PDF is saved, and a download button is presented for the user to download the quiz PDF.
- PDF Display: The PDF is displayed within the Streamlit app using an embedded iframe.

<!-- ## Demo:
![Demo](demo_img/demo1.png)
![Demo](demo_img/demo2.png) -->