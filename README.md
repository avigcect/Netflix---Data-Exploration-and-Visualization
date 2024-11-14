# Netflix---Data-Exploration-and-Visualization\

Netflix Data Analysis.

Firstly I defined the problem statements clearly.

Then after, I Imported the dataset Netflix as a DataFrame named df.
Checked for the nulls is any present in the dataset.
Found many nulls in the director, cast, and country columns.
Also many columns were nested i.e. they had multiple values at the same record which makes the analysis very difficult.
So, firstly I had to unnest the columns like Directors, Cast, Listed_in, and Country.
After unnesting the number of records went to 201991 from 8807 before unnesting.
Now I had to clean up the null and missing values from the dataset.
But deleting nulls was not an option because the dataset was small and amount of nulls was huge.
So I wanted to impute the nulls with the most suitable data intelligently and efficiently, instead of just filling the nulls with some random data or mean, etc.
So, suppose I need to fill up a record that has the director attribute as null. So I looked at the actor's column and the country column and found out the mode of the directors from other records who have worked with the same actors and are from the same country. Then I got the maximum mode record i.e. the director name who has worked with the same actors many times and is from the same country. So this is the best possible replacement for the null value in the director column.
Similarly I imputed the nulls in the country based on the directors and actors.
Similarly I imputed the nulls in the actors' column by getting mode based on directors, and country.
Similarly nulls in the date_added column were also imputed.
Once all the nulls are imputed then I checked for the datatype of all the attributes and changed the datatype wherever required.
Finally the imputed columns and the remaining columns were all merged and then we got the final DataFrame named df_final.
Then the visualization process started as usual.
