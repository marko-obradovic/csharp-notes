```
<access-modifier> class <class-name> {
	
}
```

e.g
```cs
public class Person {
	// Property
	public string Name;
	
	// Method
	public void Introduce() {
		Console.WriteLine("Hi, my name is " + Name);
	}
}
```

# Creating Objects and using their methods/properties:
```cs
Person person = new Person();
person.Name = "Mosh";
person.Introduce();
```

# Using a static modifier
```cs
public class Calculator {
	public void Add(int a, int b) {
		return a + b;
	}
}
```

We can access this method directly in the `Calculator` class itself. An object doesn't need to be created. 

You CANNOT access static members from objects.

Without the static modifier, you would create 3 objects of this class, each one in the memory will have the add method. But when you apply the static modifier, the add method will only be in one place in memory, and that is the calculator class itself.

The static modifier is used when you want to present a concept that only a single instance of that should exist in memory.

The `Main()` method is an example:

```cs
class Program {
	static void Main() {	
	}
}
```

It is a method that can only exist once in memory, that returns `null`.