# Regex date *YYYY-MM-DD* *YYYY/MM/DD* *YYYY.MM.DD*
Date regex matching months with 31 and 30 days and leap years.

## Regex
```re
/^(?:(?:[1-9]\d*)(\/|-|\.))(?:(?:(?:0?[13578]|1[02])(?:\1)31)|(?:(?:0?[13-9]|1[0-2])\1(?:29|30)))$|^(?:(?:(?:[1-9]\d*)?(?:0[48]|[2468][048]|[13579][26])|(?:(?:[12468][048]|[13579][26])00))(\/|-|\.)(?:0?2\2)29)$|^(?:[1-9]\d*)(\/|-|\.)(?:(?:0?[1-9])|(?:1[0-2]))\3(?:0?[1-9]|1\d|2[0-8])$/
```

## Patterns 
- Date separator group: `(\/|-|\.)`
- Repeat previous group: `\1` `\2` `\3`
- Years: `(?:[1-9]\d*)`
- 31 days months: `31(\/|-|\.)(?:0?[13578]|1[02])`
- 29 and 30 days months: `(?:29|30)(\/|-|\.)(?:0?[13-9]|1[0-2])`
- 29th of february: `29(\/|-|\.)0?2`
  - Leap year last two digits: `0[48]|[2468][048]|[13579][26]`
  - Leap years ending in 00: `(?:[12468][048]|[13579][26])00`
- Any DD-MM | D-MM | D-M | DD-M combination up to 28th day: `0?[1-9]|1\d|2[0-8])(\/|-|\.)(?:(?:0?[1-9])|(?:1[0-2])`

# Reference
Regex [dd-mm-yyyy](date-dd-mm-yyyy.md)