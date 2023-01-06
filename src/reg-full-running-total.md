# Full Running Total

You can list the transactions since the last month while displaying the full running total.

```shell
ledger reg checking -d "d>=[last month]"
```

The parameter `-d EXPR` or `--display EXPR` will limit the display to the postings specified in the EXPR, while the calculations will still include *all* the records.

The command above will result in a report that only displays the transactions since the last month, yet displaying the cummulative running total for all dates.

Example:

For the transactions

```ledger
2022-12-30 Allowance
    Income:Allowance
    Assets:Cash  150 EUR

2023-01-01 Party
    Expenses:Entertainment
    Assets:Cash  -100 EUR

2023-01-02 Coffee & donuts
    Expenses:Entertainment
    Assets:Cash  -10 EUR
```

the register report for all dates displays

```
22-Dec-30 Allowance             Assets:Cash                 150 EUR      150 EUR
23-Jan-01 Party                 Assets:Cash                -100 EUR       50 EUR
23-Jan-02 Coffee & donuts       Assets:Cash                 -10 EUR       40 EUR
```

But with the `-d` filter `ledger reg cash -d "date>=[2023-01-01]"` it will list

```
23-Jan-01 Party                 Assets:Cash                -100 EUR       50 EUR
23-Jan-02 Coffee & donuts       Assets:Cash                 -10 EUR       40 EUR
```

Note that the running total for the account is correct.

This may be useful for checking the transactions for a specific period on an account that has been active a long time, i.e. comparing bank statements.
