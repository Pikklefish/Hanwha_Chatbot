# Hanwha PDF Chat App
------------
TO Check ChatBot answers for the Hanwha 2024 Global internship program on `AI Track(Data Lab)_Case Study 기초자료` check the `Hanwha_Chatbot_Q&A` folder and the images inside it. Thank you~

## Introduction
------------
The MultiPDF Chat App is a Python application that allows you to chat with multiple PDF documents. You can ask questions about the PDFs using natural language, and the application will provide relevant responses based on the content of the documents. This app utilizes a language model to generate accurate answers to your queries. Please note that the app will only respond to questions related to the loaded PDFs.

## How It Works
------------
>This project is based off on alejandro's "ask-multiple-pdf" repository [repo](https://github.com/alejandro-ao/ask-multiple-pdfs)

The application follows these steps to provide responses to your questions:

1. PDF Loading: The app reads multiple PDF documents and extracts their text content.

2. Text Chunking: The extracted text is divided into smaller chunks that can be processed effectively.

3. Language Model: The application utilizes a language model to generate vector representations (embeddings) of the text chunks.

4. Similarity Matching: When you ask a question, the app compares it with the text chunks and identifies the most semantically similar ones.

5. Response Generation: The selected chunks are passed to the language model, which generates a response based on the relevant content of the PDFs.

## Dependencies and Installation
----------------------------
To install the MultiPDF Chat App, please follow these steps:

1. This project works best on Github Codespaces but you may also Clone the repository to your local machine.

2. Install the required dependencies by running the following command:
   ```
   pip install -r requirements.txt
   ```

3. Obtain an API key from OpenAI and add it to the `.env` file in the project directory.
```commandline
OPENAI_API_KEY=your_secrit_api_key
```

## Usage
-----
To use the MultiPDF Chat App, follow these steps:

1. Ensure that you have installed the required dependencies and added the OpenAI API key to the `.env` file.

2. Run the `main.py` file using the Streamlit CLI. Execute the following command:
   ```
   streamlit run app.py
   ```

3. The application will launch in your default web browser, displaying the user interface.

4. Load multiple PDF documents into the app by following the provided instructions.

5. Ask questions in natural language about the loaded PDFs using the chat interface.


##Errors and Troubleshooting
-------
1. In Github Codespaces, "bash: streamlit: command not found"
2. This is an error where "streamlit" is not recognized in the PATH.
3. To resolve this issue find where "streamlit" is located using this command ```find /home/codespace -name streamlit   ```
4. Depending on where "streamlit" is located the PATH is different but usually it's this ```export PATH=$PATH:/home/codespace/.local/lib/python3.10/site-packages/bin```
5. When that runs you may now try the program again ```streamlit run app.py```

1. WHile `pip install` on your local machine sometimes SWIG and RUST might not work.
2. Install those packages separately online and add them to PATH.
3. Double check in the command prompt SWIG and RUST are installed by checking their `-version`.
4. Re-run the progam
## License
-------
The MultiPDF Chat App is released under the [MIT License](https://opensource.org/licenses/MIT).
