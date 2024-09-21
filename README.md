# SQL Chatbot Using LLM - LangChain and Hugging Face

This project is a **SQL Chatbot** that uses **LangChain**, **Hugging Face Transformers**, **SQLAlchemy**, and **Streamlit** to allow users to ask natural language questions about a SQL database. The chatbot converts user queries into SQL statements, retrieves data, and responds in natural language, making database interaction intuitive and user-friendly.

## Features

- **Natural Language Queries**: Users can ask questions in plain English.
- **SQL Query Generation**: Automatically converts questions into SQL queries.
- **Natural Language Responses**: SQL responses are transformed into user-friendly, natural language answers.
- **Entity Recognition**: Recognizes user names and converts them into email addresses if needed.
- **Conversation History**: Retains chat history for context in future questions.
- **Spacy Integration**: Uses Spacy for named entity recognition (NER) to handle queries involving user names.

## Technology Stack

- **LangChain**: For chaining the user input, SQL generation, and natural language responses.
- **Hugging Face Transformers**: Leverages the `Mixtral-8x7B-Instruct` model to handle large language queries.
- **SQLAlchemy**: To connect and interact with the SQL database using Python.
- **Streamlit**: For building an interactive web UI to facilitate communication between the user and the chatbot.
- **Spacy**: For entity recognition to detect names in user queries.

## Project Setup

### Prerequisites

- Python 3.8+
- SQL Server with the `AllWorkItems` table
- ODBC Driver 17 for SQL Server installed

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/VRAJ-07/SQL-Chatbot-Using-LLM.git
   cd SQL-Chatbot-Using-LLM
   ```

2. Install required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Create a `.env` file for database credentials:
   ```bash
   touch .env
   ```
   Add your SQL database credentials:
   ```
   DB_USERNAME=your_username
   DB_PASSWORD=your_password
   DB_HOST=your_host
   DB_NAME=your_database
   ```

4. Run the Streamlit application:
   ```bash
   streamlit run app.py
   ```

## Usage

1. Open the app on your local machine via `localhost` or the provided network URL.
2. Interact with the SQL chatbot by typing your natural language queries in the input box.
3. The chatbot will convert your query into a SQL statement, execute it on the database, and return the results in natural language.

### Example Queries

- "List any 10 projects."
- "How many users started tasks today?"
- "List unique project managers."

## Future Enhancements

- Add more advanced SQL query handling for complex joins and conditions.
- Improve entity recognition and query understanding using custom-trained models.
- Expand database schema support to multiple tables.
