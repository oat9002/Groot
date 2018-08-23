# I am Groot
https://www.nuget.org/packages/Groot/1.0.0#
Just a CSV Util Package! keep it simple, let's groot do it for you!
# Features

Input Examples (CSV Format)
```csv
  name, tree_height
  groot, 36.468
  another_groot, 24.128
  more_groot, 24.35
```
- **Csv file to List of Key-Value** (string, string) Dictionary
```csharp
  var iamGroots = Groot.GetDictFromCsv(path);
  
  Console.WriteLine($"Groot's height is {iamGroots[0]["height"]}");
```
- **Csv file to List of Objects**
```csharp
  #Tree
  public class Tree
  {
        [GrootField("name")]
        public string name { get; set; }
        
        [GrootField("tree_height")]
        public decimal Height { get; set; }
  }
  
  //GrootField is the header column in csv files
  
  var iamGroots = Groot.GetObjectFromCsv<Tree>(path);
  Console.WriteLine($"Groot's height is {iamGroots[0].height}");
  
```
