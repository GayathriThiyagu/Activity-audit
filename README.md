
# EXPERIMENT 4
# NAME  : GAYATHRI T
# REGNO : 212223100007

## ASSET-ORIENTED RISK ASSESSMENT OF STORAGE ASSETS IN AWS 


## Aim

To identify storage assets in **AWS S3**.


## Software / Cloud Services Required

- AWS Account
- Microsoft Azure Account
- Web Browser
- Internet Connection

### Cloud Services Used

| Cloud Platform | Storage Service |
|---|---|
| AWS | Amazon S3 |


## AWS S3 STORAGE ASSESSMENT

## Step 1: Login to AWS

1. Open the AWS Management Console.
2. Sign in using your AWS account.
3. Search for **S3**.
4. Select **Amazon S3**.


## Step 2: Select the S3 Bucket

1. Click **Buckets**.
2. Select the S3 bucket created in the previous experiment.
3. Record:
   - Bucket name
   - AWS Region
   - Number/type of objects

<img width="1919" height="1017" alt="Screenshot 2026-08-21 134314" src="https://github.com/user-attachments/assets/778c10c9-9dae-4d4a-a28d-b8e2b219af1b" />


## Step 3: Check Block Public Access

1. Open the S3 bucket.
2. Select **Permissions**.
3. Locate **Block public access (bucket settings)**.
4. Check **Block all public access**.

### Record

- **ON** → Secure configuration
- **OFF** → Potential public-access risk

<img width="1919" height="1017" alt="image" src="https://github.com/user-attachments/assets/8eebec0d-6771-4ab9-90a5-ed7bbc54f637" />



## Step 4: Check Bucket Versioning

1. Select the **Properties** tab.
2. Locate **Bucket Versioning**.
3. Record whether it is:
   - Enabled
   - Disabled

### Security Purpose

Versioning helps recover previous versions of objects after accidental deletion or modification.

<img width="1919" height="1013" alt="image" src="https://github.com/user-attachments/assets/da1b25e6-7f63-4db5-9fc4-f58504d8d17f" />
<img width="1919" height="1017" alt="image" src="https://github.com/user-attachments/assets/df5871d8-caa3-491c-bdf1-f9da6198283e" />



## Step 5: Check Default Encryption

1. Stay in the **Properties** tab.
2. Locate **Default encryption**.
3. Record the encryption type.

### Possible Configurations

- SSE-S3
- SSE-KMS
- DSSE-KMS

### Security Purpose

Encryption protects stored data from unauthorized disclosure.
<img width="1919" height="1017" alt="Screenshot 2026-08-21 134417" src="https://github.com/user-attachments/assets/61feccbb-86d0-41ec-a18a-8a681f77619b" />


## Step 6: Check Bucket Policy

1. Select **Permissions**.
2. Locate **Bucket policy**.
3. Check whether a bucket policy exists.

### Record

- Policy exists
- No policy

> **Note:** A missing bucket policy is not automatically a vulnerability. Access may be controlled through IAM and other AWS security mechanisms.

<
<img width="1919" height="1013" alt="image" src="https://github.com/user-attachments/assets/8c5d38d9-88e9-472b-8491-f711dd508bb4" />
<img width="1919" height="990" alt="image" src="https://github.com/user-attachments/assets/8479d563-36d8-4129-8650-3bac033ec405" />


## Step 7: Check Object Ownership and ACL

1. In **Permissions**, locate **Object Ownership**.
2. Record the current configuration.

A common secure configuration is:

**Bucket owner enforced**

This means:

- ACLs are disabled.
- Objects are owned by the bucket owner.
- Access is controlled using policies.

<img width="1919" height="1020" alt="image" src="https://github.com/user-attachments/assets/a39175ce-6ff9-49e7-8e59-a133ecedaa81" />
<img width="1919" height="1015" alt="image" src="https://github.com/user-attachments/assets/ceb28edb-cbe1-4139-8cc0-5f3a39c4bbcd" />


## Step 8: Check Server Access Logging

1. Go to **Properties**.
2. Locate **Server access logging**.
3. Record whether it is:
   - Enabled
   - Disabled

### Security Purpose

Logging helps investigate suspicious or unauthorized access to the bucket.

<img width="1919" height="1015" alt="image" src="https://github.com/user-attachments/assets/9fb1fadd-7fd1-4abe-985b-75b900231aad" />
<img width="1919" height="1015" alt="image" src="https://github.com/user-attachments/assets/c8fb7ca5-6594-48b7-ba9b-3fc9f4a8a0d6" />




## Result

~~~
AWS S3 security configurations were analyzed and potential risks were identified.
~~~



