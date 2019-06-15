## Usefull regeual expressions

1. For getting JSON value by field name
```
(?<="<field_name>")\s*:\s*"(.*?)"
```

2. Mask IBAN
```
(?<=[a-zA-Z0-9]{2,2})([a-zA-Z0-9])(?=[a-zA-Z0-9]{4,4})
```

## RegEx exercises
1. RegExp that can find a value of a field in JSON which size is greater than the specified limit.
The value can contain any special characters (especially `",{}`), numbers and Latin letters.

## General rules
