# News Summarization & Sentiment Analysis with Hindi TTS

## Overview

This project provides news summarization and sentiment analysis, enhanced with Hindi text-to-speech (TTS) functionality. It fetches news articles for a given company, summarizes them, analyzes the sentiment, and provides the summaries in Hindi audio.

## Features

-   **News Fetching:** Retrieves news articles from the NewsAPI based on a company name.
-   **Summarization:** Generates concise summaries of the fetched articles.
-   **Sentiment Analysis:** Analyzes the sentiment of the articles (Positive, Negative, or Neutral).
-   **Hindi Translation:** Translates the English summaries into Hindi.
-   **Text-to-Speech (TTS):** Converts the Hindi summaries into audio files, allowing users to listen to the news summaries.
-   **Comparative Analysis:** Provides a comparative analysis of the sentiment distribution across articles.
-   **Streamlit UI:** Offers a user-friendly interface to input company names and view the analysis results.

## Getting Started

### Prerequisites

-   Python 3.6+
-   pip (Python package installer)
-   A NewsAPI key (You can obtain one from [NewsAPI](https://newsapi.org/))

### Installation

1.  **Clone the repository:**

    
    git clone 
    cd 
    

    Replace `` with the actual URL of your GitHub repository and `` with the name of the cloned directory.

2.  **Create a virtual environment (recommended):**

    
    python -m venv venv
    source venv/bin/activate  # On Linux/macOS
    venv\Scripts\activate  # On Windows
    

3.  **Install dependencies:**

    
    pip install -r requirements.txt
    

### Configuration

1.  **Set the NewsAPI Key:**
    *   In the `api.py` file, replace `"bf5d8ff575214d8f8e70888191b83d63"` with your actual NewsAPI key.

### Usage

1.  **Run the Flask API:**

    
    python api.py
    

    This will start the Flask API server. By default, it runs on `http://127.0.0.1:5000`.

2.  **Run the Streamlit App:**

    
    streamlit run app.py
    

    This will open the Streamlit app in your web browser.

3.  **Using the App:**

    *   Enter a company name in the text input field.
    *   Click the "Analyze News" button.
    *   The app will display the news articles, their summaries, sentiment analysis, and Hindi audio for each summary.  It will also provide a comparative analysis and a final sentiment summary with audio.

### Project Structure


news-sentiment-analysis/
├── api.py          # Flask API for handling requests and processing data
├── app.py          # Streamlit UI for user interaction
├── utils.py        # Utility functions for fetching news, summarizing, sentiment analysis, etc.
├── requirements.txt  # List of Python dependencies
├── README.md       # This file
└── venv/           # (Optional) Virtual environment directory


### Dependencies

-   `Flask==2.2.3`
-   `requests==2.28.2`
-   `beautifulsoup4==4.12.2`
-   `textblob==0.17.1`
-   `gTTS==2.3.2`
-   `streamlit==1.26.0`
-   `googletrans==4.0.0-rc1`

### API Endpoints

-   `/` : Welcome message.
-   `/analyze` (POST): Analyzes news for a given company.  Requires a JSON payload with a `"company"` field.

    Example:

    
    {
        "company": "Apple"
    }
    

### Contributing

Contributions are welcome! Feel free to fork the repository, make changes, and submit pull requests.

### License

[Specify the license here, e.g., MIT License]

### Acknowledgements

-   This project uses the [NewsAPI](https://newsapi.org/) for fetching news articles.
-   Sentiment analysis is performed using [TextBlob](https://textblob.readthedocs.io/en/dev/).
-   Hindi translation is done using [googletrans](https://pypi.org/project/googletrans/).
-   Text-to-speech functionality is provided by [gTTS](https://gtts.readthedocs.io/en/latest/).
-   The user interface is built with [Streamlit](https://streamlit.io/).


Citations:
[1] https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/58026210/4dbb6cc7-8bf8-4405-b686-27581f575e31/requirements.txt
[2] https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/58026210/f71f61fc-652d-491f-96f4-74bbce4603c9/api.py
[3] https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/58026210/0bc7a756-1581-42c3-bb07-c18bcfedaa68/app.py
[4] https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/58026210/9b4b6bf2-a0c5-408d-bd1b-b006c1c28936/utils.py
