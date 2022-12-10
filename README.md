# lambda

* Creating a lambda function connected to an s3 bucket.

#  Requirement: basic understanding of AWS

Overview: create an  s3 bucket, create a lambda fuction and connecting it to the s3 bucket.

Architecture

![ARCHITECTURE LAMBDA](https://user-images.githubusercontent.com/94189602/206864222-ddda1e80-9a6c-4e0e-a820-c2d912191bee.PNG)

            LET'S GO!!

STEP1: CREATE AN S3 BUCKET

* create an s3 bucket( we won't be going through that cause have already taught that already in my AWS STATIC WEBSITE repo, so i would recommend you to look at that. Thats if you dont know how to create one.

STEP2: CREATE A LAMBDA 

* From the aws management console page at the top search for lambda

![lamda_search](https://user-images.githubusercontent.com/94189602/206865032-98b2ae32-f4fa-42d9-aaaf-9b796f729e8d.PNG)

* when in the dashboard of lambda, use the create FUNCTION wizard button to create lambda function. 
 
![dashbard lambda](https://user-images.githubusercontent.com/94189602/206865387-83e10d96-2dbc-42a6-98ce-7dc5f5a2b96a.PNG)

* Select AUTHOR FROM SCRATCH option
* Use the following basic information below to create function

                                  -FIELD        |       VALUE     
                                  FUNCTION NAME |    Your choice
