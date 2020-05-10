# airtable-formulas
A collection of Airtable formulas that I find useful.

### Extract URL from Attachment field
```javascript
MID({Attachment Field},FIND("(",{Attachment Field})+1,(FIND(")",{Attachment Field})-1)-(FIND("(",{Attachment Field})))
```

### Simple IF formula
```javascript
IF(
  {Field}=BLANK(),
  "",
  "Otherwise {Field}"
  )
```

### Remove some special characters, convert to lowercase, and change spaces to underscores
```javascript
SUBSTITUTE(
    SUBSTITUTE(
        SUBSTITUTE(
            SUBSTITUTE(
                SUBSTITUTE(
                    SUBSTITUTE(
                        SUBSTITUTE(
                            SUBSTITUTE(
                                SUBSTITUTE(
                                    SUBSTITUTE(
                                        SUBSTITUTE(
                                            SUBSTITUTE(
                                                SUBSTITUTE(
                                                    SUBSTITUTE(
                                                        SUBSTITUTE(
                                                            LOWER(Name),
                                                            " ",
                                                            "_"
                                                        ),
                                                        "'",
                                                        ""
                                                    ),
                                                    "/",
                                                    "_"
                                                ),
                                                "\"",
                                                ""
                                            ),
                                            "”",
                                            ""
                                        ),
                                        ":",
                                        "_"
                                    ),
                                    "“",
                                    ""
                                ),
                                "&",
                                "and"
                            ),
                            ".",
                            ""
                        ),
                        ",",
                        "_"
                    ),
                    "’",
                    ""
                ),
                "*",
                ""
            ),
            "/",
            ""
        ),
        "(",
        ""
    ),
    ")",
    ""
)```
