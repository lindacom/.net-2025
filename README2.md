Working with files
-----------------------
ETL - extract, transform, load

Extract - Use system.IO - used to extract data from files.  Tryparse and error handling
Transform - LINQ - Language integrated query to query data and filter data

Read data from a file
------------------------------
```
private static string filename = @"c:\users\text.txt";

public void sampleFile() {
using (var text = new StreamReader(filename)) {
text.ReadLine();
var data = mydata.ReadAll(text);
}
}
```
