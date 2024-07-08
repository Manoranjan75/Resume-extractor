# Resume Parser

Resume Parser is a Streamlit-based web application that extracts and parses information from PDF resumes. The application leverages `pdfminer` for text extraction and `nltk` for natural language processing to identify key details such as names, phone numbers, emails, skills, and educational institutions from the resume.

## Features

- **Text Extraction**: Extracts text from PDF files using `pdfminer`.
- **Name Extraction**: Identifies names using `nltk`'s named entity recognition.
- **Phone Number Extraction**: Extracts phone numbers using regular expressions.
- **Email Extraction**: Extracts email addresses using regular expressions.
- **Skill Extraction**: Identifies skills from a predefined database of common skills.
- **Education Extraction**: Identifies educational institutions using named entity recognition and keyword matching.
- **JSON Output**: Displays the extracted information in a structured JSON format.

## Installation

1. **Clone the repository**:
    ```bash
    git clone https://github.com/your-username/resume-parser.git
    cd resume-parser
    ```

2. **Create and activate a virtual environment**:
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```

3. **Install the required packages**:
    ```bash
    pip install -r requirements.txt
    ```

## Usage

1. **Run the Streamlit application**:
    ```bash
    streamlit run app.py
    ```

2. **Upload a PDF resume**: Open the local URL provided by Streamlit (usually `http://localhost:8501`), and use the file uploader to upload a resume in PDF format.

3. **View the parsed data**: The application will extract and display the parsed information in JSON format.

## File Structure

- `app.py`: The main Streamlit application script.
- `requirements.txt`: List of Python packages required to run the application.

## Example

Here's an example of how the extracted information is structured in JSON format:

```json
{
    "names": ["John Doe"],
    "phone_number": "+1234567890",
    "emails": ["john.doe@example.com"],
    "skills": ["Python", "Machine Learning", "Data Analysis"],
    "education": ["University of Example"]
}
```

## Dependencies

- `streamlit`: For creating the web interface.
- `pdfminer.six`: For extracting text from PDF files.
- `nltk`: For natural language processing tasks.
- `re`: For regular expression matching.

## Contributing

Contributions are welcome! Please open an issue or submit a pull request for any bugs, improvements, or feature requests.
