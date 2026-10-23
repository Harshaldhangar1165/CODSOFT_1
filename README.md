# CodBot — Expanded Rule-Based Chatbot
### CodSoft Artificial Intelligence Internship · Task 1

CodBot is a command-line chatbot built with Python. It uses predefined responses, regular expressions, and a small typo-tolerant fallback to answer a wider range of common questions.

## Features

- Greetings, small talk, identity, capabilities, and help
- Thanks, apologies, mood support, jokes, fun facts, and motivation
- Study tips
- Introductory explanations of Python, variables, functions, algorithms, AI, machine learning, deep learning, NLP, chatbots, databases, Git, GitHub, APIs, neural networks, overfitting, data science, and plagiarism
- Current local date and time
- Unknown-question fallback that suggests supported prompts
- Basic typo tolerance for common short words
- Automated unit tests
- No third-party dependencies

## Requirements

Python 3.9 or newer. No `pip install` step is required.

## Run

```bash
python chatbot.py
```

Type `help` for example questions. Type `bye`, `goodbye`, `exit`, or `quit` to end the session.

## Run tests

```bash
python -m unittest -v
```

## Example prompts

```text
Hello!
What can you do?
What is Python?
Explain AI.
What is the difference between AI and machine learning?
What is overfitting?
Tell me a joke.
Motivate me.
Give me study tips.
What time is it?
What is today's date?
bye
```

## How it works

1. Normalizes the message by trimming and collapsing whitespace, then converts it to lowercase.
2. Checks the message against an ordered list of regular-expression rules.
3. Returns one of the predefined responses for the first matching rule. Date and time responses are generated at runtime.
4. Uses a conservative fuzzy match for common short words if no rule matches.
5. Returns a helpful fallback if no rule matches.

## Important limitation

CodBot is still a **rule-based** chatbot, not a generative AI system. It does not understand every question, learn from conversations, or verify factual answers online. It can only answer patterns covered by its rules. The typo-tolerant fallback is intentionally limited.

## Project structure

```text
CODSOFT_TASK1/
├── chatbot.py
├── test_chatbot.py
├── README.md
├── requirements.txt
└── .gitignore
```
