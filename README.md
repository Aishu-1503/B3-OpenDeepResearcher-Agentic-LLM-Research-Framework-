# LLM Search Project

A Python application that combines OpenAI's GPT models with Zenserp web search API to provide intelligent, real-time answers to user questions by searching the web and synthesizing information.

## Features

- **Intelligent Query Generation**: Uses GPT-3.5-turbo to generate optimized search queries from user questions
- **Real-time Web Search**: Integrates with Zenserp API to fetch current web search results
- **AI-Powered Summarization**: Leverages OpenAI's language models to synthesize search results into comprehensive answers
- **Date-Aware Responses**: Includes current date context for time-sensitive queries
- **Error Handling**: Robust error handling for API failures and network issues

## How It Works

1. **Query Generation**: The user asks a question, and the app uses GPT-3.5-turbo to generate an optimized web search query
2. **Web Search**: The generated query is sent to Zenserp API to fetch relevant web search results
3. **Answer Synthesis**: GPT-3.5-turbo analyzes the search results and generates a comprehensive answer
4. **Response**: The synthesized answer is presented to the user with proper formatting

## Prerequisites

- Python 3.7 or higher
- OpenAI API key
- Zenserp API key

## Installation

1. **Clone the repository**:
   ```bash
   git clone <repository-url>
   cd LLM_search_proj
   ```

2. **Create a virtual environment**:
   ```bash
   python -m venv venv
   ```

3. **Activate the virtual environment**:
   - On Windows:
     ```bash
     venv\Scripts\activate
     ```
   - On macOS/Linux:
     ```bash
     source venv/bin/activate
     ```

4. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

## Configuration

1. **Create a `.env` file** in the project root directory:
   ```env
   OPENAI_API_KEY=your_openai_api_key_here
   ZENSERP_API_KEY=your_zenserp_api_key_here
   ```

2. **Get API Keys**:
   - **OpenAI API Key**: Sign up at [OpenAI Platform](https://platform.openai.com/) and generate an API key
   - **Zenserp API Key**: Sign up at [Zenserp](https://zenserp.com/) and get your API key

## Usage

1. **Run the application**:
   ```bash
   python llm_tavily_search_app.py
   ```

2. **Ask questions**: The app will prompt you to ask any question. Examples:
   - "What are the latest developments in artificial intelligence?"
   - "How to cook pasta carbonara?"
   - "What's the weather like today?"
   - "Tell me about the stock market trends"

3. **View results**: The app will:
   - Generate an optimized search query
   - Fetch relevant web results
   - Provide a synthesized answer based on the search results

## Dependencies

The project uses the following Python packages:

- `openai` - OpenAI API client for GPT models
- `requests` - HTTP library for API calls
- `python-dotenv` - Environment variable management
- `httpx` - Modern HTTP client
- `pydantic` - Data validation
- `tavily` - Alternative search API (installed but not used in current implementation)

## Project Structure

```
LLM_search_proj/
├── llm_tavily_search_app.py    # Main application file
├── venv/                       # Virtual environment
├── .env                        # Environment variables (create this)
└── README.md                   # This file
```

## API Services Used

### OpenAI API
- **Model**: GPT-3.5-turbo
- **Usage**: Query generation and answer synthesis
- **Rate Limits**: Subject to OpenAI's usage policies

### Zenserp API
- **Service**: Web search results
- **Usage**: Fetching real-time web search data
- **Rate Limits**: Subject to your Zenserp plan

## Error Handling

The application includes comprehensive error handling for:
- API key validation
- Network connectivity issues
- API rate limiting
- Invalid responses
- Timeout errors

## Example Output

```
Welcome to LLM + Zenserp Web Search App!
Ask me anything: What are the latest AI developments in 2024?

🔍 Search query generated: AI developments 2024 latest news breakthroughs

🧠 Answer:
Based on the latest search results, here are some key AI developments in 2024...
[Comprehensive answer based on web search results]
```

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## License

This project is open source. Please check the license file for more details.

## Troubleshooting

### Common Issues

1. **API Key Errors**: Ensure your `.env` file contains valid API keys
2. **Network Issues**: Check your internet connection and API service status
3. **Rate Limiting**: Wait before making additional requests if you hit rate limits
4. **Module Not Found**: Ensure you've activated the virtual environment and installed dependencies

### Getting Help

If you encounter issues:
1. Check the error messages in the console
2. Verify your API keys are correct
3. Ensure all dependencies are installed
4. Check your internet connection

## Future Enhancements

Potential improvements for this project:
- Support for multiple search engines
- Caching of search results
- Interactive conversation mode
- Web interface
- Search result filtering and ranking
- Support for different AI models
- Batch processing capabilities
