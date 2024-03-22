# Beyond Homeworld
## Chapter III: Cooking game

<p>After enjoying the four-room appartment and a deterministic investment game which cost our agent her life-saving (not really). She now works at a restaurant as a untrained cook. Firt step is to choose correct ingredients and how to do with it. In this setting, our Agent receives a task (a descriptive description of the dish) and must explore her way through trial and error to learn the correct way to prepare the meal.</p>

### The world
<p>The world is a tupple of $\mathcal{H,A,O,R}$. In a game, the Agent will be assign a state, which charaterised by the meal to be prepared. However, the state is partially observable to her, through a short description about the state, e.g., "I want rice which is prepared in frying pan and oil, side dish is boiled shrimp" refers to state h_i (<b>rice-fried-shrimp-boiled</b>). For our problem, main dishes are rice, bread, noodle with 3 ways of preparation: steam, fry, bake. Side dishes consist of shrimp, chicken, vegie with three ways to serve: boil, fry, steam. Mathematically speaking, this map to3 to power of 4, hence or <b>hidden state space $\mathcal{H}$. </b></p>

<p><b>Observed information $\mathcal{O}$:</b> as said is a codomain that related to our hidden state domain with a many-to-one relation. For each of state $h_i \in \mathcal{H}$, there will be multiple description about the meal to be served. Each statement in Observed space mapping to a unique states (Note: this is not a classification problem). The hidden state- observed description is prepare in a synthetic way (e.g.,  string <i>2gdzb##*</i> means <i>"I want fried rice with fry veggie"</i> for no particular reason.)</p>

<p><b>Action space A:</b> after observe o_i, agent will choose ingredidents and what to do with them. This mean the action space is "equal" to the state space. (??)</p>

<p><b>Rewards:</b> reward is received at the end of the game only (no immediate reward) which make sense in this one-step only game. If our agent correctly prepare the meal, she will receive a reward of $+100$. For every meal that is half correct, main dish or side dish, the reward is $0$ while getting all incorrect is a negative reward of $-100$.</p>
