# Requirements

## Functional requirements (what the system must DO)
1. The system will permit the user to enter any food item left over, along with its estimated quantity and shelf life in days.
2. The system will determine whether the entered ingredients violate any safety threshold defined by the pre-LLM food safety rule engine.
3. The system will formulate the LLM prompt such that leftover ingredients with an expiry period of less than 48 hours get the top priority.
4. The system will generate the recipes exclusively using the ingredients entered by the user and basic pantry ingredients.
5. The system will provide a repurposed meal recipe in the form of the recipe name, estimated preparation time, and cooking steps.
6. The system will also present the urgency rating and waste reduction advice for every generated recipe in accordance with the chosen ingredients.

## Non-functional requirements (how the system must PERFORM)
1. This process should take no more than 5.0 seconds for the completion of the entire process.
2. The system should facilitate first-time users to input their leftover food items and obtain a recipe within 3 steps or less.
3. The system should be able to parse successfully over 95% of the structured recipe output from the LLM API into JSON.
4. The repurposed recipes that will be generated must show at least a 30% reduction in preparation steps relative to regular from-scratch recipes.
