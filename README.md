### Capstone Preview: College to NBA Player Performance Prediction
[Link to Jupyter Notebook](https://github.com/d-veli/college_to_nba_preview/blob/main/college_to_nba_preview.ipynb)

**Author: Dave Li**

#### Executive summary
A player's college basketball performance does not always translate to NBA performance due to a variety of factors (ie. change in rules, play styles, level of competition, usage). This work aims to improve on the status quo by applying machine learning to more accurately predict whether or not a given college player will be performant in the NBA.

#### Rationale
**Why should anyone care about this question?**
From a business perspective, NBA drafts have been notorious crapshoots where it is not uncommon for players drafted from college to end up underperforming their expected value. This a huge waste of organizational investment in terms of time and money, not to mention the opportunity cost of a better replacement player. Thus, being able to determine a college player's likelihood of being performant in the NBA becomes a valuable tool for teams when investing in new talent direct from college. 


#### Research Question
**What are you trying to answer?**
To be explicit then, our research question and data mining objective is to make use of machine learning so that NBA prospects coming out of college can be more accurately assessed on their likelihood to be performant in the big leagues. 

#### Data Sources
**What data will you use to answer you question?**

[College Basketball 2009-2021 + NBA Advanced Stats](https://www.kaggle.com/datasets/adityak2003/college-basketball-players-20092021)
- **Description**: Contains college statistics from 2009-2021 + advanced NBA stats from 2014-2022. 
- **Rationale**: This source will provide the college performance data to be used as the independent variables.

[20 Years of NBA Draft Data](https://www.kaggle.com/datasets/benwieland/nba-draft-data)
- **Description**: NBA statistics for every pick, along with NCAA stat page links for data scraping. 
- **Rationale**: This source will provide the list of college players who were drafted into the NBA. This will be the primary source on which the college statistics will be merged against. Additionally, the NBA statistics cover the length of each players career to date which will be used as inputs to our dependent variable.

#### Methodology
**What methods are you using to answer the question?** The methodologies used include:
- **Data Preparation:** Pandas and Numpy to join data sources and manage data quality
- **Data Exploration:** Seaborn and Matplotlib to visualize relationships
- **ML Modeling:** Sklearn to preprocess, transform, and search for optimal classfication models

#### Results
**What did your research find?**
In the intial research we defined a performant player as one who lasted at least three years in the league, had positive WS/48 (Win shares), and positive VORP (Value Above Replacement Player). Using this definition as our target class, the logistic regression model indicated the following:

High importance to being performant
- Points over replacement per adjusted game
- Adjusted defensive rating
- Stops
- Part of Pac-10 Conference
- Defensive points over replacement per adjusted game

Low importance to being performant
- Part of Big Ten Conference
- Minutes Played
- Points
- Went to Syracuse
- Last year was Senior

This should be taken with a grain of salt, as none of the models explored (albiet with limited hyperparameter coverage at this point in time) has test accuracy performance beyond 60% (depsite training accuracy reaching 73%). This will be an area to improve upon in the subsequent round of research.

#### Next steps
**What suggestions do you have for next steps?** As identified, the as-is results leave something to be desired. In the next iteration, possible areas of exploration include:
1. Inclusion of additional features such as
    - Player vitals (ie. weight, wingspan, college injuries)
    - Expanded college statistics (ie. multi-year, additional advanced stats)
2. Reframing the problem differently (ie. regression - predicting VORP)
3. Acquire primary data to improve data quality
4. Inclusion of international players
5. Inclusion of undrafted college players that made it into NBA


#### Outline of project

- [College to NBA Capstone Preview - Jupyter Notebook](https://github.com/d-veli/college_to_nba_preview/blob/main/college_to_nba_preview.ipynb)


#### Contact and Further Information