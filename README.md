# Post Pilot

A Claude Code project for automated LinkedIn post generation using specialized subagents.

## Getting Started

### Prerequisites

- [Claude Code](https://claude.ai/code) installed and configured
- Terminal access

### Usage

1. Start Claude Code in the project directory:
   ```bash
   claude
   ```

2. Run the LinkedIn post generation command:
   ```bash
   /linkedin
   ```

3. Follow the interactive prompts:
   - Provide your LinkedIn post topic
   - The system will automatically:
     - Research the topic using the `linkedin-researcher` subagent
     - Write the post using the `linkedin-writer` subagent  
     - Recommend an image using the `linkedin-image` subagent

### Output

The `/linkedin` command provides:
- A complete LinkedIn post ready for publishing
- Relevant research links and sources
- A description of the recommended image

### Project Structure

```
.claude/
├── agents/           # Specialized subagent definitions
├── commands/         # Custom slash commands
└── settings.local.json
```

## How It Works

The LinkedIn command orchestrates three specialized subagents:

1. **linkedin-researcher** - Conducts web research on the specified topic
2. **linkedin-writer** - Creates engaging LinkedIn content based on research
3. **linkedin-image** - Recommends appropriate visual content

Each subagent operates with its own context and specialized tools, enabling parallel processing and domain expertise.