# Lots

## Sorting by Date

To sort the lots by date, the following command can be used on Linux:

```
ledger b --lots ass and vas_ax$ --no-total --flat | sort -t ' ' -k5

ledger -f file.dat bal account --lots | sort -t ' ' -k5
```

The expression below was created for this purpose but still has issues. Keeping it here for reference and a reminder.

```
ledger bal --lots "Account" -f myfile.dat \
-S 'lot_date(total) || date' -y "%Y-%m-%d" 
```
This will sort on the lot date of the total, or the date if
no lot date exists.
