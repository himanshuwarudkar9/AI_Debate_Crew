# AI Debate Crew

Welcome to the AI Debate Crew project, powered by [crewAI](https://crewai.com). This project features a multi-agent AI system where agents engage in structured debates on controversial topics, providing balanced perspectives through proposition, opposition, and final decision-making.

![new](https://github.com/user-attachments/assets/76649585-6b67-41aa-ad2f-29ac3d22e5f4)


## Project Overview

This debate system uses three specialized AI agents to analyze and discuss complex topics:

- **Proposer Agent**: Presents compelling arguments in favor of the topic
- **Opposer Agent**: Provides counter-arguments and challenges the proposition
- **Decider Agent**: Analyzes both perspectives and provides a balanced conclusion

### Example Debate Topic

The project includes a complete debate on: **"AI will replace human creativity in the next decade"**

Output files are generated in the `output/` folder:
- `propose.md` - Arguments supporting AI replacing human creativity
- `oppose.md` - Arguments against AI replacing human creativity
- `decide.md` - Final analysis and balanced perspective

## Installation

Ensure you have Python >=3.10 <3.13 installed on your system. This project uses [UV](https://docs.astral.sh/uv/) for dependency management and package handling, offering a seamless setup and execution experience.

First, if you haven't already, install uv:

```bash
pip install uv
```

Next, navigate to your project directory and install the dependencies:

```bash
crewai install
```

### Configuration

**Add your API key into the `.env` file:**

```bash
MODEL=gemini/gemini-2.0-flash-exp
GEMINI_API_KEY=your_api_key_here
```

Supported models:
- Gemini (Free tier available)
- DeepSeek (Requires credits)
- Groq (Fast and free)
- OpenRouter (Multiple model options)

### Customizing

- Modify `src/debate/config/agents.yaml` to define your agents
- Modify `src/debate/config/tasks.yaml` to define your debate tasks
- Modify `src/debate/crew.py` to add your own logic, tools and specific args
- Modify `src/debate/main.py` to add custom debate topics

## Running the Project

To start a debate with your AI agents, run this from the root folder of your project:

```bash
crewai run
```

This command initializes the Debate Crew, where agents will:
1. Propose arguments for the topic
2. Oppose with counter-arguments
3. Provide a final balanced decision

The debate results will be saved in the `output/` folder as markdown files.

## Understanding Your Crew

The AI Debate Crew consists of three specialized agents:

1. **Proposer**: Builds strong arguments supporting the debate topic
2. **Opposer**: Challenges the proposition with logical counter-arguments
3. **Decider**: Synthesizes both perspectives into a balanced conclusion

Each agent has unique goals and capabilities defined in `config/agents.yaml`, and their tasks are orchestrated through `config/tasks.yaml`.

## Project Structure

```
debate/
├── src/debate/
│   ├── config/
│   │   ├── agents.yaml    # Agent definitions
│   │   └── tasks.yaml     # Task configurations
│   ├── crew.py            # Crew orchestration
│   └── main.py            # Entry point
├── output/                # Debate results
├── knowledge/             # User preferences and context
└── .env                   # API keys and configuration
```

## Support

For support, questions, or feedback regarding the AI Debate Crew or crewAI:
- Visit our [documentation](https://docs.crewai.com)
- Reach out through the [GitHub repository](https://github.com/joaomdmoura/crewai)
- [Join our Discord](https://discord.com/invite/X4JWnZnxPb)
- [Chat with our docs](https://chatg.pt/DWjSBZn)

## License

This project is built with crewAI framework.

---

Let's explore complex topics through the power of AI-driven debates! 🤖💭
