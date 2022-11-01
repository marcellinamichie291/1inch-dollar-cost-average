# 1inch-dollar-cost-average

# 1inch-bot

1inch exchange trade bot that dollar cost averages the dips once every hour/day/week

# configuring the app

## install dependencies

`yarn` or `npm i`

## configure pairs, interval and timeframe

copy the `.env-example` and rename it to `.env`, adjust the values.

```
PUBLIC_KEY=""
PRIVATE_KEY=""
REFRESH_INTERVAL=10000
TRADEPAIRS=['WETHUSDC','WBTCUSDC']
DOLLAR_AMOUNT_PER_PURCHASE=10
MINUTES_BEFORE_NEXT_PURCHASE=60 * 24
PURCHASE_DIPS=true
CANDLES_TIMEFRAME=1h
```

## hook it up to your wallet

copy the `.env-example` and rename it to `.env`, adjust the values.

`REFRESH_INTERVAL` is the interval the bot updates prices/trades in milliseconds. The example is set to 1 minute

you can extract your public and private keys from your metamask browser extention.

\*\*Also be sure to approve the allowances in the 1inch app first, I still need to add a piece of code that approves the allowances in the bot.

# compiling and running the app

## compilation

be sure you have typescript installed

`tsc`

## running after compilation

`node dist/main`
