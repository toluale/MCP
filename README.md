# MCP Paper Analysis System

Model Context Protocol (MCP) implementation for academic paper research and analysis using the Anthropic Claude API and ArXiv integration.

## Overview

This on-going project demonstrates the implementation of the Model Context Protocol (MCP) to create an intelligent paper analysis system that can:
- Search for academic papers on ArXiv
- Extract and analyze paper content
- Generate comprehensive summaries
- Provide comparative topic analysis
- Save analysis results to files

## Features

### 🔍 **Paper Search & Management**
- Search ArXiv database by topic
- Automatically organize papers by topic
- Store paper metadata (title, authors, abstract, publication date)
- Generate unique paper IDs for easy reference

### 📊 **Advanced Analysis**
- **Comprehensive Paper Summaries**: Extract key information including:
  - Abstract and problem statement
  - Methodology and frameworks used
  - Existing solutions and their limitations
  - Proposed improvements and innovations
  - Experimental results and findings
  - Key contributions and limitations

- **Topic-Based Analysis**: Comparative analysis across multiple papers including:
  - Common themes and research trends
  - Methodological approaches comparison
  - Research gaps identification
  - Practical applications assessment

### **Data Persistence**
- Save summaries and analyses to formatted text files
- Organized file structure with timestamps
- Support for both basic and comprehensive summary formats

### **Interactive Chat Interface**
- Natural language queries
- Tool-based response system
- Real-time paper analysis
- Conversational interface for research assistance

## Project Structure

```
claude_mcp/
├── mcp_tutorial.ipynb          # Main notebook with MCP implementation
├── papers/                     # Paper storage directory
│   ├── machine_learning/       # Topic-based subdirectories
│   │   └── papers_info.json   # Paper metadata
│   └── [other_topics]/
├── summaries/                  # Generated analysis files
│   ├── [paper_id]_comprehensive_summary.txt
│   ├── [paper_id]_basic_info.txt
│   └── [topic]_topic_analysis.txt
└── README.md                   # This file
```

## Installation

1. **Clone the repository**:
   ```bash
   git clone [repository-url]
   cd claude_mcp
   ```

2. **Install required packages**:
   ```bash
   pip install arxiv anthropic python-dotenv PyPDF2 requests
   ```

3. **Set up API credentials**:
   - Create a `.env` file in the project root
   - Add your Anthropic API key:
     ```
     ANTHROPIC_API_KEY=your_api_key_here
     ```
   - Or directly edit the `ANTHROPIC_API_KEY` variable in the notebook **NOT ADVISABLE**

## Usage

### Getting Started

1. **Open the Jupyter notebook**:
   ```bash
   jupyter notebook mcp_tutorial.ipynb
   ```

2. **Execute the setup cells** to import libraries and initialize the system

3. **Start the chat interface** by running the `chat_loop()` function

### Available Tools

The system provides six main tools accessible through natural language queries:

| Tool | Description | Example Query |
|------|-------------|---------------|
| `search_papers` | Search ArXiv for papers on a topic | "Search for papers about machine learning" |
| `extract_info` | Get basic paper information | "Get info for paper 1909.03550v1" |
| `summarize_paper` | Generate comprehensive analysis | "Summarize paper 1909.03550v1" |
| `analyze_papers_by_topic` | Compare papers in a topic | "Analyze machine learning papers" |
| `save_summary_to_file` | Save paper analysis to file | "Save summary of paper XYZ to file" |
| `save_topic_analysis_to_file` | Save topic analysis to file | "Save machine learning analysis to file" |

### Example Queries

```
Query: Search for papers about deep learning
Query: What are the key findings in paper 2106.09685v2?
Query: Analyze all papers on natural language processing
Query: Save comprehensive summary of paper 1909.03550v1
Query: Compare methodologies in computer vision papers
```

## Dependencies

- `arxiv`: ArXiv API integration
- `anthropic`: Claude API client
- `PyPDF2`: PDF text extraction
- `requests`: HTTP requests for PDF download
- `python-dotenv`: Environment variable management
- `json`: Data serialization
- `os`: File system operations

