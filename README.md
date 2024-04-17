
# Web-app for monitoring reviewers performance using Gradio

## Introduction
This project was done for improving the code review quality so that more defects can be caught. The code review was done in platform called <b>Crucible</b> by [Atlassian](https://www.atlassian.com/software/crucible)

<h2>Data</h2>
<br>
<image src="https://github.com/Soukumarya-Datta/review-statistics/blob/main/data/crucible-review-closed.png" alt="Crucible Review" width="600" height="350" class="center">
<br>
The source of data are the crucible reviews. Here we can see all the details for each review which shows <i>time spent, number of comments, number of defects</i>, etc,
<br>
<br>
But this is for a single review. What if we want to see performance of the reviewers of past quarter or past 3 years. Here we can use this web-app. It works as follows:
<br>
<ul>
<br>
<li>It utilizes crucible-api endpoints to collect all datas of each review based on the timeframe we want.</li>
<li>Makes a json of the whole data</li>
<li>Creates a pandas dataframe from the json which contains these datas as per the timeframe given:</li>
<ul><br>
  ✅ Associate/reviewer IDs <br>
  ✅ Time spent on reviews (in hours) <br>
  ✅ Number of comments made <br>
  ✅ Number of defects caught in code review <br>
  ✅ Number of review Done by the reviewer
</ul></ul>

<h2>Gradio</h2>
Now we pass this dataframe into <b>Gradio</b> by creating different Gradio methods:

<ul><br>
<li><u><b>tables()</b></u>: Passes the dataframe and creates a Gradio dataframe for given timeframe.</li>
<li><b><u>associate()</u></b>: Searches the associate ID in the tables</li>
<li><b><u>Plots():</u></b> Creates plots for Associate Vs Number of Defects/Number of Comments/Number of reviews/Time spent</li>
</ul>

<h2>Demo</h2>

You can try out the demo of the app [here!](https://soukumarya-review-stats.hf.space)
<br>
<br>
<image src="https://github.com/Soukumarya-Datta/review-statistics/blob/main/data/Demo.jpeg" alt="Demo web-app" width="900" height="420" class="center">
