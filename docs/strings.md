# General notes
Strings are immutable.

[Strings docs](https://learn.microsoft.com/en-us/dotnet/csharp/programming-guide/strings/#string-escape-sequences)

For a list of all string escape sequences, visit the Strings docs and find the sentence *"String escape sequences"* on the page
# Concatenation
```cs
string firstName = "John" + " " + "Doe";
```

Or like this (preferred):
```cs
string name = string.Format("{0} {1}", firstName, lastName);
```

# Creating strings using `string.join`
```cs
int[] numbers = new int[3] { 1, 2, 3 };
string list = string.Join(",", numbers);
```

# String elements
```cs
string name = "John";
char firstChar = name[0];
```
