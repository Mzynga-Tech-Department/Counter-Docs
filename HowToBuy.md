## How to Buy

This part of the system covers the buyer facing flow.
It is made of several simple steps ordered as follows 
```
order → order1 → order2 → order3 → order4 → order5
```
A buyer should follow the following steps to purchae crypto from the platform.

### Step 1 :- [order](pages/orders/order.md)

This page initiates the buyer's order by showing asset price,dollar to KES exchange rate of the order,minimum and maximum purchase prices. 
Upon confimration the buyer locks in the order.

### Step 2 :- [order1](pages/orders/order1.md)

On this page the buyer locks in the amount in KES they are willing to spend on the transaction.
NB:- The maximum amount one can spend is KES 150,000 and the minimum is KES 150

### Step 3 :- [order2](pages/orders/order2.md)

The buyer enters the destination Ethereum wallet on which the ethereum bought will be sent.

### Step 4 :- [order3](pages/orders/order3.md)

On this page you will have locked order details i.e 
Ethereum price for this transaction in KES
Payment amount required for the transaction
Paybill number to recieve the payment
Receiving ETH amount
Receiving address
The order recieves a payment status of PENDING PAYMENT and it is preserved for 3 minutes before being purged

### Step 5 :- [order4](pages/orders/order4.md)

To move from step 4 above to this step the buyer makes payment to the required account and confirms the payment on this page by entering the payment code recieved from the payment provider.
NB:- The system is able to recieve notification of payments recieved by the payment gateway and process them accordingly updating order and releasing funds to the right address.

### Step 6 :- 

On this step the order will be confirmed showing the address that has recieved the Ethereum,the amount and the money in KES that has been paid for it.
All RPC request are powered by https://api.pocket.network
