# Transactions

## Specific Transfers

To find transfers from a specific account (Checking) to another specific account (Liabilities:Something), one could try the following:

```
ledger print --raw Checking | ledger -f - --permissive reg Liabilities:Something
```

In case you get errors in transactions with balance assertions, the first command can be run separately to create an intermediary file.

```
ledger print --raw Checking > temp.ledger
```

Then run the second report on this file.

```
ledger -f temp.ledger --permissive reg Liabilities:Something
```
