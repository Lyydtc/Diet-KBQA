## Notes: 

For this task, we start off with 9640 foods as can be found in the `food_tagging.csv` file from the work done for previous papers. There are 2 main goals: 

1. Removing non-recommendable foods & reducing the total number of foods that are included in the Q&A benchmark creation process. This increases the quality and reduces the quantity of foods.

2. Creating a manageable set of questions & answers from all the possible combinations of user & food. Currently, we have 2819 users (2413 opioid users & 406 recovered users), together with 9640 foods, the total number of possible combinations of user-food pairs is 27M. Suppose that we can reduce the number of foods, we still need to do substantial filtering to make sure the final Q&A benchmark is only around 1000-5000 pairs.

### Task 1: 

There are many ways we can potentially reduce the number of foods to only keep highly recommendable & relevant items. Below are the 3 approaches I experimented with - they are not meant to be the final approach as we have discussed and come up with potential alternatives/additions to these approaches: 

* 1. Using the food name and make API calls to food.com to find a relevant recipe card. This approach didn't work because if we use the food_desc field directly to search on food.com, most of the time, we won't be able to find a recipe card with an exact match, hence error code 200. Question: can we somehow simplify the food name, or extract the semantic meaning of the food name before looking up on food.com to have successful lookups?
 
* 2. Same approach as 1 but looking up on allrecipes.com. Jason suggested that we should try to use food.com instead as it's linked to FNDDS data with nutrition info.
 
* 3. Creating a food evaluation agent with Autogen. We give it some instructions on the types of foods that should not be recommended, then prompt the agent to judge if a food is recommendable or not. In the end, this approach resulted in a reduction to 7.5k food items. This is still a substantial number of foods so we can either finetune our instructions to the agent and have a round of human review with manual filtering conditions to reduce the size of the foods list even more.

### Task 2: 

More details about my initial approach for this task can be found under the section Task 2: Constructing the Q&A in the Benchmark Construction file for now. I will update the readme soon as this step is in a very early draft version. 
