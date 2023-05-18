# Lots Basic Use

This is an illustration on the use of Lots.

Lots are created automatically when a price is specified for a commodity.

```ledger
2004-05-01 Stock purchase
    Assets:Broker                     50 AAPL @ $30.00
    Expenses:Broker:Commissions        $19.95
    Assets:Broker                  $-1,519.95
```    

This will create a lot of 50 units of AAPL, with the original cost of $30 per unit. The lot date is 2004-05-01.

The basic report is `ledger balance Broker --lots`.

The lots are specified for the sale transaction:

```ledger
2005-08-01 Stock sale
    Assets:Broker                    -50 AAPL {$30.00} [2004-05-01] @ $50.00
    Expenses:Broker:Commissions        $19.95
    Income:Capital Gains           $-1,000.00
    Assets:Broker                   $2,480.05
```

This transaction will precisely identify the lot to be sold and calculate the capital gains. For example, if you leave out the Capital Gains posting, the transaction will be reported as invalid by Ledger.
