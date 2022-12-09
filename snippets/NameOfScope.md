# `nameof(parameter)` Scope


## C# 10
```cs
using System.Diagnostics.CodeAnalysis;

[return: NotNullIfNotNull("x")]
static string? Method(string? x)
    => x;
```



## C# 11
```cs
using System.Diagnostics.CodeAnalysis;

[return: NotNullIfNotNull(nameof(x))]
static string? Method(string? x)
    => x;
```