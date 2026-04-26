A list is similar to an array in that it stores multiple elements of the same type, but unlike arrays, its size can change dynamically as items are added or removed.

To create a list:
```cs
var numbers = new List<int>();
```

`List<T>` is a _generic type_

[TODO] write more on generic types

You can also write the values you want stored the same way you do with arrays:
```cs
var numbers = new List<int>() { 1, 2, 3, 4 };
```

# Useful methods:
- Add()
- AddRange()
- Remove()
- RemoveAt()
- IndexOf()
- Contains()
- Count()

[Link to docs outlining all methods](https://learn.microsoft.com/en-us/dotnet/api/system.collections.generic.list-1?view=net-10.0)