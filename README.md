# ReAct Agent with Dynamic Replanning

## 📌 Project Overview

This project demonstrates the implementation of a **ReAct (Reason + Act) Agent** using Python. The agent follows a reasoning-and-action-based approach to solve a real-world planning problem.

The objective is to plan a **2-night student trip from Pune to Goa within a budget of ₹9,000**.

The agent follows a continuous cycle of:
- **Thought:** Analyzes the current situation and decides what to do next.
- **Action:** Selects and executes an appropriate tool.
- **Observation:** Evaluates the result returned by the tool.
- **Replanning:** Modifies its plan whenever an assumption fails or a constraint is not satisfied.

## 🎯 Objectives

- Understand the working of the ReAct agent architecture.
- Implement the Thought → Action → Observation cycle.
- Demonstrate tool usage through Python functions.
- Handle unexpected situations through dynamic replanning.
- Verify budget constraints before generating the final itinerary.

## ⚙️ Technologies Used

- Python 3
- Jupyter Notebook
- Rule-Based Reasoning
- ReAct Agent Architecture

## 🧠 Agent Architecture

The agent uses a structured workflow:

1. **Initial Planning:** Creates a sequence of tasks for the trip.
2. **Transport Search:** Checks train availability first. If unavailable, it switches to a bus or flight.
3. **Weather Checking:** Checks the weather conditions in Goa.
4. **Accommodation Search:** Initially considers a beach resort and switches to a hostel if the budget is exceeded.
5. **Budget Verification:** Calculates the total estimated cost.
6. **Dynamic Replanning:** Revisits previous tasks whenever constraints are not satisfied.
7. **Final Output:** Generates the trip itinerary after successful budget verification.

## 🛠️ Tools Implemented

| Tool | Purpose |
|---|---|
| `search_transport()` | Checks train, bus, and flight availability and prices. |
| `check_weather()` | Checks simulated weather conditions in Goa. |
| `find_stay()` | Searches for accommodation options. |
| `compute_total()` | Calculates the total trip cost and checks the budget. |

## 🔄 ReAct Workflow

The agent follows this execution pattern:

**Thought → Action → Observation → Replanning (if required) → Final Answer**

For example:
- Thought: Try the train as the first transport option.
- Action: Search for train availability.
- Observation: Train is sold out.
- Replanning: Switch to the bus.
- Action: Search for bus availability.
- Observation: Bus is available at ₹1,400 each way.

The same approach is used for accommodation and budget verification.

## 💰 Budget Details

| Expense | Estimated Cost |
|---|---:|
| Bus (Round Trip) | ₹2,800 |
| Hostel (2 Nights) | ₹2,400 |
| Food and Local Transport | ₹1,000 |
| **Total** | **₹6,200** |
| Maximum Budget | ₹9,000 |

The agent selects the hostel after evaluating the resort option and verifies that the final estimated cost is within the specified budget.

## ▶️ How to Run

1. Clone the repository:

   ```bash
   git clone YOUR_GITHUB_REPOSITORY_URL
   ```

2. Navigate to the project folder:

   ```bash
   cd YOUR_PROJECT_FOLDER
   ```

3. Install Jupyter Notebook if required:

   ```bash
   pip install notebook
   ```

4. Open Jupyter Notebook:

   ```bash
   jupyter notebook
   ```

5. Open `ReAct_Agent.ipynb`.

6. Run all cells to execute the agent and observe its reasoning, actions, observations, and replanning process.

## 📂 Project Structure

```text
ReAct-Agent/
│
└── ReAct_Agent.ipynb
│
└── README.md
```

## 📌 Key Learning Outcomes

- Understanding the ReAct architecture.
- Learning how AI agents interact with external tools.
- Implementing decision-making using Python.
- Handling failures and changing plans dynamically.
- Understanding how agents work towards a goal while respecting constraints.

## ⚠️ Limitations

- The reasoning mechanism is rule-based rather than powered by an LLM.
- Transport, accommodation, and weather information are simulated.
- Prices and availability are predefined and do not represent real-time booking information.
- The project demonstrates a basic ReAct workflow and can be extended using an LLM and real-world APIs.

## 🚀 Future Enhancements

- Integrate an LLM for dynamic reasoning.
- Connect real travel and weather APIs.
- Add multiple destination options.
- Include user preferences such as travel dates and number of travellers.
- Implement memory to retain previous observations and decisions.

## 👨‍💻 Author

Developed as part of an academic assignment on **AI Agents and Agentic AI By Jayesh**, demonstrating the ReAct architecture with dynamic replanning using Python.
