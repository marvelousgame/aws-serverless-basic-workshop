# Amazon S3

In this module you'll configure Amazon Simple Storage Service (S3) to host the static resources for your web application. 

## Implementation Instructions
Each of the following sections provide an implementation overview and detailed, step-by-step instructions. The overview should provide enough context for you to complete the implementation if you're already familiar with the AWS Management Console or you want to explore the services yourself without following a walkthrough.


### 1. Login to AWS Console
1. Go to your AWS Console

2. Login as IAM user which have enough privilege

3. Select AWS region: **N. Virginia**

### 2. Generate the SDK for your API

1. Go to **API Gateway** console

1. Click **SuperHeroes** API from the left pane

1. Click **Stages**, and choose **prod**

1. Click **SDK Generation** tab

1. For **Platform**, click **Javascript**

1. Click **Generate SDK**. You will automatically download a ZIP

1. Open the directory (your Downloads folder) and extract the contents of the ZIP to your local computer

1. Next, you will retrieve an HTML page that you will use to test your API. Go to [here](index.html)

1. Save the HTML file as **index.html**  
**Important**: When you save the index.html file, make sure you save it as a web page "HTML only". You only need the HTML of this page.

1. On your local computer, copy the **index.html** file and paste it into the extracted **apiGateway-js sdk** folder. Recall that you downloaded the ZIP file and extracted the contents to your local computer in previous steps.

1. Open index.html in your browser

1. Using the index web page, retrieve mission details. Review the output.

### 3. Integrate with S3 Static Website

- On the **Services** menu, click **S3**

- Click **Create Bucket** 

- Type a bucket name. Note that your bucket name must be unique. 

- For **Region**, click **US Standard**

- Click **Create**

- Click your bucket to open it, then click the **Properties** tab (at top right).

- In the **Permissions** section, click **Add Bucket Policy**.

- Copy the following bucket policy and paste it into editor.

```
{
"Version": "2012-10-17",  
"Statement": [   
{"Sid": "PublicReadForGetBucketObjects",
"Effect": "Allow",
"Principal": "*",
"Action": "s3:GetObject",
"Resource": "arn:aws:s3:::<my-unique-bucket-name>/*"
}
]
}
```

- Replace **<my-unique-bucket-name>** with the name of your bucket.

- Click **save**

- Click **Upload** (at the top left)

- Open the folder where you saved the Javascript SDK

- Select the **apiGateway-js-sdk** folder

- Drag and drop the whole folder into the Console target area (you will see a section labeled "Drag and drop files and folders to upload here").

- Click **Start Upload**. Wait until the upload is complete

- Open a new browser tab/window.

- Navigate to the following URL, replacing **<my-unique-bucket-name>** with the name of your S3 bucket.
`http://<my-unique-bucket-name>.s3-website-us-east-1.amazonaws.com/apiGateway-js-sdk/index.html  `

- You can now look up data stored in your DynamoDB database.