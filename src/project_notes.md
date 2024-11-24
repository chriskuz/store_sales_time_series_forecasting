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

**GLOBAL MANIPULATION** <font color="teal">[SUSTAINED FEATURE MANIPULATION]</font>

- Dated dfs (`training`, `transx`, `oil`, `holidays`) had their `date` columns converted to datetime from sting.

**LOCAL MANIPULATION** <font color="yellow">[CONSIDER REDUCTION OR REWORK MORE SOPHISTICATION]</font>

- Creation of `days_diff` for these dataframes around each dataframes' difference of dates. 
    - All dfs apart from `holidays` showcased minimal `days_diff` in their `date` column spread. 
    - `holidays` received attention first to understand its column composition. 

# Observation of the `Holidays` section

- There are some notes on aggregation. Generally the notes will need to be cleaned
- Holidays have similar subset prefix `description`s with a number denoting the days post holidays. 
    - This column will neeed more nominal interpretation vs ordinal interpretation (using ordered numbers to denote categories will mistreat the information in the column). 
- A breakdown of some features' counts and unique counts are provided. Broken on `locale`. 
- A showcasing and discussion on holiday `description`s not coinciding across `locale`, meaning there isn't an apparant overlap in information (somewhat lightly addresses duplicates). 
- Some quick notes
     - Possible redundant columns like `locale` showcasing nations and regional holidays. For efficient, we could keep it and omit the true `locale_names`. For added granularity, we could remove such and use the `locale_name` to sustain this breakdown as "National" corresponds already to the `locale_name` of "Ecaudor". However, doing such will also remove the recognition of the "Local" breakdown. 
     - We will have to drop the `days_diff` column before merges as it will not be consistent on any merge. 
     - Will remove the `+n` from some names on holidays. Good to showcase in a presentation.

- Multiple tables generated for some reason. <font color="red">[NOT SURE WHAT WAS HAPPENING HERE]</font>




Possible futures
- Suggestion to explore `type` next...
- Imprtantly should check what are the event `types`
- Most importantly, shrinking the `"National"` `locale` values could be useful in preventing overabundance for feature increase. 

- `type`s and others
    - Not sure how to address `transferred`. If I cannot infer what it means, I'm going to drop it with the belief that I shouldn't be putting features into my model that I cannot explain. It would impair the study as it could be a column that creates a lot of overfitting (and we wouldn't really know until we start iterating to get a best guess). <font color="yellow">[CONSIDER IF DROPPING RELATED COLUMNS ARE SUSTAINED FEATURE OR NOT.]</font>


# Transactions and Training

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
    

# QUESTIONS

- How do I address plotting? How should I store it and move it around? I think I should generate plots in the sections corresponding understanding and and then generate them in an organized area later or otherwise reorganize entirely. 