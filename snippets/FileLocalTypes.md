# File Local Types

## A.cs

```cs
public static class Foo
{
    public static void Invoke()
    {
        var x = new FileLocalType();  // OK
        Console.WriteLine(x);
    }
}


file class FileLocalType
{ }
```


## B.cs

```cs
public static class Bar
{
    public static void Invoke()
    {
        var x = new FileLocalType();  // NG
        Console.WriteLine(x);
    }
}
```