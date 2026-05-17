# Task 3 - Create a Serverless Function using AWS Lambda and API Gateway

## Objective
The objective of this task was to create a serverless function using AWS Lambda that returns a JSON response and make it publicly accessible using API Gateway.

---

# Services Used
- AWS Lambda
- Amazon API Gateway
- Python 3.10

---

# Step 1: Creating the Lambda Function

1. Logged into AWS Management Console
2. Opened the Lambda service
3. Clicked on **Create Function**
4. Selected:
   ```bash
   Author from scratch
   ```
5. Entered function details:

| Setting | Value |
|---|---|
| Function Name | MyFirstFunction |
| Runtime | Python 3.10 |
| Architecture | x86_64 |

6. Clicked:
   ```bash
   Create Function
   ```

---

# Step 2: Adding the Code

Added the following Python code inside the Lambda editor:

```python
import json

def lambda_handler(event, context):
    return {
        'statusCode': 200,
        'body': json.dumps({
            'message': 'Hello from Serverless!',
            'status': 'Success'
        })
    }
```

Clicked:
```bash
Deploy
```

to save and deploy the function.

---

# Step 3: Testing the Function

1. Clicked:
   ```bash
   Test
   ```

2. Created a new test event named:
   ```bash
   test
   ```

3. Used the default JSON event:

```json
{
  "key1": "value1",
  "key2": "value2",
  "key3": "value3"
}
```

4. Executed the function successfully.

---

# Output Response

```json
{
  "statusCode": 200,
  "body": "{\"message\": \"Hello from Serverless!\", \"status\": \"Success\"}"
}
```

---

# Step 4: Adding API Gateway Trigger

1. Clicked:
   ```bash
   Add Trigger
   ```

2. Selected:
   ```bash
   API Gateway
   ```

3. Chose:
   ```bash
   HTTP API
   ```

4. Security Setting:
   ```bash
   Open
   ```

5. Added the trigger successfully.

AWS automatically generated a public API endpoint.

---

# Step 5: Final Output

Opened the generated API endpoint in the browser.

The Lambda function returned the JSON response successfully.

---

# Live API Endpoint

https://6em186373l.execute-api.ap-southeast-2.amazonaws.com/default/myfirstfunction

---

# Status

✅ Task Completed Successfully

---

# Learning Outcomes

Through this task, I learned:
- Basics of Serverless Computing
- Creating AWS Lambda Functions
- Using Python in Lambda
- Testing Lambda Functions
- Integrating API Gateway with Lambda
- Deploying Public APIs on AWS

---

# Author

Shreya Mittal
```
