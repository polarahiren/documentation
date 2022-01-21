# Updating Invoice Reference Number (Transaction Number)

###you can use below steps to update slot and hired invoices( transaction )

###Details you need before continue further
- `transactionNumber` *or* `transactionId`. 

###Steps

1. find transaction from above detail.
2. update transaction number manually in the database. **( make sure number is not already used in other transaction. )**
3. run below script to regenerate invoice, pass transaction id in it.
```
    CustomScripts::regeneratePdf(transactionId);
```
