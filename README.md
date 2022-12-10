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
                                  RUNTIME       |    Node.js 12.x
                                  PERMISSION    |    Use default
    
    ![create function](https://user-images.githubusercontent.com/94189602/206866513-1164ae14-4298-4e52-b233-cfba9d2a1a6b.PNG)
          
                        NEXT, THE WIZARD WILL AUTOMATICALLY DISPLAY THE DETAILS OF THE NEWLY FUNCTION CREATED
 
 STEP3: ADD A TRIGGER
 
 ![add triger](https://user-images.githubusercontent.com/94189602/206866868-0d85d75f-1a8b-4a5b-8e2e-cfb5dd165ddc.PNG)
 
 * On the Add trigger screen,select "s3" 
 
 * Select the s3 bucket name for the bucket
 
 * For Event Type, select "All object create events".
 
            THIS MEANS THAT ANYTIME A FILE IS CREATED OR UPLOADED TO THE SELECTED S3 BUCKET, THE LAMBDA FUNCTION WILL  BE TRIGGERED.
 

* Acknowledge the Recursive invocation message 

* Click the Add button. Congratulations, you've added a trigger!

STEP4: CONFIGURE TEST EVENT
