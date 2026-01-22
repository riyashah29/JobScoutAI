# Job Search Automation System

An intelligent job search automation system that leverages AI agents to streamline the federal job application process through the USAJobs API.

## Features

- **Automated Job Search**: Fetch relevant job postings from USAJobs API based on your criteria
- **AI-Powered Analysis**: Intelligent job description analysis to match your skills and experience
- **Resume Tailoring**: Automatically customize your resume for each position
- **Cover Letter Generation**: Create personalized cover letters aligned with job requirements
- **Application Tracking**: Comprehensive logging and tracking of all your applications
- **Streamlit Interface**: User-friendly web interface for easy interaction

## Project Structure

```
Job Search/
├── agents/
│   ├── jd_analyst.py           # Job description analysis agent
│   ├── messaging_agent.py      # Communication handling agent
│   └── resume_cl_agent.py      # Resume and cover letter generation agent
├── utils/
│   ├── config.py               # Configuration management
│   ├── tracking.py             # Application tracking utilities
│   └── .env                    # Environment variables (not tracked)
├── data/
│   ├── applications_log.csv    # Application history
│   ├── sample_resume.txt       # Base resume template
│   └── cover_letters/          # Generated cover letters
├── orchestrator.py             # Main workflow orchestration
├── streamlit_app.py            # Web interface
└── usajobs_api.py             # USAJobs API integration

```

## Prerequisites

- Python 3.8 or higher
- USAJobs API key
- Google Gemini API key

## Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd "Job Search"
```

2. Install required dependencies:
```bash
pip install -r requirements.txt
```

3. Set up environment variables:
Create a `.env` file in the `utils/` directory with the following:
```
USAJOBS_API_KEY=your_usajobs_api_key_here
GEMINI_API_KEY=your_gemini_api_key_here
```

## Usage

### Running the Streamlit App

```bash
streamlit run streamlit_app.py
```

### Using the Orchestrator

```python
python orchestrator.py
```

## Configuration

Edit `utils/config.py` to customize:
- Search criteria (keywords, location, salary range)
- AI model parameters
- Output preferences

## API Keys

### USAJobs API Key
1. Visit [USAJobs API](https://developer.usajobs.gov/APIRequest/Index)
2. Request an API key
3. Add it to your `.env` file

### Google Gemini API Key
1. Visit [Google AI Studio](https://makersuite.google.com/app/apikey)
2. Create an API key
3. Add it to your `.env` file

## Data Management

- **applications_log.csv**: Tracks all job applications with timestamps and status
- **cover_letters/**: Stores generated cover letters with job title and timestamp
- **sample_resume.txt**: Your base resume used for tailoring
