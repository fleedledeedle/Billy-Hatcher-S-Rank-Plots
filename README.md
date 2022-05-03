# Run through command line
0) Install python3 and Jupyter (will link a better tutorial, for now just google)


1) Clone repository to your computer:
> git clone https://github.com/fleedledeedle/Billy-Hatcher-S-Rank-Plots.git


2) Download latest version of CSV with scoreboard data
https://docs.google.com/spreadsheets/d/1EPOkUzAVbZkwTmy9fTVmbnpnm5Eh7poHXCw-IXjz904/edit?usp=sharing (this link is in the first block of "allScoreboards-lazycode.ipynb")

File > Download > CSV
Save as "all-levels.csv"


3) Open Jupyter notebook:
> jupyter notebook 

That opens browser window. Open "allScoreboards-lazycode.ipynb"


4) Run the code:
Cell > Run All

This will give the updated version of the plots. They are in the "plots" folder


# Billy-Hatcher-S-Rank-Plots
""" 
Billy Hatcher scoreboards, turned into plots with score/clear time/rank
(jupyter notebook put together by fleedle_deedle, 15 Dec 2021)

Google Sheet (the CSV) with all the most recent scoreboard data: 
https://docs.google.com/spreadsheets/d/1EPOkUzAVbZkwTmy9fTVmbnpnm5Eh7poHXCw-IXjz904/edit?usp=sharing

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

I could definitely make this code much cleaner with a Python loop
and/or a function or two, using an array of all the mission names.
[Forest 1, Forest 2, Forest 3, Forest 4, Forest 5, Forest 6, Forest 7, Forest 8, Pirate 1, Pirate 2, Pirate 3, Pirate 4, Pirate 5, Pirate 6, Pirate 7, Pirate 8, Dino 1, Dino 2, Dino 3, Dino 4, Dino 5, Dino 6, Dino 7, Dino 8, Blizzard 1, Blizzard 2, Blizzard 3, Blizzard 4, Blizzard 5, Blizzard 6, Blizzard 7, Blizzard 8, Circus 1, Circus 2, Circus 3, Circus 4, Circus 5, Circus 6, Circus 7, Circus 8, Sand 1, Sand 2, Sand 3, Sand 4, Sand 5, Sand 6, Sand 7, Sand 8, Giant Palace 1, Giant Palace 2, Giant Palace 3, Giant Palace 4, Giant Palace 5, Giant Palace 6, Giant Palace 7, Giant Palace 8]

It would also be good to have 1 or 2 non-S ranks for every mission in
the CSV so that it plots properly and I don't have to forget about
which lines have the data replotted from the previous plot.
""";
