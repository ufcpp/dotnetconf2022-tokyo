# Generic Attribute

## C# 10

```cs
class MyAttribute : Attribute
{
    private Type Type { get; }

    public MyAttribute(Type type)
        => this.Type = type;
}

[My(typeof(int))]
class MyClass
{ }
```


## C# 11

```cs
class MyAttribute<T> : Attribute
{ }

[My<int>]
class MyClass
{ }
```