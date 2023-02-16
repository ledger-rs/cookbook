# Reverse Stock Split

A Reverse Stock Split, per [Investopedia](https://www.investopedia.com/terms/r/reversesplit.asp), is a corporate action that consolidates the number of existing shares of stock into fewer (higher-priced) shares.

This reduces the number of shares outstanding and increases their price.

# Example

For holdings acquired as

```
2016-09-28 Buy EMLC
    Assets:Investments:Shares USD:EMLC  44 EMLC @ 19.10 USD
    Expenses:Commissions                 2 USD
    Assets:Investments:Cash USD
```

A reverse stock split would be entered as

```
2018-10-26 Reverse Stock Split
	; 1:2
	Assets:Investments:Shares USD:EMLC  -44 EMLC {19.10 USD} [2016-09-28]
	Assets:Investments:Shares USD:EMLC   22 EMLC {38.20 USD} [2016-09-28]
```

Which replaces the holding of 44 shares with 22 shares of EMLC, effectively halving them. The date of the lot remains the same. The price doubles from 19.10 USD to 38.20 USD. The net balance in USD is the same.
