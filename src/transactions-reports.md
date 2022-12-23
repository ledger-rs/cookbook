# Transactions

## Specific Transfers

To find transfers from a specific account (Checking) to another specific account (Liabilities:Something), one could try the following:

```
ledger print --raw Checking | ledger -f - reg Liabilities:Something
```

Unfortunately, this will not work if there are balance assertions on the Checking account.
