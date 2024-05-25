# Llama2 Travel Chatbot

## Introduction

The Llama2 Travel Chatbot is an AI-powered chatbot designed to assist users with travel-related inquiries. Leveraging the power of language models, the chatbot provides accurate and reliable information to users about various travel destinations, tips, and itineraries. This project utilizes FAISS for efficient similarity search and Chainlit for creating interactive web applications.

## Tech Stack

- **Python**: Primary programming language used for the development of the project.
- **FAISS**: A library for efficient similarity search and clustering of dense vectors.
- **Chainlit**: A framework for building and deploying web applications quickly.
- **Virtual Environment (venv)**: Used to manage project dependencies.
- **PDF Processing**: Tools to handle and process PDF files.

## Project Structure


## Project Flow

1. **Data Ingestion**:
    - PDF files located in the `data` directory are processed and converted into a format suitable for vector storage.
    - `ingest.py` handles the ingestion and preprocessing of these PDF files, creating vector embeddings.

2. **Vector Storage**:
    - FAISS is used to create and manage a vector store.
    - Processed embeddings are saved in `index.faiss` and `index.pkl` within the `vectorstore` directory.

3. **Model Deployment**:
    - The main chatbot functionality is defined in `model.py`.
    - Chainlit is used to create a web interface for interacting with the chatbot. The configuration and settings for Chainlit are specified in `chainlit.md`.

4. **Environment Setup**:
    - A virtual environment (`venv`) is used to manage project dependencies.
    - Dependencies are listed in `requirements.txt` and can be installed using `pip`.

5. **Running the Application**:
    - Ensure the virtual environment is activated.
    - Run the application using Chainlit to start the web server and interact with the chatbot.

## Installation

1. Clone the repository:
    ```sh
    git clone https://github.com/yourusername/Llama2-Travel-Chatbot.git
    cd Llama2-Travel-Chatbot
    ```

2. Set up the virtual environment:
    ```sh
    python -m venv venv
    source venv/bin/activate   # On Windows use `venv\Scripts\activate`
    ```

3. Install dependencies:
    ```sh
    pip install -r requirements.txt
    ```

4. Run the data ingestion script:
    ```sh
    python ingest.py
    ```

5. Start the Chainlit application:
    ```sh
    chainlit run model.py
    ```

## Usage

Once the application is running, open your web browser and navigate to the local server address provided by Chainlit. You can now interact with the Llama2 Travel Chatbot to get information about travel destinations, tips, and itineraries.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
