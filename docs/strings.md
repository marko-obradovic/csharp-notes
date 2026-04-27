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

# Searching
```cs
// These return the index of the first, or last occurance of a letter/word
IndexOf('a');
LastIndexOf('a');

// This will take a start index, and then capture all the characters to the length you give
Substring(startIndex);
Substring(startIndex, length);

// Null checking
String.IsNullOrEmpty(str);
String.IsNullOrWhiteSpace(str);

// Splitting
str.Split(' ');

// Converting Strings to Numbers
string s = "1234";
int i = int.Parse(s);
// ToInt32 will give you zero if the string is null or empty, int.parse(s) will give you an exception
int j = Convert.ToInt32(s);

// Converting numbers to strings
string i = 1234;
int s = i.ToString(); // Output: "1234"
// You can also format the string
int t = i.ToString("C"); // Output: "$1,234.00"
int t = i.ToString("C0"); // Output: "$1,234"
```

[ToString Format Specifiers](https://learn.microsoft.com/en-us/dotnet/standard/base-types/formatting-types#the-tostring-method-and-format-strings)

# StringBuilder
Strings are immutable. Once you create a string object, you cannot modify its content.
In a situation where you have a lot of string manipulation operations, you can use a StringBuilder.

A StringBuilder is a mutable string object

Defined in the `System.Text` namespace

Not optimized for searching, so it DOES NOT give you methods like:
- `IndexOf()`
- `LastIndexOf()`
- `Contains()`
- `StartsWith()`
- ...

It DOES have methods like this:
- `Append()`
- `Insert()`
- `Remove()`
- `Replace()`
- `Clear()`

[Full StringBuilder API](https://learn.microsoft.com/en-us/dotnet/api/system.text.stringbuilder?view=net-10.0)
The main