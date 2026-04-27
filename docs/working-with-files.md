# System.IO

### File, FileInfo
Provides methods for creating, copying, deleting, moving, and opening files

They have very similar interfaces, the only difference is:

#### **File**: provides **static** methods
Use when:
- You're doing simple or one-off operations
- You don't need to keep referencing the same file

```cs
File.Delete("test.txt");
File.Copy("a.txt", "b.txt");
```

✔ Simple  
✔ No object creation  
✔ Great for quick scripts

#### **FileInfo**: provides **instance** methods
Use when:
- You’re working with **the same file repeatedly**
- You want **cleaner, object-oriented code**
- You want to access **file metadata easily**
```cs
var file = new FileInfo("test.txt");

file.CopyTo("copy.txt");
file.Delete();
```
✔ Groups operations around one file  
✔ Slightly cleaner for repeated use  
✔ Can cache some file metadata (like length, timestamps)

#### Useful methods
- `Create()`
- `Copy()`
- `Delete()`
- `Exists()`
- `GetAttributes()`
- `Move()`
- `ReadAllText()`

[Full list of methods for `File` and `FileInfo`](https://learn.microsoft.com/en-us/dotnet/api/system.io.file?view=net-10.0)
### Directory, DirectoryInfo
This works exactly the same way as File and FileInfo but with directories.
#### Useful methods
- `CreateDirectory()`
- `Delete()`
- `Exists()`
- `GetCurrentDirectory()`
- `GetFiles()`
- `Move()`
- `GetLogicalDrives()`

[Full list of methods for `Directory` and `DirectoryInfo`](https://learn.microsoft.com/en-us/dotnet/api/system.io.directory?view=net-10.0)
### Path
Provides methods to work with a string that contains file or directory path information

#### Useful methods
- `GetDirectoryName()`
- `GetFileName()`
- `GetExtension()`
- `GetTempPath()`

[Full list of methods for `Path`](https://learn.microsoft.com/en-us/dotnet/api/system.io.path?view=net-10.0)