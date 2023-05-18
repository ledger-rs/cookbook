# Capital Gains

## Introduction

The calculation of the Capital Gains/Loss will depend on the method chosen for calculating the value of the holdings in an account.

Some standard ways of calculating the value include

- [First In, First Out](https://www.investopedia.com/terms/f/fifo.asp)
- [Average Cost Basis Method](https://www.investopedia.com/terms/a/averagecostbasismethod.asp), Investopedia
- LIFO
- Hight-Cost and Low-Cost
- Specific Identification Method

Choosing a method will have a huge impact on the resulting amount and the tax liability.

## Ledger Implementation

Ledger calculates Capital Gain/Loss based on the information contained in the [Lots](lots.md).

## Reports

A gain/loss report is created by using `-G` option.

For example:
```
ledger bal investments -G -X EUR
```
would show the balances report of the Investmens accounts, listing the gain/loss expressed in Euros.
