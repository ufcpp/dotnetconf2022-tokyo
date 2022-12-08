# Newlines in Interpolations

## C# 10

```cs
var a = 1;
var b = 2;

// For $@"...", C# 10 or earlier is OK
var s = $@"a: {a
    }, b: {b}";
```


## C# 11

```cs
var a = 1;
var b = 2;

// For $"...", line break is allowed in C# 11 or later
var s = $"a: {a
    }, b: {b}";
```