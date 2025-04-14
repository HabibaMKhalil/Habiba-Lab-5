# LLM Workflow Implementation: From Basics to Advanced

This project demonstrates various LLM (Large Language Model) workflows designed to transform blog content into summaries, social media posts, and email newsletters. The implemented workflows include:

- **Pipeline Workflow**: A structured approach where tasks are executed sequentially.  
- **Workflow with Reflexion**: A self-improving workflow that enhances content quality through iterative refinement.  
- **Agent-Driven Workflow**: A flexible approach where an LLM agent determines the task execution order.  
- **Workflow Comparison**: Analyzes and contrasts different workflow strategies based on performance and output quality.

---

## Table of Contents
1. [Prerequisites](#prerequisites)  
2. [Setup Guide](#setup-guide)  
3. [Executing the Script](#executing-the-script)  
4. [Workflow Breakdown](#workflow-breakdown)  
5. [Evaluating Workflows](#evaluating-workflows)  

---

## Prerequisites
Before running the script, ensure you have:  
- **Python 3.10+**: The script requires Python version 3.10 or later.  
- **OpenAI API Key**: Needed to interact with OpenAI's API.  
- **Required Libraries**:  
  ```bash
  pip install openai python-dotenv
  ```
1. openai: For API integration with OpenAI models.
2. python-dotenv: To manage environment variables.
3. requests: For HTTP requests (included in Python by default).

--- 

## Setup Guide
Clone the repository:

```bash
git clone https://github.com/your-username/llm-workflow-assignment.git
cd llm-workflow-assignment
```

---

## Create a .env file:
Add the following to .env:
```ini
API_KEY=your_openai_api_key
BASE_URL=https://api.openai.com/v1
LLM_MODEL=gpt-4
MODEL_SERVER=OPENAI
```
- Replace your_openai_api_key with your actual API key.

--- 
## Provide a Sample Blog Post:
Save a blog post as sample-blog-post.json in the project directory:


{                         
  "title": "The Impact of Artificial Intelligence on Modern Healthcare",                               
  "content": "Artificial intelligence (AI) is revolutionizing the healthcare industry...",                             
  "author": "Dr. Sarah Johnson",
  "date_published": "2025-03-10",
  "tags": ["healthcare", "artificial intelligence", "technology", "medicine"]
}

--- 

## Executing the Script
Run the script:
```bash
python llm_workflow.py
```

## What Happens During Execution?
- Reads the blog post from sample-blog-post.json.
- Processes content using three workflows:
- Pipeline Workflow: Sequential generation of summary, social media posts, and newsletter.
- Workflow with Reflexion: Self-correcting iterative refinement.
- Agent-Driven Workflow: Dynamic task execution by an LLM agent.
- Displays final outputs in JSON format.

## Workflow Breakdown
1. Pipeline Workflow
Steps:
-Extract key points → Generate summary → Create social media posts → Compose newsletter.
- Output: JSON with summary, social posts, and newsletter.

2. Workflow with Reflexion
Steps:
-Extract key points with self-correction → Enhance summary → Improve social posts → Refine newsletter.
-Output: JSON with improved content.

3. Agent-Driven Workflow
Steps:
-LLM agent dynamically orders tasks (key points, summary, social posts, newsletter).
-Output: JSON with processed content or error message.

--- 

## Evaluating Workflows
Run the script to compare workflows:

```bash
python llm_workflow.py
```


## Comparison Metrics
- Quality Score: Effectiveness of each workflow.
- Execution Time: Processing efficiency.

## Best Approach Recommendation: Optimal workflow for different content types.

## Displayed Results
- Comparative ranking of workflows.
- Strengths and limitations.
- Recommendations for summaries, social posts, and emails.
