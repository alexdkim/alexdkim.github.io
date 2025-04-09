---
layout: default
title: Homework 6
---

# Altair Visualizations
[The Data](https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_data/main/building_inventory.csv)
[The Analysis](https://github.com/alexdkim/alexdkim.github.io/blob/master/python_notebooks/Workbook.ipynb)

### Plot 1
This chart displays the number of buildings constructed each year in the Illinois building inventory 
dataset. This visualization shows the distribution of state buildings in Illinois by their year of 
construction. The x-axis is the year of construction (parsed from the "Year Constructed" column), and 
the y-axis represents the number of buildings. The main goal of the visualization is to explore and 
observe patterns over time, such as burst of construction activity and slow development in state 
buildings and infrastructures. I applied a color encoding using the Bldg Status field 
(e.g., "In Use", "In Progress") to differentiate building statuses over time. This helps distinguish 
between older buildings that are still in use versus those that are being developed or decommissioned. 
I chose this color map to clearly contrast between statuses without overwhelming the viewer. I chose this 
design to highlight trends in state infrastructure development over time.

For data quality and cleaning, I performed a transformation in Python to clean up the Year Constructed 
column: I converted it to numeric values and filtered out any rows where the year was 0 or missing. This 
ensured that the histogram would not include invalid or non-informative data points. Unlike Homework#5, 
this plot focuses on temporal patterns. Therefore, this visualization is an entirely new direction in 
terms of analysis and presentation.


### Plot 2
This second visualization displyas the total square footage of buildings owned by each Illinois state 
agency, allowing viewers to explore how much physical space different agencies manage. This also includes 
a dropdown menu that lets users filter the chart by building usage type, such as Education, Storage, or 
Administrative. This interactivity helps highlight how various categories of buildings are distributed 
across state agencies.

I used a horizontal bar chart for this plot. The y-axis encodes the Agency Name, sorted in descending 
order of square footage, while the x-axis encodes the sum of Square Footage for each agency. I used color 
encoding for the Usage Description field, which also acts as the filterable variable. This color scheme 
visually distinguishes types of buildings within agencies, and works well because the dropdown filter 
allows for easy focus on one type at a time.

In my Python notebook, I first filled missing values in the Usage Description column with "Unknown" to 
make filtering smoother. Then, I grouped the data by Agency Name and Usage Description, summing up the 
Square Footage for each group. This aggregate dataset was used to drive the visualization. Interactivity 
was implemented using Altair’s selection_point and binding_select features, allowing users to explore 
different usage types without overwhelming the screen with all categories at once.

While Homework #5 also included a bar chart building part, that version was static and lacked 
interactivity. In contrast, this plot adds interactivity and filters to enable deeper exploration 
of the dataset, especially when comparing different types of facilities. This makes the visualization 
much more engaging and informative, particularly for understanding the functional diversity within each 
agency's real estate holdings.
