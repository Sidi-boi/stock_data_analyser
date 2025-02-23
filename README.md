# Stock Data Analysis

## Overview
This project provides a Python-based stock data analysis tool that fetches historical stock data from Yahoo Finance, processes it, and generates a summary using either OpenAI's GPT-4 or a locally hosted LLM (Ollama). The goal is to help investors and analysts understand stock trends over a three-year period.

## Features
- **Fetch historical stock data** from Yahoo Finance (up to three years).
- **Parse HTML data** using BeautifulSoup.
- **Generate AI-driven analysis** of stock performance.
- **Summarize trends and calculate total returns** over the specified period.
- **Supports OpenAI API and local Ollama LLM** for processing.

## Installation
### Prerequisites
Ensure you have the following installed:
- Python 3.8+
- Pip
- Virtual Environment (optional but recommended)
- Docker (if using Ollama)

### Setup
1. **Clone the repository**
   ```sh
   git clone https://github.com/yourusername/stock-data-analysis.git
   cd stock-data-analysis
   ```
2. **Create a virtual environment (optional)**
   ```sh
   python -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   ```
3. **Install dependencies**
   ```sh
   pip install -r requirements.txt
   ```
4. **Set up API keys**
   - Create a `.env` file in the root directory and add your OpenAI API key:
     ```sh
     OPENAI_API_KEY=your_openai_api_key_here
     ```

## Usage
### Using OpenAI API
Run the following command in a Jupyter Notebook or script:
```python
from stock_analysis import display_analysis

display_analysis("GOOG")
```
This will fetch Google (GOOG) stock data and generate an AI-powered summary.

### Using Ollama (Local LLM)
1. **Ensure Ollama is installed** and running on your system:
   ```sh
   ollama pull llama3.2
   ```
2. **Run the script**:
   ```python
   from stock_analysis import analyse_stock_trends_ollama

   analyse_stock_trends_ollama("GOOG")
   ```

## API Configuration
This project supports two AI models:
- **OpenAI GPT-4 API** (default)
- **Ollama (Llama3.2)** (local processing)

Modify the script to switch between OpenAI and Ollama based on your preferences.

## Contributing
1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Commit your changes (`git commit -m 'Add new feature'`).
4. Push to the branch (`git push origin feature-branch`).
5. Open a pull request.


## Acknowledgments
- [Yahoo Finance](https://finance.yahoo.com/) for stock data.
- [OpenAI](https://openai.com/) for AI-powered analysis.
- [Ollama](https://ollama.ai/) for local LLM support.

