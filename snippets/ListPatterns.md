# List Patterns

```cs
static ReadOnlySpan<byte> RemoveBom(ReadOnlySpan<byte> utf8)
    => utf8 is [0xEF, 0xBB, 0xBF, .. var noBom]
    ? noBom
    : utf8;
```

```cs
static bool Palindrome(ReadOnlySpan<int> list)
    => list switch
    {
        [] or [_]
            => true,

        [var first, .. var rest, var last]
            => first == last
            && Palindrome(rest),
    };
```