## Regenerate Invoice PDF

- to regenerate invoice pdf in LB, just execute below command.
```
    tenant()->setTenant(Website::first());
    
    Invoice::find(invoiceID)->savePdf()
```