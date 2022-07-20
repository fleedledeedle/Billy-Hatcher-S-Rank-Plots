# Run through command line
0) Install Anaconda to use the python script on your computer: (google "anaconda python installation")  
Or install matplotlib and pandas libraries for a python installation that you already have: 
> pip install matplotlib
> pip install pandas 
Or use Jupyter notebook in your browser: https://jupyter.org/try


1) Clone repository to your computer:
> git clone https://github.com/fleedledeedle/Billy-Hatcher-S-Rank-Plots.git


2) Download latest version of CSV with scoreboard data
https://docs.google.com/spreadsheets/d/1EPOkUzAVbZkwTmy9fTVmbnpnm5Eh7poHXCw-IXjz904/edit?usp=sharing 
(this link is in the first block of "allScoreboards-lazycode.ipynb")
File > Download > CSV, 
Save as "all-levels.csv"


3) Run the python script: "python makeAllPlotsScript-global.py"
Or open Jupyter notebook: "allScoreboards-edf-function-attempt.ipynb" Then run the code with "Cell > Run All"

This will give the updated version of the plots. They are in the "plots" folder


# Billy-Hatcher-S-Rank-Plots

![Example Plot](https://raw.githubusercontent.com/fleedledeedle/Billy-Hatcher-S-Rank-Plots/main/plots/BH1-1-Forest1Ranks.png)

Billy Hatcher scoreboards, turned into plots with score/clear time/rank
(jupyter notebook put together by fleedle_deedle, 15 Dec 2021)

This code imports all the data on the "Mission Result" screen 
from a CSV and puts it into a DataFrame. This lets us pull specific 
columns of the data by name. 

In this case, I pulled Clear Time and Total Score, which I believe 
are the only things that decide Rank in each mission. I plotted 
these for each mission separately. I hope this makes it easier to see 
which missions are "hard" to S rank or are easy to get enough points 
on.

The next addition I want to make to the plots is a "staircase" of 
acceptable scores you can have when you are expecting a certain 
Clear Time. This would be drawing horizontal lines from right to 
left on the plot for the lowest-score S rank at the highest time. 
The horizontal line would turn down when there is an S rank below it 
(lower score & lower time S rank), then the "stairs" would keep being 
drawn from right to left. For example, a staircase on the Forest 1 
plot would have stairs on scores 8100, 6800, and 4200. 

Another idea could be to mark an S-rank point on the plot with the least 
number of additional "moves" used to combo in the scoreboard ("Driver,"	
"Dunk,"	"Shoot") by adding another circle around the point.

I could definitely make this code much cleaner with a Python loop
and/or a function or two, using an array of all the mission names.
(as listed in "mission-names.txt")

It would also be good to have 1 or 2 non-S ranks for every mission in
the CSV so that it plots properly and I don't have to forget about
which lines have the data replotted from the previous plot.
