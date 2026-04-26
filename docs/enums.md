A datatype that represents a set of name/value pairs (constants).

E.g.:
Imagine an application for a post company, and it supports a few different shipping methods.

You can create an enum for all the methods:
```cs
public enum ShippingMethod {
	RegularAirMail = 1;
	RegisteredAirMail = 2;
	Express = 3;
}
```

This is the equivalent of doing this:
```cs
const int RegularAirMail = 1;
const int RegisteredAirMail = 2;
const int Express = 3;
```

But cleaner.

You use this because you want to group a number of related constants.

You can then use it with the dot notation:

```cs
var method = ShippingMethod.Express;
```

All the values in an enum are integers by default. You can change it like this:

```cs
public enum ShippingMethod : byte {
	RegularAirMail = 1;
	RegisteredAirMail = 2;
	Express = 3;
}
```

Check `csharp-notes.canvas` for more notes.