# `printf`

Format and print data in the terminal
## Syntax

```C
void printf(
	[in] const char  *format,
	...
);
```

## Parameters 

`[in] const char *format`

A string representing how the data is to be formatted using `%` + flag e.g. `%s`, `%d` like in C.
You can visit the heading about [formatting](#Formatting).

`...`

The additional parameters that are used to replace the `%` formatting with the values passed.
For example: `printf("%s", "string")`.

## Exception
> [Demonstration image](../Images/kernel_panic.png)

1. If you try to print to screen a **pointer with a wrong formatting flag** it will go into *kernel panic*.

```C
char *string_out = readline();

printf("%s", *string_out); // *string_out is a ERROR
```

## Formatting

In the `printf` or similar function you can format the output using the characters: `%` and `#`.

`%` + flag
You can use it to insert types and variables using the additional parameters, for example:

```C
printf("%d + %d = %d", 1, 1, 1+1);
```

`#` + `{0x+hex_color}`

> Only `printf` holds *RGB* coloring functionality

This version of `printf` features you to have *RGB* coloring using **hexadecimal as the formatting reference**, for example:

```C
printf("#{0xd16512} %s #{0x6d6d6d}", "Welcome to Saturn9");
```

### Basic formatting
| Flag | Type |
| ---- | ---- |
| d | Int |
| c | Char |
| s | String |
| x | HEX |
