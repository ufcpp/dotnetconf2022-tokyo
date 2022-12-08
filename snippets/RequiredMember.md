# Required Member

```cs
var p = new Person  // Error : CS9035
{
    //Name = "xin9le",  // Required member ‘Person.Name’ must be set in the object initializer or attribute constructor. 
    Age = 38,
};

class Person
{
    public required string Name { get; init; }
    public required int Age;
}
```


```cs
class C
{
    // C# 11 : No warn
    public required string X { get; init; };

    // C# 10 : Suppress the compiler warning by null forgiving
    public string Y { get; init; } = default!;
}
```