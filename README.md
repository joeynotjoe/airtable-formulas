# airtable-formulas
A collection of Airtable formulas that I find useful.

### Extract URL from Attachment field
`MID(GIF,FIND("(",GIF)+1,(FIND(")",GIF)-1)-(FIND("(",GIF)))`
