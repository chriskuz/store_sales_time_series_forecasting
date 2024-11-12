# Project Notes

Here will be stored notes on the project that can be better used as a more detailed reference to what's going on to the project. It will include some cusotm highlights. 

# Data

7 dataframes:
- 5 used for training
    - `training`
    - `transx`
    - `stores`
    - `oil`
    - `holidays`
- 1 used for testing
    - `testing`
- 1 shown as a sample submission
    - `sample_submission`
        - I don't think we actually will use this for any practical purpose 

# Attributes

# Cleaning

**GLOBAL MANIPULATION**

- Dated dfs (`training`, `transx`, `oil`, `holidays`) had their `date` columns converted to datetime from sting.

**LOCAL MANIPULATION** <font color="yellow">[CONSIDER REDUCTION OR REWORK MORE SOPHISTICATION]</font>

- creation of `days_diff` for these dataframes around each dataframes' 


# IDEAS

- see if we need to include scaling

- <font color="lightgreen">[OPEN]</font> It would be good to show maybe a plot of geographical data with the cities and stuff
    - Can aggregate sales here as bubble chart (if possible to aggregate towards some sales). A slideer on dates could be nice to include. 
    - can do region subplot with cities and see if also cities fall under regions and if others don't

- consider extrapolation for nulls in `oil`....if worth it. 
    - compliment a timeseries plot of the pricing. 

- num holidays/day construction
    - counts the presence of national, regional, and city holidays found within a day
    - we will use a globalized number for num_holidays/day (meaning unique cities + unique regions + national presence)
    - we 

- subplotting
    - sales/day 
    - oil prices/day
    - num_holidays/day
    