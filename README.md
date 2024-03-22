# Beyond Homeworld
## Chapter III: Cooking game

After enjoying the four-room apartment and a deterministic investment game which cost our agent her life savings (not really), she now works at a restaurant as an untrained cook. The first step is to choose the correct ingredients and how to deal with them. In this setting, our Agent receives a task (a descriptive description of the dish) and must explore her way through trial and error to learn the correct way to prepare the meal.

### The world
The world is a tuple of \( \mathcal{H, A, O, R} \). In a game, the Agent will be assigned a state, which is characterized by the meal to be prepared. However, the state is partially observable to her, through a short description about the state, e.g., "I want rice which is prepared in a frying pan and oil, the side dish is boiled shrimp" refers to state \( h_i \) (**rice-fried-shrimp-boiled**). For our problem, main dishes are rice, bread, noodle with 3 ways of preparation: steam, fry, bake. Side dishes consist of shrimp, chicken, vegie with three ways to serve: boil, fry, steam. Mathematically speaking, this maps to \( 3^4 \), hence our **hidden state space \( \mathcal{H} \)**.

**Observed information \( \mathcal{O} \)**: as said is a codomain that relates to our hidden state domain with a many-to-one relation. For each state \( h_i \in \mathcal{H} \), there will be multiple descriptions about the meal to be served. Each statement in the Observed space mapping to a unique state (Note: this is not a classification problem). The hidden state-observed description is prepared in a synthetic way (e.g., string "2gdzb##*" means "I want fried rice with fry veggie" for no particular reason.)

**Action space \( \mathcal{A} \)**: after observing \( o_i \), the agent will choose ingredients and what to do with them. This means the action space is "equal" to the state space. (??)

**Rewards**: the reward is received at the end of the game only (no immediate reward) which makes sense in this one-step only game. If our agent correctly prepares the meal, she will receive a reward of \( +100 \). For every meal that is half correct, main dish or side dish, the reward is \( 0 \) while getting all incorrect is a negative reward of \( -100 \).
