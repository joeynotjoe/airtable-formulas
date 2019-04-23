# airtable-formulas
A collection of Airtable formulas that I find useful.

### Extract URL from Attachment field
`MID({Attachment Field},FIND("(",{Attachment Field})+1,(FIND(")",{Attachment Field})-1)-(FIND("(",{Attachment Field})))`

### Simple IF formula
```IF(
  {Field}=BLANK(),
  "",
  "Otherwise {Field}"
  )```
