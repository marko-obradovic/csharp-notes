A data structure to store a collection of variables of the same type.

An array is an object behind the scenes.

So when you declare an array, internally, the compiler creates an instance of that class - that's why you need to allocate memory for it.

Arrays are zero indexed.

E.g.:
```cs
int[] numbers = new int[3];
```

you can then set them like this:

```cs
numbers[0] = 1;
numbers[1] = 2;
numbers[2] = 3;
```

Or you can use the object initialization syntax to declare what values you want to have:

```cs
int[] numbers = new int[3] {1, 2, 3};
```

And then this:

```cs
Console.WriteLine(numbers[0]);
Console.WriteLine(numbers[1]);
Console.WriteLine(numbers[2]);
```

would give you:

```
1
2
3
```