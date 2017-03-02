### Project Description:
An interactive chart of BMI and blood pressure by gender and country. This project was built with D3. This is the 6th project of Udacity data analyst nano degree.

### Final Folders and Files:
- lib: documents of javascript libraries
- logo: png pictures or genders
- raw_data: original BMI and BP datasets in xlsx format. I downloaded them from Gapminder, which were originally published by MRC-HPA Centre for Environment and Health
- data_cleaning.ipynb/html: python scripts to read data from xlsm, reshape and export to csv for chart building
- male_combine.csv/female_combine.csv: cleaned csv dataset 
- index.html: final interactive chart
- use_d3.html and use_dimple.html: I started this project with dimple and then found out it is not flexible enough to add customized features (such as vertical and horizontal lines that show average). So I switched to pure d3. use_d3 is the precedent of final index.html file. 


### Visualization Summary:
- The key message I want to deliver: 
	- In general, both female and male around the world are getting fatter since 1980. 
	- The blood pressure does not have an uniform pattern between genders: the BP of females in most continents was decreasing, while the BP of males in most continents was decreasing from 1980 to 2000 and started to bounce back up after 2000.
- Audience Exploration:
	- Beneathe the general pattern, the pattern of each continent is significantly different from each others. For example, Oceania males and females went through the most drastic BMI increases, while the increase of BMI in S/N America and Europe is relatively small. Some countries in Asia and Africa suffered from low BMI in 1980s but they gradually catched up. 
	- The variance of those two parameters across all countries became smaller. Those points used to spread all over, but they tend to gathered into a more dense cluster as time progressed.
	- I didn't describe those patterns in detail, since I want to leave this exploration to the audiences.     

### Feedback & Design Revisions:
- The subtitle that shows the year was originally located above the description paragraph. My friend told me that when she watch the animation, the year subtitle is outside the screen so she can't track the year change. I then moved this year subtitle inside the svg.
- I forgot to mark the data source, somebody reminded me and I then added the source information near the x axis.
- I follow the advice adding a gender icon near the description paragraph, so audiences can be easily awared of which gender is presented in the chart. 

### Resources:
- I copied some code blocks from lecture example files as starting point
- Documentation of d3 is my major resource. 
- I also browsed many stackoverflow discussions, but didn't document their links.
