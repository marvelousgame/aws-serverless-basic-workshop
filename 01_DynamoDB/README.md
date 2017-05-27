# Amazon DynamoDB

In this module you will create, configure, and insert record to DynamoDB table.

## Implementation Instructions
Each of the following sections provide an implementation overview and detailed, step-by-step instructions. The overview should provide enough context for you to complete the implementation if you're already familiar with the AWS Management Console or you want to explore the services yourself without following a walkthrough.


### 1. Login to AWS Console
1. Go to your AWS Console


2. Login as IAM user which have enough privilege


3. Select AWS region: **N.Virginia**

### 2. Create an Amazon DynamoDB Table

1. From the AWS Management Console, choose **Services** then select **DynamoDB** under Databases.

2. Choose **Create table**.

3. For **Table name**, type `SuperMission`

4. For **Primary Key**, type `SuperHero`

5. Under **Table settings**, make sure that **Use default settings** is selected.

6. Click **Create**

7. You will see a status that "Table is being created".

8. Once the table creation process is complete, go to **Overview** tab, in **Table details** make a note of your DynamoDB table's **ARN**
 - for example: arn:aws:dynamodb:us-east-1:999999999999:table/SuperMission

### 3. Insert Amazon DynamoDB Records

- Click the **Items** tab, then click **Create item**.
 
- System will pop up new window
 
- At the top left of your screen, switch to **Text** mode 

- You will see a text editor. Remove all the placeholder code.

- Copy the code below

```
{
  "SuperHero": "Superman",
  "Villains": ["Doomsday", "General Zod","Lex Luthor"],
  "MissionStatus": "In progress",
  "SecretIdentity": "Clark Kent"
}
```

- Paste the code into the editor

- Click **Save**

- Repeat the above steps with below items


```
{
  "SuperHero": "Batman",
  "Villains": ["Joker", "Bane","Ras Al Ghul"],
  "MissionStatus": "Complete",
  "SecretIdentity": "Bruce Wayne"
}
```

```
{
  "SuperHero": "Iron Man",
  "Villains": ["Apocalypse", "Doctor Doom","Loki"],
  "MissionStatus": "In Progress",
  "SecretIdentity": "Tony Stark"
}
```






