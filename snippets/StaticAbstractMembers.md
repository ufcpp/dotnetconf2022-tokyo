# Static Abstract Members in Interfaces


```cs
using System.Numerics;

static T Sum<T>(IEnumerable<T> items)
    where T : INumber<T>
{
    var sum = T.Zero;
    foreach (var x in items)
        sum += x;
    return sum;
}

Console.WriteLine(Sum(new byte[] { 1, 2, 3, 4, 5 }));
Console.WriteLine(Sum(new int[] { 1, 2, 3, 4, 5 }));
Console.WriteLine(Sum(new float[] { 1, 2, 3, 4, 5 }));
Console.WriteLine(Sum(new double[] { 1, 2, 3, 4, 5 }));
Console.WriteLine(Sum(new decimal[] { 1, 2, 3, 4, 5 }));
```