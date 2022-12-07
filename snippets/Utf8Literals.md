# UTF-8 Literals

## C# 10

```cs
class Constants
{
    public static ReadOnlySpan<byte> a
        => new byte[] { (byte)'t', (byte)'r', (byte)'u', (byte)'e' };

    public static ReadOnlySpan<byte> b
        => new byte[] { (byte)'f', (byte)'a', (byte)'l', (byte)'s', (byte)'e' };

    public static ReadOnlySpan<byte> c
        => new byte[] { (byte)'n', (byte)'u', (byte)'l', (byte)'l' };

    public static ReadOnlySpan<byte> d
        => new byte[] { (byte)'$', (byte)'t', (byte)'y', (byte)'p', (byte)'e' };
}
```


## C# 11

```cs
class Constants
{
    public static ReadOnlySpan<byte> a
        => "true"u8;

    public static ReadOnlySpan<byte> b
        => "false"u8;

    public static ReadOnlySpan<byte> c
        => "null"u8;

    public static ReadOnlySpan<byte> d
        => "$type"u8;
}
```