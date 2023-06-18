
## Aave on Polygon mainnet 

Terminal 1: Fork Polygon mainnet using Alchemy and implement a flashloan

$ source .env
npx ganache-cli i --fork https://polygon-mainnet.g.alchemy.com/v2/$WEB3_ALCHEMY_POLYGON_ID \
--unlock $USDC_WHALE \
--unlock $DAI_WHALE \
--unlock $WETH_WHALE \
--networkId 999


Terminal 2: Run the test
$ source .env
env $(cat .env) npx truffle test --network polygon_main_fork test/test.js