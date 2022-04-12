# training-santhosh
Assignments space as part of java training group

Assignment: Candidate Evaluation Tool

Business Process:
Job Opening:
•	From different departments based on the workload, they will require resources and they will take the requirements to stake holders.
•	Based on the budget and feasibility, the HR team and the stake holders will come up with plan. 
•	HR Team will open the Jobs (Level, Tech stack, Budget, Timelines, Other info)
1.	HR Team, will be able to update the Job and it’s fields at any point of time.
2.	HR also will be able to Invalidate or close the Job. [For invalidation, reason and invalidation is fine and for closing, they have to enter the candidates who are accepted the offer]
3.	At any point of time, The Active jobs will be shown or served as a response.
Candidate short listing process:
•	Based on the Openings, Hiring team will get mails to start with Hiring process.
•	Hiring team will get the profiles from third party tools.
•	Screening will happen.
•	Selected Candidates from Hiring team will go through the Candidate Evaluation process.
Evaluation Process:
•	Based on screening, assign the category and sub category to the candidate [Hiring team], this is stage where the evaluation form gets created based the details collected so far.
•	Based on above assignment, Find Interviewer and available interview slots.
•	Then trigger an interview process.
•	At interview, the interviewer will go to the portal and based on the template he will start evaluating the candidate and will update the template by the end of interview. 
•	Once he submits the template, an email will trigger to the Hiring team for next steps.
•	Hiring team, will check the template and based on the results, then take necessary actions.
•	Hiring team will revert back to the candidate.
-If positive, proceed with the next round of interview
-if not, revert back with negative feedback!
•	Upon successful interview, Hiring team collect the Candidate details either by giving the link to Candidate or by Updating details in portal from hiring team itself.

[Not part of Candidate selection process tool]Offer release and Onboarding (This is beyond the candidate selection process, need to revisit this, so that we can change the way the offer and onboarding happens currently):
•	HR will upload the Offer PDF
•	Candidate can access the portal and accept the Number
•	Then a email triggers to accept the offer by signing it through email
•	Once HR receives the email, they can trigger On boarding Process
•	Candidate will have a link which re-directs to portal to upload all the related documents



End-to-End application architecture and related details and diagrams:
Services we can offer:
Users
Jobs
Candidates
CEF (Candidate Evaluation Forms)
CEP (Candidate Evaluation process)
[Note: Considering the org and even the future, we don’t need to modularize the application, instead we can have only one backend service which will handle all the jobs]


APIs we expose for the UI/Third party to consume:
[These are sample and not the concrete set, we will add additional calls as when it the application is growing/ on demand basis]
Jobs:
POST:      /job/open-job
GET:        /job/jobs?status=active
PUT:        /job/modify-job/{id} 
DELETE:  /job/remove-job/{id}
DELETE:   /job/remove-jobs?
Users:
POST:     /user/add-user
GET:       /user/all-active-users
PUT:       /user/



Note: Few of the enhancements and modification we could do on incremental basis
1)	Enhancing and Integrating the Offer release and Onboarding process
2)	Extending the tool access to third part Talent acquisition and Outsourcing Partners and integrating them to the system.
3)	Now we are open to take interviews from remote, so we can think of providing interview tools in our system so that the interview and its related work is recorded!
4)	[Required and will do it for every service in later stages of 1st phase development]Auditing at every stage and for every service
a)	History of candidate evaluation process
b)	History of job and it’s updates



