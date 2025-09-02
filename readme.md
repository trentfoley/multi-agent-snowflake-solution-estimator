# CrewAI Multi-Agent Snowflake Solution Estimator

A multi-agent AI system built with CrewAI that provides automated Snowflake solution architecture and cost estimation. This demo showcases how multiple AI agents can collaborate to deliver comprehensive technical solutions.

## Overview

This project demonstrates a multi-agent workflow where two specialized AI agents work together:

1. **Snowflake Architect Agent**: Designs comprehensive solution architectures for specific topics
2. **Cost Management Analyst Agent**: Provides detailed cost estimates based on the proposed architecture

The agents collaborate to deliver end-to-end solutions, from architectural design to cost analysis, using Snowflake's pay-as-you-go pricing model.

## Features

- 🤖 **Multi-Agent Collaboration**: Two specialized agents working in sequence
- 🏗️ **Solution Architecture**: Automated design of Snowflake components and features
- 💰 **Cost Estimation**: Detailed monthly cost breakdowns by component
- 📊 **Markdown Reports**: Clean, formatted output for easy consumption
- 🔧 **Configurable Topics**: Easy to modify for different solution domains

## Prerequisites

- Python 3.8 or higher
- Google Gemini API key

## Installation

1. **Clone the repository**:
   ```bash
   git clone <repository-url>
   cd crewAI-multi-agent-demo
   ```

2. **Install required Python packages**:
   ```bash
   pip install crewai crewai-tools langchain_community
   ```

3. **Set up environment variables**:
   Create a `.env` file in the project root and add your Gemini API key:
   ```
   GEMINI_API_KEY=your_gemini_api_key_here
   ```

   **Important**: Replace `your_gemini_api_key_here` with your actual Gemini API key. You can obtain one from [Google AI Studio](https://makersuite.google.com/app/apikey).

## Usage

1. **Open the Jupyter notebook**:
   ```bash
   jupyter notebook snowflake-solution-estimator.ipynb
   ```

2. **Run the cells sequentially**:
   - The notebook will install dependencies if needed
   - Configure the LLM with Gemini
   - Create the specialized agents
   - Define tasks for architecture and cost estimation
   - Execute the crew workflow

3. **Customize the topic**:
   Modify the topic in the final cell to analyze different solutions:
   ```python
   result = crew.kickoff(inputs={"topic": "Your Custom Topic Here"})
   ```

## Example Output

The system generates comprehensive reports including:

- **Solution Architecture**: Detailed list of Snowflake components, warehouses, and task schedules
- **Cost Breakdown**: Monthly cost estimates broken down by:
  - Warehouse compute costs
  - Storage costs
  - AI services costs
  - Other Snowflake services

## Configuration

### Modifying Agents

You can customize the agents by editing their roles, goals, and backstories in the notebook:

- **Architect Agent**: Modify the `role`, `goal`, and `backstory` to focus on different architectural aspects
- **Analyst Agent**: Adjust the cost estimation parameters and methodology

### Changing Topics

The system is designed to work with any topic. Simply change the `topic` parameter in the `crew.kickoff()` call to analyze different solutions.

## Project Structure

```
crewAI-multi-agent-demo/
├── readme.md                           # This file
├── snowflake-solution-estimator.ipynb  # Main Jupyter notebook
└── .env                                # Environment variables (create this)
```

## Dependencies

- **crewai**: Multi-agent framework for AI collaboration
- **crewai-tools**: Additional tools and utilities for CrewAI
- **langchain_community**: Community integrations for LangChain
- **jupyter**: For running the notebook interface

## Troubleshooting

### Common Issues

1. **API Key Error**: Ensure your `.env` file is in the project root and contains a valid `GEMINI_API_KEY`
2. **Import Errors**: Make sure all dependencies are installed using the pip command above
3. **Notebook Issues**: Ensure Jupyter is installed and running properly

### Getting Help

If you encounter issues:
1. Check that all dependencies are properly installed
2. Verify your Gemini API key is valid and has sufficient quota
3. Ensure the `.env` file is in the correct location

## Contributing

Feel free to submit issues, feature requests, or pull requests to improve this demo.

## License

This project is open source and available under the [MIT License](LICENSE).
