[DateTime docs](https://learn.microsoft.com/en-us/dotnet/api/system.datetime?view=net-10.0)

DateTime objects are immutable. once you create them, you cannot change them.

**Usage Examples:**
```cs
var dateTime = new DateTime();

var now = DateTime.Now;
var today = DateTime.Today;

var nowMinute = now.Minute;
var nowHour = now.Hour;

var tomorrow = now.AddDays(1);
var yesterday = now.AddDays(-1);

Console.WriteLine(now.ToLongDateString());
// Output: Saturday, 23 May 2015
Console.WriteLine(now.ToShortDateString());
// Output: 23/05/2015
Console.WriteLine(now.ToLongTimeString());
// Output: 12:43:51 PM
Console.WriteLine(now.ToLongTimeString());
// Output: 12:43 PM
Console.WriteLine(now.ToString());
// Output: 23/05/2015 12:43 PM

```

```cs
// You can also provide a format specifier in the arguments of ToString
Console.WriteLine(now.ToString("yyyy-MM-dd HH:mm"));
// Output: 2015-05-23 12:43
```

[ToString Format Specifiers](https://learn.microsoft.com/en-us/dotnet/standard/base-types/formatting-types#the-tostring-method-and-format-strings)

# TimeSpan
Represents a length of time

[TimeSpan docs](https://learn.microsoft.com/en-us/dotnet/api/system.timespan?view=net-10.0)

# Creating TimeSpan objects:

```cs
// TimeSpan(hours, minutes, seconds)
var timeSpan = new TimeSpan(1, 2, 3);

// This is a bit unclear so we use the methods it comes with:
var timeSpan1 = TimeSpan.FromHours(1);

// You can also take 2 DateTime objects, subtract them, and you'll get a TimeSpan object.
var start = DateTime.Now;
var end = DateTime.Now.AddMinutes(2);
var duration = end - start;

Console.WriteLine("Duration: " + duration);
// Output: Duration: 00:02:00.0010000 (has a small delay)


// If you want to get the value placed in the minutes argument in TimeSpan():
Console.WriteLine("Minutes: " + timeSpan.Minutes);
// Output: 2

// If you want to get the entire length of time provided in the arguments added up, including hours, minutes and seconds, but in the format of minutes:
Console.WriteLine("Total Minutes: " + timeSpan.TotalMinutes);
// Output: 62.05
// (The equivalent of 1 hour, 2 minutes, and 3 seconds provided in TimeSpan(1, 2, 3))
// 


// TimeSpans are immutable, but you can use Add and Subtract methods to output what the value of the object would be when adding/subtracting another timespan object.
Console.WriteLine("Add example: " + timeSpan.Add(TimeSpan.FromMinutes(8)));
// Output: Add example: 01:10:03
Console.WriteLine("Subtract example: " + timeSpan.Subtract(TimeSpan.FromMinutes(2)));
// Output: Subtract example: 01:00:03

// So to be clear, this will not output 2016 years, but 2015 instead
var dateTime = new DateTime(2015, 1, 1);
dateTime.AddYears(1);
Console.WriteLine(dateTime.Year);
// It does not modify anything in place
// Internally, it creates a brand new DateTime with the updated year and returns it

// Converting to and from strings

// This is how you convert from a TimeSpan object TO a string
Console.WriteLine("ToString: " + timeSpan.ToString());
// Here, .ToString() will be greyed out because Console.WriteLine() already converts objects in its arguments to strings.
// But if you AREN'T using Console.WriteLine(), this is how you would convert to a string.

// This is how you convert FROM a string to a TimeSpan object
Console.WriteLine("Parse: " + TimeSpan.Parse("01:02:03"));
```