# Return of Capital

A company issues a Return of Capital event, returning the capital to the shareholders.

The returned funds are not income and therefore this is not a taxable event. But the dates need to be preserved to correctly calculate the capital gains/losses when the securities are disposed of in the future.

The event also adjusts the cost basis, affecting the price of the security.

## Syntax

The syntax for this case is as follows:

```
2000-01-01 * Bought IPE
   Assets:Investments:Broker:Shares:IPE     100 IPE {10.00 USD} [2000-01-01] @ 10.00 USD
   Assets:Investments:Broker:Cash      -1000.00 USD 

2019-04-01 * Return of capital
   Assets:Investments:Broker:Shares:IPE    -100 IPE {10.00 USD} [2000-01-01] @ 5.00 USD
   Assets:Investments:Broker:Shares:IPE     100 IPE { 5.00 USD} [2000-01-01] @ 5.00 USD
   Assets:Investments:Broker:Cash        500.00 USD
```

## Explanation

The first transaction is the original purchase of a security. It is used here for reference and comparison of the data points that need to be endered in the second transaction record.

In the first transaction we are using the full Lot syntax, explicitly specifying the date and the price although this is normally not necessary. The dates (`[2000-01-01]`) are inferred from the transaction date and the price from the price syntax (`@ 10.00 USD`). Here we are illustrating the example only.

The first transaction buys 100 units of IPE in the value of $1000.

The second transaction marks the Return of Capital event:

- 500 USD is returned to the investor
- 100 units of IPE, purchased at $10 is removed, "sold" at $5
- 100 unites of IPE added to the account with the same date and the price of $5

This results in

- $500 returned to the investor
- the remaining 100 units of IPE with the price of $5 have $500 total value

## References

- [Return of Capital: What It Is, How It Works, and Examples](https://www.investopedia.com/terms/r/returnofcapital.asp)
