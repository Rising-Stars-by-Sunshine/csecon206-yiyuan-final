# Tree vs. Crop
## Project information
- **Author**: [Yiyuan][Qin], [Data Science], [2023], Duke Kunshan University
- **Instructor**: Prof. Luyao Zhang, Duke Kunshan University
- **Disclaimer**: Submissions to the Final Project for [COMPSCI/ECON 206 Computational Microeconomics, 2023 Spring (Seven Week - Second)](https://ce.pubpub.org/) instructed by Prof. Luyao Zhang at Duke Kunshan University.
- **Acknowledgments**: [How to Acknowledge?](https://www.scribbr.co.uk/thesis-dissertation/acknowledgements/)
[notes: please include all professors, students, and staff who have contributed to your completetion of the project.]
- **Project Summary**: 
  - [Summarize the Background/Motivation]
This research builds upon the integration of game theory to analyze the relationship between the environment and the economy. It recognizes that traditional approaches often overlook the complex interactions and trade-offs between these domains. By considering the environment and the economy as interdependent systems, game theory provides a framework to understand the strategic behavior of stakeholders and their decision-making processes. However, existing game theory literature often assumes perfect rationality and neglects the influence of psychological and social factors on decision-making. This research aims to address this gap by incorporating psychological and social factors into the analysis and considering the evolving preferences of individuals towards the coexistence of economic development and environmental sustainability. It intends to provide insights into decision-making processes, inform policy development, and promote a more holistic understanding of the environment-economy dynamics.
 
  - [Research Questions]
 This research aims to answer questions regarding individuals' decision-making processes and strategies in balancing the environment and the economy within the proposed game concept. It seeks to understand how psychological and social factors influence decision-making, the extent to which these factors impact individuals' choices, and how the integration of game theory, environmental science, and economics enhances our understanding of the environment-economy relationship. The research also addresses the importance of incorporating psychological and social factors in decision-making models, as well as the limitations and potential challenges associated with this approach. By exploring these questions, the study contributes to a more comprehensive understanding of decision-making in the context of the environment and the economy, informing policy development and resource management strategies that achieve a sustainable balance between these domains.

  - [Application Scenario]
  The proposed game concept is applicable in various scenarios, including rural development, sustainable resource management, policy development and decision-making, and environmental education and awareness. It provides insights into individual decision-making and strategies in balancing the environment and the economy. By incorporating psychological and social factors, the game concept offers a more realistic representation of how individuals prioritize their decisions based on values, beliefs, and personal motivations. This allows for a nuanced understanding of decision-making processes in real-world contexts. The game concept can inform policy development, resource management strategies, and educational initiatives by highlighting the trade-offs and synergies between economic and environmental outcomes. It offers a practical tool for analyzing decision-making and guiding sustainable development efforts in various domains.
  - [Methodology]
  The methodology for this research involves the definition of factors, simulation, benchmarking, and model building.
The factors considered in the research include psychological factors (risk aversion, environmental concerns, time preference, and altruism) and social factors (education and awareness, social norms, competitive pressure, and collaboration/cooperation). These factors are defined based on their influence on decision-making processes in the context of the environment and the economy.
In the simulation, each player is assigned a unique value for each factor, ranging from 0 to 1, representing their preferences and inclinations towards economic or environmental outcomes. These values are used to calculate an aggregated preference score, represented by the variable alpha. The alpha value determines the probability of a player's preference towards the economy or the environment.
A benchmark is established by creating a rational equilibrium model where players randomly choose strategies without the influence of external factors. This benchmark allows for a comparison between the proposed model and the rational equilibrium model to understand how the inclusion of psychological and social factors affects decision-making.
The model-building phase involves formulating the objective for each player, which is to maximize their overall payoff, considering both economic and environmental benefits. The objective function incorporates the alpha value, the player's choice of strategy (tree or crop), and the corresponding economic and environmental benefits associated with each choice. The objective is then solved using the PULP optimization library, which formulates the problem as a linear programming model.

  - [Results]
  The proposed solution concept in this research differs from existing solutions by incorporating psychological and social factors, considering multiple objectives, and accounting for evolving preferences. It provides a more comprehensive and realistic representation of decision-making processes in the context of the environment and the economy. The model advances strategic thinking by capturing the complexities and nuances of individual decision-making, exploring strategies that balance economic and environmental outcomes, and aligning with changing societal values and environmental awareness.
However, there are several limitations to the model. Firstly, it simplifies decision-making processes by reducing the factors to predefined psychological and social factors, potentially overlooking other influential factors. Secondly, its applicability and generalizability may be limited to specific contexts and populations, requiring adaptation and validation for different settings. Thirdly, the model assumes static decision-making processes without considering dynamic interactions or the opportunity for players to revise their strategies. Fourthly, it neglects individual heterogeneity by assuming that all players have the same predefined factors. Additionally, the model relies on simplified payoff calculations and lacks real-time feedback, which may not capture the complexities of economic and environmental outcomes or players' learning processes.
Addressing these limitations is crucial to enhance the model's applicability, accuracy, and usefulness in understanding decision-making processes in the context of the environment and the economy. Future studies can expand the factors considered, incorporate dynamic elements into the model, account for individual heterogeneity, refine the payoff calculations, and introduce real-time feedback mechanisms. By addressing these limitations, the model can provide more realistic and nuanced insights into decision-making processes, leading to more effective strategies and policies that achieve a sustainable balance between the environment and the economy.




  - [Intellectual Merits and Practical impacts of your project.]
  From an intellectual standpoint, this research contributes to the understanding of decision-making processes by incorporating psychological and social factors into the analysis. By exploring the interplay between individual preferences, values, and external influences, the research provides insights into the complexities and nuances of decision-making in real-world contexts. It advances strategic thinking by considering multiple objectives and recognizing the evolving preferences towards a balance between the environment and the economy. The research also opens avenues for further investigations, inspiring researchers to explore the applicability of the proposed game concept in specific contexts, delve into the impact of additional factors, study the dynamics of decision-making over time, and assess the effects of external factors and policy interventions.
In terms of practical impacts, the research can be applied to solve real-world issues related to sustainable land use, resource management, policy development, sustainable urban development, corporate sustainability, environmental education, and natural resource management. By applying the insights from the research, decision-makers can make more informed choices, develop strategies, and implement interventions that promote environmental sustainability while considering economic development. This can lead to more effective land management practices, the design of sustainable policies and incentives, the creation of greener and more resilient cities, the adoption of sustainable practices in corporate settings, the promotion of environmental education and awareness, and the implementation of sustainable resource management strategies.
The research findings can drive positive change by providing decision-makers with a holistic understanding of the environment-economy nexus and guiding them toward more sustainable practices and policies. The research's application scenarios span various sectors and contexts, allowing stakeholders to address specific challenges and work towards a more balanced and resilient future.
This research has both intellectual merits and practical impacts. It advances the understanding of decision-making processes, inspires further research, and can be applied to solve real-world issues in diverse fields related to the environment and the economy. By incorporating psychological and social factors, considering multiple objectives, and accounting for evolving preferences, the research provides valuable insights and guidance for decision-makers striving to achieve a sustainable balance between the environment and the economy.



## Table of Contents

- model
- code
- spotlight
- more about the author
- references

### Model
- Game Environment

The game rule is shown below: Each player has the choice to plant either a tree or a crop on their land. Trees provide an environmental benefit by absorbing carbon dioxide, but they take longer to mature and provide less immediate economic benefit. Crops provide an economic benefit by being able to be sold for profit, but they do not provide any environmental benefit. Players must choose whether to plant a tree or a crop on their land, and their choice is kept secret until all players have made their choice. Once all players have made their choice, the environmental benefit of the trees is calculated based on the number of trees planted by all players, and the economic benefit of the crops is calculated based on the number of crops planted by all players.
The objective is to maximize the total environmental benefit for all players and to maximize players' own economic benefit. 
The table below shows the strategies and payoff of the game. 
<img src = "https://github.com/Rising-Stars-by-Sunshine/csecon206-yiyuan-final/blob/main/model/payoff.png" width = 80%, height=80%><br/> 

- Solution Concept
<img src = "https://github.com/Rising-Stars-by-Sunshine/csecon206-yiyuan-final/blob/main/model/solution.png" width = 80%, height=80%><br/> 
- Evaluations: e.g. efficiency and fairness
	- Efficiency:
	The new solution concept has several strengths that contribute to its efficiency. Firstly, it aims to maximize both economic and environmental benefits, recognizing the interdependence of these objectives. By considering both objectives as multiple outcomes, decision-makers can allocate resources in a way that optimizes the overall benefits in both domains. This approach promotes efficiency by avoiding extreme prioritization of one objective at the expense of the other.
	Additionally, the solution concept takes into account the trade-offs between economic and environmental outcomes. By explicitly acknowledging these trade-offs, decision-makers can make informed choices that balance the costs and benefits associated with different strategies. This consideration of trade-offs contributes to efficient resource allocation and decision-making processes.
	However, it's important to note that the solution concept relies on simplified payoff calculations, which may limit its ability to capture the full complexity of economic and environmental outcomes. The simplicity of the model's calculations may impact the accuracy of the efficiency in resource allocation. To enhance the efficiency of the solution, there is an opportunity to incorporate more sophisticated modeling techniques and real-world data to improve the accuracy of payoff calculations and better capture the complexities of economic and environmental outcomes.
	- Fairness:
	The new solution concept also has strengths that contribute to fairness. By incorporating social factors such as social norms and collaboration/cooperation, the concept aims to consider the interests and values of different stakeholders. This consideration of social factors promotes fairness by aligning decision-making processes with societal expectations and fostering cooperation among stakeholders.
	Moreover, the solution concept seeks to balance the interests of different stakeholders by maximizing both economic and environmental benefits. By integrating economic and environmental objectives, the concept aims to achieve a fair distribution of benefits and costs, avoiding extreme prioritization of one domain over the other. This balance contributes to fairness in decision-making processes.
	However, it's important to recognize that the predefined set of social factors in the solution concept may oversimplify the complexities of fairness considerations. Fairness is a multifaceted concept influenced by various factors such as distributional equity, procedural fairness, and intergenerational fairness. The limited set of social factors may not fully capture all dimensions of fairness, which could impact the concept's ability to address individual fairness concerns and cater to the diverse needs and perspectives of stakeholders.
	To enhance fairness, there is an opportunity to incorporate more comprehensive fairness considerations into the solution concept. This could involve expanding the set of social factors, engaging stakeholders in decision-making processes, and ensuring transparency, inclusivity, and accountability in the allocation of resources and decision-making procedures.
	
	
### Code
All the code is in the Colab link: https://drive.google.com/file/d/1chEmmTIPqgKKVTw-nGptDnl5qzRL7byP/view?usp=sharing


### Spotlight
- Posters
- Figures
- Slides
- Presentations
- Review articles
- Media appearance

### More about the Author
- headshot
- self-introduction
- Final reflections 
  - intellectual growth
  - professional growth
  - living a purposeful life

### References

- Literature References in [Chicago Author-Date](https://www.chicagomanualofstyle.org/tools_citationguide/citation-guide-2.html) Style and [BibTex](https://scholar.google.com/) 

Levin, Dan, and Luyao Zhang. 2020. “Bridging Level-K to Nash Equilibrium.” *The Review of Economics and Statistics* 104 (6): 1329–40. https://doi.org/10.1162/rest_a_00990.
[](https://www.plant-ecology.com/article/2015/1005-264X/1005-264x-39-2-140.shtml)

```
@article{HuHaiqing2015LesserKhinganMountains,
  title={Biomass carbon density and carbon sequestration capacity of seven typical forest types in Lesser Khingan Mountains},
  author={Hu Haiqing, Luo Bizhen, Wei Shujing, Wei Shuwei , Sun Long, Rossheng, Ma Hongbin},
  journal={Journal of Plant Ecology},
  volume={39},
  number={2},
  pages={140--158},
  year={2015}
}
```

