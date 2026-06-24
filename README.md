# Counter

Self custody peer to peer Ethereum market place.
This system currently supports accounts of type MPESA Paybill and Ethereum Token on Ethereum Mainnet.

The target user of this platform are individuals who want to sell and buy ethereum.
See the guides below :-

[How to buy](HowToBuy.md)

[How to sell](HowToSell.md)

The goal is to provide a self custody settlement layer for peer to peer transactions.

The seven modules powering this settlement layer are :-

-Confirmation service -  this exposes an endpoint for the payment gateway to write the receipt for payment that has been made,through fiat and for what crypto in this case Eth.

-Signer service - this is the service that signs the Eth amount that has been bought.The rpc provider is https://api.pocket.network

-Generator service - this service allows for generation of wallet address.Currently supporting Ethereum chain and has the ability to support more chains hence more tokens.

-Heart Beat  - this service keeps system monitored ensuring a RPC pulse every 5 secs,Validates orders and generates signatures.

-API service - this exposes the endpoints that handle all CRUD operations.

-CouchDB - for persistence data storage - majorly consumed by API service .

The entire system RPC is powered by https://api.pocket.network/