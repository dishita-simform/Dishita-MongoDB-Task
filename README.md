
# MongoDB Assignment

This repository demonstrates various MongoDB operations such as Batch Creation, Batch Update, Indexing, and Finding Duplicates using Aggregation.

# MongoDB Queries

1. Create Collection

```sql
db.createCollection("my_collection")
```
2. Get Collection Name
```sql
db.getCollectionNames()
```
3. Batch Create 100 Records in MongoDB
```sql
db.my_collection.insertMany([
  { name: "John", age: 28, city: "New York" },
  { name: "Alice", age: 25, city: "Los Angeles" },
  { name: "Bob", age: 30, city: "Chicago" },
  { name: "Charlie", age: 35, city: "San Francisco" },
  { name: "David", age: 40, city: "Miami" },
  { name: "Emma", age: 22, city: "Boston" },
  { name: "Frank", age: 50, city: "Seattle" },
  { name: "Grace", age: 31, city: "Dallas" },
  { name: "Hannah", age: 29, city: "Austin" },
  { name: "Ivy", age: 45, city: "San Diego" },
  { name: "Jack", age: 38, city: "Atlanta" },
  { name: "Kenny", age: 60, city: "Seattle" },
  { name: "Lily", age: 27, city: "Denver" },
  { name: "Megan", age: 33, city: "Washington D.C." },
  { name: "Nina", age: 24, city: "Phoenix" },
  { name: "Olivia", age: 41, city: "Miami" },
  { name: "Paul", age: 36, city: "Chicago" },
  { name: "Quincy", age: 30, city: "Los Angeles" },
  { name: "Rachel", age: 37, city: "Houston" },
  { name: "Steve", age: 47, city: "San Francisco" },
  { name: "Tina", age: 28, city: "New York" },
  { name: "Ursula", age: 32, city: "Boston" },
  { name: "Victor", age: 50, city: "Dallas" },
  { name: "Wendy", age: 22, city: "Austin" },
  { name: "Xander", age: 40, city: "Seattle" },
  { name: "Yara", age: 26, city: "San Diego" },
  { name: "Zach", age: 30, city: "Phoenix" },
  { name: "Aiden", age: 27, city: "New York" },
  { name: "Bella", age: 33, city: "Washington D.C." },
  { name: "Cody", age: 42, city: "Dallas" },
  { name: "Diana", age: 29, city: "Miami" },
  { name: "Eli", age: 36, city: "San Francisco" },
  { name: "Fiona", age: 50, city: "Seattle" },
  { name: "Gavin", age: 34, city: "Los Angeles" },
  { name: "Holly", age: 27, city: "Chicago" },
  { name: "Isaac", age: 41, city: "Boston" },
  { name: "Jasmine", age: 26, city: "Atlanta" },
  { name: "Kyle", age: 34, city: "Houston" },
  { name: "Lena", age: 31, city: "San Diego" },
  { name: "Mark", age: 45, city: "Phoenix" },
  { name: "Nadia", age: 38, city: "Dallas" },
  { name: "Owen", age: 32, city: "Seattle" },
  { name: "Penny", age: 29, city: "San Francisco" },
  { name: "Quinn", age: 33, city: "Los Angeles" },
  { name: "Reed", age: 40, city: "Chicago" },
  { name: "Sophia", age: 25, city: "Miami" },
  { name: "Tony", age: 37, city: "San Diego" },
  { name: "Ursula", age: 45, city: "Washington D.C." },
  { name: "Vera", age: 29, city: "New York" },
  { name: "Will", age: 41, city: "Phoenix" },
  { name: "Xander", age: 32, city: "Seattle" },
  { name: "Yasmine", age: 30, city: "Los Angeles" },
  { name: "Zane", age: 37, city: "Houston" },
  { name: "Amelia", age: 33, city: "San Francisco" },
  { name: "Brian", age: 48, city: "Dallas" },
  { name: "Clara", age: 24, city: "New York" },
  { name: "David", age: 50, city: "San Francisco" },
  { name: "Eleanor", age: 39, city: "Chicago" },
  { name: "Felix", age: 34, city: "Los Angeles" },
  { name: "Grace", age: 29, city: "San Francisco" },
  { name: "Henry", age: 52, city: "San Diego" },
  { name: "Isla", age: 36, city: "Seattle" },
  { name: "Jack", age: 25, city: "Dallas" },
  { name: "Kate", age: 44, city: "Miami" },
  { name: "Leo", age: 31, city: "Washington D.C." },
  { name: "Maya", age: 22, city: "Austin" },
  { name: "Nolan", age: 47, city: "Chicago" },
  { name: "Olga", age: 40, city: "Houston" },
  { name: "Piper", age: 38, city: "Los Angeles" },
  { name: "Quinn", age: 29, city: "Seattle" },
  { name: "Riley", age: 41, city: "San Diego" },
  { name: "Sam", age: 50, city: "Phoenix" },
  { name: "Tess", age: 35, city: "San Francisco" },
  { name: "Uma", age: 28, city: "Washington D.C." },
  { name: "Vince", age: 38, city: "New York" },
  { name: "Wes", age: 26, city: "Miami" },
  { name: "Xander", age: 42, city: "Phoenix" },
  { name: "Yara", age: 31, city: "Dallas" },
  { name: "Zoe", age: 33, city: "San Diego" },
  { name: "Alex", age: 29, city: "New York" },
  { name: "Beth", age: 34, city: "Houston" },
  { name: "Chloe", age: 25, city: "Los Angeles" },
  { name: "Derek", age: 39, city: "Seattle" },
  { name: "Eva", age: 30, city: "San Diego" },
  { name: "Fred", age: 32, city: "Phoenix" },
  { name: "George", age: 45, city: "Chicago" },
  { name: "Hilda", age: 36, city: "Washington D.C." },
  { name: "Ingrid", age: 50, city: "San Francisco" },
  { name: "Jackie", age: 41, city: "Dallas" },
  { name: "Kyle", age: 29, city: "Miami" },
  { name: "Lena", age: 38, city: "San Diego" },
  { name: "Mason", age: 33, city: "Houston" },
  { name: "Nina", age: 31, city: "Chicago" },
  { name: "Oscar", age: 28, city: "Seattle" },
  { name: "Paige", age: 36, city: "New York" },
  { name: "Quinn", age: 42, city: "Dallas" },
  { name: "Rita", age: 37, city: "Los Angeles" },
  { name: "Stan", age: 30, city: "San Francisco" },
  { name: "Tom", age: 44, city: "Miami" },
  { name: "Ursula", age: 29, city: "Austin" },
  { name: "Vanessa", age: 33, city: "Phoenix" },
  { name: "Walter", age: 41, city: "Houston" },
  { name: "Xander", age: 39, city: "Seattle" },
  { name: "Yasmin", age: 38, city: "San Francisco" },
  { name: "Zane", age: 40, city: "Los Angeles" }
]);

```
4. Batch Update Records with status= “Active” for those with age>30
```sql
db.my_collection.updateMany(
  { age: { $gt: 30 } },
  { $set: { status: "Active" } }
);
```
5. Indexing on 3 fields - name, age, city

```sql
// Create index on "name" field
db.my_collection.createIndex({ name: 1 });

// Create index on "age" field
db.my_collection.createIndex({ age: 1 });

// Create index on "city" field
db.my_collection.createIndex({ city: 1 });

```

```sql
db.my_collection.find(
    {
        age:{$gt:30}
    }
).explain("executionStats");
```
6. Finding Duplicate Values using Aggregation
```sql
db.my_collection.aggregate([
  { $group: { _id: "$name", count: { $sum: 1 } } },
  { $match: { count: { $gt: 1 } } }, 
  { $project: { _id: 0, name: "$_id", count: 1 } }, 
]);

``` 
