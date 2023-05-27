Auction Engine Contract

This Solidity contract represents an auction engine where users can create auctions for various items. The contract allows sellers to create auctions with a starting price, duration, and discount rate. Bidders can participate in the auction by buying the item at the current price.

Features:
- Create Auction: Sellers can create new auctions by specifying the starting price, discount rate, item name, and optional duration.
- Get Price: Bidders can retrieve the current price for a specific auction based on the elapsed time and discount rate.
- Buy: Bidders can participate in an auction by sending the required funds to purchase the item. The contract calculates the final price, deducts a fee, and transfers the funds to the seller.

Usage:
1. Deploy the contract on the Ethereum network.
2. Call the `createAuction` function to create a new auction, specifying the starting price, discount rate, item name, and optional duration.
3. Use the `getPriceFor` function to retrieve the current price for a specific auction.
4. Call the `buy` function to participate in an auction, providing the auction index and the required funds.
5. After the auction ends, the contract emits the `AuctionEnded` event with the final price and the address of the winner.

This contract ensures that the starting price is greater than or equal to the product of the discount rate and the duration. It also applies a fee (10%) to the final price before transferring the funds to the seller.

Note: The contract includes a `withdraw` function that allows the contract owner to withdraw funds.

This contract is built using Solidity and demonstrates the implementation of an auction engine with basic functionalities.

## Testing

```
yarn hardhat test
