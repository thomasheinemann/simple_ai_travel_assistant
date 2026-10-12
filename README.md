# AgentsVille Trip Planner

This project is a Jupyter notebook-based AI travel assistant that plans a trip to the fictional city of AgentsVille. The notebook walks through building a travel-planning agent using LLM prompting patterns, structured data validation, weather/activity context, and iterative feedback loops.

## Project goal

The goal is to create an AI system that can:

- model a vacation with traveler preferences, dates, destination, and budget
- review weather and activity data for the trip window
- generate a day-by-day itinerary tailored to the travelers' interests
- evaluate the quality of the plan against constraints
- revise the itinerary using a ReAct-style workflow with tool calls
- produce a polished final travel recommendation

## What is included

- a Jupyter notebook for the full trip-planning workflow
- helper utilities in `project_lib.py`
- dependencies for OpenAI, Pydantic, pandas, and notebook execution
- a simulated travel dataset and activity/weather context for the fictional city

## Project structure

simple_ai_travel_assistant/
├── project_starter.ipynb   # Main notebook with the assignment and implementation steps
├── project_lib.py          # Shared helper classes and utilities
├── requirements.txt        # Python dependencies
├── environment.yml         # Conda environment definition
├── README.md               # Project documentation
└── .env                    # Optional local environment file for API keys


## Main concepts covered

This notebook demonstrates several agent design techniques:

- Role-based prompting
- Chain-of-thought style itinerary generation
- Structured validation with Pydantic
- Tool-based planning and evaluation
- ReAct reasoning: Thought -> Action -> Observation
- Feedback-driven revision of the final itinerary

## Setup

### 1. Create and activate a Python environment

Using Conda:

```bash
conda env create -f environment.yml
conda activate env_simple_ai_travel_assistant
```

Or install the requirements directly:

```bash
pip install -r requirements.txt
```

### 2. Configure your API key

Create a `.env` file in the project root or export the key in your shell:

```bash
OPENAI_API_KEY=your_key_here
```

The notebook uses the OpenAI client to generate and evaluate the travel plan.

## Run the project

Open the notebook and run the cells in order:

```bash
jupyter notebook project_starter.ipynb
```

Or use Jupyter Lab:

```bash
jupyter lab
```

Then open `project_starter.ipynb` and execute the cells from the beginning.

## Example workflow

The notebook typically does the following:

1. defines vacation details such as destination, dates, budget, and traveler interests
2. loads mock weather and activity data for AgentsVille
3. validates the vacation data using Pydantic models
4. creates an itinerary agent that plans a trip for each day
5. evaluates the itinerary for correctness and quality
6. implements tool-based revision logic to improve the plan
7. outputs a final, polished travel recommendation

## Notes

- This is an educational project stemming from a udacity assignment (in the framework of the course "Agentic AI") and uses simulated/mock travel data.
- It is designed to help learn how LLM agents can reason about structured planning tasks.
- You can customize the traveler profiles, dates, interests, and budget for different scenarios.

## License

This project is provided for learning purposes as part of the course exercise. Please check the repository license files for any additional usage terms.
