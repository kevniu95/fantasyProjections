# fantasyProjections

Source code available at:https://github.com/kevniu95/fantasyProjections

## 1. My Projections Comparison
As of 10/10/2022:

1. My Projections R^2:      0.483
2. ESPN Projections R^2:    0.504
3. Baseline R^2:            0.401

- Baseline projections are regression based on average draft position alone


## 2. How projections are generated
Run "src" files in the following order:

1. **import_data.ipynb** (imports data from various sources)
2. **prepRegSets.ipynb** (prepares datasets for models)
3. **predict.ipynb** (tests and evaluates various models)

**comparison.ipynb** runs the comparison between the model projections and ESPN's 2022 projections using prorated data to this point in the season.


## 3. Use Draft Tool 
Draft tool can be found in the file "projections2022.xlsx"
#### How to use
  - Assuming ten-team league and snake draft, update cell AI3 with your first pick in snake draft
  - Columns "R - AF" indicate each player's value in indicated round. 
    - For instance, from cell R3, we can see Chrisitan McCaffery is "worth" 25.2 points in round 1 based on my player projections
    - He would be "worth" 34.5 points if he was still available in the round 2.
    - *Note these values will change as the value in AI3 changes*
  - Drafted players should be marked with a 1 in column P
  - In any given round *i*, best available player is the player with the highest value in column corresponding to round *i* (out of columns R - AF)

Values in columns R - AF are the expected points scored of *this* player taken in this round less the *expected points of player at this position selected in the next round*

#### Does it work?
Team drafted according to projections and tool (described below)
  - Team Niu - https://fantasy.espn.com/football/league/standings?leagueId=1458708918
  - Click "PF" under **Season Stats** section to sort by points scored
  - Currently **1st** in league of 10 in points scored
