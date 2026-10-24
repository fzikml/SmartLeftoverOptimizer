# Specialized Technology

## Concepts
For the purpose of this assignment, the specific technology selected is Large Language Models (LLMs), which would be used using the process of Prompt Engineering and Constraint-Based Reasoning. An LLM is a highly developed form of Artificial Intelligence, built from extremely large data sets of texts through neural networks called Transformers. In contrast to normal software, which uses query matching from databases or conditional (if-then) programming constructs, LLMs have the ability to understand context and generate responses.

In the Smart Leftovers Optimizer, the LLM is used as a zero-shot cooking reasoning model. It does not perform an exhaustive search for recipes from the database but takes an arbitrary combination of excess ingredients in the household and creates a cooking recipe for it.

## Key Concepts
- Zero-Shot Prompting and In-Context Learning: The capability of an LLM to engage in domain-specific reasoning for example cooking recipe generation under constraints on the fly without any need for model finetuning or custom training data.
- Persona of System & Prompt Engineering: Establishing guidelines for operations, role-based behaviour and safety constraints in the system prompt before feeding in user inputs into the model.
- Deep Neural Network Architecture of Transformer and Self-Attention: The basic neural network architecture which determines the semantic connections between words in a sequence.

## Worked Example
- React Frontend User Input: “2 grilled chicken thighs, half a red bell pepper, quarter onion, jasmine rice leftovers” (Servings: 3, Maximum Time: 20 min, Dietary Requirements: Halal).
- Back-end processing (FastAPI): Takes inputs, applies Halal guidelines and zero waste system guidelines, and requires JSON output.
- Reasoning for LLM (API Layer): Checks the safety of handling cooked poultry, computes the scaling of portions for 3 servings, selects pantry spices (garlic powder, soy sauce, vegetable oil), and formulates cooking instructions.
- Output Generation (React UI): Returns a validated JSON payload rendered onto the recipe interface.

## Frameworks, models, methods and tools
For the incorporation of LLMs in the Smart Leftover Optimizer, the following three major frameworks, models, approaches, and tools have been applied:
- OpenAI / Gemini Foundation Models
Description: Pre-trained Large Language Models based on the Transformer (e.g., GPT-4o / Gemini 1.5 Flash) trained on large text datasets via deep neural networks.

Function: The main engine that generates inference. It performs natural language understanding on the unstructured remaining input, does semantic ingredient pairing, calculates scaling factors based on number of servings, and dynamically generates cooking instructions.

- Prompt Engineering & System Persona Structuring
Description: An NLP technique for crafting system prompts, runtime context, and constraints that will help steer an LLM’s output without changing the underlying model weights.

Function: Ensures that operations remain within their boundaries, defines roles such as "Zero-Waste Culinary Assistant", food safety handling processes, and JSON schema formatting of the output during the execution of API requests.

- FastAPI with Pydantic
Description: An excellent python web framework (FastAPI) with a data validation package (Pydantic).

Function: Acts as middleware between the frontend UI in React and the external LLM API. It takes in ingredient input from users, checks whether the format of the payload is valid, handles the API authentication key, and makes sure that the JSON produced by the LLM is exactly in line with the frontend recipe schema.

## Fit to your problem
Fit to Problem: The traditional recipe app fails when there is some arbitrary collection of leftovers that the user owns since the application needs exact database tags. This problem is solved through the Smart Leftover Optimizer as it uses the LLM to reason semantically about combining arbitrary ingredients into a meal.

System Benefits: It has infinite recipe creation ability, needs minimal user effort (no manual scanning of barcodes/weights), deals with food waste behavior in the area (The Star, 2024), and has food safety instructions built right into the recipe preparation process (Svartebekk et al., 2025; van Rooijen et al., 2024).


