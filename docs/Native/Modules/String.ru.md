# String

## Доступные функции

### String_FindSubstr

```c++
cs_char *String_FindSubstr(cs_str str, cs_str strsrch);
```

### String_TrimExtension

```c++
cs_str String_TrimExtension(cs_str str);
```

### String_Compare

```c++
cs_bool String_Compare(cs_str str1, cs_str str2);
```

### String_CaselessCompare

```c++
cs_bool String_CaselessCompare(cs_str str1, cs_str str2);
```

### String_CaselessCompare2

```c++
cs_bool String_CaselessCompare2(cs_str str1, cs_str str2, cs_size len);
```

### String_Length

```c++
cs_size String_Length(cs_str str);
```

### String_Append

```c++
cs_size String_Append(cs_char *dst, cs_size len, cs_str src);
```

### String_Grow

```c++
cs_char *String_Grow(cs_char *src, cs_size add, cs_size *new);
```

### String_Copy

```c++
cs_size String_Copy(cs_char *dst, cs_size len, cs_str src);
```

### String_FormatError

```c++
cs_uint32 String_FormatError(cs_uint32 code, cs_char *buf, cs_size buflen, va_list *args);
```

### String_FormatBufVararg

```c++
cs_int32 String_FormatBufVararg(cs_char *buf, cs_size len, cs_str str, va_list *args);
```

### String_FormatBuf

```c++
cs_int32 String_FormatBuf(cs_char *buf, cs_size len, cs_str str, ...);
```

### String_LastChar

```c++
cs_char *String_LastChar(cs_str str, cs_char sym);
```

### String_FirstChar

```c++
cs_char *String_FirstChar(cs_str str, cs_char sym);
```

### String_AllocCopy

```c++
cs_str String_AllocCopy(cs_str str);
```

### String_GetArgument

```c++
cs_size String_GetArgument(cs_str args, cs_char *arg, cs_size len, cs_int32 index);
```

### String_CountArguments

```c++
cs_uint32 String_CountArguments(cs_str args);
```

### String_IsSafe

```c++
cs_bool String_IsSafe(cs_str str);
```

### String_FromArgument

```c++
cs_str String_FromArgument(cs_str args, cs_int32 index);
```

### String_ToInt

```c++
cs_int32 String_ToInt(cs_str str);
```

### String_StrToLong

```c++
cs_long String_StrToLong(cs_str str, cs_char **strend, cs_int32 radix);
```

### String_ToFloat

```c++
cs_float String_ToFloat(cs_str str);
```

### String_SizeOfB64

```c++
cs_size String_SizeOfB64(cs_size inlen);
```

### String_ToB64

```c++
cs_size String_ToB64(const cs_byte *src, cs_size len, cs_char *dst);
```

