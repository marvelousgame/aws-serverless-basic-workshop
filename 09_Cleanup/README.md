# Workshop Cleanup

This page provides instructions for cleaning up the resources created during the preceding modules.

## Resource Cleanup Instructions

- **S3** Cleanup
	- Go to **S3** console
	- Find YOUR_BUCKET
	- Empty YOUR_BUCKET
	- Delete YOUR_BUCKET
- **API Gateway** Cleanup
	- Go to **API Gateway** console
	- Select the API that you created
	- Delete the API
- **AWS Lambda** Cleanup
	- Go to **Lambda** console
	- Select the `GetHeroesList` function and delete
	- Select the `GetMissionDetails` function and delete
- **AWS IAM Role** Cleanup
	- Go to **IAM** console
	- Select **Roles** from the navigation menu
	- Find `lambda-supermission-role` and delete
- **DynamoDB Table** Cleanup
	- Go to **DynamoDB** console
	- Choose **Tables** in the navigation menu.
	- Choose the `SuperMission` table you created.
	- Delete table
- **CloudWatch Logs** Cleanup
	- From the AWS Console click **Services** then select **CloudWatch** under Management Tools.
	- Choose **Logs** in the navigation menu.
	- Select the **/aws/lambda/GetHeroesList** log group. If you have many log groups in your account, you can type `/aws/lambda/GetHeroesList` into the **Filter** text box to easily locate the log group.
	- Choose **Delete log group** from the **Actions** drop-down.
	- Choose **Yes, Delete** when prompted to confirm.
	- Repeat above steps for log group **/aws/lambda/GetMissionDetails**

