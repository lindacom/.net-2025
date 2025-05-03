Working with files
-----------------------
ETL - extract, transform, load

Extract - Use system.IO - used to extract data from files.  Tryparse and error handling
Transform - LINQ - Language integrated query to query data and filter data

Write data from a create form to a text file (MVC app)
-----------------------------------------------------
Open the model file 
above the create statement that says (if(ModelState.IsValid) enter

```
TextWriter txt = null;

```
within the create statement that says (if(ModelState.IsValid) after the existing text that inserts data into the database add the following code before the return statement:

```
string JsonValue = Newtonsoft.json.JsonConvert.SerializeObject(@themodelname);
string curFile = "C:\\Users\\filepath\\filename.txt";

txt =new StreamWriter(curFile, append: true);
txt.WriteLine(JsonValue);
txt.Close();
```

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

Read the first line from a text file (MVC app)
---------------------------------------------

```
string[] lines = {};
string curFile = "c:\\Users\\path\\file.txt;
lines = System.IO.File.ReadAllLines(curFile);

<yourvariable> = JsonConvert.DeserializeObject< <yourobject> > (lines[0]);
```
