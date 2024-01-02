# `itoa`

Convert integer to string

## Syntax

```C
void itoa(
	[in] int     num,
	[out] char   str[],
	[in] int     base
);
```

## Parameters

`[in] int num`

Value to be converted to string

`[out] char str[]`

The array where the result of the conversion is saved

`[in] int base`

Numerical base, for example: $10$ means decimal base, $16$ hexadecimal, $8$ octal and $2$ binary

