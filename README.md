# Beyond Homeworld
## Chapter III: Cooking Game

After enjoying the four-room apartment and a deterministic investment game, which cost our agent her life savings (not really), she now works at a restaurant as an untrained cook. The first step is to choose the correct ingredients and how to deal with them. In this setting, our Agent receives a task (a descriptive description of the dish) and must explore her way through trial and error to learn the correct way to prepare the meal.

### The World
The world is a tuple of `\( \mathcal{H, A, O, R} \)`. In a game, the Agent will be assigned a state, which is characterized by the meal to be prepared. However, the state is partially observable to her, through a short description about the state, e.g., "I want rice which is prepared in a frying pan and oil, the side dish is boiled shrimp" refers to state \( h_i \) (**rice-fried-shrimp-boiled**). For our problem, main dishes are rice, bread, noodle with 3 ways of preparation: steam, fry, bake. Side dishes consist of shrimp, chicken, veggie with three ways to serve: boil, fry, steam. Mathematically speaking, this maps to \( 3^4 \), hence our **hidden state space `\( \math
