# Search Comments

An expression
```
expr note =~ /REGEX/
```
is a regular expression that matches against a transaction’s note field. This searches all comments in the transaction, including comments on individual postings.

The query
```
ledger reg "expr" "note =~ /landline/"
```

will match all the three examples below

```
2014/1/29  Phone bill
    Assets:Checking                           $50.00
    Expenses:Phone                           $-50.00  ; landline bill

2014/1/29  Phone bill  ; landline bill
    Assets:Checking                           $50.00
    Expenses:Phone                           $-50.00

2014/1/29  Phone bill
    ; landline bill
    Assets:Checking                           $50.00
    Expenses:Phone                           $-50.00

```

To search only posting comments, see [Search posting comments](search-posting-comments.md).

