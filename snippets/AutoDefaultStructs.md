# Auto Default Structs

## C# 10

```cs
var s = new Sample(1, 2);

struct Sample
{
    private int _x;
    private int _y;
    private int _z;

    public Sample(int x, int y)
    {
        // Error : CS0188
        Method();  // The 'this' object cannot be used before all of its fields are assigned to

        _x = x;
        _y = y;

        Method();
    }

    private void Method()
        => Console.WriteLine($"{_x}, {_y}, {_z}");
}
```



## C# 11

```cs
var s = new Sample(1, 2);

struct Sample
{
    private int _x;
    private int _y;
    private int _z;

    public Sample(int x, int y)
    {
        Method();  // _z is automatically initialized by 0.

        _x = x;
        _y = y;

        Method();
    }

    private void Method()
        => Console.WriteLine($"{_x}, {_y}, {_z}");
}
```