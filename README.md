## Creating Pareto Chart Using Plotly - A Tutorial on Tokyo 2020 Olympic Medal Count

#### What is Pareto Chart?
The Pareto chart is a visual representation of the 80-20 rule by combining a bar + line chart. The 80-20 rule, also know as the Pareto Principle, is a widely seen phenomenon that people sometimes don't realize its existense. It's named after Villefredo Pareto who found that approximately 80 percent of all wealth of Italian cities he researched was held by only 20 percent of the families. According to Wikipedia, the Pareto principle states that for many outcomes, roughly 80% of consequences come from 20% of causes (Wikepedia, "Pareto principle", 2022).

#### Why Plotly 
Plotly is much more interactive & visually flexible than Matplotlib or Seaborn. It works well with my dataset (a csv file) via pandas and it's easy to do a Pareto Chart to visualize my dataset. The interactivity feature makes a pareto chart more readable especially when your data have many rows(categories). The dataset I will use in my demonstration "2021 Tokyo Olympics Medals Count" contains 93 countries, so the interactivity feature is vital. You can hover over each measure to see it's count.

#### Installation
We can execute the below code to install the package and necessary extensions for Jupyter Lab. Just copy and paste them into a cell, then run the cell.

!pip install plotly

!jupyter labextension install jupyterlab-plotly

!pip install "jupyterlab>=3" "ipywidgets>=7.6"

#### Data
The dataset I picked is the "Tokyo 2020 Olympic Medal Count(2021)" dataset downloaded from Kaggle (ALAN, 2021).

Data Source : https://www.kaggle.com/datasets/berkayalan/2021-olympics-medals-in-tokyo

The 2020 Summer Olympics , officially the Games of the XXXII Olympiad and branded as Tokyo 2020, is an ongoing international multi-sport event being held from 23 July to 8 August 2021 in Tokyo, Japan.

From the top of my head I believe that the count of Olympic Medals by country follows the 80-20 rule approximately. I wanted to verify it through a Pareto Chart. 

#### See coding in the notebook for interactive features https://github.com/YanyingJiangUmich/Plotly_TokyoOlympic_Medal_Count/blob/main/Plotly_ParetoChart_Tutorial.ipynb

#### Final Visualizations: 

![image1](https://github.com/YanyingJiangUmich/Plotly_TokyoOlympic_Medal_Count/blob/main/olympic1.png)

Now if you mouse over to Bulgaria in the above chart, you can see that Bulgaria is ranked at 24th. Our dataset has 93 countries. So 24/93 countries comprises 80% of the total Gold medal counts. It's not exactly 20/80, but very close! So the Pareto chart is a great visualization technique that can help us determine whether our dataset follows the 80/20 rule, and identify where the cutoff is.

Using the same dataset, let's create subplots to see Gold, Silver and Bronze Medal counts altogether. Firstly let's create dataframes for silver and bronze medal charts respectively. Note that we need to sort each dataframe seperately, by the medal count column so we can calculate cumulative percentages correctly:

![image2](https://github.com/YanyingJiangUmich/Plotly_TokyoOlympic_Medal_Count/blob/main/olympic2.png)

The above chart clearly tells us that all three subplots follows the Pareto principle. But the trend is more significant in Gold Medal and Silver Medal charts. I didn't draw the 80% line and the vertical line in this chart, but thanks to the interactive functionality of Plotly, I can still get the same info by hovering over the chart and doing a little big calculation.

For the silver medal chart: Republic of Korea, ranked 26th, is the cutoff for cumulative 80%. So 26 out of 93 countries won 80% of the silver medals, proving that it approximately follows the 80-20 principle.

For the Bronze medal chart: Azerbaijan, ranked 29th, is the cutoff for cumulative 80%. 29 out of 93 countries won 80% of the Bronze medals. It is more close to a 70-30 relationship, still a good pattern of Pareto principle.

#### Summary
In summary, Pareto principle is everywhere. I chose the Olympic dataset according to my common sense, so it's kind of like guessing. But it indeed follows the Pareto principle! It's very interesting to see and prove it.

In addition, Plotly does a great job in helping us do interactive visualization, with limited lines of code. The visualization made from Plotly are beautiful and professional enough for business presentations and publications. It makes data exploration much more easier. Thus it's a great tool that we can use in exploratory data analysis. We may need to do more analysis to further investigate the dataset depending on the needs, but what I've just walked through is a great start!

Hope you enjoyed this tutorial!
