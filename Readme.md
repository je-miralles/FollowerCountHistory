# Twitter Follower Count History via Internet Archives
This is a Python script that collects follower counts from the Internet Archives, given a Twitter username. This script grabs the follower counts by identifying various CSS Selectors that match the follower count element on the historical Twitter pages for almost every major overhaul their page layout has gone through.

## Installation and Usage
### Dependencies
* Python 3
* R* (to create graph)
* bs4 
* urllib
* [archivenow](https://github.com/oduwsdl/archivenow)* (push to archive) 
* datetime* (push to archive)

*optional
 
### Usage
```shell	
$ git clone https://github.com/okrand/FollowerCountHistory.git
$ cd FollowerCountHistory
$ python FollowerHist.py [-g] [-p] <twitter-handle-without-@> 
```
To just create the graph from a csv file
```shell	
$ git clone https://github.com/okrand/FollowerCountHistory.git
$ cd FollowerCountHistory
$ Rscript --vanilla follower_count_linechart.R <twitter-handle-without-@> 
```
This will create a new folder with the name: <twitter-handle-without-@> and create two files in this folder.
* A .csv file that contains the data collected with associated timestamps
* A .png file that contains a line chart of the data collected with X axis representing time
The R script is called from within the Python script so no additional action is required. 

### Options

 	python FollowerHist.py [-g] [-p] <twitter-handle-without-@> 
  
	-g	  Create graph.
	-p	  Push to internet archive. Will only push if last memento is not within current month. Need additional dependencies 	datetime and archivenow.


