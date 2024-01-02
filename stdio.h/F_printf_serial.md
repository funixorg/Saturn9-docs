# `printf_serial`

Format and print data in the serial
## Syntax

```C
void printf_serial(
	[in] const char  *format,
	...
);
```

## Parameters

`[in] const char *format`

A string representing how the data is to be formatted using `%` + flag e.g. `%s`, `%d` like in C.
You can visit the heading about [formatting](F_printf.md#Formatting).

`...`

The additional parameters that are used to replace the `%` formatting with the values passed.
For example: `printf_serial("%s", "string")`.

