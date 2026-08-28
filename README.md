# EXPERIMENT 5 - AUDITING CLOUD ACTIVITY USING AWS CLOUDTRAIL

## NAME: GAYATHRI T
## REG. NO: 212223100007

## OBJECTIVE:
To audit and monitor cloud activity in AWS using AWS CloudTrail by viewing and analyzing recorded AWS events and identifying important audit information such as user identity, event name, event time, AWS service, region, and operation status.

## REQUIREMENTS:
•	AWS Account 
•	Web Browser 
•	Internet Connection 
•	Amazon S3 access 
•	AWS CloudTrail 

## PART A - ACCESS AWS CLOUDTRAIL

## Step 1: Login to AWS
1.	Open the AWS Management Console. 
2.	Sign in using your AWS account. 
3.	In the AWS search bar, type CloudTrail. 
4.	Select AWS CloudTrail. 

<img width="1917" height="1028" alt="Screenshot 2026-08-28 133557" src="https://github.com/user-attachments/assets/c2b3d4d0-b92b-4fab-a6ff-6268df49bf01" />

## Step 2: Open Event History
1.	In the CloudTrail navigation menu, select Event history. 
2.	CloudTrail displays recent AWS activity. 
3.	Review the available events. 
The Event History page may display information such as:
•	Event time 
•	Username 
•	Event name 
•	Event source 
•	Resource type 
•	Resource name 

<img width="1898" height="1010" alt="Screenshot 2026-08-28 133643" src="https://github.com/user-attachments/assets/fae59f1d-09a4-4a20-b548-f4e9652c2d3c" />

## PART B - ANALYZE A CLOUDTRAIL EVENT

## Step 3: Select an Event
1.	From the Event History list, select an S3-related event. 
2.	Click the event to open its details. 
3.	Examine the event information and the event record/JSON. 
For this experiment, a CreateBucket event can be used.

<img width="1900" height="1015" alt="Screenshot 2026-08-28 134324" src="https://github.com/user-attachments/assets/094d6793-170d-4314-a04b-2cf5a98309fa" />


## Step 4: Analyze the CreateBucket Event
The CreateBucket event indicates that an Amazon S3 bucket creation operation occurred.

<div align="center">

| **Parameter** | **Observation** |
|:-------------:|:---------------:|
| Event Time |  |Aug 05, 2026, 10:58:59|
| User Name | __________________ |
| Event Name | CreateBucket |
| Event Source | s3.amazonaws.com |
| AWS Region | __________________ |
| Read-only | __________________ |
| Error Code | __________________ |
| Activity | S3 bucket creation |

</div>
