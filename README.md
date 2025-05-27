# Cryptoscope
MCA Major Project

# Cryptoscope - Explore the World of Cryptocurrency

## Introduction
This is a code repository. 
we will create a cryptocurrency app. We're going to use React and multiple APIs powered by https://rapidapi.com.

# Cryptoscope 🌐📈 - Cryptocurrency Price Prediction & Monitoring Platform

![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![Redux](https://img.shields.io/badge/Redux-593D88?style=for-the-badge&logo=redux&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Chart.js](https://img.shields.io/badge/Chart.js-FF6384?style=for-the-badge&logo=chartdotjs&logoColor=white)

A full-stack cryptocurrency analytics platform featuring AI-powered price predictions, real-time market data, and portfolio management tools.

## Table of Contents
- [Key Features](#key-features-)
- [Live Demo](#live-demo-)
- [Installation Guide](#installation-guide-)
- [Configuration](#configuration-)
- [API Setup](#api-setup-)
- [Running the Application](#running-the-application-)
- [Project Architecture](#project-architecture-)
- [Troubleshooting](#troubleshooting-)
- [Security](#security-considerations-)
- [License](#license-)

## Key Features 🚀

### 📊 Market Dashboard
- Real-time cryptocurrency prices and market caps
- Interactive historical price charts (1D, 1W, 1M, 1Y)
- Global market statistics and trends

### 🤖 AI Price Predictions
- Machine learning-powered price forecasting
- News sentiment analysis using NLP
- 7-day price trajectory predictions

### 🔔 Portfolio Management
- Personalized cryptocurrency watchlist
- Portfolio performance tracking
- Price alert notifications

### 📈 Comparison Tools
- Side-by-side cryptocurrency comparisons
- Market cap vs volume analysis
- Historical performance benchmarking

### 📰 News Aggregator
- Real-time cryptocurrency news
- Multi-source news integration
- Sentiment-categorized articles

## Live Demo 📱
Explore our live demo: [demo.cryptoscope.app](https://demo.cryptoscope.app)  
*(Replace with your actual demo URL when deployed)*

## Installation Guide 📦

### System Requirements
- Node.js v16+ [Download](https://nodejs.org/)
- Python 3.9+ [Download](https://www.python.org/)
- npm v8+ or Yarn v1.22+
- Git

### Clone Repository
```bash
git clone https://github.com/yourusername/cryptoscope.git
cd cryptoscope

Frontend Setup
npm install
# OR
yarn install

AI Backend Setup
pip install -r requirements.txt

### Configuration ⚙️
Create .env file in root directory with following variables:

Variable Name	Description	Example Value
REACT_APP_RAPIDAPI_KEY	RapidAPI master key	1234567890abcdef1234567890abcdef
REACT_APP_CRYPTO_API_URL	Coinranking API endpoint	https://coinranking1.p.rapidapi.com
REACT_APP_NEWS_API_KEY	News API access key	0987654321zyxwvu0987654321zyxwvu
REACT_APP_AI_API_URL	Local AI server URL	http://localhost:5000
REACT_APP_PORTFOLIO_API_URL	Portfolio service URL	http://localhost:5001
ESLINT_NO_DEV_ERRORS	Disable ESLint build errors	true
API Setup 🔑
1. Coinranking API
Create RapidAPI account

Subscribe to Coinranking API

Copy API key to REACT_APP_RAPIDAPI_KEY

Verify host in REACT_APP_CRYPTO_RAPIDAPI_HOST

2. Google News API
Subscribe to Google News API

Copy API key to REACT_APP_NEWS_API_KEY

Verify host in REACT_APP_NEWS_RAPIDAPI_HOST

Running the Application 💻
Development Mode
npm run dev  # Starts all services (Client + Server + AI)

Production Build

npm run build
serve -s build

Individual Services
Command	                       Description	                Port
node src/server/index.js	   Start React frontend	        3000
npm start	                   Launch Express server	    5001
python ai/prediction_model.py  Start AI prediction model	5000

Troubleshooting 🛠️
Common Issues

Missing Environment Variables

Error: process.env.REACT_APP_RAPIDAPI_KEY is undefined
Solution: Verify .env file exists in root directory with correct variables

AI Model Connection Issues
POST http://localhost:5000/predict 500 (Internal Server Error)
Resolution Steps:
# Check AI service status
curl http://localhost:5000/health

# Verify Python dependencies
pip list | grep -E 'flask|torch|transformers'

# Check model download
ls ~/.cache/huggingface/hub

OpenSSL Legacy Provider Error
Error: error:0308010C:digital envelope routines::unsupported
Fix:
export NODE_OPTIONS=--openssl-legacy-provider
# Add to package.json scripts:
"scripts": {
  "start": "react-scripts --openssl-legacy-provider start"
}

Security Considerations 🔒
Authentication
JSON Web Token (JWT) implementation

Secure HTTP-only cookies for session management

Password encryption using bcrypt

Data Protection
API rate limiting (100 requests/minute)

HTTPS enforcement for all API calls

Sensitive data encryption at rest

Best Practices
Never commit API keys to version control

Use environment variables for configuration

Regular dependency updates (npm audit, snyk test)

License 📄
MIT License - See LICENSE for full text.

Permissions
✅ Commercial Use
✅ Modification
✅ Distribution
✅ Private Use

Limitations
❌ Liability
❌ Warranty

Acknowledgements 🙏

Market data from Coinranking API

Financial news powered by Google News API

Machine learning models provided by Hugging Face

UI components from Ant Design

Support 💬
Report issues: GitHub Issues
