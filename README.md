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
| Read-only | false |
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
    <th>Event 1</th>
    <th>Event 2</th>
  </tr>

  <tr>
    <td><strong>Event Time</strong></td>
    <td>August 05, 2026, 10:58:59</td>
    <td>August 05, 2026, 11:01:28</td>
  </tr>

  <tr>
    <td><strong>User Name</strong></td>
    <td>root</td>
    <td>-</td>
  </tr>

  <tr>
    <td><strong>Event Name</strong></td>
    <td>CreateBucket</td>
    <td>AutomatedDefaultVpcCreation</td>
  </tr>

  <tr>
    <td><strong>Event Source</strong></td>
    <td>s3.amazonaws.com</td>
    <td>ec2.amazonaws.com</td>
  </tr>

  <tr>
    <td><strong>AWS Region</strong></td>
    <td>ap-south-1</td>
    <td>ap-south-1</td>
  </tr>

  <tr>
    <td><strong>Read-only</strong></td>
    <td>false</td>
    <td>false</td>
  </tr>

  <tr>
    <td><strong>Error Code</strong></td>
    <td>-</td>
    <td>-</td>
  </tr>

  <tr>
    <td><strong>Activity</strong></td>
    <td>S3 bucket creation</td>
    <td>Automated VPC creation</td>
  </tr>

</table>

</div>

# PART E — SECURITY AUDIT ANALYSIS

## Step 8: Identify Who, What, When and Where

For each event, identify the following details:

## Event 1 — CreateBucket

| Question | Answer |
|:---:|:---|
| WHO? | `root` |
| WHAT? | `CreateBucket` — S3 bucket creation |
| WHEN? | August 05, 2026, 10:58:59 |
| WHERE? | `ap-south-1` |
| RESULT? | Successful — No error code |

## Event 2 — AutomatedDefaultVpcCreation

| Question | Answer |
|:---:|:---|
| WHO? | `-` (AWS automated service activity) |
| WHAT? | `AutomatedDefaultVpcCreation` — Automated VPC creation |
| WHEN? | August 05, 2026, 11:01:28 |
| WHERE? | `ap-south-1` |
| RESULT? | Successful — No error code |

## Step 9: Prepare the Final Audit Table

| Parameter | Event 1 | Event 2 |
|:---:|:---:|:---:|
| Event Time | August 05, 2026, 10:58:59 | August 05, 2026, 11:01:28 |
| User | root | - |
| Event Name | CreateBucket | AutomatedDefaultVpcCreation |
| Service | Amazon S3 | Amazon EC2 |
| Region | ap-south-1 | ap-south-1 |
| Read-only | false | false |
| Result | Successful | Successful |
| Activity | S3 bucket creation | Automated VPC creation |

## RESULT:
The cloud activities in AWS were successfully audited using AWS CloudTrail Event History. Different AWS events were examined based on event time, user identity, event name, event source, AWS Region, read-only status, and error status. The experiment demonstrated how AWS CloudTrail provides an audit trail for monitoring, accountability, and investigation of cloud activities.
