# Print

The `print` command outputs the transactions the way they are entered in the journal. The output is automatically formatted. It will not display the balance assertions, for example.
The argument `--raw` can be used to output the transactions exactly like they were entered, including all the left-out bits.

This command, like other report commands, accepts query parameters which can be used to filter down transactions.

The advantage of this command is that the full transaction is displayed in the output, together with any comments. This can be used to parse the output by a software tool or just provide the full information to the user.

Example

The command
```
ledger print "expr" "note =~ /apple/"
```

outputs

```
2021-10-24 Local Market
    ; Apple Pencil 1
    Expenses:InfoComm:Hardware             50.00 EUR
    Assets:Cash

2021-12-26 Petra
    ; Apple headphones
    Expenses:InfoComm:AudioVideo            5.00 EUR
    Assets:Active:Cash EUR

2022-01-15 Giorgi
    ; Apple Lightning cables
    Expenses:InfoComm:Electronics           8.00 EUR
    Assets:Cash
```
