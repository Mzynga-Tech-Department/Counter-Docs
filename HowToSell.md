## How to sell

To sell Ethereum on counter you need to have a payment gateway configured.
The gateway must support Kshs and accounts of type MPESA Paybills.

This process involves several steps that are easy to set up.
To sell on counter you have to publish your sell orders in a dashboard.
The dashboard is public and is the entry point through which the system is accessible by buyer.
The set up of dashboard though needs an already configured account.

## Dashboard set up flow

```
welcome → termsandcondtions → instructions → setProfile → setAsset → genMne → setTreasury
```

### Setting up a dashboard

The flow is as follows 

Step 1 :- [Welcome](pages/dashboardOnboarding/welcome.md)
Confirms the indentity of the URL you are visiting and spells out the configured identity.

Step 2 : - [TermsConditions](pages/dashboardOnboarding/termsandcondtions.md)
Highlights the leagal boundaries that should be observed during the configuration of the dashboard and what are the defaults.

Step 3 : - [Instructrions](/pages/dashboardOnboarding/instructions)
This page is responsible for displaying the instructions on how to create dashboards and what are the limits that exist.

Step 4 : - [Set profile](/pages/dashboardOnboarding/setProfile)
On this page the seller creates a new dashboard profile.The maximum number of dashboards a seller can create at a time are 20 dashboards.

Step 5 : - [Set Asset](/pages/dashboardOnboarding/setAsset)
On this page the seller chooses which asset to support on the dashboard.The default chosen is Ethereum on Ethereum Mainnet.

Step 6 : - [Generate a wallet](/pages/dashboardOnboarding/genMne)
At this point the seller generates a wallet address that holds the crypto tokens that will be available for sale.The system takes a mnemonic phrase from the seller and generates a wallet address to sign the crypto that will be released.
The system does not save the mnemonic phrase.

Step 7 : - [Set Treasury](/pages/dashboardOnboarding/setTreasury) 
This is an important step since it combines step 5,6 into one treasury made up of the generated address,balance and withdrawal address
NB:- A withdrawal address is any ethereum address which is saved on the platform to allow for emergency withdrawals.The seller has full control of this address.

The UI repository is https://github.com/MikeMwambia-TrojanSystem/UI-Counter

The back end repository can be found at 
