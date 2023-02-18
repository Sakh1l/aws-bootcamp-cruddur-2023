# Week 0 — Billing and Architecture


# Setting up the billing alert & Configuring AWS CLI on Gitpod Workspace

log-in to root account and go to billing dashboard on the consle tab and select budges tab below cost explorer and click on "creat budget". You can set two budget alerts for free using the aws free tier.
Also note, you can check the tab "free tier " tab below "cost allocation tag" service and check on the free-tier usage summary.

Step-2: Setting up IAM user account 

search IAM in console and select IAM service and creat the IAM user in the root account define the usergroup name and add administrator policy in the role.

don't forget to setup 2FA acess in the security settetings for both root account and IAM user account. 

now logout and login to IAM user in the login page select IAM user and provide the alias name set to the IAM user in the root account and once you logged in it will ask for IAM username (note this is the one that we defined in the usergroup name) and login.

Step3: download the gitpod browser extension for gitpod from this link according to your browser.

now, restart  go to your githup account and you can see the gitpod green button enabled.
Now click to open the gitpod codespace from your aws-cruddar-bootcamp main repo.

we need to install aws cli on the gitpod codespace, for that 

ps: we can enable aws autoprompt in cloudshell by typing "aws `[--cli-auto-prompt](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-options.html#cli-configure-options-cli-auto-prompt)`

do the sanity check to check we are in correct account when using cloudshell.

aws sts get-caller-identity  "sts - security token service" 

# AWS Pricing and Billing Walkthrough

Pricing Various region to region.

1. Click on Free-tier link to check the free-tier usage details.
2. Go to Billing preferences and tick the checkbox for "receive free-tier alert" and "receive billing alert" and save the preferences.
3. And on same page above "save preferences" click on Manage billing alerts link (this is basically a Cloudwatch aws managed service for monitoring usage metrics). This service is region specifc and present only N.Virgina
4. click on "Alarm" tab on the left services tab and expand to "in alarm" tab to creat or view the present billing alarm
5. Create alarm -> select Metrics -> select Billing -> Total  Estimated Changes -> select the USD charges and edit the metric name and modify the required conditions. Here set the define threshold value to $10 USD and click Next
6. Set Alarm state triger to "In alarm"  -> Select create new topic and provide the required name and email -> click creat new topic -> click Next 
7. 10 alarms are fee on the free-tier. Give the name to the alarm set and click "Next"
8. click finally on " Create Alarm" and you will get the green notification on top as successfully created alarm with the alarm name you set. 

# Cost Allocation Tags

Go to billing Dasboard from the user menu on the top right dropdown on your aws account user name.
after setting the budget alters (2 budget alerts are free) in budget tab got to cost allocation tag link and add the tags with key: value pair names based on your user defined names. This is a free form text. This will help to filter the services based on the tag names for report genrations later

# Cost Explorer 

Again go to Billing dashboard and select the cost explorer link under Cost Managment Tab to exploer on the report genaration as per the finance need for reconcliation. 

# Applying/Redeeming aws credit

Go to credits and click on redeem credit to apply the voucher code

# AWS Calculator

Go to https://calculator.aws click on create estimate to check the estimated cost by selecting the required services
