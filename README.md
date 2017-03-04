### Project Description:
An interactive chart of BMI and blood pressure by gender and country. This project was built with D3. This is the 6th project of Udacity data analyst nano degree.

### Submission information:
- This is my second submission. I made code format adjustion and rewrite this README file according to the feedback of first grader.
- The bug of filter error has been fixed, now you try the same setting (Male/Asia/1986) there will be no error. Other combination of filter should also work.
- I also disabled button when animation is playing, since I found that interrupting the animation would cause some problems on year display.


### Final Folders and Files:
#### Data and Libraries
- lib: documents of javascript libraries
- logo: png pictures or genders
- raw_data: original BMI and BP datasets in xlsx format. I downloaded them from Gapminder, which were originally published by MRC-HPA Centre for Environment and Health
- data_cleaning.ipynb/html: python scripts to read data from xlsm, reshape and export to csv for chart building
- male_combine.csv/female_combine.csv: cleaned csv dataset 

#### Charts of different versions:
I kept 3 major versions:

- index_v1.html: This is a sketch chart quickly made with Dimple. I started this project with dimple and then found out it is not flexible enough to add customized features (such as vertical and horizontal lines that show average). So I switched to pure d3 later.
- index_v2.html: A work-in-progress d3 chart, the interaction and animation function are done, but gender option is not added yet (only female data in this version), the chart also has no legend and no explanatory description.
- index_final.html: final chart for submission.


### Visualization Summary:
- The key message I want to deliver: 
	- In general, both female and male around the world are getting fatter since 1980. 
	- The blood pressure does not have an uniform pattern between genders: the BP of females in most continents was decreasing, while the BP of males in most continents was decreasing from 1980 to 2000 and started to bounce back up after 2000.
- Audience Exploration:
	- Beneathe the general pattern, the pattern of each continent is significantly different from each others. For example, Oceania males and females went through the most drastic BMI increases, while the increase of BMI in S/N America and Europe is relatively small. Some countries in Asia and Africa suffered from low BMI in 1980s but they gradually catched up. 
	- The variance of those two parameters across all countries became smaller. Those points used to spread all over, but they tend to gathered into a more dense cluster as time progressed.
	- I didn't describe those patterns in detail, since I want to leave this exploration to the audiences.     

### Design:
- I choose this scatter chart type because there are more than 100 countries with 2 quantitative parameters(BMI and BP), scatter chart is most appropriate choice to present all those individual data points altogether, with x and y axis presenting two quantitative parameters.
- Besides x and y axis, there are two more dimensions: continent and year. 
		- Since continent is a categorical variable, it is appropriate to present this variable with color hue. The color is chosen from ColorBrewer website.
		- Year dimension is presented with animation, to demonstrate the historical trend of changing. Audience can also stop at certain year point to view static chart.
- I also added one horizontal and one vertical line to present the average value of each quantitative parameters. The movement of those two lines would help audience track the trend easier.

### Feedback & Design Revisions:
1. I showed this chart to a friend by my side on my computer.
	- Feedback: when she watch the animation, the year subtitle is outside the screen so she can't track the year change (The subtitle that shows the year was originally located above the description paragraph)
	- Revision: I moved the year subtitle inside the svg as shown in the final submission

2. I posted the bl.ock link in my social network (douban, a Chinese book/music/movie community) to collect feedback from other ones.
	- Feedback: More than one people told me there is no data source. 
	- Revision: I then added the source information near the x axis.

3. I also showed this chart to my mother, who can barely read English. 
	- Feedback: She can't tell which gender is presented in the chart (because I only mention the gender in title text). 
	- Revision: This inspired me to add a gender icon near the description paragraph, so audiences can be easily awared of which gender is presented in the chart. 

### Resources:
- I copied some code blocks from lecture example files as starting point
- Documentation of d3 is my major resource. 
- I also browsed many stackoverflow discussions, but didn't document their links.
