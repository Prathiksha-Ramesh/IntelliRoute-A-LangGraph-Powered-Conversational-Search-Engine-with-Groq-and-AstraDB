# IntelliRoute: A LangGraph-Powered Conversational Search Engine with Groq and AstraDB

IntelliRoute is an advanced conversational search engine that intelligently routes user queries to either a specialized vector store or external knowledge sources like Wikipedia, based on the nature of the question. Powered by LangGraph for stateful execution and Groq for high-performance NLP, IntelliRoute provides accurate, context-aware responses tailored to the user's needs.

## Project Structure

```
project-directory/ 
│ ├── app.py 
├── requirements.txt 
├── .env 
├── README.md 
├── LICENSE 
└── .gitignore


## Getting Started

### Prerequisites

Ensure you have the following installed:
- Python 3.8 or higher
- Pip (Python package installer)
- Google Colab (for running the code, or you can run it locally)

### Installation

1. Clone the repository:

```bash
git clone https://github.com/yourusername/intelliroute.git
cd intelliroute
```

2. Install the required Python packages:

```bash
pip install -r requirements.txt
```

3. Set up your environment variables in the `.env` file or via Google Colab:

```bash
from google.colab import userdata
groq_api_key = userdata.get('groq_api_key')
os.environ["GROQ_API_KEY"] = groq_api_key
```

Replace the placeholder with your actual API keys.

## Running the Application
1. Ensure your `.env` file is properly configured with your Groq API key.

2. Run the Python script:
```bash
python app.py
```
3. Alternatively, you can run the project in Google Colab:
- Set up the environment variables in Google Colab as described above.
- Run the cells in the notebook sequentially.
-IntelliRoute will prompt you to enter user input, route the question to the appropriate tool (vector store or Wikipedia), and generate responses accordingly.

## Example Usage
- Input a question related to agents, prompt engineering, or adversarial attacks to see results from the vector store.
- Input a general question to see results from Wikipedia.

## Integration Details

-`LangGraph`: Manages the state and graph-based flow control, ensuring that each question is routed to the most relevant data source.
- `Groq API`: Provides high-performance NLP capabilities using the Gemma2-9b-It model.
- `AstraDB`: Hosts the vector store, allowing for efficient retrieval of specialized documents.
- `Wikipedia & Arxiv`: Integrated for answering general knowledge questions, providing users with a broad range of information.

## Files

- `app.py`: The main Python script that drives the IntelliRoute system, including API integrations, state management, and query routing.
- `requirements.txt`: Lists all the Python dependencies needed to run IntelliRoute.
- `.env`: Contains the API keys for Groq and other services. This file should not be included in version control.
- `README.md`: This file, providing an overview of the IntelliRoute project.
- `LICENSE`: The project's license, specifying how others may use the code.
- `.gitignore`: Specifies files and directories that should be ignored by Git, such as the .env file and any other sensitive information.

## License
This project is licensed under the MIT License - see the `LICENSE` file for details.

## .gitignore
The following files are ignored in the version control:
```bash
.env
__pycache__/
*.pyc
*.pyo
*.pyd
```

## Contributing
Feel free to fork this repository and submit pull requests. For major changes, please open an issue first to discuss what you would like to change.

## Acknowledgments
- Thanks to LangGraph for providing the foundation for advanced state management and execution flow.
- Thanks to Groq for offering robust NLP tools and models.
- Thanks to AstraDB for powering the vector store with high efficiency.
- Thanks to Wikipedia and Arxiv for serving as comprehensive external knowledge bases.


