# HW-Verif-Agent

## Overview

A Python-based LLM agent that autonomously generates Verilog testbenches, compiles them with Icarus Verilog, and iteratively refines them using compiler feedback, RAG, and Skills-based context management.

## Setup

```bash
# 1. Install dependencies
pip install -r requirements.txt

# 2. Install Icarus Verilog
# brew install icarus-verilog   # macOS
sudo apt install iverilog   # Ubuntu

# 3. Configure API keys
cp .env-default .env
# Edit config/.env with your keys (For now, free option is Google AI Studio)

# 4. Run the agent on the test module 1
python main.py test=1

# or if you are using a virtual environment

./venv/bin/python main.py test=1
```

**Skills** are loaded on-demand into the LLM context (not all at once in the system prompt). This is the primary context management approach.