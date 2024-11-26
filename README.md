java c
Project in Advanced Algorithms and   Data Structures
COMP4134
Overview
For this   project, you are tasked with solving a   real-world   transportation   problem.   Formally   speaking,   it   is   called the   pickup and delivery   problem with time windows   (PDPTW). The   pickup   and   delivery   problem (PDP)   is a type of vehicle   routing   problem   in which customers   are   paired together,   and   a   pair   must   be   serviced   by   the   same   vehicle, seehttps://developers.google.com/optimization/routing/pickup_delivery   for example.   In other words,a   load   must   be collected from one   location   and   delivered to   another   location   by a single vehicle. Clearly, there are   also   ordering   or   precedence   constraints   to   ensure that   the   collection site   is visited   before the delivery site.   If there are   time   windows   during   which   the   customers must   be visited, then the   problem   is   known as the   PDPTW. This   problem commonly   arises   in   real-world logistics, and solution   methodologies   have significant   practical applications.While   planning   the   routes,   there   are   some   driver   break   regulations   that   have   to   be   met,   which   include   drivers'   hours   rules   and working time   rules. To   reduce   complexity, we   will focus   on   the   rules   highlighted   in   red   circles,   which   pertain   to   the   daily   transportation   problem.   The   objective   is   to   decrease   the   total   duty time   necessary for the delivery of   all   orders.The   two regulations   are briefly introduced below;   detailed information   can be   found in   Table 1 (see
https://assets.publishing.service.gov.uk/media/5e14b5b040f0b65dbed713a0/simplified-guidance-eu-drivers-hours-working-time-rules.pdfand Table 2).   Regarding   Regulation (EC)   No 561/2006, the following   constraints should   be   met:
•          The   maximum daily   driving time   is   9   hours.
•          Driver   breaks could   be   one   of   the   following:   (a)   For   every   4.5   hours   of   driving,   drivers   must   take   a   break   of   at   least   45   minutes.   This   break   starts   a   new   4.5-hour   driving   period.   (b)   For   every   4.5   hours   of   driving,   drivers   can   take   either   one   45-minute   break   or   two   smaller   breaks,   one   of   at   least   15   minutes followed   by another of at   least   30   minutes.Another   regulation   is   Directive   2002/15/EC,   which   is   a   legislative   act   concerning   the   working   time   for   mobile   workers   engaged   in   road   transport   activities.   It   sets   out   the   maximum   limits   on   working   time,   including driving time, other work-related activities, and on-call time. The following constraints   should   be   met:
•          Drivers   cannot   work   more   than   6   hours   without   a   break;   a   break   should   be   at    least    15   minutes   long.
•          Drivers   need   a   30-minute   break   if they work   between   6   to   9   hours   in   total.
   
Table 1 A summary of   the EU drivers’ hours rules and sector specific working time rules
   
Table 2 Summarised daily allowed drive time, duty time   and route duration
Deadline   and   Late   penalty
Deadline   is 6pm   Monday the 9th of   December, for   each   day   the   coursework   is   late,   a   penalty   of   10%   will   be   deducted.
Plagiarism   is   not allowed, and your source code   and   documentation   will   be   examined   for   similarities.
Please   note that this   is   individual work,   not a group   project. You   are   encouraged to   conduct   individual research and free to   implement algorithms that   have already   been   published,   but   copying   others’   work   is strictly forbidden.   (Please consult the academic   misconduct   policy for further   details:
https://www.nottingham.ac.uk/studentservices/servicedetails/appeals-complaints-and-   conduct/academic-misconduct.aspx)
Submission   instructionsTo   submit your   code   and   report for this   module,   please   use the   provided   link   on   the   Moodle   page.   Your      algorithm   should   be   implemented   in   Java,   and   your   report,   which   is    limited   to   2000   words,   must   be      submitted in PDF format. Please refer   to the   “Grading Criteria” section below, which lists the requirements.   The submission link will be active before the deadline.   Please   note that submissions sent via   email will   not      be   accepted.   For   comprehensive   guidelines   on the   submission   process,   please   consult the “Submission”   section   below.
Submission
Given that this   is a   Master's   level   project,   it   is designed to   emphasize   independent study   and   research.         However, certain algorithms and data   structures   relevant to   the   project   will   be   introduced   in   the   course   module COMP4133.   Proficiency   in Java   is   required for the successful completion of this   project.
The   necessary files for this assignment are available for   do代 写COMP4134 Project in Advanced Algorithms and Data StructuresJava
代做程序编程语言wnload from   Moodle. These   include:
•          `Input.json`: An example file that you   will   read   as   input.
•          `Output.txt`: A sample output file that   corresponds   to   the `Input.json`   input.
Your Java code should fulfill the following   requirements:
1.          Read the content   of `Input.json`.
2.         You are   required to devise your own algorithm   and   apply   it to   solve   the   given   problem.
Implementing an existing algorithm from the   literature   is fine,   but   please   cite   it   in your   report.   You   may select from various algorithmic approaches,   including   but   not   limited to   dynamic
programming,   linear   programming, and   heuristics. Your   implementation will   be submitted for   grading.
3.          Print the solution follow the   expected   ‘Output.txt’   .
For   instance, given the content of 'Input.json'   provided:
Please   refer to the video   recording on the   module   page for this   module for a detailed   explanation   of   the JSON content.
   
The   expected   'Output'should   look   like   this:
   
Which appears as follows   in the   text   file:
VehicleName,JobId,JourneyTime,ArrivalTime,WaitTime,DelayTime,ServiceTime,DepartureTime,Break1Ti   me,Break1Duration,Break2Time,Break2Duration
1,Vehicle   1 start,0h0m,08:00,0h0m,0h0m,0h0m,8h0m,,,,   1,C-0,0h0m,08:00,0h0m,0h0m,0h0m,8h0m,,,,
1,C-1,4h0m,12:00,0h0m,0h0m,0h0m,12h0m,,,,
1,D-0,0h0m,12:00,0h0m,0h0m,2h0m,14h0m,14:00,0h15m,14:45,0h30m   1,D-1,2h0m,16:45,0h0m,0h0m,0h0m,16h45m,,,,
1,Vehicle   1 end,0h30m,17:15,0h0m,0h0m,0h0m,17h15m,,,,
Grading   Criteria
Criteria of code   50%
Full   mark
Comment
Is the output   correct?
20%
The correct answer   will   receive full   marks.   Marks   maybe deducted for
the following   reasons:   partially
correct answers with   minor
mistakes, or correct   output
accompanied   by other   issues. This      will   be tested   using a   new   dataset,   which   is   not   provided   by the
module.   For   programs   involving            randomness, ensure that you   use   your student   ID   as the   seed.
How   is the time complexity of the   program?
10%
For those who   provide the correct   answer, their   runtime   will   be
recorded. Those   whose   runtime
falls   into the first quantile   will
receive full   marks. Those   in the
second quantile will   receive   7.5% of   the total   marks, the third quantile            5%, and the   last   quantile   2.5%.
How   is the solution quality of the   program?
10%
Please   indicate the duration
required for the solution to
complete all the service   requests   (i.e.   pickup and delivery   pairs)
within   runtime   of   30 seconds.   For       those whose solution   is   better than   the   benchmark solution, the
ranking will   be determined   by the   speed of completion; the   quicker      the completion, the   higher the
ranking.   Participants whose
solutions fall within the   top 25%
will   be awarded full   points. Those            in the second 25%   bracket   will   earn   75% of the total score,   the   third
25% will get 50%,   and   the   bottom   25% will   receive   25%.
Well formatted code
5%
Is the   program well formatted   (following Java   naming
conventions,   high   readablity,
   
   
appropriate error   handling, adhere   to Object-Oriented   Programming            paradigm   etc.)
Appropriate comments
5%
Does the   program contain   appropriate comments?
Criteria of   report 50%
   
   
Well-written   literature   review
10%
In the   literature   review,   is the
literature sufficient,   up-to-date,
well-organised, and does   it follow   proper   logical flow? The   report
should   be confined to   a   maximum         of 2000 words, excluding   literature   and   pseudo code.
Evaluation of the Chosen Algorithm,   Data structure   and   Methodology
15%
Provide a clear   rationale   for   the   algorithmselected and the
approach taken to solve the   problem.
Indicate whether the algorithm   is            entirely of your own   design   or   if   it         is an   implementation of   an   existing   algorithm from the   literature.
Discuss the   innovative aspects or            novelties that you   have   introduced   to the   project.
Provide clear and effective documentation   of your   algorithm
10%
In your   report, ensure that you   provide a   clear   and concise
explanation of your algorithm.
Utilise clear   instructions, supported   by   pseudocode, diagrams, and
other visual aids as   necessary   to   enhance   understanding.
Evaluating solution quality and   output validation   accuracy
10%Justify   the   solution’squality   and   confirm that the given   output   is      correct.
Report the   result clearly
5%
Report the   results clearly, for
example,   by   using visuals,   plots,
and statistics such   as the   mean   and   standard deviation of   a   number   of         runs.
   

         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
