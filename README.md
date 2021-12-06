# utils-regex-list
Useful regex list to use as a reference.

## Date: [*DD-MM-YYYY* or DD-MM-YY](date-dd-mm-yyyy.md)
```re
/^(?:\d+(\/|-|\.))(?:(?:(?:0?[13578]|1[02])(?:\1)31)|(?:(?:0?[13-9]|1[0-2])\1(?:29|30)))$|^(?:(?:(?:(?:\d{2})?(?:0[48]|[2468][048]|[13579][26])|(?:(?:[12468][048]|[13579][26])00)))(\/|-|\.)(?:0?2\2)29)$|^(?:\d+)(\/|-|\.)(?:(?:0?[1-9])|(?:1[0-2]))\3(?:0?[1-9]|1\d|2[0-8])$/
```