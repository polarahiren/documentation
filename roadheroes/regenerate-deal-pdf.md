### Regenerate deal pdf.

- This can be useful, when an invalid pdf path is stored for deal. 
- You can execute below code block to regenerate deal pdf.

- eg.
```injectablephp
$deal = Deal::find($dealId);
$deal->savePdf();
```
- **CAUTION**: If our deal is customized, then please confirm the generated pdf with respective team member.
