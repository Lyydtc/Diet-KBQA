## Notes: 

For this task, we start off with 9640 foods as can be found in the `food_tagging.csv` file from the work done for previous papers. There are 2 main goals: 

1. Removing non-recommendable foods & reducing the total number of foods that are included in the Q&A benchmark creation process. This increases the quality and reduces the quantity of foods.

2. Creating a manageable set of questions & answers from all the possible combinations of user & food. Currently, we have 2819 users (2413 opioid users & 406 recovered users), together with 9640 foods, the total number of possible combinations of user-food pairs is 27M. Suppose that we can reduce the number of foods, we still need to do substantial filtering to make sure the final Q&A benchmark is only around 1000-5000 pairs.
