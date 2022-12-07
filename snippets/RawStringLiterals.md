# Raw String Literals

## C# 10

```cs
X.Parse("false", out bool x);
Console.WriteLine(x);

// <PackageReference Include="ScribanSourceGenerator" Version="1.0.0" />

[ScribanSourceGeneretor.ClassMember(@"{{
$types = [""bool"",""byte"",""sbyte"",""short"",""ushort"",""int"",""uint"",""long"",""ulong"",""float"",""double"",""DateTime"",""DateTimeOffset"",""TimeSpan""]
for $t in $types
~}}
    public static void Parse(string s, out {{$t}} x) => x = {{$t}}.Parse(s);
{{ end }}")]
static partial class X
{ }
```


## C# 11

```cs
X.Parse("false", out bool x);
Console.WriteLine(x);

// <PackageReference Include="ScribanSourceGenerator" Version="1.0.0" />

[ScribanSourceGeneretor.ClassMember("""
    {{
    $types = ["bool","byte","sbyte","short","ushort","int","uint","long","ulong","float","double","DateTime","DateTimeOffset","TimeSpan"]
    for $t in $types
    ~}}
        public static void Parse(string s, out {{$t}} x) => x = {{$t}}.Parse(s);
    {{ end }}
    """)]
static partial class X
{ }
```