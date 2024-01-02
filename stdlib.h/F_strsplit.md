# `strsplit`

Divides strings using a delimiter, much like `tok_split` function
## Syntax

```C
char **strsplit(
	[in] char         *s,
	[in] const char   delim,
);
```

## Parameters

`[in] char *s`

The *string* that you want to split

`[in] const char delim`

*Delimiter* that will truncate the string

## Return value

Returns an array of *strings* (which are the *truncated parts*) under *pointer*