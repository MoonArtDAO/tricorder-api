# tricorder-api

A web service for categorizing Solana transactions.

## API Overview

Tricorder provides a versioned API that returns human and computer readable events for a Solana transaction based on the [MoonRank](https://moonrank.app/) indexer.

### API Endpoints

At the moment, only the transaction categorization endpoint is live. It can be accessed at:

`https://tricorder.moon.art/[response version]/tx/[signature]`

Where `[response version]` is either `0` or `latest`, and `[signature]` is a Solana transaction signature.

An example request:
 `https://tricorder.moon.art/0/tx/4p8dzgWpwTZAcJBLGcWL9Wq2a9hsCu3ahHJidgRT9BLTbyu2tQz7r5H8261ZUwvRJFKEYMkyC3AzKWxU1biVdJAU`

### API Coverage

(Please open an issue if the program or event you'd like to see supported isn't on this list.)

#### Magic Eden v2 `(M2mx93ekt1fmXSVkTrUL9xVFHkmME8HTUi5Cyc5aF7K)`

##### Supported Events

All Magic Even v2 events are supported. 

| Event Type | Event ID |
|--|--|
| Listing | `nft.listing.create` ([example](https://tricorder.moon.art/latest/tx/3Eg82bcpVFRu1HPqkNT5phciPknoEcyC9mnnws7dSWnrpxuYvm9Go6u1q6jrLL2yH76QZRztRpHFjajsG6WCnZ9V))|
| Delisting | `nft.listing.cancel` ([example](https://tricorder.moon.art/latest/tx/55DKkW41WdMtjFMGsyfN1Lv4o1ZyCwASy87mwT62PsxFqbSZum3f3caYkVXwgXzBQGsftJw2eoPJyJqHD5HczKQo))|
| Sale | `nft.sale` ([example](https://tricorder.moon.art/latest/tx/4p8dzgWpwTZAcJBLGcWL9Wq2a9hsCu3ahHJidgRT9BLTbyu2tQz7r5H8261ZUwvRJFKEYMkyC3AzKWxU1biVdJAU))|
| Sale by offer | `nft.sale.offer` ([example](https://tricorder.moon.art/latest/tx/27QXb5eFojKtJ64rzY6exjH9235Rbr5xr39FsQgqeJGaecgoNLk1nRpZNK8iUhBsu85H8UWEdtYfSLHWZ687d1Fu))|
| Place Bid | `nft.bid.place` ([example](https://tricorder.moon.art/latest/tx/gQ1Jh2XhEqqRH76Cm6FVxEoEnWdyWPwCiYNGBohp4AYnzhuhZZSPg3n6naQDcBCzuQTaxM6qBqmw7PftqWiLkbg))|
| Cancel Bid | `nft.bid.cancel` ([example](https://tricorder.moon.art/latest/tx/5FCwf3zHFP6DQ9YHrzDdGu7ufzfX3gAwVXyxLSoazyh71XLWWBhTdTYtjdREqv1eTXWBrJo1GYKhK18tiscw941Q))|
| Deposit | `market.wallet.deposit` ([example](https://tricorder.moon.art/latest/tx/4U5Z2nSTayMdWZcnsu3dr3rDX7uwKjGYxmDFQZAq9DkB26P4p6prz8p9u1V6Dt5GwfcqnhYiUzCgu8JBRH7fMGWa))|
| Withdraw | `market.wallet.withdraw` ([example](https://tricorder.moon.art/latest/tx/2enVjNUrNZ6PymB5dKZbZVVX82KoUSsR75jK8kewRt6Ka6DdjdUFJbpoHuZhA2mbBwupWwDvMZPYwKMeVSMhcU7o))|
| Withdraw From Treasury | `market.treasury.withdraw` ([example](https://tricorder.moon.art/latest/tx/2wXe2ihoiZz6ARuKEGZzq1Mn1fF22Tk5umGohXNvVZy4ay6KXvEfTD2bt1Ck4nardJwwjyuzbJjUnqByFpCUddJg))|


#### Auction House`(hausS13jsjafwWwGqZTUQRmWyvyxn9EQpqMwV1PBBmk)`

Includes support for OpenSea, CoralCube and Solanart v2.

##### Supported Events

| Event Type | Event ID |
|--|--|
| Listing | `nft.listing.create` ([example](https://tricorder.moon.art/latest/tx/38815K1Ewjn66XnQhZ84jqEzvmevDwC2gYnE2zpLCXLynZeAfoZFsFAzBPiMje1vZhWhxSr8XkuJWcb9DPRcc4VN))|
| Delisting | `nft.listing.cancel` ([example](https://tricorder.moon.art/latest/tx/5bwrQwU35H3uri6mQdu3i9JT1hU94oyrmGxw5UQWcmd9aZu93qyqvcA5gmL6VaD9fDuX65soaVD4dUqDFzVKGMm1))|
| Sale | `nft.sale` ([example](https://tricorder.moon.art/latest/tx/s3fRmDFz2TP5fnv4BQCujD57c7TgsBvby8DLLEJ8ffXcThwyZVX6bYrUNPm9w3VQbWnPBPZSL4L2oXj5yqwzy9C))|
| Sale by offer | `nft.sale.offer` ([example](https://tricorder.moon.art/latest/tx/27QXb5eFojKtJ64rzY6exjH9235Rbr5xr39FsQgqeJGaecgoNLk1nRpZNK8iUhBsu85H8UWEdtYfSLHWZ687d1Fu))|
| Place Bid | `nft.bid.place` ([example](https://tricorder.moon.art/latest/tx/2DW1Rm5XhnwbuDVxzFhcdS9JMA3iQuVdHKubJQRTWmo7vB6CrnzC9MiT5kPQpw9YqXcyychkjd7mPvtfGi9wb1Gj))|
| Cancel Bid | `nft.bid.cancel` ([example](https://tricorder.moon.art/latest/tx/4XJYD9WcyNasUrQCeUCKCfx4rSGUpbmpwCmodTvBtqHhtV3zd4phjo4AdzP312STdcr1RchsFt2zoyXa1LA6qxEi))|
| Deposit | `market.wallet.deposit` ([example](https://tricorder.moon.art/latest/tx/4U5Z2nSTayMdWZcnsu3dr3rDX7uwKjGYxmDFQZAq9DkB26P4p6prz8p9u1V6Dt5GwfcqnhYiUzCgu8JBRH7fMGWa))|
| Withdraw | `market.wallet.withdraw` ([example](https://tricorder.moon.art/latest/tx/2enVjNUrNZ6PymB5dKZbZVVX82KoUSsR75jK8kewRt6Ka6DdjdUFJbpoHuZhA2mbBwupWwDvMZPYwKMeVSMhcU7o))|


#### Yawww `(5SKmrbAxnHV2sgqyDXkGrLrokZYtWWVEEk5Soed7VLVN)`

##### Supported Events

All Yawww events are supported.

| Event Type | Event ID |
|--|--|
| Listing | `nft.listing.create` ([example](https://tricorder.moon.art/latest/tx/ttmMedGgHy9yZEeBJPkTdGg2SvCT4WYEDTo56mh5apnrZ1epjSjFpWFPphbkKUhKAyvCgUaSfgkTHKf9CcDz7bv))|
| Delisting | `nft.listing.cancel` ([example](https://tricorder.moon.art/latest/tx/5bR7R2JiRU8jZc1Xv7ajkJ25dvs5QV11szzvtkfQJoW6eYkdLw3cB2ABgiyRZqFwfAmyeBcf2adxnnUUW8vSajgj))|
| Sale | `nft.sale` ([example](https://tricorder.moon.art/latest/tx/5aoZMjzBaiRu1L1nDWBVPME68FktnFgfdeXoEHTytDzkiK85J8PWArzY8AReovJAQGK24agqSBbdz9ZtxnCWX1uc))|
| Sale by offer | `nft.sale.offer` ([example](https://tricorder.moon.art/latest/tx/4r7mbGHAxXmVTbtfvSqZpUN4K32CTS46P7RjVDi1MEasTu1xPkoWG74AtwdLoKF9DScuFYjZ5BymgcThQPxPQ4QH))|
| Place Bid | `nft.bid.place` ([example](https://tricorder.moon.art/latest/tx/35bB8y3Qw6qaaaRDw1M5LM7yG1SYTvr776oYy6WFzLdTDawWZiR5R8u7cCYe7ur5rgayGBmbpbC5tHBQYkAc4z7U))|
| Cancel Bid | `nft.bid.cancel` ([example](https://tricorder.moon.art/latest/tx/3P8SWL9vtfLRp9Yy7xY5W3jqJ8bCYyBCUZpJFHJNuFMDEjYUYrfs1epbYYYdpFtfY6nsLT38fKxDELuDhysLRrTQ))|
