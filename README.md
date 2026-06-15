# AI-Powered Website Content Summarizer

## Overview

This project combines web scraping and Large Language Models (LLMs) to automatically extract and summarize website content. Using Python, BeautifulSoup, and the Llama 3.2 model via Ollama, the application retrieves webpage text, removes irrelevant elements, and generates concise summaries in Markdown format.

The project demonstrates how AI can be integrated with web scraping techniques to transform unstructured web content into readable insights.

---

## Features

- Scrapes webpage content from any public URL
- Removes irrelevant HTML elements such as:
  - Scripts
  - Styles
  - Images
  - Input fields
- Extracts webpage titles automatically
- Generates AI-powered summaries using Llama 3.2
- Formats responses in Markdown
- Supports summarization of announcements and news content

---

## Technologies Used

- Python
- BeautifulSoup (bs4)
- Requests
- Ollama
- Llama 3.2
- Markdown Rendering
- Prompt Engineering

---

## Project Workflow

1. User provides a website URL.
2. The application retrieves the webpage using HTTP requests.
3. BeautifulSoup parses the HTML content.
4. Unnecessary elements are removed.
5. Clean text is extracted from the webpage.
6. A structured prompt is sent to the Llama 3.2 model.
7. The model generates a concise Markdown summary.
8. The summary is displayed to the user.

---

## Example Input

```python
display_summary("https://ollama.com/")
```

## Example Output

```markdown
# Ollama Website Summary

## Overview

Ollama provides a platform for running and deploying open-source AI models locally and through cloud infrastructure. The platform simplifies the process of launching AI applications such as OpenClaw and other model-powered tools.

## Key Features

- Local deployment of open-source models
- Cloud infrastructure for larger AI workloads
- Subscription plans for advanced usage
- Integration with AI development tools

## Announcements

- OpenClaw support available through Ollama Launch
- Cloud-based scaling options for larger models
```

---

## Skills Demonstrated

- Web Scraping
- HTML Parsing
- Data Cleaning
- Large Language Model Integration
- Prompt Engineering
- Object-Oriented Programming
- API and Model Interaction
- Natural Language Processing (NLP)

---

## Challenges Encountered

### 1. Removing Website Noise

Webpages contain large amounts of navigation menus, footers, advertisements, and other non-essential content that can negatively impact summary quality.

**Solution:**  
HTML elements such as scripts, styles, images, and input fields were removed before sending content to the language model, significantly improving the relevance of generated summaries.

### 2. Handling Different Website Structures

Each website uses a unique HTML structure, making it difficult to reliably extract meaningful content using fixed selectors.

**Solution:**  
A generalized scraping approach using BeautifulSoup's text extraction methods was implemented to work across a wide range of websites.

### 3. Prompt Design and Summary Quality

Initial summaries often included navigation links and repeated website content instead of focusing on the main information.

**Solution:**  
A structured system prompt was created to instruct the model to ignore navigation-related text and focus on summarizing meaningful content.

### 4. Large Content Volumes

Some websites contain thousands of words, which can increase processing time and exceed model context limits.

**Solution:**  
Content cleaning and preprocessing were used to reduce unnecessary text before passing data to the model. Future improvements may include chunking and hierarchical summarization.

### 5. Model Performance Trade-offs

Balancing summary quality against inference speed required testing multiple local models.

**Solution:**  
Llama 3.2 was selected because it provided a good balance between response quality, speed, and local deployment efficiency.

---

## Key Learning Outcomes

Through this project, I gained experience in:

- Building end-to-end AI-powered applications
- Integrating local LLMs with Python workflows
- Web scraping and HTML preprocessing
- Designing effective prompts for summarization tasks
- Handling noisy real-world web data
- Working with locally hosted AI models using Ollama

---

## Future Improvements

- Multi-page website summarization
- PDF and document summarization support
- Automatic content chunking for long webpages
- Keyword extraction and sentiment analysis
- Interactive web interface using Streamlit
- Batch processing of multiple URLs

---

## Author

Developed as a learning project to explore the integration of web scraping techniques and Large Language Models for automated content summarization.
