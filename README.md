## Final-Year-Project

Automate internship discovery, evaluation, and reporting on Internshala using Playwright and ChatGPT.

## Features

- **Automate** browser interactions to log in, search, and scrape internship listings  
- **Extract** key details (title, company, stipend, deadline) and assemble structured data  
- **Analyze** your resume to tailor summaries and cover-letter snippets via ChatGPT  
- **Generate** a clean HTML report summarizing top matches  
- **Schedule** or email reports on demand  

## Prerequisites

- Python 3.9+  
- A valid Internshala account (email & password)  
- OpenAI API key  

## Installation

1. Clone this repo  
   ```bash
   git clone https://github.com/Vishwakant-coder/Final-Year-Project
   cd internshala-automation

2. Install dependencies
pip install -r requirements.txt

3. Install Playwright browsers
playwright install


## Configuration
Open config.py in the project root.

Replace the placeholder values:


INTERNSHALA_EMAIL = "your_internshala_email"
INTERNSHALA_PASSWORD = "your_internshala_password"
OPENAI_API_KEY      = "your_openai_api_key"
OUTPUT_DIR          = "reports"
(Optional) Tweak search keywords, filters or report filename in main.py.

## Project Structure
__main__.py
• Launches the tool as a module (python -m internshala_automation).

main.py
• Orchestrates browser setup, scraping flow and hands off data for analysis and reporting.

resume_handler.py
• Loads and parses your resume (PDF/DOCX) into plain text for prompt tailoring.

chat_gpt.py
• Wraps OpenAI’s API; crafts prompts to generate personalized summaries and cover-letter snippets.

generate_report.py
• Builds an HTML report (index.html) from scraped listings and AI-generated insights.

config.py
• Holds all hard-coded credentials and global settings.

## Usage
- Run interactively
python -m internshala_automation

- Run directly
python main.py
View report
Open reports/index.html in your browser after a successful run.

## Customize

Edit main.py to adjust search keywords, locations or stipend filters.
Modify generate_report.py to change HTML layout or add CSV export.
Tweak prompt templates in chat_gpt.py for different AI-generated outputs.

## Troubleshooting

Playwright errors: ensure playwright install ran without errors.
Login failures: verify your Internshala credentials in config.py.
API errors: confirm OPENAI_API_KEY in config.py matches your OpenAI dashboard.