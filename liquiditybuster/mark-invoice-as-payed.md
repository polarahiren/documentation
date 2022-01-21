## Mark Invoice As Payed

- Remember the Invoice ID
- Go to Transactions table
- Find subject_id by using Invoice ID
- You'll get Transaction ID
- Now follow below given steps

```
    tenant()->setTenant(Website::first());
    
    Transaction::find(transactionId)->forceMarkAsPayed(now());
    
```