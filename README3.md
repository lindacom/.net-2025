Arrays and colections
=======================
Arrays
------
Arrays are indicated by square brackets. You need to specify type. Arrays have a fixed size which is set when you create the array. Arrays contain positions.

N.b. you cannot mix types in an array

Array example
To create an array enter the following in a method:

```

// create new instance of the array
var groceryList = new string[3];

// add items to the array
groceryList[0] = "milk";
groceryList[1] = "cheese";
groceryList[2] = "Apples";

```

N.b. to make the array available enter public string [] groceryList outside of the method.

To crate an array and fill it at the same time:

var groceryList = new string [3] {"milk", "chese", "apples"}

To get items in the array by index:

groceryList[2] or Console.WriteLine(groceryList[2]);

To resize the array:

array.Resize(ref groceryList, 6);

You can then add more items to the array. N.b. ref you can get a variable by reference.

To access all items in the array you can use a for each loop. e.g.

foreach (var grocery in groceryList) { Console.WriteLine(grocery); }

Multidimensional array
-------------------------
To create an array with three rows and four values(coluns similar to a spreadsheet):
```

var multi = new int[3,4] {
{0, 1, 2, 3}
{4, 5, 6, 7}
{8, 9, 10, 11}
};

```

You can access the multi array by row and position e.g multi [2,3] will return 11.

Lists
=======
No need to specify size. Uses system.collection.gneric. Before method ener public List sauces{get; set;}

To create a list:

var awesomeSauces = new List();

To add to list:

awesomeSauces.add("tobasco");

To get an item

awesomeSauces[0]

N.b. you can also sort (sort() to sort alphabetically) and reverse items in a list.

Linq
-------
Language integrated query - to operate on lists and collections

.sum() .Average() .Where(item -> item >=3) - this will return items in list that are greater or equal to three

Filter data using system.linq

```
public static string filename  @"c:\users\text.txt";

var start = "";
var end = "";

using (var text = new StreamReader(filename) {
var data = mydata.ReadRange(text, start, end);
}
```

Dictionary
=============
A dictionary Uses key value pairs. Need to specify type of key and type of value. Keys must be unique.

To create a dictionary:

var dictionaryWords = newDictionary<string, sring>();

To add to dictionary:

dictionaryWords.Add("var", "shorthand for variable");

To access dictionary item by key:

dictionaryWords["var"]

To count items in a dictionary:

dictionaryWords.count or Console.WriteLine("Count: {0}", dictionaryWords.Count);

To return all keys in a dictionary:

dictionaryWords.keys

To find an item in the dictionary by key:

Console.WriteLine("Keyvalue:{0}, dictionaryWords["var"]);

To search for an item in the dictionary by either key or value:

Console.WriteLine(dictionaryWords.ContainsKey("var"); Console.WriteLine(dictionaryWords.ContainsValue("shorthand for variable");
