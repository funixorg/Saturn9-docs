# `readline`

Gets user input via `stdin`
## Syntax

```C
char *readline();
```

## Return value

Get a *character array **pointer*** namely a *string under **pointer*** ending with `\0` (null-terminated)

## Example

```C
char *string_out = readline();

printf("%s", string_out);
```