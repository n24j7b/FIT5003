java c
FIT5003 Software Security Assignment-2 (S2 2024) 
Total Marks 100 
Due on Oct 4th, 2024, Friday midnight, 11:55:00 pm 
1 Overview The primary learning objective of this assignment is to provide you with firsthand experience in exploiting SQL Injection, Cross-site Scripting and Cross-site Request Forgery vulnerabilities.  Additionally, it aims to deepen your understanding of these vulnerabilities.  This assessment does not require a specific virtual machine (VM) and can be executed on any operating system.  You can utilize the same setup as the Lab07 and Lab08.
2 Submission 
You will need to submit a report (one single PDF file).  Typeset your report into  .pdf format (make sure it can be opened with Adobe Reader) and name it as the format: [Your Name]-[Student ID]-FIT5003- Assignment.pdf. All payloads, if required, should be embedded in your report.  In addition, if a demonstration video is required, you should record your screen demonstration with your voice explanation and upload the video to your Monash Google Drive or any online service which allows you to share videos.  The shared URL of the video should be mentioned in your report wherever required. You can use this free tool to make the video:https://monash-panopto.aarnet.edu.au/ ; other tools, such as Zoom, are also fine.
Important notes and penalties: 
•  It is the student’s responsibility to ensure that the video content is accessible to the teaching staff. Failure to provide accessible video will result in the relevant task being assessed without consideration of the video.
•  A part of the submitted video (at a corner) must clearly show your face at all times.  Penalties may apply when that’s not the case.
• Video demonstration should be a live exploitation of the vulnerabilities.
•  Late submissions incur a 10-point deduction per day.  For example, if you submit 2 days and 1 hour late, that incurs 30-point deduction. Submissions more than 7 days late will receive a zero mark.
•  If you require extension or special consideration, refer to https://www.monash.edu/students/ admin/assessments/extensions-special-consideration. No teaching team mem-ber is allowed to give you extension or special consideration, so please do not reach out to a teaching team member about this. Follow the guidelines in the aforementioned link.
•  The maximum allowed duration for the recorded video is 15 mins in total.  Therefore, only the first 15:00 mins of your submitted video will be marked. Any exceeding video components will be ignored.
•  If your device does not have a camera (or for whatever reason you can’t use your device), you can borrow a device from Monash Connect or Library.  It’s your responsibility to plan ahead for this. Monash Connect or Library not having available devices for loan at a particular point in time is not a valid excuse.
•  You can create multiple video parts at different times, and combine and submit a single video at the end. Make sure that the final video is clear and understandable.
•  You can do (online) research in advance, take notes and make use of them during your video recording. You may also prepare exploit scripts in advance. But you cannot simply copy-paste commands to carry out the tasks without any explanations.  Explanations (of what the code does) while completing the tasks are particularly important.
•  Zero tolerance on plagiarism and academic integrity violations: If you are found cheating, penalties  will apply, e.g., a zero grade for the unit. The demonstration video is also used to detect/avoid plagia-  rism. University policies can be found at https://www.monash.edu/students/academic/ policies/academic-integrity. 
3 Web Application Vulnerabilities 
Q1:  Complete three labs from PortSwigger Labs, one from SQL Injection, one from Cross-Site Scripting, and one from Cross-Site Request Forgery section. Please select labs designated as PRAC- TITIONER or EXPERT; APPRENTICE labs will not be accepted.  You are permitted to utilize the solutions and demonstrations available on the PortSwigger website for assistance.  However, please do not copy walkthrou代 写FIT5003 Software Security Assignment-2 (S2 2024)SQL
代做程序编程语言ghs from the PortSwigger website.  Your solution should include the logical steps that lead to the exploitation, which may not be covered in the walkthroughs on the PortSwigger website. [60 Marks] 
Record a video and write a report to answer the following questions for each lab.  At the beginning of each lab recording, please state your name, student ID, and the name of the lab you are solving; no marks can be awarded without this information.
1.  How did you identify the vulnerability? (5 Marks)
2.  Which payload was chosen for exploitation and why? (5 Marks)
3.  What an attacker could achieve using the vulnerability? (5 Marks)
4.  How the vulnerability can be mitigated? (theoretically, no demonstration is required) (5 Marks)
The video submission must demonstrate solving the lab, addressing the questions outlined above. In case time runs short during the video, you may use the report to address any unanswered ques- tions, making references to relevant sections of the video.  However, it is important that the video includes, at a minimum, a demonstration of the lab. The report does not need to be in detail, it should briefly address the mentioned questions,i.e. it can contain one or two-line answer for each question, payloads, important screenshots (if necessary) and the video link(s).  The marks mentioned above are for the videos and report combined. The word limit for each sub-question is 200 words, i.e. maximum 800 words are allowed for Q1 per lab. 
Q2:  Download the Q2 .html file from Moodle.   Assume you are browsing monash.edu, and it  is hypothetically vulnerable to various web attacks (although it is not).  While  navigating monash .edu, assume you open another tab in the same browser, and visit attacker .com (as- suming attacker convinced you to do that).  You click the Submit button on the attacker .com webpage, which contains Q2 .html, initiating attacks on monash .edu. Examine Q2 .html (you can open the file in the browser and intercept the request in BurpSuite if desired) and respond to the following questions. No video is required for this question. The word limit for each sub-question is 200 words, i.e. maximum 600 words are allowed for Q2. [20 Marks] 
1.  Which vulnerability/vulnerabilities attacker .com is trying to exploit on monash .edu? (please explain the scenario outlining how this exploitation could occur) (10 Marks) 
2.  If successful, what is the consequence of the attack(s)? (5 Marks)
3.  What mitigation(s) would you suggest for monash .edu to counter attack(s) launched by attacker.com? (5 Marks) 
Note: The parameter values in the HTML file are URL encoded. 
Q3: Assume you visit monash .edu and it tries to talk to lms .monash .edu, the browser issues an OPTIONS method to lms .monash .edu and gets a response, below is the HTTP request and its response: 
OPTIONS  /doc  HTTP/1 . 1 Host:  lms .monash .edu
User-Agent:  Mozilla/5 . 0   (Macintosh;  Intel  Mac  OS  X  10 . 14;  rv:71 . 0) Accept:  text/html,application/xhtml+xml,application/xml 
Accept-Language:  en-us,en;q=0 .5 Accept-Encoding:  gzip,deflate
Connection:  keep-alive
Origin:  monash .edu
Access-Control-Request-Method:  POST
Access-Control-Request-Headers:  x-requested-with
HTTP/1 . 1  204  No  Content
Date:  Mon,  01  Dec  2008  01:15:39  GMT Server:  Apache/2 
Access-Control-Allow-Origin:  *
Access-Control-Allow-Methods:  POST,  GET,  OPTIONS Access-Control-Allow-Headers:  x-requested-with
Access-Control-Allow-Credentials:  true
Access-Control-Max-Age:  86400   Vary:  Accept-Encoding,  Origin   Keep-Alive:  timeout=2,  max=100 Connection:  Keep-Alive
Explain the Cross-Origin Resource Sharing (CORS) HTTP headers in the above HTTP request and response. Would browser change future requests based on the above HTTP response? No video is required for this question. The word limit for Q3 is 300 words. [10 Marks] 
4 Report Completion and Quality of Presentation [10 Marks]
Marks are allocated to the quality and clarity of presentation in the report and the video.







         
加QQ：99515681  WX：codinghelp
