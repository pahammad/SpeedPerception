# SpeedPerception / PHASE-1

<b>Slide deck with overview and a few preliminary insights</b>:

https://github.com/pahammad/SpeedPerception/blob/master/Phase-1/2016_10_SpeedPerception_Phase1.pdf

<b>Basics</b>:

Source URLs: Internet Retailer top-500 list <br>
Web Performance Testing & Data Collection Framework: WebPagetest.org (for obtaining HAR files, videos, perf metrics etc.) <br>
Time of Data Collection: June 2016 <br>
Browser: Chrome <br>
Mode: Desktop rendering mode <br>
Network Speed: Cable <br>

<b>SpeedPerception:PHASE-1 Benchmark Basics</b>:

Total votes: 77482 <br>
Total valid (h_score >=80%) votes: 58212 <br> 
Number of Total sessions: 5444 <br>
Number of Complete sessions: 2914 <br>
Number of Valid sessions (h_score >=80%): 2772 <br>
Number of Valid sessions (h_score =100%): 2016 <br>
Number of Incomplete sessions: 2530 <br>

<b>Additional Information</b>:

PHASE-1 Web app code / Experimental Design Criteria: https://github.com/pdey/SpeedPerceptionApp <br>
PHASE-1 crowd-sourcing challenge was hosted at http://speedperception.meteorapp.com/ <br>
PHASE-1 crowd sourcing duration: 28th July 2016 to 30th September 2016. <br>
PHASE-1 results: https://github.com/pahammad/SpeedPerception/tree/master/Phase-1 <br>

<b>Variables contained in the benchmark dataset</b>:
Our SpeedPerception-Phase1 benchmark contains 4 files formatted in CSV (comma separated value) format and named accordinly as csv1, csv2, csv3, csv4 and csv5. Each of them contains data either from the crowdsourcing component, or measurements obtained from WPT (WebPagetest) on the sample urls. These data sets have been curated to better serve the analysis purpose. <br>

<b>csv1.csv</b> (115 rows, 32 columns) <br>
This file contains all webpage measurements from HAR. It is combined with application level metrics such as Page Load Time, Total Bytes Size, visual metrics such as SpeedIndex and RenderStart. It also contains some ad-hoc metrics such as _loadTime_image_size, which indicates the byte size of image has been loaded until the time of onLoad. The last column <b>uid</b> is an unique key for each of the sampled websites. 

<b>csv2.csv</b> (160 rows, 3 columns) <br>
This file helps us to map the VideoPair ID to each individual webpage ID (uid in csv1). 

<b>csv3.csv</b> (44352 rows, 5 columns)) <br>
This file has all <b>valid (80% or higher on honeypot video pairs)</b> responses from our experiment. 'sessionID' represent each individual participant, and for each sessionID, there are 16 'pairID' asscosiated with it. 'TimeToClick_InMS' is another metrics we record during each participant's session, so that we know how long it took a use to make a decision. 'userAgent' is the browser they used when launching at our app. Finally, 'vote' is the choice user made when looking at each video pair. 

<b>csv4.csv</b> (2772 rows, 2 columns)) <br>
This file is a simple tracking on the score of each participant for our honeypot mechanism. Each session contained 5 honeypot pairs, and a session is considered valid if the user makes no more than 1 mistake out of the 5 honeypot pairs.

<b>csv5_SIandPSI.csv</b> (160 rows, 5 columns)) <br>
Refer to https://arxiv.org/abs/1704.01220 for results using modified SI/PSI using onLoad and TTC (time to click) as the cut-off points for the SI/PSI integrals.

<b>Analysis Scripts</b>:
There are two notebook scripts we provide here, one contains some helper functions and the other is the main analysis. You may copy the code to write your own .py file or you can use Jupyter Notebook to run our code. You can follow the instruction here to download, install and run Jupyter Notebook. http://jupyter-notebook-beginner-guide.readthedocs.io/en/latest/what_is_jupyter.html



