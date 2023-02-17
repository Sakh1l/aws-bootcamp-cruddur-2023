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
