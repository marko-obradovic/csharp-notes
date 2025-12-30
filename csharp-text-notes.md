```c#
using System;

namespace HelloWorld
{
  class Program
  {
    static void Main(string[] args)
    {
      int w = 256; // Try 257, then 258, etc.
      byte y = (byte)w;
      string z = Convert.ToString(y, 2);
      Console.WriteLine("int: {0}\nbyte: {1}\nbinary: {2}", w, y, z);
    }
  }
}
```
You can see how a byte behaves when you push the byte limit past 255. It just resets



```c#
using System;

namespace HelloWorld
{
  class Program
  {
    static void Main(string[] args)
    {
      // This will change a before it assigns the value to b
      // So output would be a=2, b=2
      int a = 1; 
      int b = ++a; 
      Console.WriteLine("a={0}\nb={1}", a, b);
	  // This will change a after it assigns the value to b
      // So output would be a=2, b=1
      int a = 1; 
      int b = ++a; 
      Console.WriteLine("a={0}\nb={1}", a, b);
    }
  }
}
```