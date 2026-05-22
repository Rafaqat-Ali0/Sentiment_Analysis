# Sentiment Analysis

A powerful web-based sentiment analysis tool that extracts and analyzes customer reviews from Amazon and Flipkart to provide valuable insights into product sentiment.

## Overview

This application leverages natural language processing (NLP) to automatically classify product reviews as positive, negative, neutral, or special sentiments like sarcasm and excitement. The tool scrapes reviews from major e-commerce platforms and performs comprehensive sentiment analysis with detailed metrics including polarity and subjectivity scores.

## Features

- **Multi-Platform Support**: Analyze reviews from Amazon and Flipkart
- **Advanced Sentiment Detection**: Classify sentiments including:
  - Positive 😊
  - Negative 😠
  - Neutral 😐
  - Sarcasm 😏
  - Excitement 🎉
- **Sentiment Metrics**: Get polarity and subjectivity scores for each review
- **Aggregated Insights**: View average polarity and subjectivity across all analyzed reviews
- **Robust Web Scraping**: Intelligent HTML parsing with fallback mechanisms for dynamic content
- **User-Friendly Interface**: Clean, responsive web interface for easy interaction

## Technology Stack

- **Backend**: Flask 2.3.3
- **Web Scraping**: BeautifulSoup 4, Requests, Playwright
- **NLP**: TextBlob 0.17.1
- **Frontend**: HTML, CSS, JavaScript

## Installation

### Prerequisites
- Python 3.8 or higher
- pip (Python package manager)

### Setup Steps

1. Clone the repository:
   ```bash
   git clone https://github.com/ChaithanyaKasturi-20/Sentiment-Analysis.git
   cd Sentiment-Analysis
   ```

2. Create a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Usage

1. Start the Flask development server:
   ```bash
   python app.py
   ```

2. Open your web browser and navigate to:
   ```
   http://localhost:5000
   ```

3. Enter an Amazon or Flipkart product URL in the input field

4. Click "Analyze" to extract and analyze reviews

5. View the sentiment analysis results with polarity scores and sentiment classifications

## Project Structure

```
.
├── app.py                 # Flask application and core logic
├── requirements.txt       # Project dependencies
├── templates/
│   └── index.html        # Web interface
└── static/
    └── Emojis.jpg        # Background image
```

## API Endpoints

### POST /analyze
Analyzes reviews for a given product URL.

**Request:**
```json
{
  "url": "https://www.amazon.com/dp/ASIN"
}
```

**Response:**
```json
{
  "reviews": [
    {
      "review": "Great product!",
      "polarity": 0.7,
      "subjectivity": 0.6,
      "sentiment": "Positive 😊"
    }
  ],
  "average_polarity": 0.65,
  "average_subjectivity": 0.58
}
```

## Supported Domains

- Amazon (amazon.com, smile.amazon.com, etc.)
- Flipkart (flipkart.com)

## Limitations

- Review extraction depends on website structure and may be affected by page layout changes
- Some e-commerce sites may block automated scraping
- Sentiment analysis is based on keyword matching and general NLP patterns

## Future Enhancements

- Support for additional e-commerce platforms
- Machine learning models for improved sentiment accuracy
- Multi-language sentiment analysis
- Historical trend analysis
- Review comparison features

## Contributing

Contributions are welcome! Feel free to submit issues or pull requests to improve the project.

## License

This project is open source and available under the MIT License.

## Author

[ChaithanyaKasturi-20](https://github.com/ChaithanyaKasturi-20)
