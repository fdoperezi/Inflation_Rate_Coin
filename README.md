# INFCoin

# Inflation Coin

Inflation, by definition, is a general increase in prices and fall in the purchasing value of money. In the last year alone, inflation has risen by 7% according to the Consumer Price Index, or CPI.
For our project, we created an ERC20 coin called INFCoin. We also created an INFCrowdSale to allow users to purchase tokens.  INFCoin, or Inflation Coin, uses the percent change in CPI to adjust the amount of the holder's tokens. The tokens are added or subtracted monthly, depending on if inflation increases or decreases.
For INFCoin, we created an ERC20 coin that includes a check inflation function.  The check inflation function checks for the percent change in inflation and then loops though an array of the current token holders, to add or subtract the tokens based on the inflation rate, to each token holder’s balance. This coin is a hedge against inflation.
Our coin is currently a proof of concept, as we still need to add an oracle to check inflation programmatically instead of manually.
To demonstrate:
First, we deployed the INFCoin sale. INFCoin sale inherited from crowdsale.  The CrowdSale contract uses the interface of ERC20 to sell the token, and for our token unique requirement of storing every owner address in an array, we had to modify the ERC20 interface to implement a function for adding to that array.
<img width="1429" alt="INFCoin Deployer" src="https://user-images.githubusercontent.com/87285522/149602309-bd6daffd-556d-4e04-891a-e51aadb78f01.png">
Then, we deployed the contract for the crowdsale using the token sale address generated by the coin sale contract.
<img width="1433" alt="INFCoin Crowdsale w:Token sale address" src="https://user-images.githubusercontent.com/87285522/149603764-3ef5531c-46f5-4fa2-a573-b951707bca65.png">
Following this, we purchased 1 ether's worth of tokens to our ganache wallet.
<img width="1432" alt="Buy Tokens at Ganache Address" src="https://user-images.githubusercontent.com/87285522/149603880-ccfaa5ef-bc33-45e5-b156-b7d4d08e704b.png">
Next, we deployed our INFCoin contract using our token address.
<img width="1435" alt=" INFCOIN contract w:token address" src="https://user-images.githubusercontent.com/87285522/149603964-be6c4b31-a067-4cd6-a7af-096edb3beab2.png">
Once the INFCoin contract was deployed, we checked our ganache account balance.
<img width="1434" alt="check balance of Ganache acct" src="https://user-images.githubusercontent.com/87285522/149603985-632991f2-429d-4cfa-94c9-e34f471f0c02.png">
In the next step we checked the inflation and checked to see our tokens increased.
<img width="1431" alt="check inflation and check adjusted balance" src="https://user-images.githubusercontent.com/87285522/149604092-b83b3ecc-5a7d-4083-8134-7ead5a2c987b.png">
Finally, we added INFCoin to our metamask wallet.
<img width="1297" alt="Add INF to Metamask " src="https://user-images.githubusercontent.com/87285522/149604588-f9386d85-fef5-4b4b-a560-7576d14433a3.png">
Inflation Coin is a store of value for your fiat currency that hedges against inflation, something your bank does not do.
