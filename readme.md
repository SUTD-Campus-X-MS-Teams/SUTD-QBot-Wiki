# SUTD QBot

## Deployment
Original guide could be found in the [UNSW QBot Repository](https://github.com/unsw-edu-au/QBot).

Here, we will detail the step-by-step process of deploying the application including setting up the Azure resources in case user is unfamiliar with the Azure ecosystem.

### 1. Setting Up Azure Subscription
First, in order to deploy any resources on Azure, we need a subscription set up. 
In portal.azure.com, go to the Subscriptions page and click on the "Add" button.
![](https://i.imgur.com/fUBdc0G.png)

For this deployment, leave all the details to default and click on the "Create" button.

:::info
Sanity check: The subscription plan takes about 10 minutes to create. Afterwardds, if you go to Home > Subscriptions, you should be able to see the new subscription plan.
:::

Next, if you are not the billing administrator of this project, you could modify the billing details of this project to another account.

First, navigate to `Cost Management + Billing` and click the triple dot on the relevant subscription, followed with `Transfer billing ownership`.

![](https://i.imgur.com/F7yDoti.png)
 