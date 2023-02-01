# Search posting comments

An expression
```
comment =~ /REGEX/
```

is a regular expression that matches against a posting’s comment field. This searches only a posting’s field, not the transaction’s note or comment field.

Example:

```
ledger reg "expr" "comment =~ /landline/"
```
will match

```
2014/1/29  Phone bill
    Assets:Checking                           $50.00
    Expenses:Phone                           $-50.00  ; landline bill
```

but will not match

```
2014/1/29  Phone bill  ; landline bill
    ; landline bill
    Assets:Checking                           $50.00
    Expenses:Phone                           $-50.00
```

To search for transaction comments, see [Search comments](search-comments.md).
