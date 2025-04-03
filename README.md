### LLM Workflow Implementation: From Basics to Advanced

This project demonstrates various LLM (Large Language Model) workflows designed to transform blog content into summaries, social media posts, and email newsletters. The implemented workflows include:

-Pipeline Workflow: A structured approach where tasks are executed sequentially.
-Workflow with Reflexion: A self-improving workflow that enhances content quality through iterative refinement.
-Agent-Driven Workflow: A flexible approach where an LLM agent determines the task execution order.
-Workflow Comparison: Analyzes and contrasts different workflow strategies based on performance and output quality.

### Table of Contents

1.Prerequisites
2.Setup Guide
3.Executing the Script
4.Workflow Breakdown
5.Evaluating Workflows

### Prerequisites

Before running the script, make sure you have the following:
-Python 3.10+: The script requires Python version 3.10 or later.
-OpenAI API Key: Needed to interact with OpenAI's API.
-Required Libraries:
    1. openai: For API integration with OpenAI models.
    2. python-dotenv: To manage environment variables using a .env file.
    3. requests: For handling HTTP requests (included in Python by default).

### To install the required dependencies, run:

pip install openai python-dotenv

### Setup Guide

Clone the repository
git clone https://github.com/your-username/llm-workflow-assignment.git
cd llm-workflow-assignment

### Create a .env file

Inside the project directory, create a .env file and add the necessary API credentials:
API_KEY=your_openai_api_key
BASE_URL=https://api.openai.com/v1
LLM_MODEL=gpt-4
MODEL_SERVER=OPENAI

### Replace your_openai_api_key with your actual API key.

Provide a Sample Blog Post
Save a blog post as sample-blog-post.json in the project directory. Example format:

{
  "title": "The Impact of Artificial Intelligence on Modern Healthcare",
  "content": "Artificial intelligence (AI) is revolutionizing the healthcare industry...",
  "author": "Dr. Sarah Johnson",
  "date_published": "2025-03-10",
  "tags": ["healthcare", "artificial intelligence", "technology", "medicine"]
}

### Executing the Script
Run the script using the command:

python llm_workflow.py

### What Happens During Execution
1. The script reads the blog post from sample-blog-post.json.

2. It processes the content using three different workflows:

    -Pipeline Workflow: Generates a summary, social media content, and an email newsletter in a sequential manner.

    -Workflow with Reflexion: Enhances content by applying a self-correction mechanism.

    -Agent-Driven Workflow: Uses an LLM agent to determine the task execution order dynamically.

3. The final outputs from each workflow are displayed in JSON format.

### Workflow Breakdown
1. Pipeline Workflow
Steps:

    -Extract key points from the blog post.

    -Generate a concise summary.

    -Create social media posts for platforms like Twitter, LinkedIn, and Facebook.

    -Compose an email newsletter.

Output: A JSON object containing the summary, social media posts, and newsletter content.

2. Workflow with Reflexion
Steps:

    -Extract key points with an iterative self-correction mechanism.

    -Generate an enhanced summary.

    -Improve social media post generation with feedback loops.

    -Refine the email newsletter content.

    -Output: A JSON object with the improved summary, social media posts, and newsletter.

3. Agent-Driven Workflow
Steps:

    -The LLM agent determines the order of execution dynamically.

    -Tasks include extracting key points, generating a summary, creating social media posts, and composing an email newsletter.

Output: A JSON object with the processed content or an error message in case of failure.

### Evaluating Workflows
To analyze the performance of different workflow approaches, run:

python llm_workflow.py

### Comparison Metrics
    -Quality Score: Measures the effectiveness of each workflow.

    -Execution Time: Assesses processing efficiency.

    -Best Approach Recommendation: Identifies the most suitable workflow based on different content requirements.

### Displayed Results
    -A comparative ranking of the workflows.

    -Strengths and limitations of each approach.

    -Recommendations on the best workflow for summaries, social media posts, and email content.