## Setup
- create an `.env` file with `apiKey`, `apiURL` in it
- `npm i`: install the dependencies




## FYI

- First of all, we have to get the blocks for querying later by running: 
  - `node ./scripts/getDailyBlocks.js` 
- Now we're ready to extract the spot prices from 1inch aggregator: 
  - `node ./scripts/get1InchSpotPrices.js`
- The same has to be done in order to get the cl price feed answers:
  - `node ./scripts/getChainlinkPrices.js`
- Then, compute the disrepancy by running:
  - `node ./scripts/computeDiscrepancy.js`


### Note
- In order to query a huge amount of blocks, it's recommended to query by parts and then merge those parts into a single .json file for further analysis. 
  - The `./scripts/merger.js` is there just in case of that reason. 