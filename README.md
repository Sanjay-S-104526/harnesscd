DevSecOps Maturity
Level 1 (Initial) → Level 2 (Low) → Level 3 (Medium) → Level 4 – Continuous Delivery (High)	Pre OJA Implementation  Implementation Level 
	Post OJA Implementation   Level 
Lead Time for Changes 
What is your lead time for changes for the primary application or service you work on (i.e., How long does it take to go from code committed to running in production (we will use the Ready for Production flag) successfully?)
L1 = Unknown, L2 <= 6 Months >1 Month, L3 <= 1 Month >1 week, L4 <= 1 Week	L2	
Release Frequency (Deployment Frequency)
Deployment frequency for the primary application or service you work on, how often does your organization deploy to production or release it to end users?
L1 = Unknown, L2 <= 6 Months >1 Month, L3 <= 1 Month >1 week, L4 <= 1 Day	L2	
Change Failure Rate
For the primary application or service, you work on, what percentage of changes to production or released to users result in degraded service (e.g., lead to service impairment or service outage) and subsequently require remediation (e.g., require a hotfix, rollback, fix forward, patch)
L1 = Unknown, L2 <= 45% >30%, L3 <= 30% >15%, L4 <= 15%	L3	
Time to Restore Service - Repair Time (MTTR)
For the primary application or service, you work on, how long does it generally take to restore service when a service incident or a defect that impacts users occurs (e.g., unplanned, outage, or service impairment)
L1 = Unknown, L2 <= 1 Month >1 Week, L3 <= 1 Week >1 Day, L4 <= 1 Day	L2	
DevSecOps Maturity Level
The DevSecOps  Maturity Metrics is calculated based on the below logic.
•	All the 4 Sub Metrics (Lead Time, Release Frequency, Failure Rate, Repair Time) Values will be calculated individually.
•	Out of Individual 4 individual sub metrics value, the lowest value will be the maturity level. e.g:  If Lead time =Level4, RF= Level3 , Failure Rate= Level 3, Repair Time= Level 2, then Final Result for maturity would be Level 2 which is minimum.
•	If None of the Level Matches or either one Sub Metrics is having value as Unknown, then maturity level will have Final Result will be Level1 ~= Unknown		
...
Checklist Question	Answer	Additional Comments
What you are deploying -Build Artifact type - Jar, Ear, War, exe, dll, etc.	Jar	
Where are you deploying - Target Environment - JBoss, Tomcat, IIS, EKS etc.	Microservices	
How you are deploying - Deployment Process and Steps		
Any Deployment and 
Dependency Configuration required.		
When you want it deployed - Scheduled, on demand or Event based triggers.	Event based triggers	
Who can approve deployment stages - approval processes and steps.	EBT Platform	
Are all the artifacts follow any particular deployment sequence like SIT->QA->UAT->Prod?	DEV>QC->UAT->Perf->Prod->DR	
Does the application have Automated Test Case suite for - Regression Testing?	No	
Does the application have Automated Test Case suite for - Smoke Testing?	No	
Does the application have Automated Test Case suite for - Functional Testing?	No	
Does the application have Automated Test Case suite for - Performance Testing?	No	
Does the application have Automated Test Case suite for - Security Testing?	No	
DoD Checklist
	Checklist Question	Answer (Yes/No)	Exception	Additional Comments	Handoff Status
1	Pre-requisite: Are all the applications/components with different technology or packaging clearly defined?	Yes			
2	Pre-requisite: Is the source code moved to Bitbucket?	Yes			
3	Pre-requisite: Is the Build stored to Artifactory.	Yes			
4	Is there a CD pipeline build or defined.	No			
5	Are there automated test cases written for the application - Regression, Functional, Integration	No			
6	Is the QA Deployment environment defined and mimics a Prod like environment?	Yes			
7	Is there a QA Environment that OJA can utilize for implementing the CD Pipeline without interrupting the Development Cycle.	Yes			
8	Are there Automated Performance Testing scripts written. 	No			
9	Are there IaC scripts defined to create the infrastructure.	No			
10	Is there monitoring and logging in place to visualize successful deployment.	No			
11	What is the GO criteria for a successful deployment?	Harness pipeline (CD)			
12	Is there a Rollback criterion defined for the Application	Yes			
13	Post CD Completion: Is there sufficient documentation on the exact playbook, pipeline execution (on confluence) that has been reviewed/approved by the platform team?	No			
14	Post CD Completion: Has the hand-off between OJA DevOps team and Platform DevOps team complete to their satisfaction?				
15	Post CD Completion: Is there sufficient evidence of logging/monitoring of the pipelines in lower environments to support the Definition of Done?	No			
16	What is the versioning strategy you follow and is there any metadata available with artifact to support deployment?	Yes			
17	Is Deployment done via a Tool or is it done Manually?	Jenkins			
18	Is deployment done through an automated pipeline	Yes			
19	Is the Pipeline invoked Manually or auto triggered on artifact upload?	Auto triggered from Jenkins			
20	Is deployment done in FIS network or on Clients network?	FIS N/W			
21	Is the Database Deployment done manually or Automated?	Datawarehouse team			
22	Is Rally/Jira Integration there today for the application	Yes			
23	Is Service Now integrated with CI and CD pipelines	Yes			
24	Does the deployment require any stack/service restart?	Yes			
25	Can this application deployed independently or it's part of any deployment group?	Independently			
26	What's your rollback strategy? How do you decide and can it be automated?	Rollback from Backup (5 backups maintained in the server)			
27	Is there any Deployment Process you are specifically follow?	No			
28	Do you consider any gating criteria for deployment or promotion of artifact ? It can be any scan or any approval requirement?	Compliant Change gate report			
29	Does the Application need any post CI scans checks like CheckMarx or Blackduck scan output?	Yes			
30	Unit Testing is available?	No			
DoD Checklist for DB - Not Applicable
Checklist Question	Answer	Additional Comments
Are the database scripts moved to Bitbucket?		
For Prod env before deployment DBA used to take backups to do roll backs? 		
How to handle the rollback scenario?		
How to handle multiple script execution in order?		
		
