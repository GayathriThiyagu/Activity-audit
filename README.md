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
| Event Time |  | Aug 05, 2026, 10:58:59 |
| User Name | root |
| Event Name | CreateBucket |
| Event Source | s3.amazonaws.com |
| AWS Region | ap-south-1 |
| Read-only | fase |
| Error Code | - |
| Activity | S3 bucket creation |

</div>

<div align="center">

### Meaning of Important Fields

<table>
  <tr>
    <th>Field</th>
    <th>Meaning</th>
  </tr>
  <tr>
    <td><b>Event Time</b></td>
    <td>Time at which the activity occurred</td>
  </tr>
  <tr>
    <td><b>User Name</b></td>
    <td>User/identity associated with the activity</td>
  </tr>
  <tr>
    <td><b>Event Name</b></td>
    <td>AWS operation that was performed</td>
  </tr>
  <tr>
    <td><b>Event Source</b></td>
    <td>AWS service that generated the event</td>
  </tr>
  <tr>
    <td><b>AWS Region</b></td>
    <td>Region where the activity occurred</td>
  </tr>
  <tr>
    <td><b>Read-only</b></td>
    <td>Indicates whether the event was only a read operation or involved a change</td>
  </tr>
  <tr>
    <td><b>Error Code</b></td>
    <td>Indicates whether an error occurred for the operation</td>
  </tr>
</table>

</div>

## PART C - IDENTIFY ANOTHER CLOUDTRAIL EVENT

## STEP 5: SELECT ANOTHER EVENT:
1.	Return to CloudTrail → Event history. 
2.	Select another event. 
3.	Open its details. 
4.	Record the important fields. 
For example, an event such as:AutomatedDefaultVpcCreation may be present.
This event is associated with Amazon EC2.
<img width="1896" height="1018" alt="Screenshot 2026-08-28 134516" src="https://github.com/user-attachments/assets/9a7d4b23-b719-43cf-ad7c-5aeaf1f2bb0a" />


## Step 6: Analyze the Second Event
Record:
<div align="center">

| **Parameter** | **Observation** |
|:-------------:|:---------------:|
| Event Time | August 05, 2026, 11:01:28 |
| User Name | - |
| Event Name | AutomatedDefaultVpcCreation |
| Event Source | ec2.amazonaws.com |
| AWS Region | ap-south-1 |
| Read-only | false |
| Error Code | - |
| Activity | EC2 creation |

</div>

## PART D — COMPARE THE EVENTS

## Step 7: Prepare the Audit Comparison

Compare the two CloudTrail events.

<div align="center">

<table>
  <tr>
    <th>Parameter</th>
    <th>Observation</th>
  </tr>

  <tr>
    <td>Event Time</td>
    <td>August 05, 2026, 10:58:59<br>August 05, 2026, 11:01:28</td>
  </tr>

  <tr>
    <td>User Name</td>
    <td>root<br>-</td>
  </tr>

  <tr>
    <td>Event Name</td>
    <td>CreateBucket<br>AutomatedDefaultVpcCreation</td>
  </tr>

  <tr>
    <td>Event Source</td>
    <td>s3.amazonaws.com<br>ec2.amazonaws.com</td>
  </tr>

  <tr>
    <td>AWS Region</td>
    <td>ap-south-1<br>ap-south-1</td>
  </tr>

  <tr>
    <td>Read-only</td>
    <td>false<br>false</td>
  </tr>

  <tr>
    <td>Error Code</td>
    <td>-<br>-</td>
  </tr>

  <tr>
    <td>Activity</td>
    <td>S3 bucket creation<br>Automated VPC creation</td>
  </tr>

</table>

</div>

