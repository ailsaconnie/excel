# Microsoft Excel
Exploratory data analysis in Microsoft Excel.

Dataset: https://www.kaggle.com/datasets/jasmeet0516/bird-flu-dataset-avian-influenza?resource=download
- This dataset was uploaded to Kaggle by the user Jasmeeto516.
- It is a vast dataset around the topic of avian influenza (H5N1) infections in Irish bird species including individual bird details, precise locational information and binomial data (positive or negative for H5N1).

DISCLAIMER: The data manipulation and analysis shown here has not been conducted with the usual scientific rigor I would apply; this EDA is made simply to showcase my ability with Microsoft Excel. Certain factors have been omitted/changed to streamline my presentation, however in a real-world setting all relevant data would be included. If I were to expand on this analysis, I would likely use R to produce a binomial generalised linear model for example. I could also use GIS to make a heatmap of infections by locality. I used mainly one dataset for this section of my portfolio, however several things I have learned have been expressed through other examples due to relevancy.

---------------------------------
Exploratory data analysis stages:

1. Converted data into table
2. Used the UNIQUE() function to find all unique species names in the data and to ensure there were no duplicates, using the code: =UNIQUE(Table1[Scientific_Name])
3. Used the SUMIF() function to find the total number of positive cases of bird flu in each species, using the code: =SUMIF(Table1[Scientific_Name],S2,Table1[target_H5_HPAI])
4. Generated a pivot table showing species name and the sum of positive results, then filtered to only include species with positive results
5. Created and edited a bar graph with this information
6. Added 'Year' to the pivot table and added a conditional formatting scale (red = higher number of infections, green = lower number of infections)
7. Created a graph of the sum of positive H5N1 results per species by year
8. Used the UNIQUE function to find all unique 'County' values, using the code: =UNIQUE(Table1[County]}
9. Used the SUMIF function to find the total positive responses from each county, using the code: =SUMIF(Table 1[County],S665,Table1[target_H5_HPAI])
10. Used the IFS function to categorise the total positive responses from each county as low, medium or high, using the code: =IFS(T665<30,"Low",T665>=100,"High",T665>=30,"Medium")
11. Produced a table with conditional formatting based on the categories in the previous stage
12. Created a pivot table and added a slicer to more easily view the risk of infection in each county (additional examples of more complex pivot tables and slicers included, as well as using SWITCH statements)
13. Created a forecast of H5N1 infections
