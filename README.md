# lambda

* Creating a lambda function connected to an s3 bucket.

#  Requirement: basic understanding of AWS

Overview: create an  s3 bucket, create a lambda fuction and connecting it to the s3 bucket.

Architecture

![ARCHITECTURE LAMBDA](https://user-images.githubusercontent.com/94189602/206864222-ddda1e80-9a6c-4e0e-a820-c2d912191bee.PNG)

            LET'S GO!!

STEP1: CREATE AN S3 BUCKET

* create an s3 bucket( we won't be going through that cause have already taught that already in my S3 BUCKET repo, so i would recommend you to look at that. Thats if you dont know how to create one.

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
 
            THIS MEANS THAT ANYTIME A FILE IS CREATED OR UPLOADED TO THE SELECTED S3 BUCKET, THE LAMBDA FUNCTION WILL BE TRIGGERED.
 

* Acknowledge the Recursive invocation message 

* Click the Add button. Congratulations, you've added a trigger!

STEP4: CONFIGURE TEST EVENT

* Click on the TEST button

 ![TEST NAV](https://user-images.githubusercontent.com/94189602/206868117-dcd8e99d-1967-48aa-a901-53dd2a1f5a13.PNG)

* Ensure the Event Template is HELLO WORLD

* For the Event name  "your choice"

* Update the JSON to the statement below, replacing the string value with your name or anything of your choice

                                    {
                                                "key1": "Place your name here"
                                    }
                                    
Step 5: Modify a Lambda Function

* Go to the Function code section, where you can view the following default JS code:

* Replace the code on Line 5 with the statement below, and save your code:
  
                                    body: JSON.stringify('Hello ' + event.key1 + ' from Lambda!'),

![code lambda](https://user-images.githubusercontent.com/94189602/206868559-3097f91e-7136-4461-8f63-411a08a07e6a.PNG)

* Deploy your saved function by clicking on the Deploy button at the top-middle of the current section.

* Edit the Basic Settings section, and save the following values and leave other fields as default, buh getting there go to the cofiguration button, under configuration by the left go to permission:

![basic settings](https://user-images.githubusercontent.com/94189602/206868932-aed81878-1511-4033-b692-9e11b11d3cfa.PNG)

                                    -Field                  |           Value
                                    Description             |           "your-choice"
                                    Timeout                 |           10 minutes
                                    
 * Make sure the Execution role filed uses an existing role.
 
 Step 6: Test a Lambda Function
 
* Click the Test function button.
 
* The output will be displayed in the Execution results section at the top. Expand the Details to review the output.
 Congratulations on writing your first Lambda function!

![test result](https://user-images.githubusercontent.com/94189602/206869262-89060530-7a55-4786-82f6-b48b4fb36e02.PNG)

Step 7: Add files to the  S3 bucket

* We already know how to do that.
 
 * Check if the Lambda function is triggered.
 
 * Go back to the Lambda console, and select your function to view its details.
 
 * Click on the Monitoring tab to view the metrics that show the number of times the Lambda function is triggered as a response to file(s) upload in the S3 bucket.
 
 ![monitor](https://user-images.githubusercontent.com/94189602/206869364-f6df0322-4f81-439c-9b27-7e3f853bf419.PNG)

* You can view the detailed Invocations chart in the CloudWatch console.

![new-metric](https://user-images.githubusercontent.com/94189602/206869427-4c769695-58ce-4c39-9721-9a31164a4c72.PNG)

* The detailed graph in the CloudWatch console shows that the Lambda function was triggered thrice. See the snapshot below.

![metric](https://user-images.githubusercontent.com/94189602/206869492-b99f8b46-6b75-4106-adc0-4d766bc7d19c.PNG)

                                    CloudWatch metrics showing the number of invocations of the Lambda function. Recall that anytime a file is created (or uploaded) to the selected S3 bucket, the lambda will be triggered.
                                    
# WE HAVE SUCCESSFULLY LEARNED LAMBDA. CONTRATULATIONS
