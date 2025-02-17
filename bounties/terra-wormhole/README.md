# Terra - Wormhole

### Wormhole

DECODE - Which Chain the TX comes from.

```
SELECT 
 block_timestamp, msg_value:sender::string as sender, 
 HEX_ENCODE(BASE64_DECODE_BINARY(msg_value:execute_msg:submit_vaa:data::string)) as vaa_data,
 CASE 
   WHEN vaa_data ILIKE '%ec7372995d5cc8732397fb0ad35c0121e0eaa90d26f828a534cab54391b3a4f5%' THEN 'Solana'
   WHEN vaa_data ILIKE '%0000000000000000000000003ee18b2214aff97000d974cf647e7c347e8fa585%' THEN 'Ethereum'
   WHEN vaa_data ILIKE '%000000000000000000000000b6f6d86a8f9879a9c87f643768d9efc38c1da6e7%' THEN 'BSC'
   WHEN vaa_data ILIKE '%0000000000000000000000005a58505a96d1dbf8df91cb21b54419fc36e93fde%' THEN 'Polygon'
   ELSE 'Unknown Chain'
 END as emitter_chain
FROM terra.msgs
WHERE tx_id = '05A1DF7D5B88490E0652A47EE069092A3123FCF0B9F5EAF4D89FFF5C2C6C3ED4' -- sol test tx
```

## Bridges

{% embed url="https://github.com/certusone/wormhole/blob/14ba777cc179f0a5c5afb007c755a97cf921b261/explorer/.env.sample" %}

## Assets

{% embed url="https://github.com/scottincrypto/analytics/blob/e0d187d2f5f86c879a88a5aac5a7f4d9387186ef/data/wormhole_bridge_assets.csv" %}

## Tokens

{% embed url="https://github.com/forgxyz/flipside/blob/main/data/wh_token_addresses.csv" %}

## BEST SUBMISSIONS (To Be Sorted)

### QUESTION 101

https://jp12.medium.com/terra-wormhole-bridge-data-analysis-4147e06c07aa

https://www.techdreams.org/crypto-currency/terra-blockchain-users-wormhole-adoption/11276-20211124

https://app.flipsidecrypto.com/dashboard/101-elite-crypto-cosmology-part-1-wormhole-KTaVPE&#x20;

https://app.flipsidecrypto.com/dashboard/into-the-wormhole-Sqv35x&#x20;

https://app.flipsidecrypto.com/dashboard/crypto-cosmology-part-1-0-ioEB

### QUESTION 103

https://app.flipsidecrypto.com/dashboard/ust-wormhole-transfers-from-terra-DvStIo&#x20;

https://colab.research.google.com/drive/12KCDeXeoYZFAD8dSdYxhy94hRAL\_NcF5?usp=sharing&#x20;

https://app.flipsidecrypto.com/dashboard/into-the-multichain-verse-yJ4igh&#x20;

https://jp12.medium.com/wormhole-ust-analysis-740531efdd01&#x20;

https://app.flipsidecrypto.com/dashboard/from-wormhole-to-terra-q2LzZF&#x20;

https://app.flipsidecrypto.com/dashboard/from-terra-with-love-kYoQ8w&#x20;

https://app.flipsidecrypto.com/dashboard/103-elite-from-wormhole-to-terra-3\_utCM&#x20;

https://app.flipsidecrypto.com/dashboard/analysis-of-ust-sent-from-terra-through-wormhole-bridge-gna286&#x20;

https://colab.research.google.com/drive/1YAA8TKZ7FmGPMRubs0laNyzbbGQsvOJJ?usp=sharing&#x20;

https://app.flipsidecrypto.com/dashboard/103-elite-from-terra-with-love-z\_e8LY&#x20;

https://www.techdreams.org/crypto-currency/wormhole-terra-usd-ust-dashboard/11350-20211128&#x20;

https://scottincrypto.github.io/analytics/terra/wormhole/2021/12/01/UST-into-the-Wormhole.html&#x20;

https://app.flipsidecrypto.com/dashboard/from-terra-with-love-ust-transactions-via-wormhole-out-of-terra-6FmD1f https://app.flipsidecrypto.com/dashboard/103-elite-from-terra-with-love-TfzilA

### QUESTION 104

https://hexagonal-telescope-6b0.notion.site/Binance-Comparison-Analysis-ae865c30a9ad40f480cd32b61b2c4425 https://app.flipsidecrypto.com/dashboard/comparisons-of-transactions-from-terra-to-bsc-via-shuttle-and-wormhole-BGqEr\_&#x20;

https://app.flipsidecrypto.com/dashboard/104-elite-binance-comparison-3N9xy7&#x20;

https://analytics.zoho.in/open-view/213608000000013488/05e261732c278cafb1b9c93ea635d102&#x20;

https://app.flipsidecrypto.com/dashboard/104-elite-binance-comparison-terra-jCRVay&#x20;

https://colab.research.google.com/drive/1iwrS\_HZ5RPYWRlcvzElLG37RmLauUSI1?usp=sharing&#x20;

https://app.flipsidecrypto.com/dashboard/binance-bridge-and-wormhole-comparison-qAU573&#x20;

https://jp12.medium.com/bsc-terra-shuttle-bridge-vs-wormhole-a8533073295d&#x20;

https://colab.research.google.com/drive/1ueT5KrdAynpJFaOEFqSSavD7pJVOGZyy?usp=sharing&#x20;

https://app.flipsidecrypto.com/dashboard/terra-104-binance-shuttle-vs-wormhold-QQxReS&#x20;

https://app.flipsidecrypto.com/dashboard/terra-bounty-binance-comparison-rI9vgn&#x20;

https://app.flipsidecrypto.com/dashboard/comparison-of-bridges-terra-binance-smart-chain-TuoT8n&#x20;

https://colab.research.google.com/gist/YusefAN/eacb1473029a216af6e85df12d0de7af/-104-binance-comparison-zefwow-submission.ipynb#scrollTo=PQTIWA-TSqZp&#x20;

https://app.flipsidecrypto.com/dashboard/brads-bsc-comparison-terra-bridge-vs-wormhole-hkWgTG https://app.flipsidecrypto.com/dashboard/elite-binance-comparison-VJW0qN

