
# NBA Game Day Notifications / Sports Alerts System

## **Project Overview**
This project is an alert system that sends real-time NBA game day score notifications to subscribed users via SMS or email. It leverages **AWS Lambda**, **Amazon SNS**, **Amazon EventBridge**, and **NBA API** (via SportsData.io) to provide sports fans with up-to-date game information. The system demonstrates cloud computing principles, efficient notification mechanisms, and serverless architecture.

### **My Contributions:**
- Configured **AWS Lambda** functions to process API responses from the NBA SportsData.io API.
- Set up **Amazon SNS** for sending notifications via SMS and email to subscribers.
- Created **EventBridge** rules to automate the scheduled sending of game day notifications based on the NBA game schedule.
- Designed and implemented **IAM security policies** based on the principle of least privilege to ensure secure service interactions between Lambda, SNS, and EventBridge.

---

## **Features:**
- Fetches live NBA game scores using the **SportsData.io API**.
- Sends real-time score updates to users via **SMS/Email** using **Amazon SNS**.
- Automates notifications using a **cron-based schedule** in **Amazon EventBridge**.
- Implements security best practices with IAM roles and policies for least privilege.

---

## **Technical Architecture:**
![nba_API](https://github.com/user-attachments/assets/5e19635e-0685-4c07-9601-330f7d1231f9)

---

## **Technologies:**
- **Cloud Provider**: AWS
- **Core Services**: SNS, Lambda, EventBridge
- **External API**: NBA Game API (SportsData.io)
- **Programming Language**: Python 3.x
- **IAM Security**: Least privilege policies for Lambda, SNS, and EventBridge

---

## **Project Structure:**
```bash
game-day-notifications/
├── src/
│   ├── gd_notifications.py          # Main Lambda function code
├── policies/
│   ├── gb_sns_policy.json           # SNS publishing permissions
│   ├── gd_eventbridge_policy.json   # EventBridge to Lambda permissions
│   └── gd_lambda_policy.json        # Lambda execution role permissions
├── .gitignore
└── README.md                        # Project documentation
