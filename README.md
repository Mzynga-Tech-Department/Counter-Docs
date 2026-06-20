# Counter-Docs


Self custody peer to peer ethereum market place
It is made up of 6 scalable services and couchdb to hold sessions

Services on POKT

-Confirmation service - confirmation - this exposes the endpoint that the payment provider write the receipt that have been paid

-Signer service - signer - this is the service that signs the ethereum amount and releases it to the buyer's wallet transaction when fiat payment is made nd confirmed by confirmation service
The rpc provider is api.pocket.network

-Generator service - generator - This service takes a 12 word seed phrase and uses the phrase to generate an ethereum wallet that acts as a treasury/wallet address.The rpc provider is api.pocket.network

-Heart Beat  - heartbeat - This service keeps a pulse on the entire RPC health by ensuring a blocknumber and restarting the provider if it fails.It acts a authentication middleware,generating request signatures.The rpc provider is api.pocket.network

Services not POKT

-API service - apicontainer - this exposes the endpoints that handle most CRUD operations

-CouchDB - couchdb - for persistence data storage - majorly consumed by API service 


