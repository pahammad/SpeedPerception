# SpeedPerception / PHASE-1: Experiement, benchmark data and key results.

<b>Basics</b>:

Source URLs: Internet Retailer top-500 list <br>
Web Performance Testing & Data Collection Framework: WebPagetest.org (for obtaining HAR files, videos, perf metrics etc.) <br>
Time of Data Collection: June 2016 <br>
Browser: Chrome <br>
Mode: Desktop rendering mode <br>
Network Speed: Cable <br>
5444 Total sessions <br>
2914 Complete sessions <br>
2772 Valid Score = 80% sessions <br>
2016 Valid Score = 100% sessions <br>
2530 Incomplete sessions<br>
77482 Total votes <br>
58212 Total valid(80% or higher) votes <br> 

PHASE-1 Web app code / Experimental Design Criteria: https://github.com/pdey/SpeedPerceptionApp <br>
PHASE-1 crowd-sourcing challenge was hosted at http://speedperception.meteorapp.com/ <br>
PHASE-1 crowd sourcing duration: 28th July 2016 to 30th September 2016. <br>
PHASE-1 results: https://github.com/pahammad/SpeedPerception/tree/master/Phase-1 <br>

<b>Variables contained in the benchmark dataset</b>:
We will provide 4 datasets formatted in CSV and named accordinly as csv1, csv2, csv3 and csv4. Each of them contains data either the benchmark from crowdsourcing experiment, or static measurements from WPT on 115 sample urls. These data sets have been pre-cleaned to better serve the analysis purpose. <br>

<b>csv1.csv</b> (115 rows, 32 columns) <br>
This file contains all webpage measurements from HAR. It is combined with application level metrics such as Page Load Time, Total Bytes Size, visual metrics such as SpeedIndex and RenderStart. It also contains some self-computed metrics such as _loadTime_image_size, which indicates the byte size of image has been loaded until the time of onLoad. The last column <b>uid</b> is an unique key for each of 115 websites. 

<b>csv2.csv</b> (160 rows, 3 columns) <br>
This file helps us to map the VideoPair ID to each individual webpage ID (uid in csv1). 

<b>csv3.csv</b> (44352 rows, 5 columns)) <br>
This file has <b>valid (80% or higher on honeypot video pairs)</b> responses only from our experiment. 'sessionID' represent each individual participant, and for each sessionID, there are 16 'pairID' asscosiated with it. 'TimeToClick_InMS' is another metrics we record during each participant's session, so that we know how long it took a use to make a decision. 'userAgent' is the browser they used when launching at our app. Finally, 'vote' is the choice user made when looking at each video pair. 

<b>csv4.csv</b> (2772 rows, 2 columns)) <br>
This file is a simple tracking on the score of each participant for our honeypot mechanism. 




