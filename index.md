# Build. Test. Deploy.

![Build. Test. Deploy.](https://dotnet.microsoft.com/static/images/refresh/home-hero.png)
.NET is the free, open-source, cross-platform framework for building modern apps and powerful cloud services.

# Write code your way
Write functionally or prodecurally with extension methods and modern language features.  
```csharp
using System;
using System.Linq;

var fbc = Enumerable.Range(1, 100)
    .Select(n => (n, Data: (n % 3 == 0, n % 5 == 0)))
    .Select(nd => nd.Data switch
            {
                (true, true) => "FB",
                (true, _) => "F",
                (_, true) => "B",
                _ => nd.n.ToString()
            });

Console.WriteLine(string.Join('\n', fbc));
```
