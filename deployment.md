# SUTD QBot Deployment
Original guide could be found in the [UNSW QBot Repository](https://github.com/unsw-edu-au/QBot).

Here, we will detail the step-by-step process of deploying the application including setting up the Azure resources in case user is unfamiliar with the Azure ecosystem.

## 1. Setting Up Azure Subscription
First, in order to deploy any resources on Azure, we need a subscription set up. 
In portal.azure.com, go to the Subscriptions page and click on the "Add" button.
![](https://i.imgur.com/fUBdc0G.png)

For this deployment, leave all the details to default and click on the "Create" button.

**Sanity check**: The subscription plan takes about 10 minutes to create. Afterwards, if you go to Home > Subscriptions, you should be able to see the new subscription plan.

Next, if you are not the billing administrator of this project, you could modify the billing details of this project to another account.

First, navigate to `Cost Management + Billing` and click the triple dot on the relevant subscription, followed with `Transfer billing ownership`. This will send a request to the email entered.

![](https://i.imgur.com/F7yDoti.png)
 
## 2. Creating a Resource Group
This step is optional, but recommended to collate all resources under this logical container. 
First, click on the search bar and find`Resource Groups`. Click create on the Resource Groups page, fill up the details, and finally click on "Create".
![](https://i.imgur.com/r0hvLuP.png)


## 3. Creating the Resources
The "base" resources required to deploy Q-Bot are detailed in the original repository. However, some of the services have been deprecated and/or rebranded. A more updated list of resources (as of May 2022) could be found here:


| #   | Resource Type          | Description                                                      |
| --- | ---------------------- | ---------------------------------------------------------------- |
| 1   | Resource Group         | App logical container                                            |
| 2   | Azure Bot              | (Previously Bot Channels Registration)                           |
| 3   | QnA Maker              | (Previously QnA Service and QnA Knowledge Base) QBot NLP Service |
| 4   | Azure Cognitive Search | (Previously from Azure Search Service) Supports QnA Maker        |
| 5   | SQL Database           | Stores processing data                                           |
| 6   | App Service            | Hosts QBot API Web Service                                       |
| 7   | App Service            | Hosts Dashboard Tab Angular App                                  |
| 8   | App Service            | Hosts Questions Tab Angular App                                  |
| 9   | App Registration       | Supports QBot API Authentication                                 |
| 10  | App Registration       | Supports Graph API Access                                        |
| 11  | Function App           | (Previously Azure Function) Supports QnA Maker                   |

Within the Resource Group created in the previous section, we will proceed to create each resource.
