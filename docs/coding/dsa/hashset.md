# HashSet

- `HashSet` is store unique elements. 

- It like a box where you can put items, but you cannot put the same item in more than once. 

- If you trying to add an item that already in the box, it won't be added again.

### Example: 

```csharp
// Create a new HashSet of strings
HashSet<string> fruits = new HashSet<string>();

// Add some fruits to the HashSet
fruits.Add("Apple");
fruits.Add("Banana");
fruits.Add("Orange");
fruits.Add("Apple");  // Duplicate entry

// Display the contents of the HashSet
foreach (string fruit in fruits)
{
    Console.WriteLine(fruit);
}

```


### Result:

![hashset result](/img/hashset-example-result.png)

Since the duplicate are not allowed, "Apple" will be printed once. 