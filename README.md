# 🚀 CrewAI Framework – Structured Learning Notes

**CrewAI** is a multi-agent orchestration framework designed to coordinate multiple AI agents working together toward a common goal. It enables complex workflows through structured collaboration between agents.

---

## 🧩 Core Components

- **Agents** – Virtual team members with specific roles, goals, and tools.
- **Tasks** – Specific jobs assigned to agents.
- **Processes** – Defines how agents and tasks are structured and executed.

---

## 👤 CrewAI Agent Characteristics

Each agent in CrewAI has:
- **Role** – Defines the function (e.g., Researcher, Coder, Reviewer).
- **Goal** – Describes the agent's objective in the crew.
- **Tools** – Functional capabilities (e.g., web search, calculator).
- **Backstory** – Provides contextual background for better LLM alignment.
- **Memory** – Maintains context across interactions.
- **Language Model** – Powers the agent's understanding and responses.

> Agents are essentially **virtual team members** capable of autonomous decision-making within defined constraints.

---

## 🔄 Process Types in CrewAI

1. **Sequential Process**  
   Linear execution: Output of one agent becomes the input to the next.

2. **Hierarchical Process**  
   A **Manager Agent** oversees and delegates to subordinate agents.  
   Ideal for complex workflows requiring coordination and evaluation.

---

## 🧠 Agent Types in CrewAI

| Type                | Description                                                                 |
|---------------------|------------------------------------------------------------------------------|
| Task-Specific Agent | Expert in a specific task (e.g., summarization, coding).                    |
| General-Purpose     | Versatile, can adapt to a range of tasks.                                  |
| Coordinator Agent   | Acts as a project manager—allocates and monitors tasks.                    |
| Learning Agent      | Improves over time using feedback and historical data.                     |
| Reactive Agent      | Provides fast, rule-based responses.                                        |
| Deliberative Agent  | Maintains internal state and plans based on goals and environment.         |

---

## 🛠️ Tools vs. Tasks

- **Tools**: Capabilities agents use to accomplish tasks (e.g., browser, Python REPL).
- **Tasks**: Jobs assigned to agents (e.g., write a report, generate a summary).

---

## ⚙️ Implementation Workflow

### 1. Install Required Modules

```python
from crewai import Agent, Task, Crew, Process
from crewai_tools import SerperDevTool
