---
jupyter:
  kernelspec:
    display_name: Python 3 (ipykernel)
    language: python
    name: python3
  language_info:
    codemirror_mode:
      name: ipython
      version: 3
    file_extension: .py
    mimetype: text/x-python
    name: python
    nbconvert_exporter: python
    pygments_lexer: ipython3
    version: 3.10.14
  nbformat: 4
  nbformat_minor: 4
---

::: {.cell .markdown}
# Predicting League of Legends Match Length After 10 Minutes

**Name**: Elliot Baker

**Website Link**: <https://github.com/ejbaker00/LoL-Match-Analysis>
:::

::: {.cell .code execution_count="1" ExecuteTime="{\"end_time\":\"2019-10-31T23:36:28.652554Z\",\"start_time\":\"2019-10-31T23:36:27.180520Z\"}"}
``` python
import pandas as pd
import numpy as np

import plotly.express as px
pd.options.plotting.backend = 'plotly'

# from lec_utils import * # Feel free to uncomment and use this. It'll make your plotly graphs look like ours in lecture!
```
:::

::: {.cell .markdown}
## Introduction
:::

::: {.cell .markdown}
#### The Data

The dataset used in this analysis contains competitive League of Legends
(LoL) match data collected from 2014 to 2024. It provides detailed
information about matches, including game statistics, team compositions,
and outcomes. There are 994,200 rows, with each game corresponding to 12
rows (one for each of the 10 players in a game, and rows for each of the
teams), equaling 82,850 games represented. This analysis focuses on the
question:

How can statistics at the 10-minute mark predict the total duration of a
game?

#### Why This Matters

Game duration is a critical factor in League of Legends, as it reflects
the pacing and strategic flow of a match. Predicting game length based
on early-game statistics offers valuable insights into how initial
performance translates into long-term outcomes. This is particularly
relevant for players, coaches, and analysts aiming to refine early-game
strategies and optimize decision-making.

#### Relevant Columns

To address this research question, the following columns from the
dataset are particularly relevant:

-   gamelength: The lengh of a game, measured in seconds.
-   position: The position the player plays - top, jng (jungle), mid,
    bot (bottom), or sup (support). This can be used in conjunction with
    the other statistics to determine whether there is a difference in
    game time depending on which position has an early lead or early
    disadvantage. There is also a \'team\' position where the statistics
    for each player on a team are consolidated.
-   side: The side the team or player is playing on, red or blue. This
    can be used to determine whether the side of the team with a lead
    impacts the game time.
-   golddiffat10: The gold difference between each player and between
    the two teams at the 10-minute mark. This metric captures early game
    performance and the ability to establish a lead.
-   xpdiffat10: The experience difference between each player and
    between the two teams at the 10-minute mark. This indicates how well
    teams are farming and gaining levels.
-   killsat10: The total kills achieved by each player at the 10-minute
    mark. This reflects early aggression and skirmish success.
-   assistsat10: The total assists achieved by each player at the
    10-minute mark. This complements kill statistics by showing team
    coordination.
-   deathsat10: The total deaths each player has at the 10-minute mark.
    This shows which players are dying in the early game.
-   csdiffat10: The creep score difference at the 10-minute mark. This
    measures efficiency in farming resources during the early game.
:::

::: {.cell .markdown}
## Data Cleaning and Exploratory Data Analysis
:::

::: {.cell .markdown}
#### Data Cleaning

Since our analysis focuses on the 10-minute mark and match duration,
only rows with valid data for golddiffat10, xpdiffat10, killsat10,
assistsat10, deathsat10, csdiffat10, and gamelength were retained. Rows
with missing values in these critical columns were dropped, reducing
noise and ensuring robust predictions. Rows missing the gameid were also
dropped to ensure that data was accurately matched to the relevant game,
since each game is represented by 12 rows.

From the 161 columns, only those directly relevant to the research aim
were retained. These included gameid, golddiffat10, xpdiffat10,
killsat10, assistsat10, deathsat10, csdiffat10, gamelength, side, and
position. Excluding unrelated metrics reduced memory usage and
streamlined the analysis process.

The gamelength column was divided by 60 to obtain the game length in
minutes, as it\'s a more readily understandable metric.

The data cleaning steps ensured that the dataset was both reliable and
focused on the research question. By removing irrelevant and incomplete
data, we minimized noise and improved the quality of the insights
derived. Preserving the magnitude of numerical metrics allowed us to
maintain the interpretability of key features and their influence on
game duration. Filtering ensured computational efficiency while
maintaining the focus on the research aim.

These steps aligned with the data-generating process by addressing
typical inconsistencies and gaps in esports match data, such as missing
records. The resulting dataset offers a robust foundation for predictive
modeling and analysis, ensuring that findings are both accurate and
actionable.

#### Exploratory Data Analysis
:::

::: {.cell .code ExecuteTime="{\"end_time\":\"2019-10-31T23:36:28.657068Z\",\"start_time\":\"2019-10-31T23:36:28.654650Z\"}"}
``` python
```
:::

::: {.cell .markdown}
## Step 3: Framing a Prediction Problem
:::

::: {.cell .code ExecuteTime="{\"end_time\":\"2019-10-31T23:36:28.657068Z\",\"start_time\":\"2019-10-31T23:36:28.654650Z\"}"}
``` python
# TODO
```
:::

::: {.cell .markdown}
## Step 4: Baseline Model
:::

::: {.cell .code ExecuteTime="{\"end_time\":\"2019-10-31T23:36:28.662099Z\",\"start_time\":\"2019-10-31T23:36:28.660016Z\"}"}
``` python
# TODO
```
:::

::: {.cell .markdown}
## Step 5: Final Model
:::

::: {.cell .code ExecuteTime="{\"end_time\":\"2019-10-31T23:36:28.662099Z\",\"start_time\":\"2019-10-31T23:36:28.660016Z\"}"}
``` python
# TODO
```
:::
