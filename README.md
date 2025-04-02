# AWS IAM Grant Temporary Permissions using Roles and STS

In this hands-on exploration of AWS Identity and Access Management (**IAM**), I walked through how to **grant temporary, scoped permissions** to a new IAM user by leveraging roles and AWS Security Token Service (STS).

Steps covered: 

a) **Create** a new **IAM user**

b) **Define a custom IAM role** with a trust relationship

c) **Create a policy** to allow s3:ListAllMyBuckets access

d) **Attach** the **policy to the role**

e) **Create** a new Amazon **S3 bucket**

f) Assume the role and successfully **listed all S3 buckets**

This approach ensures least-privilege access while enabling secure, time-bound operations — a best practice for managing access in AWS environments.

## 1. We login in AWS Console

We login AWS Console with an Admin User different to the Root User

![image](https://github.com/user-attachments/assets/bc0b9df7-b3f3-4c0f-ac6f-96465d328659)

We input the username and password

![image](https://github.com/user-attachments/assets/5cdde26d-ff81-4359-8671-6eff30b6cac2)

## 2. We Create a new User

We navigate to the IAM resource in AWS

![image](https://github.com/user-attachments/assets/9f409800-801a-4f5e-926b-97eeb4e4cf90)

We select Users menu option and we press the Create button for creating a new User

![image](https://github.com/user-attachments/assets/ac6a2828-96b8-4a7e-98b5-577c6bf0aacc)

![image](https://github.com/user-attachments/assets/dfeecf14-c723-4b75-84d5-cb0b713e8e2f)

![image](https://github.com/user-attachments/assets/f2b6c36b-aa44-4850-b870-d0cdc93e35a9)

![image](https://github.com/user-attachments/assets/007e01cf-f726-4fc7-9705-5699906039be)

![image](https://github.com/user-attachments/assets/6ea310dc-4873-49aa-b337-dfc5375249d6)

## 3. We Create a new Role

In the IAM resources we select Roles in the left hand side menu and we create a new role

![image](https://github.com/user-attachments/assets/adfa1db8-3d72-48c5-bdaa-290f66b195ed)

We select a Custom Trust Policy

![image](https://github.com/user-attachments/assets/ea4c62aa-062a-4793-bc3b-1d92839dfe85)

We input the Role definition

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Principal": {
        "AWS": "arn:aws:iam::954718177936:user/iam-test-user"
      },
      "Action": "sts:AssumeRole"
    }
  ]
}
```

![image](https://github.com/user-attachments/assets/a393feda-7dda-46fd-b924-c821db7d1e99)

We press the Create Role button and leave the other options with the default values

![image](https://github.com/user-attachments/assets/110adbfb-fa26-4f8f-af40-56bed7754954)

We can verify the new role was created

![image](https://github.com/user-attachments/assets/74c176cc-ed80-4ad3-98ad-ca7247f8b2f7)

## 4. We Create a new Policy

We navigate to IAM reources in AWS Console and we select Policies option

We create a new Policy

![image](https://github.com/user-attachments/assets/fa03c388-2ab1-442a-878b-7ef6bd347392)

We 



## 5. We Attach the Policy to the Role




## 6. We create a new S3 bucket



## 7. We list buckets in the S3











 
