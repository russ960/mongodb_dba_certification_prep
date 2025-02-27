**1.1 Identify the characteristics of MongoDB.**

1\. Which of the following best describes MongoDB?  
a) A relational database management system  
b) A NoSQL document-oriented database  
c) A graph-based database  
d) A key-value store

2\. Which of the following is NOT a characteristic of MongoDB?  
a) Schema-less design  
b) Horizontal scaling  
c) Uses SQL for queries  
d) Stores data in BSON format

3\. What type of data storage does MongoDB use?  
a) Tabular format  
b) JSON-like documents  
c) Flat files  
d) Key-value pairs only

4\. Which of the following is a key feature of MongoDB's scalability?  
a) Vertical scaling only  
b) Horizontal scaling with sharding  
c) Single-node database clusters  
d) Only supports on-premise deployment

5\. How does MongoDB handle relationships between data?  
a) Using foreign keys like SQL databases  
b) By embedding documents and using references  
c) Through predefined joins in the schema  
d) It does not support relationships at all

Answer Page  
b) A NoSQL document-oriented database  
c) Uses SQL for queries  
b) JSON-like documents  
b) Horizontal scaling with sharding  
b) By embedding documents and using references

**1.2 Identify the differences between a MongoDB and RDBMS database.**

1\. Which of the following is a key difference between MongoDB and RDBMS?  
a) MongoDB uses tables, while RDBMS uses collections  
b) RDBMS stores data in JSON, while MongoDB uses tables  
c) MongoDB is schema-less, while RDBMS requires a predefined schema  
d) Both MongoDB and RDBMS require predefined schemas

2\. In MongoDB, relationships between data are typically handled by:  
a) Foreign keys  
b) Embedding documents or using references  
c) Complex joins  
d) Stored procedures

3\. Which of the following is a major advantage of MongoDB over RDBMS?  
a) Complex transactions and ACID compliance  
b) Built-in horizontal scaling and sharding  
c) Native support for SQL queries  
d) Strong schema enforcement

4\. How does MongoDB store data differently from an RDBMS?  
a) As key-value pairs  
b) In relational tables with rows and columns  
c) As JSON-like documents in collections  
d) In hierarchical file structures

5\. Which feature of RDBMS is not present in MongoDB by default?  
a) Document-oriented storage  
b) Horizontal scaling  
c) Multi-document ACID transactions  
d) Flexible schema

Answer Page  
c) MongoDB is schema-less, while RDBMS requires a predefined schema  
b) Embedding documents or using references  
b) Built-in horizontal scaling and sharding  
c) As JSON-like documents in collections  
c) Multi-document ACID transactions

**1.3 Identify the methods to access and administer a MongoDB.**

1\. Which command-line tool is commonly used to interact with MongoDB?  
a) mongos  
b) mongod  
c) mongosh  
d) mysql

2\. How can an administrator check the status of the MongoDB server?  
a) db.status()  
b) show dbs  
c) db.runCommand({ serverStatus: 1 })  
d) systemctl start mongod

3\. What is the default port number for MongoDB?  
a) 3306  
b) 5432  
c) 27017  
d) 8080

4\. Which MongoDB shell command is used to switch to a different database?  
a) use \<database\_name\>  
b) db.switch(\<database\_name\>)  
c) connect \<database\_name\>  
d) db.change(\<database\_name\>)

5\. How can an administrator create an index on a MongoDB collection?  
a) db.collection.createIndex({ field: 1 })  
b) db.createIndex({ field: 1 })  
c) db.index({ field: 1 })  
d) create index on collection (field)

Answer Page  
c) mongo  
c) db.runCommand({ serverStatus: 1 })  
c) 27017  
a) use \<database\_name\>  
a) db.collection.createIndex({ field: 1 })

**1.4 Identify the function of sharding.**

1\. What is the purpose of sharding in MongoDB?  
a) To improve database security  
b) To enable vertical scaling  
c) To distribute large datasets across multiple servers  
d) To enforce a strict schema

2\. Which component of MongoDB manages sharded clusters?  
a) mongod  
b) mongos  
c) config servers  
d) Both b and c

3\. How does MongoDB determine which shard stores a document?  
a) Based on a primary key  
b) Using a shard key  
c) Randomly assigns data to shards  
d) Uses foreign keys

4\. What is a shard key in MongoDB?  
a) A key that encrypts data across shards  
b) A unique identifier for each document in a collection  
c) A field or fields that determine data distribution across shards  
d) A foreign key used for joining documents

5\. What happens if a poorly chosen shard key is used?  
a) The database operates normally  
b) Data is evenly distributed among shards  
c) Some shards may store significantly more data than others, causing performance issues  
d) MongoDB will automatically balance the shards

Answer Page  
c) To distribute large datasets across multiple servers  
d) Both b and c  
b) Using a shard key  
c) A field or fields that determine data distribution across shards  
c) Some shards may store significantly more data than others, causing performance issues

**2.1 Given a scenario with a type of structured document that needs to be inserted into a database, identify properly and improperly formed insert commands.**

1\. Which of the following is a correctly formatted insert command in MongoDB?  
a) db.collection.insertOne({ "name": "Alice", "age": 25 })  
b) INSERT INTO collection VALUES ("Alice", 25);  
c) db.collection.insert({ name: "Alice", age: 25 })  
d) db.collection.add({ "name": "Alice", "age": 25 })

2\. Which of the following will correctly insert multiple documents into a collection?  
a) db.collection.insertMany(\[{ "name": "Alice" }, { "name": "Bob" }\])  
b) db.collection.insert({ "name": "Alice" }, { "name": "Bob" })  
c) INSERT INTO collection VALUES ("Alice"), ("Bob");  
d) db.collection.addMany(\[{ "name": "Alice" }, { "name": "Bob" }\])

3\. What is a potential issue with using insert() instead of insertOne() or insertMany()?  
a) insert() is deprecated in newer versions of MongoDB  
b) insert() only allows inserting one document at a time  
c) insert() requires a predefined schema  
d) insert() only works in transactions

4\. Which of the following is NOT a valid BSON data type that can be inserted in MongoDB?  
a) String  
b) Integer  
c) Table  
d) Object

\*5. What happens if an insert command is missing required fields?  
a) The document is inserted with null values for missing fields  
b) The insert fails unless a default value is provided  
c) MongoDB automatically generates missing fields  
d) The insert is rejected due to schema validation

Answer Page  
a) db.collection.insertOne({ "name": "Alice", "age": 25 })  
a) db.collection.insertMany(\[{ "name": "Alice" }, { "name": "Bob" }\])  
a) insert() is deprecated in newer versions of MongoDB  
c) Table  
a) The document is inserted with null values for missing fields (unless validation rules are enforced)

**2.2 Give an update scenario where an entire updated document (no update operators used) is provided, identify the output and how the database changed state.**  
Multiple Choice Questions  
1\. What happens when an update operation is executed without using update operators?  
a) Only the specified fields are updated  
b) The entire document is replaced with the provided document  
c) A partial update is performed  
d) MongoDB throws an error

2\. Given the following existing document:

json  
Copy  
Edit  
{ "\_id": 1, "name": "Alice", "age": 25, "city": "New York" }  
What will be the final state of the document after running the update command below?

js  
Copy  
Edit  
db.users.updateOne({ "\_id": 1 }, { "name": "Bob", "age": 30 })  
a)

json  
Copy  
Edit  
{ "\_id": 1, "name": "Bob", "age": 30, "city": "New York" }  
b)

json  
Copy  
Edit  
{ "\_id": 1, "name": "Bob", "age": 30 }  
c)

json  
Copy  
Edit  
{ "\_id": 1, "name": "Alice", "age": 30 }  
d) The command will fail

3\. Which method should be used to ensure only specific fields are updated while keeping the rest of the document unchanged?  
a) updateOne()  
b) replaceOne()  
c) updateMany()  
d) findAndModify()

4\. If an update operation replaces an entire document, what must be included to prevent errors?  
a) All previous fields, including \_id  
b) The $set operator  
c) An index on \_id  
d) The $replace operator

5\. How does MongoDB handle fields that existed in the original document but are missing in the updated document?  
a) They remain unchanged  
b) They are deleted  
c) They are set to null  
d) The update is rejected

Answer Page  
b) The entire document is replaced with the provided document  
b) { "\_id": 1, "name": "Bob", "age": 30 }  
a) updateOne()  
a) All previous fields, including \_id  
b) They are deleted

**2.3 Give an update scenario where $set is used, identify the output and how the database changed state.**  
Multiple Choice Questions  
1\. What is the purpose of the $set operator in MongoDB?  
a) To replace an entire document  
b) To update only the specified fields  
c) To delete a document  
d) To insert a new document

2\. Given the following existing document:

json  
Copy  
Edit  
{ "\_id": 1, "name": "Alice", "age": 25, "city": "New York" }  
What will be the final state of the document after running the command below?

js  
Copy  
Edit  
db.users.updateOne({ "\_id": 1 }, { $set: { "age": 30 } })  
a)

json  
Copy  
Edit  
{ "\_id": 1, "name": "Alice", "age": 30, "city": "New York" }  
b)

json  
Copy  
Edit  
{ "\_id": 1, "age": 30 }  
c)

json  
Copy  
Edit  
{ "\_id": 1, "age": 30, "city": "New York" }  
d) The command will fail

3\. What happens when $set is used on a field that does not exist in the document?  
a) The update is rejected  
b) The field is added to the document  
c) The document remains unchanged  
d) The database throws an error

4\. Which update method allows $set to be applied to multiple documents at once?  
a) updateOne()  
b) updateMany()  
c) replaceOne()  
d) findOneAndUpdate()

5\. What is the difference between using $set and omitting update operators in an update command?  
a) $set replaces the whole document, whereas omitting it only updates fields  
b) $set only modifies specified fields, while omitting update operators replaces the entire document  
c) $set deletes fields not included in the update  
d) There is no difference

Answer Page  
b) To update only the specified fields  
a) { "\_id": 1, "name": "Alice", "age": 30, "city": "New York" }  
b) The field is added to the document  
b) updateMany()  
b) $set only modifies specified fields, while omitting update operators replaces the entire document

**2.4 Give a scenario about updating a document and information about where it should be inserted if it does not exist, identify the upsert command that should be used.**  
Multiple Choice Questions  
1\. What does the upsert option do in an update operation?  
a) It updates an existing document only  
b) It inserts a document if no match is found  
c) It deletes a document if it does not exist  
d) It prevents updates

2\. Which command correctly performs an upsert operation?  
a)

js  
Copy  
Edit  
db.users.updateOne({ "name": "Alice" }, { $set: { "age": 25 } }, { upsert: true })  
b)

js  
Copy  
Edit  
db.users.upsert({ "name": "Alice" }, { "age": 25 })  
c)

js  
Copy  
Edit  
db.users.updateOne({ "name": "Alice" }, { $upsert: { "age": 25 } })  
d)

js  
Copy  
Edit  
db.users.insertOne({ "name": "Alice", "age": 25 }, { upsert: true })  
3\. If an upsert operation finds a matching document, what happens?  
a) The document is updated  
b) A new document is inserted  
c) The operation fails  
d) The database is locked

4\. What happens if an upsert operation does not find a matching document?  
a) A new document is inserted  
b) The database throws an error  
c) The update is skipped  
d) The operation fails

5\. Which method can use the upsert option?  
a) updateOne()  
b) updateMany()  
c) replaceOne()  
d) All of the above

Answer Page  
b) It inserts a document if no match is found  
a) db.users.updateOne({ "name": "Alice" }, { $set: { "age": 25 } }, { upsert: true })  
a) The document is updated  
a) A new document is inserted  
d) All of the above  
I’ll finish the last two topics in the next message\!

**2.5 Give a scenario where multiple documents need to be updated, identify the correct update expression.**  
Multiple Choice Questions  
1\. Which MongoDB method is used to update multiple documents in a collection?  
a) updateOne()  
b) updateMany()  
c) replaceOne()  
d) findOneAndUpdate()

2\. Given the following collection:

json  
Copy  
Edit  
\[  
  { "\_id": 1, "status": "pending" },  
  { "\_id": 2, "status": "pending" },  
  { "\_id": 3, "status": "approved" }  
\]  
Which command will update all "pending" statuses to "completed"?  
a)

js  
Copy  
Edit  
db.orders.updateOne({ "status": "pending" }, { $set: { "status": "completed" } })  
b)

js  
Copy  
Edit  
db.orders.updateMany({ "status": "pending" }, { $set: { "status": "completed" } })  
c)

js  
Copy  
Edit  
db.orders.update({ "status": "pending" }, { $set: { "status": "completed" } })  
d)

js  
Copy  
Edit  
db.orders.findAndModify({ "status": "pending" }, { $set: { "status": "completed" } })  
3\. What happens if an updateMany() operation is executed without a filter?  
a) It updates a single document  
b) It updates all documents in the collection  
c) It returns an error  
d) It does nothing

4\. How does MongoDB ensure atomicity when updating multiple documents?  
a) It locks the entire database  
b) Each document is updated in a separate atomic operation  
c) It wraps the update in a transaction automatically  
d) It uses foreign keys

5\. If you need to update multiple documents and return the modified documents, which method should be used?  
a) updateMany()  
b) findAndModify()  
c) updateOne()  
d) replaceOne()

Answer Page  
b) updateMany()  
b) db.orders.updateMany({ "status": "pending" }, { $set: { "status": "completed" } })  
b) It updates all documents in the collection  
b) Each document is updated in a separate atomic operation  
b) findAndModify()

**2.6 Give a findAndModify scenario where another operation is run concurrently, identify the output and how the database changed state.**  
Multiple Choice Questions  
1\. What does findAndModify() do in MongoDB?  
a) Finds a document and deletes it  
b) Finds a document, modifies it, and returns the updated document  
c) Finds a document and locks it for editing  
d) Modifies multiple documents at once

2\. Given the following command:

js  
Copy  
Edit  
db.users.findAndModify({  
    query: { "name": "Alice" },  
    update: { $set: { "age": 30 } },  
    new: true  
})  
What will be returned?  
a) The document before the update  
b) The document after the update  
c) All documents in the collection  
d) Nothing, since the update is performed in the background

3\. If another operation tries to update the same document at the same time, what happens?  
a) Both operations are executed sequentially  
b) The second operation fails  
c) Both updates are applied simultaneously  
d) The database locks all updates

4\. How does findAndModify() differ from updateOne()?  
a) findAndModify() allows retrieval of the modified document  
b) updateOne() updates multiple documents  
c) updateOne() returns the modified document by default  
d) findAndModify() cannot modify documents

5\. What is a common use case for findAndModify()?  
a) Batch updates across multiple documents  
b) Implementing atomic read-modify-write operations  
c) Creating new documents  
d) Deleting a collection

Answer Page  
b) Finds a document, modifies it, and returns the updated document  
b) The document after the update  
a) Both operations are executed sequentially  
a) findAndModify() allows retrieval of the modified document  
b) Implementing atomic read-modify-write operations  
**2.7 Give a scenario where a document should be deleted from the database, identify the delete expression that should be used.**

Which scenario best justifies deleting a document from the database?  
a) A user updates their profile information  
b) An order is canceled and should no longer exist in the system  
c) A new product is added to the catalog  
d) A user logs into their account

Which MongoDB method should be used to delete a single document?  
a) deleteMany()  
b) remove()  
c) deleteOne()  
d) drop()

What happens when you call deleteMany() with an empty filter?  
a) It deletes all documents in the collection  
b) It deletes the first document that matches the condition  
c) It throws an error  
d) It does nothing

Which of the following is the correct syntax for deleting all documents where status is "inactive"?  
a) db.collection.deleteMany({ status: "inactive" })  
b) db.collection.deleteAll({ status: "inactive" })  
c) db.collection.removeOne({ status: "inactive" })  
d) db.collection.drop({ status: "inactive" })

Which statement about delete operations in MongoDB is true?  
a) deleteOne() removes all matching documents  
b) deleteMany() removes only the first matching document  
c) deleteMany() removes all matching documents  
d) delete operations are not supported in MongoDB

Answers:  
b) An order is canceled and should no longer exist in the system\\  
c) deleteOne()  
a) It deletes all documents in the collection  
a) db.collection.deleteMany({ status: "inactive" })  
c) deleteMany() removes all matching documents  
**2.8 Give a scenario where a single document should be looked up by a simple equality constraint (e.g., {x:3}), identify the expression that should be used.**

Which MongoDB method is used to find a document with a simple equality condition?  
a) findOne()  
b) findAll()  
c) getOne()  
d) retrieve()

What will the query findOne({ name: "John" }) return?  
a) All documents with the name "John"  
b) Only the first document with the name "John"  
c) No documents  
d) The last document with the name "John"

Which of the following expressions retrieves a document where "age" is 30?  
a) db.collection.findOne({ age: 30 })  
b) db.collection.findOne({ age: { $gt: 30 } })  
c) db.collection.findAll({ age: 30 })  
d) db.collection.get({ age: 30 })

What is the difference between find() and findOne()?  
a) find() returns multiple documents; findOne() returns a single document  
b) find() returns a single document; findOne() returns multiple documents  
c) There is no difference  
d) findOne() requires an index, while find() does not

Which of the following is the correct syntax for finding a document where "category" is "electronics"?  
a) db.collection.findOne({ category: "electronics" })  
b) db.collection.find({ category: "electronics" })  
c) db.collection.search({ category: "electronics" })  
d) db.collection.retrieve({ category: "electronics" })

MongoDB Test Answers

Answers  
a) findOne()  
b) Only the first document with the name "John"  
a) db.collection.findOne({ age: 30 })  
a) find() returns multiple documents; findOne() returns a single document  
a) db.collection.findOne({ category: "electronics" })  
**2.11 Identify documents matched by an expression with $in.**  
Multiple Choice Questions  
1\. What does the $in operator do in a MongoDB query?  
a) Checks if a value is inside an array field  
b) Checks if a field’s value matches any value in a specified array  
c) Checks if a field exists in a document  
d) Filters documents based on a regular expression

2\. Given the following collection:  
\[  
  { "\_id": 1, "name": "Alice", "age": 25 },  
  { "\_id": 2, "name": "Bob", "age": 30 },  
  { "\_id": 3, "name": "Charlie", "age": 35 }  
\]  
Which query would return both Alice and Charlie?  
a)

db.users.find({ "age": { $in: \[25, 35\] } })  
b)

db.users.find({ "age": { $eq: \[25, 35\] } })  
c)

db.users.find({ "age": { $contains: \[25, 35\] } })  
d)

db.users.find({ "age": { $exists: \[25, 35\] } })  
3\. What happens if $in is used with an empty array?  
a) It returns all documents  
b) It returns an error  
c) It returns no documents  
d) It returns only the first document

4\. Which of the following queries correctly retrieves documents where the status field is either "active" or "pending"?  
a)

db.users.find({ "status": { $eq: "active", $eq: "pending" } })  
b)

db.users.find({ "status": { $or: \["active", "pending"\] } })  
c)

db.users.find({ "status": { $in: \["active", "pending"\] } })  
d)

db.users.find({ "status": "active", "status": "pending" })  
5\. Can $in be used on fields that contain arrays?  
a) Yes, it matches elements within arrays  
b) No, it only works with scalar values  
c) Only if combined with $elemMatch  
d) Only with numeric values

Answer Page  
b) Checks if a field’s value matches any value in a specified array  
a) db.users.find({ "age": { $in: \[25, 35\] } })  
c) It returns no documents  
c) db.users.find({ "status": { $in: \["active", "pending"\] } })  
a) Yes, it matches elements within arrays

**2.12 Identify documents matched by an $elemMatch expression.**  
Multiple Choice Questions  
1\. What does the $elemMatch operator do?  
a) Finds documents where an array field contains at least one element matching multiple conditions  
b) Checks if an element exists in an array  
c) Sorts elements within an array  
d) Joins two collections

2\. Given the following document:

{ "\_id": 1, "grades": \[ { "subject": "Math", "score": 80 }, { "subject": "English", "score": 90 } \] }  
Which query finds documents where the grades array has an entry with "Math" and a score above 75?  
a)

db.students.find({ "grades": { "subject": "Math", "score": { $gt: 75 } } })  
b)

db.students.find({ "grades.subject": "Math", "grades.score": { $gt: 75 } })  
c)

db.students.find({ "grades": { $elemMatch: { "subject": "Math", "score": { $gt: 75 } } } })  
d)

db.students.find({ "grades": { $in: \[{ "subject": "Math", "score": { $gt: 75 } }\] } })  
3\. Can $elemMatch be used on non-array fields?  
a) Yes  
b) No  
c) Only in embedded documents  
d) Only with $in

4\. How does $elemMatch differ from using dot notation?  
a) $elemMatch matches multiple conditions within a single array element, while dot notation applies conditions separately  
b) They are the same  
c) $elemMatch is only used for sorting  
d) Dot notation allows deeper queries

5\. Which query correctly retrieves documents where the scores array contains at least one value greater than 85?  
a)

db.students.find({ "scores": { $elemMatch: { $gt: 85 } } })  
b)

db.students.find({ "scores": { $gt: 85 } })  
c)

db.students.find({ "scores": { $in: \[85\] } })  
d)

db.students.find({ "scores": { $all: \[85\] } })  
Answer Page  
a) Finds documents where an array field contains at least one element matching multiple conditions  
c) db.students.find({ "grades": { $elemMatch: { "subject": "Math", "score": { $gt: 75 } } } })  
b) No  
a) $elemMatch matches multiple conditions within a single array element, while dot notation applies conditions separately  
a) db.students.find({ "scores": { $elemMatch: { $gt: 85 } } })  
**2.13 Identify documents matched by an expression that has several logical operators.**  
Multiple Choice Questions  
1\. Which of the following is a valid logical operator in MongoDB?  
a) $and  
b) $or  
c) $not  
d) All of the above

\*\*2. Given the following query:

js  
Copy  
Edit  
db.users.find({ $and: \[ { age: { $gt: 25 } }, { age: { $lt: 40 } } \] })  
What will it return?  
a) Documents where age is greater than 40  
b) Documents where age is between 25 and 40 (exclusive)  
c) Documents where age is less than 25  
d) Documents where age is either greater than 25 or less than 40

3\. What does the following query do?

js  
Copy  
Edit  
db.products.find({ $or: \[ { price: { $lt: 10 } }, { category: "electronics" } \] })  
a) Finds all products where price is less than 10 AND category is "electronics"  
b) Finds all products where price is less than 10 OR category is "electronics"  
c) Returns an error due to incorrect syntax  
d) Ignores the $or condition and matches only category: "electronics"

4\. What will the following query return?

js  
Copy  
Edit  
db.orders.find({ $nor: \[ { status: "shipped" }, { status: "delivered" } \] })  
a) Orders with status "shipped" or "delivered"  
b) Orders with neither "shipped" nor "delivered" status  
c) All orders in the collection  
d) Orders that are either "shipped" or "delivered", but not both

5\. Which of the following statements is true regarding $not?  
a) $not negates the effect of any operator  
b) $not only works with $eq  
c) $not can be used alone as a logical operator  
d) $not is equivalent to $nor

Answer Page  
d) All of the above  
b) Documents where age is between 25 and 40 (exclusive)  
b) Finds all products where price is less than 10 OR category is "electronics"  
b) Orders with neither "shipped" nor "delivered" status  
a) $not negates the effect of any operator

**2.14 Given a query with a sort and limit, identify the correct output.**  
Multiple Choice Questions  
1\. What does the .sort() method do in MongoDB?  
a) Sorts documents in ascending or descending order  
b) Limits the number of documents returned  
c) Filters documents based on conditions  
d) Groups documents

2\. Given the following query:

js  
Copy  
Edit  
db.users.find().sort({ age: \-1 }).limit(2)  
What does it do?  
a) Returns all users sorted by age in ascending order  
b) Returns the first 2 users sorted by age in descending order  
c) Returns users older than 2 years  
d) Returns an error

3\. What is the correct order of operations when using .sort() and .limit() together?  
a) .limit() first, then .sort()  
b) .sort() first, then .limit()  
c) The order does not matter  
d) Both must be wrapped in an $aggregate query

4\. How do you retrieve the top 5 most expensive products from a collection?  
a)

js  
Copy  
Edit  
db.products.find().sort({ price: \-1 }).limit(5)  
b)

js  
Copy  
Edit  
db.products.find().limit(5).sort({ price: \-1 })  
c)

js  
Copy  
Edit  
db.products.find().sort({ price: 1 }).limit(5)  
d)

js  
Copy  
Edit  
db.products.find().order({ price: "desc" }).limit(5)  
5\. What happens if .limit(0) is used?  
a) It returns no documents  
b) It removes the limit, returning all matching documents  
c) It returns only the first document  
d) It returns an error

Answer Page  
a) Sorts documents in ascending or descending order  
b) Returns the first 2 users sorted by age in descending order  
b) .sort() first, then .limit()  
a) db.products.find().sort({ price: \-1 }).limit(5)  
b) It removes the limit, returning all matching documents

**2.15 Identify the incorrect projection among a set of expressions.**  
Multiple Choice Questions  
1\. Which projection correctly returns only the name field?  
a)

js  
Copy  
Edit  
db.users.find({}, { name: 1, \_id: 0 })  
b)

js  
Copy  
Edit  
db.users.find({}, { name: true })  
c)

js  
Copy  
Edit  
db.users.find({}, { name: 1, age: 1 })  
d)

js  
Copy  
Edit  
db.users.find({}, { name: "only" })  
2\. What happens if you mix inclusion and exclusion in a projection?  
a) MongoDB throws an error  
b) MongoDB ignores the exclusion fields  
c) MongoDB ignores the inclusion fields  
d) MongoDB allows both

3\. What does the projection { \_id: 0, email: 1 } do?  
a) Returns only the email field  
b) Returns both \_id and email  
c) Returns all fields except email  
d) Returns an error

4\. Which of the following is an incorrect projection?  
a)

js  
Copy  
Edit  
db.users.find({}, { name: 1, age: 0 })  
b)

js  
Copy  
Edit  
db.users.find({}, { \_id: 0, email: 1 })  
c)

js  
Copy  
Edit  
db.users.find({}, { name: 1, age: 1 })  
d)

js  
Copy  
Edit  
db.users.find({}, { \_id: 1, phone: 0 })  
5\. How do you exclude only the \_id field in a projection?  
a)

js  
Copy  
Edit  
db.users.find({}, { \_id: 0 })  
b)

js  
Copy  
Edit  
db.users.find({}, { \_id: false })  
c)

js  
Copy  
Edit  
db.users.find({}, { \_id: "hide" })  
d)

js  
Copy  
Edit  
db.users.find({}, { \_id: \-1 })  
Answer Page  
a) db.users.find({}, { name: 1, \_id: 0 })  
a) MongoDB throws an error  
a) Returns only the email field  
a) db.users.find({}, { name: 1, age: 0 })  
a) db.users.find({}, { \_id: 0 })  
**2.17 Given an aggregation expression using $match, $group, identify the correct output.**  
Multiple Choice Questions  
1\. What does the $match stage do in an aggregation pipeline?  
a) Groups documents based on a specified field  
b) Filters documents based on a condition  
c) Sorts documents in ascending order  
d) Projects only specific fields

2\. Given the following collection:

json  
Copy  
Edit  
\[  
  { "\_id": 1, "category": "A", "price": 10 },  
  { "\_id": 2, "category": "B", "price": 20 },  
  { "\_id": 3, "category": "A", "price": 30 },  
  { "\_id": 4, "category": "B", "price": 40 }  
\]  
What does the following aggregation pipeline return?

js  
Copy  
Edit  
db.items.aggregate(\[  
  { $match: { category: "A" } },  
  { $group: { \_id: "$category", total: { $sum: "$price" } } }  
\])  
a) { "\_id": "A", "total": 40 }  
b) { "\_id": "B", "total": 60 }  
c) { "\_id": "A", "total": 30 }  
d) { "\_id": "A", "total": 10 }

3\. What is the purpose of the $group stage?  
a) Aggregates documents based on specified fields  
b) Filters documents in an aggregation pipeline  
c) Returns only specific fields  
d) Performs an index scan

4\. What is required when using $group?  
a) At least one accumulator like $sum or $avg  
b) A sort operation beforehand  
c) A $match stage before grouping  
d) A limit on results

5\. Which of the following pipelines groups documents by department and calculates the average salary?  
a)

js  
Copy  
Edit  
db.employees.aggregate(\[  
  { $group: { \_id: "$department", avgSalary: { $avg: "$salary" } } }  
\])  
b)

js  
Copy  
Edit  
db.employees.aggregate(\[  
  { $match: { department: { $exists: true } } },  
  { $avg: { department: "$salary" } }  
\])  
c)

js  
Copy  
Edit  
db.employees.aggregate(\[  
  { $sort: { salary: 1 } },  
  { $group: { \_id: "$department", avgSalary: { $sum: "$salary" } } }  
\])  
d)

js  
Copy  
Edit  
db.employees.aggregate(\[  
  { $group: { avgSalary: { $avg: "$salary" } } }  
\])  
Answer Page  
b) Filters documents based on a condition  
a) { "\_id": "A", "total": 40 }  
a) Aggregates documents based on specified fields  
a) At least one accumulator like $sum or $avg  
a)  
js  
Copy  
Edit  
db.employees.aggregate(\[  
  { $group: { \_id: "$department", avgSalary: { $avg: "$salary" } } }  
\])

**3.1 Given a query that is performing a collection scan, identify which index would improve the performance of this query.**  
Multiple Choice Questions  
1\. What type of index would speed up the following query?

js  
Copy  
Edit  
db.products.find({ price: 100 })  
a) Compound index on { price: 1, name: 1 }  
b) Single-field index on { price: 1 }  
c) Text index on { description: "text" }  
d) No index is needed

2\. How can you check if a query is using an index?  
a) Use .explain("executionStats")  
b) Use .aggregate(\[{ $indexScan }\])  
c) Use .find().indexStats()  
d) Use .profile()

3\. Given the following query:

js  
Copy  
Edit  
db.users.find({ tags: "mongodb" })  
Which index would improve performance?  
a) { tags: 1 }  
b) { tags: \-1 }  
c) { tags: "text" }  
d) { tags: { $exists: true } }

4\. If a query is scanning an entire collection instead of using an index, what might be the reason?  
a) The index is not selective enough  
b) The index does not exist  
c) The query does not match the index structure  
d) All of the above

5\. How do you list all indexes on a collection?  
a) db.collection.getIndexes()  
b) db.collection.indexStats()  
c) db.collection.listIndexes()  
d) db.collection.indexes()

Answer Page  
b) Single-field index on { price: 1 }  
a) Use .explain("executionStats")  
a) { tags: 1 }  
d) All of the above  
a) db.collection.getIndexes()  
**3.2 Given a query that is performing a collection scan on an equality match on an array field, identify which index would improve the performance of this query.**  
Multiple Choice Questions  
1\. Given the following query:

js  
Copy  
Edit  
db.posts.find({ tags: "mongodb" })  
Which index would improve performance?  
a) { tags: 1 }  
b) { tags: \-1 }  
c) { tags: "text" }  
d) { tags: { $exists: true } }

2\. If a field contains an array, which index type is best suited for optimizing queries that match individual elements?  
a) Compound index  
b) Single-field index  
c) Multikey index  
d) Geospatial index

3\. What is a key characteristic of a multikey index?  
a) It allows efficient sorting of array fields  
b) It creates an index entry for each element in an array field  
c) It prevents duplicates in an array field  
d) It only works for numeric values

4\. Given the following documents:

json  
Copy  
Edit  
\[  
  { "\_id": 1, "tags": \["mongodb", "database"\] },  
  { "\_id": 2, "tags": \["nosql", "database"\] },  
  { "\_id": 3, "tags": \["mongodb", "performance"\] }  
\]  
Which query would benefit from a multikey index on { tags: 1 }?  
a)

js  
Copy  
Edit  
db.posts.find({ tags: "mongodb" })  
b)

js  
Copy  
Edit  
db.posts.find({ tags: { $all: \["mongodb", "database"\] } })  
c)

js  
Copy  
Edit  
db.posts.find({ tags: { $size: 2 } })  
d)

js  
Copy  
Edit  
db.posts.find({ tags: { $exists: true } })  
5\. If a multikey index is created on an array field, what limitation does it have?  
a) It cannot be used in compound indexes  
b) It cannot be used with sorting operations  
c) It does not work with $or queries  
d) It cannot be combined with $text indexes

Answer Page  
a) { tags: 1 }  
c) Multikey index  
b) It creates an index entry for each element in an array field  
a)  
js  
Copy  
Edit  
db.posts.find({ tags: "mongodb" })  
b) It cannot be used with sorting operations

**3.3 Given a query with no constraint and a sort of two fields that is doing collection scans, identify which index would improve the performance of this query.**  
Multiple Choice Questions  
1\. Given the following query:

js  
Copy  
Edit  
db.users.find().sort({ age: 1, salary: \-1 })  
Which index would improve the performance of this query?  
a) { age: 1, salary: \-1 }  
b) { salary: \-1, age: 1 }  
c) { age: 1 }  
d) { salary: \-1 }

2\. If no index exists for a sorted query, what will MongoDB do?  
a) Perform a collection scan  
b) Return an error  
c) Automatically create an index  
d) Use the default index on \_id

3\. Which of the following statements about compound indexes is true?  
a) They can optimize queries that filter or sort on multiple fields  
b) They can only be used for filtering, not sorting  
c) The order of fields in the index does not matter  
d) Compound indexes are less efficient than single-field indexes

4\. Given a compound index { age: 1, salary: \-1 }, which query can efficiently use the index?  
a)

js  
Copy  
Edit  
db.users.find().sort({ age: 1, salary: \-1 })  
b)

js  
Copy  
Edit  
db.users.find().sort({ salary: \-1, age: 1 })  
c)

js  
Copy  
Edit  
db.users.find().sort({ salary: 1, age: \-1 })  
d)

js  
Copy  
Edit  
db.users.find().sort({ age: \-1 })  
5\. Why does the order of fields in a compound index matter?  
a) MongoDB only allows sorting on the first indexed field  
b) Indexes are used in the order they are defined  
c) Compound indexes ignore sorting requirements  
d) Sorting order is automatically determined by MongoDB

Answer Page  
a) { age: 1, salary: \-1 }  
a) Perform a collection scan  
a) They can optimize queries that filter or sort on multiple fields  
a)  
js  
Copy  
Edit  
db.users.find().sort({ age: 1, salary: \-1 })  
b) Indexes are used in the order they are defined

**3.4 Identify which index exists or the number of indexes that exist for a collection.**  
Multiple Choice Questions  
1\. How can you list all indexes on a collection?  
a) db.collection.getIndexes()  
b) db.collection.listIndexes()  
c) db.collection.indexStats()  
d) db.collection.indexes()

2\. If a collection has only the default index, how many indexes exist?  
a) 0  
b) 1  
c) 2  
d) It depends on the collection size

3\. Given the following command:

js  
Copy  
Edit  
db.products.getIndexes()  
What does it return?  
a) The names of all collections  
b) The indexes defined on the products collection  
c) The number of documents in products  
d) The schema of products

4\. Which command provides detailed information about index usage?  
a)

js  
Copy  
Edit  
db.collection.explain("executionStats").find(query)  
b)

js  
Copy  
Edit  
db.collection.indexStats()  
c)

js  
Copy  
Edit  
db.collection.listIndexes()  
d)

js  
Copy  
Edit  
db.collection.countIndexes()  
5\. What is a reason to check existing indexes on a collection?  
a) To determine if an index needs to be added for query optimization  
b) To remove unused indexes  
c) To confirm the index order for sorting  
d) All of the above

Answer Page  
a) db.collection.getIndexes()  
b) 1  
b) The indexes defined on the products collection  
a)  
js  
Copy  
Edit  
db.collection.explain("executionStats").find(query)  
d) All of the above  
**3.5 Identify the explain plan outputs that signify a potential performance issue, specifically whether an index is present or not for the given query.**  
Multiple Choice Questions  
1\. Which of the following explain output fields indicates whether an index is being used?  
a) queryPlanner.indexFilterSet  
b) queryPlanner.winningPlan.stage  
c) executionStats.totalKeysExamined  
d) queryPlanner.indexDetails

2\. If executionStats.totalDocsExamined is much higher than executionStats.nReturned, what does this indicate?  
a) The query is efficiently using an index  
b) The query is performing a collection scan  
c) The query is using a covered index  
d) The query is returning too many documents

3\. What does COLLSCAN in the queryPlanner.winningPlan.stage field indicate?  
a) The query is using an index efficiently  
b) The query is using a covered index  
c) The query is scanning the entire collection  
d) The query is sorted incorrectly

4\. How can you determine which index was used in an explain output?  
a) Look at the queryPlanner.indexFilterSet field  
b) Look at the queryPlanner.winningPlan.inputStage.indexName field  
c) Check the executionStats.nReturned field  
d) Look for the COLLSCAN keyword

5\. What is a potential performance issue when executionStats.executionTimeMillis is significantly high?  
a) The query is running too many $group operations  
b) The query is not using an index efficiently  
c) The index is too small for the dataset  
d) The query is using $lookup improperly

Answer Page  
b) queryPlanner.winningPlan.stage  
b) The query is performing a collection scan  
c) The query is scanning the entire collection  
b) Look at the queryPlanner.winningPlan.inputStage.indexName field  
b) The query is not using an index efficiently

**3.6 Identify the purpose of a hidden index.**  
Multiple Choice Questions  
1\. What is the purpose of a hidden index in MongoDB?  
a) To prevent accidental deletions  
b) To exclude an index from query execution while keeping it in the collection  
c) To allow multiple indexes with the same key  
d) To restrict access to sensitive data

2\. Which command is used to hide an index?  
a) db.collection.createIndex({ field: 1 }, { hidden: true })  
b) db.collection.hideIndex("index\_name")  
c) db.collection.disableIndex("index\_name")  
d) db.collection.setIndexHidden("index\_name")

3\. What happens when a hidden index is unhidden?  
a) It is dropped and must be recreated  
b) It becomes immediately available for queries  
c) It must be rebuilt before use  
d) It replaces all other indexes

4\. Why would an index be temporarily hidden instead of dropped?  
a) To test performance impact before removing an index  
b) To prevent errors in indexing operations  
c) To reduce query complexity  
d) To secure data

5\. How can you check if an index is hidden?  
a) db.collection.getIndexes()  
b) db.collection.listHiddenIndexes()  
c) db.collection.explain("executionStats")  
d) db.collection.indexStats()

Answer Page  
b) To exclude an index from query execution while keeping it in the collection  
b) db.collection.hideIndex("index\_name")  
b) It becomes immediately available for queries  
a) To test performance impact before removing an index  
a) db.collection.getIndexes()

**3.7 Given an error message received when creating an index, identify the multi-key index limitation that caused this.**  
Multiple Choice Questions  
1\. What is a limitation of a multi-key index?  
a) It cannot be used for sorting  
b) It cannot be used with $match  
c) It only works on numeric fields  
d) It cannot be used with text indexes

2\. Given the error message:

css  
Copy  
Edit  
Cannot create a compound index that includes a multi-key field.  
What caused this error?  
a) An attempt to index an array field in a compound index  
b) Using $text indexes on an array field  
c) An invalid index name  
d) Using $geoWithin on a multi-key index

3\. Which of the following operations can still use a multi-key index?  
a) Equality match on an array field  
b) Sorting with multiple fields  
c) A $group stage in aggregation  
d) Geospatial queries

4\. If a field has a multi-key index, what happens when trying to create a compound index with it?  
a) The index is created successfully  
b) The operation fails with an error  
c) The multi-key index is automatically removed  
d) The compound index is partially created

5\. How can you check if an index is multi-key?  
a) db.collection.getIndexes()  
b) db.collection.explain("executionStats")  
c) db.collection.indexStats()  
d) db.collection.listIndexes()

Answer Page  
a) It cannot be used for sorting  
a) An attempt to index an array field in a compound index  
a) Equality match on an array field  
b) The operation fails with an error  
a) db.collection.getIndexes()

**3.8 Identify how to validate if a query is using an index and the name of the index being used.**  
Multiple Choice Questions  
1\. How do you check if a query is using an index?  
a) db.collection.explain("executionStats").find(query)  
b) db.collection.indexStats()  
c) db.collection.listIndexes()  
d) db.collection.validateIndexes()

2\. Which field in the explain output shows the index being used?  
a) queryPlanner.indexName  
b) queryPlanner.winningPlan.inputStage.indexName  
c) executionStats.indexDetails  
d) queryPlanner.indexType

3\. What does nReturned in executionStats indicate?  
a) The number of documents examined  
b) The number of documents returned by the query  
c) The number of indexes scanned  
d) The execution time in milliseconds

4\. If a query is not using an index, what might be the reason?  
a) The index does not exist  
b) The query structure does not match the index  
c) The index is hidden  
d) All of the above

5\. What is an effective way to ensure an index is being used in a query?  
a) Use hint() to force index usage  
b) Increase the collection size  
c) Create a text index  
d) Drop unused indexes

Answer Page  
a) db.collection.explain("executionStats").find(query)  
b) queryPlanner.winningPlan.inputStage.indexName  
b) The number of documents returned by the query  
d) All of the above  
a) Use hint() to force index usage

**3.9 Given a query, identify the field that should be indexed first.**  
Multiple Choice Questions  
1\. When creating a compound index, which field should be indexed first?  
a) The most frequently queried field  
b) The field with the highest cardinality  
c) The field used for sorting  
d) All of the above

2\. If a query filters by { category: "books", price: { $gt: 20 } }, which index order is optimal?  
a) { category: 1, price: 1 }  
b) { price: 1, category: 1 }  
c) { category: \-1, price: \-1 }  
d) { price: \-1, category: \-1 }

3\. What is a reason to put a high-cardinality field first in an index?  
a) It increases index selectivity  
b) It reduces index size  
c) It speeds up $or queries  
d) It allows better query optimization

Answer Page  
d) All of the above  
a) { category: 1, price: 1 }  
a) It increases index selectivity  
**4.1 Identify the steps to start mongod.**  
Multiple Choice Questions  
1\. What is the default command to start mongod with default settings?  
a) mongo start  
b) mongod \--default  
c) mongod  
d) mongo \--start

2\. Which flag is required to specify a custom configuration file when starting mongod?  
a) \--config  
b) \--cfg  
c) \--settings  
d) \--conf

3\. What is the default port on which mongod runs if no port is specified?  
a) 27018  
b) 28017  
c) 27017  
d) 8080

4\. Which of the following is required to run mongod in the background on Linux?  
a) mongod \--background  
b) mongod &  
c) mongod \--daemon  
d) mongod \--fork

5\. What happens if mongod is started without specifying a data directory and no default directory exists?  
a) It creates a new data directory automatically  
b) It runs in memory without storing data  
c) It throws an error and fails to start  
d) It connects to a remote instance by default

Answer Page  
c) mongod  
a) \--config  
c) 27017  
d) mongod \--fork  
c) It throws an error and fails to start

**4.2 Identify how to determine if mongod is running.**  
Multiple Choice Questions  
1\. What command can you use to check if mongod is running on Linux?  
a) ps aux | grep mongod  
b) mongod \--status  
c) mongo \--check  
d) service mongod status

2\. How can you check if mongod is listening on its default port?  
a) netstat \-tulnp | grep 27017  
b) mongo \--port 27017  
c) mongod \--check-ports  
d) lsof \-i :27017

3\. What command can check the process status of mongod on Windows?  
a) tasklist | findstr mongod  
b) mongo check  
c) mongod \--status  
d) ps \-mongod

4\. If mongod is running, what happens when you run mongo without arguments?  
a) It connects to the running instance  
b) It starts a new instance of mongod  
c) It runs a diagnostic check  
d) It shuts down the running instance

5\. Which MongoDB shell command can check the server status?  
a) db.isMaster()  
b) db.serverStatus()  
c) show databases  
d) mongo.status()

Answer Page  
a) ps aux | grep mongod  
a) netstat \-tulnp | grep 27017  
a) tasklist | findstr mongod  
a) It connects to the running instance  
b) db.serverStatus()

**4.3 Identify how to stop mongod.**  
Multiple Choice Questions  
1\. What is the safest way to stop mongod using the MongoDB shell?  
a) db.shutdownServer()  
b) mongod \--shutdown  
c) systemctl stop mongod  
d) killall mongod

2\. Which Linux command stops the mongod service cleanly?  
a) sudo service mongod stop  
b) mongod stop  
c) mongo \--shutdown  
d) systemctl restart mongod

3\. What signal should be sent to gracefully stop mongod from the command line?  
a) SIGSTOP  
b) SIGKILL  
c) SIGTERM  
d) SIGHUP

4\. What could happen if mongod is forcefully killed (kill \-9)?  
a) Data corruption may occur  
b) The database shuts down safely  
c) All indexes are rebuilt automatically  
d) The data is backed up automatically

5\. How can you ensure mongod does not restart on boot?  
a) sudo systemctl disable mongod  
b) mongod \--disable  
c) rm /var/lib/mongo  
d) killall mongod

Answer Page  
a) db.shutdownServer()  
a) sudo service mongod stop  
c) SIGTERM  
a) Data corruption may occur  
a) sudo systemctl disable mongod

**MongoDB Test: Adding Parameters to mongod**  
Multiple Choice Questions  
1\. How do you specify a different data directory when starting mongod?  
a) mongod \--dataDir /data/db  
b) mongod \--dbpath /data/db  
c) mongod \--datadir /data/db  
d) mongod \--storage /data/db

2\. How do you start mongod on a different port?  
a) mongod \--setPort 28017  
b) mongod \--port 28017  
c) mongod \--changePort 28017  
d) mongod \--listen 28017

3\. Which flag enables authentication for mongod?  
a) \--auth  
b) \--secure  
c) \--enable-auth  
d) \--password-required

4\. How can you log all queries to a file?  
a) mongod \--logQueries  
b) mongod \--logpath /var/log/mongodb.log  
c) mongod \--enableLogging  
d) mongod \--queryLog /var/log/mongodb.log

5\. How do you start mongod with a specific configuration file?  
a) mongod \--config /etc/mongod.conf  
b) mongod \--useConfig /etc/mongod.conf  
c) mongod \--confFile /etc/mongod.conf  
d) mongod \--settings /etc/mongod.conf

Answer Page  
b) mongod \--dbpath /data/db  
b) mongod \--port 28017  
a) \--auth  
b) mongod \--logpath /var/log/mongodb.log  
a) mongod \--config /etc/mongod.conf

**4.5 Identify how to check a parameter value in mongod.**  
Multiple Choice Questions  
1\. What command can you run in the MongoDB shell to check a server parameter?  
a) db.runCommand({ getParameter: 1, featureCompatibilityVersion: 1 })  
b) db.getConfig("featureCompatibilityVersion")  
c) db.serverParameter("featureCompatibilityVersion")  
d) mongo \--getParameter featureCompatibilityVersion

2\. Which command lists all mongod parameters?  
a) db.adminCommand({ getParameter: '\*' })  
b) mongod \--listParameters  
c) db.listParameters()  
d) mongo \--configList

3\. How do you check the wiredTiger cache size in mongod?  
a) db.serverStatus().wiredTiger.cache\["maximum bytes configured"\]  
b) db.wiredTigerCacheSize()  
c) mongo \--cacheSize  
d) db.getParameter({ wiredTigerCacheSize: 1 })

Answer Page  
a) db.runCommand({ getParameter: 1, featureCompatibilityVersion: 1 })  
a) db.adminCommand({ getParameter: '\*' })  
a) db.serverStatus().wiredTiger.cache\["maximum bytes configured"\]  
**5.1 Identify the meaning of common alerts.**  
Multiple Choice Questions  
1\. What does the MongoDB alert "Replication Lag Detected" indicate?  
a) The secondary nodes are ahead of the primary  
b) The primary node has crashed  
c) The secondary nodes are falling behind the primary in syncing data  
d) The oplog is corrupted

2\. What does the alert "Journaling is Disabled" signify?  
a) Data is not being persisted to disk properly  
b) The database is running in a secure mode  
c) Transactions are processed faster  
d) The storage engine has switched to read-only mode

3\. What could cause the "Oplog Size is Too Small" alert?  
a) The oplog is not enabled  
b) The oplog cannot store enough changes, causing replication issues  
c) The primary node has too many indexes  
d) The secondary nodes are reading the oplog too quickly

4\. Which alert would indicate that MongoDB is experiencing excessive memory usage?  
a) "High Cache Pressure"  
b) "Write Concern Failed"  
c) "Replication Lag Detected"  
d) "Authentication Failure"

5\. What does the "Too Many Connections" alert typically mean?  
a) The database has crashed  
b) The connection pool limit has been exceeded  
c) The replication set has failed  
d) An index is corrupt

Answer Page  
c) The secondary nodes are falling behind the primary in syncing data  
a) Data is not being persisted to disk properly  
b) The oplog cannot store enough changes, causing replication issues  
a) "High Cache Pressure"  
b) The connection pool limit has been exceeded

**5.2 Identify how to run currentOp.**  
Multiple Choice Questions  
1\. What is the purpose of the currentOp command in MongoDB?  
a) It displays active operations running on the database  
b) It checks the current storage utilization  
c) It lists all users connected to the database  
d) It resets the oplog

2\. How do you execute currentOp in the MongoDB shell?  
a) db.currentOp()  
b) db.runCommand({ currentOp: 1 })  
c) db.listOperations()  
d) mongo \--currentOp

3\. Which field in the currentOp output indicates a long-running operation?  
a) secs\_running  
b) operation\_time  
c) oplog\_lag  
d) duration

4\. What type of operations can currentOp show?  
a) Only write operations  
b) Only read operations  
c) Both read and write operations  
d) Only replication-related operations

5\. How can you filter currentOp to show only long-running operations?  
a) db.runCommand({ currentOp: 1, "secs\_running": { "$gt": 10 } })  
b) db.listOperations({ duration: { "$gt": 10 } })  
c) db.showLongOperations()  
d) mongo \--opTimeout 10

Answer Page  
a) It displays active operations running on the database  
b) db.runCommand({ currentOp: 1 })  
a) secs\_running  
c) Both read and write operations  
a) db.runCommand({ currentOp: 1, "secs\_running": { "$gt": 10 } })

**5.3 Identify how to see currently active operations.**  
Multiple Choice Questions  
1\. How can you view currently running operations in MongoDB?  
a) db.currentOps()  
b) db.runCommand({ currentOp: 1 })  
c) db.viewActiveOperations()  
d) mongo \--showOps

2\. How can you identify a blocking operation in the currentOp output?  
a) The waitingForLock field is set to true  
b) The operation field is empty  
c) The execTime field is negative  
d) The lockMode field is none

3\. What does the ns field in the currentOp output represent?  
a) The namespace (database and collection) the operation is targeting  
b) The name of the primary server  
c) The number of secondary nodes  
d) The network socket being used

4\. How can you kill a running operation in MongoDB?  
a) db.killOp(opid)  
b) db.terminateOperation(opid)  
c) mongo \--shutdownOp opid  
d) db.runCommand({ killOperation: opid })

5\. How do you view only active user queries in currentOp?  
a) db.runCommand({ currentOp: 1, "active": true })  
b) db.showActiveQueries()  
c) mongo \--listActive  
d) db.listUserOps()

Answer Page  
b) db.runCommand({ currentOp: 1 })  
a) The waitingForLock field is set to true  
a) The namespace (database and collection) the operation is targeting  
a) db.killOp(opid)  
a) db.runCommand({ currentOp: 1, "active": true })

**5.4 Identify how to monitor storage.**  
Multiple Choice Questions  
1\. Which command provides details on disk space usage for a database?  
a) db.stats()  
b) db.diskUsage()  
c) mongo \--showStorage  
d) db.showStorageDetails()

2\. How can you check the total storage size of a collection?  
a) db.collection.stats().storageSize  
b) db.collection.diskUsage()  
c) db.collection.sizeOnDisk()  
d) mongo \--collectionSize

3\. What MongoDB feature helps manage storage by reclaiming unused space?  
a) WiredTiger Compression  
b) Auto-Sharding  
c) Replica Sets  
d) Auto-Indexing

4\. How can you determine the total available disk space on a MongoDB server?  
a) db.serverStatus().hostInfo  
b) db.disk.freeSpace()  
c) db.checkStorage()  
d) mongo \--diskInfo

5\. What field in db.stats() helps monitor free storage within a collection?  
a) size  
b) storageSize  
c) freeStorage  
d) remainingSpace

Answer Page  
a) db.stats()  
a) db.collection.stats().storageSize  
a) WiredTiger Compression  
a) db.serverStatus().hostInfo  
b) storageSize

**5.5 Identify the indications that storage is running out.**  
Multiple Choice Questions  
1\. Which of the following is a warning sign of low storage in MongoDB?  
a) "No Primary Available" error  
b) High Write Latency  
c) Frequent Index Rebuilds  
d) Excessive Memory Usage

2\. How can you detect if the storage engine is out of space?  
a) db.serverStatus().wiredTiger.cache\["maximum bytes configured"\]  
b) db.stats().storageSize  
c) df \-h (Linux) or dir (Windows)  
d) All of the above

Answer Page  
b) High Write Latency  
d) All of the above

**6.1 Identify the purpose of enabling TLS.**  
Multiple Choice Questions  
1\. What is the primary purpose of enabling TLS in MongoDB?  
a) To improve query performance  
b) To encrypt data in transit between clients and servers  
c) To enable automatic backups  
d) To prevent unauthorized indexing

2\. Which option is used to enable TLS when starting mongod?  
a) \--auth  
b) \--enableTLS  
c) \--tlsMode requireTLS  
d) \--encryptData

3\. Which file is required to configure TLS in MongoDB?  
a) mongodb.pem  
b) security.conf  
c) config.json  
d) mongo.cert

4\. What does the \--tlsCAFile parameter specify?  
a) The path to the CA certificate for validating client connections  
b) The path to the MongoDB user authentication file  
c) The file where TLS logs are stored  
d) The directory where encrypted data is stored

5\. What happens if TLS is enabled but a client does not support TLS?  
a) The connection is automatically downgraded to an unencrypted session  
b) The client is denied access  
c) MongoDB disables authentication  
d) The server crashes

Answer Page  
b) To encrypt data in transit between clients and servers  
c) \--tlsMode requireTLS  
a) mongodb.pem  
a) The path to the CA certificate for validating client connections  
b) The client is denied access

**6.2 Identify the purpose of enabling authentication.**  
Multiple Choice Questions  
1\. What is the purpose of enabling authentication in MongoDB?  
a) To improve indexing speed  
b) To require users to provide credentials before accessing the database  
c) To enable TLS encryption  
d) To disable anonymous connections

2\. Which command enables authentication when starting MongoDB?  
a) mongod \--auth  
b) mongod \--secure  
c) mongod \--requireAuth  
d) mongod \--tlsAuth

3\. Which database is used for storing user credentials in MongoDB?  
a) config  
b) admin  
c) users  
d) system

4\. What is required before enabling authentication in MongoDB?  
a) TLS must be enabled  
b) At least one admin user must be created  
c) All collections must be indexed  
d) The database must be in read-only mode

5\. How can an existing MongoDB instance be restarted with authentication enabled?  
a) Modify the mongod.conf file to include security.authorization: enabled and restart MongoDB  
b) Run mongod \--auth \--restart  
c) Enable user authentication through db.auth.enable()  
d) Add a user to the config.users collection

Answer Page  
b) To require users to provide credentials before accessing the database  
a) mongod \--auth  
b) admin  
b) At least one admin user must be created  
a) Modify the mongod.conf file to include security.authorization: enabled and restart MongoDB

**6.3 Identify how to define a role for authorization.**  
Multiple Choice Questions  
1\. What is a role in MongoDB authorization?  
a) A script for automating queries  
b) A predefined set of permissions assigned to users  
c) A backup configuration  
d) A method to encrypt fields

2\. How is a role defined in MongoDB?  
a) Using db.createRole()  
b) Using db.addRole()  
c) Using db.authRole()  
d) Using db.createPermission()

3\. Which database must be used to create roles?  
a) config  
b) admin  
c) system  
d) security

4\. What must a role contain?  
a) A user and a password  
b) A set of privileges and the resources they apply to  
c) A database backup policy  
d) A replication configuration

5\. What is an example of a built-in MongoDB role?  
a) backupAdmin  
b) superUser  
c) dbEditor  
d) writeMaster

Answer Page  
b) A predefined set of permissions assigned to users  
a) Using db.createRole()  
b) admin  
b) A set of privileges and the resources they apply to  
a) backupAdmin

**6.4 / 6.5 / 6.6 Assigning and Revoking Roles**  
Multiple Choice Questions  
1\. How do you assign a role to a user in MongoDB?  
a) db.grantRoleToUser()  
b) db.createUser({ roles: \[...\] })  
c) db.userRoles.add()  
d) db.auth.assignRole()

2\. How do you revoke a role from a user?  
a) db.revokeRolesFromUser()  
b) db.removeRoleFromUser()  
c) db.updateUser({ removeRole: \[...\] })  
d) db.modifyUser({ revokeRole: \[...\] })

3\. Can a user have multiple roles in MongoDB?  
a) Yes  
b) No

4\. Which command lists the roles assigned to a user?  
a) db.getUserRoles()  
b) db.runCommand({ rolesInfo: \<username\> })  
c) db.auth.listRoles()  
d) db.listUserRoles()

5\. What happens if a user is assigned conflicting roles?  
a) MongoDB denies all access  
b) MongoDB merges the permissions from all roles  
c) The last assigned role overwrites previous roles  
d) The user is locked out

Answer Page  
b) db.createUser({ roles: \[...\] })  
a) db.revokeRolesFromUser()  
a) Yes  
b) db.runCommand({ rolesInfo: \<username\> })  
b) MongoDB merges the permissions from all roles

**6.7 / 6.8 Encryption & Audit Logs**  
Multiple Choice Questions  
1\. What is the primary purpose of encryption at rest in MongoDB?  
a) To secure data when it is stored on disk  
b) To encrypt data during replication  
c) To improve query performance  
d) To enable faster indexing

2\. Which storage engine supports encryption at rest in MongoDB?  
a) WiredTiger  
b) MMAPv1  
c) RocksDB  
d) InnoDB

3\. What is a limitation of MongoDB’s encryption at rest?  
a) It does not protect data in transit  
b) It prevents indexing on encrypted fields  
c) It is only available in MongoDB Community Edition  
d) It requires a dedicated replica set

4\. What is the purpose of field-level encryption?  
a) To encrypt specific fields in a document rather than the entire database  
b) To enable automatic backups  
c) To prevent schema validation  
d) To improve indexing speed

5\. Where can MongoDB audit logs be written?  
a) A JSON file  
b) Syslog  
c) Console output  
d) All of the above

Answer Page  
a) To secure data when it is stored on disk  
a) WiredTiger  
a) It does not protect data in transit  
a) To encrypt specific fields in a document rather than the entire database  
d) All of the above  
**6.10 Identify where the audit log can be written.**  
Multiple Choice Questions  
1\. Where can MongoDB audit logs be written?  
a) Only to a JSON file  
b) Only to the console  
c) To a JSON file, syslog, or the console  
d) Only to a remote database

2\. Which parameter is used to specify the location of the audit log in MongoDB?  
a) auditLog.destination  
b) auditLog.path  
c) auditLog.enable  
d) auditLog.fileLocation

3\. What happens if auditLog.destination is set to syslog?  
a) Audit logs are written to a specified file  
b) Audit logs are sent to the system log daemon  
c) Audit logging is disabled  
d) MongoDB restarts automatically

4\. If auditLog.destination is set to file, which parameter must be specified?  
a) auditLog.format  
b) auditLog.path  
c) auditLog.rotate  
d) auditLog.bufferSize

5\. What format can the MongoDB audit log be written in?  
a) JSON  
b) BSON  
c) CSV  
d) YAML

Answer Page  
c) To a JSON file, syslog, or the console  
a) auditLog.destination  
b) Audit logs are sent to the system log daemon  
b) auditLog.path  
a) JSON  
**7.1 Identify the purpose of replication.**  
Multiple Choice Questions  
1\. What is the primary purpose of replication in MongoDB?  
a) To improve indexing speed  
b) To provide high availability and data redundancy  
c) To optimize query performance  
d) To enable automatic backups

2\. What component in MongoDB handles replication?  
a) Sharding servers  
b) Replica sets  
c) Query optimizer  
d) Config servers

3\. How does MongoDB replication work?  
a) A single node stores all data, and others act as backups  
b) Multiple nodes store the same data, with one acting as primary and others as secondaries  
c) Every node in a cluster independently stores unique data  
d) Data is stored only in memory and periodically flushed to disk

4\. How does MongoDB ensure eventual consistency in replication?  
a) Write operations are initially applied to the primary replica and then asynchronously replicated to secondary replicas  
b) The primary node pushes data updates to secondaries in real-time  
c) Updates are manually applied to each secondary node  
d) Writes are applied directly to all nodes simultaneously

5\. Which command checks the status of a replica set?  
a) db.replicationStatus()  
b) rs.status()  
c) replica.getStatus()  
d) db.replicaSetStatus()

Answer Page  
b) To provide high availability and data redundancy  
b) Replica sets  
b) Multiple nodes store the same data, with one acting as primary and others as secondaries  
a) Secondary nodes periodically request updates from the primary  
b) rs.status()

**7.2 Identify the purpose of the primary.**  
Multiple Choice Questions  
1\. What is the primary node in a MongoDB replica set responsible for?  
a) Distributing queries among secondaries  
b) Handling all write operations and synchronizing data to secondaries  
c) Managing storage engine settings  
d) Handling backup operations

2\. What happens when the primary node goes down?  
a) The replica set stops working  
b) A secondary node is elected as the new primary  
c) All secondaries delete their data  
d) Writes continue to be accepted on the secondaries

3\. How does the primary notify secondaries of changes?  
a) By writing changes to the oplog, which secondaries read  
b) By directly pushing data updates to secondaries  
c) By periodically syncing all data from the secondaries  
d) By waiting for an administrator to trigger replication

4\. What happens if two nodes claim to be the primary?  
a) MongoDB allows both to accept writes  
b) One node automatically shuts down  
c) The election process resolves the conflict  
d) All writes are blocked until resolved

5\. How can an administrator force a new primary to be elected?  
a) By restarting the primary node  
b) By running rs.stepDown() on the current primary  
c) By manually deleting the primary node’s data  
d) By running rs.forceElection()

Answer Page  
b) Handling all write operations and synchronizing data to secondaries  
b) A secondary node is elected as the new primary  
a) By writing changes to the oplog, which secondaries read  
c) The election process resolves the conflict  
b) By running rs.stepDown() on the current primary

**7.3 Identify the purpose of the secondary.**  
Multiple Choice Questions  
1\. What is the purpose of a secondary node in a replica set?  
a) To perform read operations only  
b) To replicate data from the primary and provide redundancy  
c) To store logs for the primary  
d) To manage schema updates

2\. What happens when a secondary node falls too far behind the primary?  
a) It automatically recovers and catches up  
b) It stops replicating and must be manually resynced  
c) It forces a primary election  
d) It becomes the new primary

3\. How can a secondary node be used for read operations?  
a) By setting the readPreference to secondary  
b) By promoting it to primary  
c) By disabling write concern  
d) By using db.readSecondary()

4\. What is delayed replication in MongoDB?  
a) A secondary node applies updates with a set delay  
b) A secondary node is only used for storing logs  
c) A secondary node never applies updates from the primary  
d) The primary delays sending updates to secondaries

5\. How can a secondary node be forced to become primary?  
a) By running rs.stepDown() on the current primary  
b) By disconnecting the current primary  
c) By modifying the oplog directly  
d) By restarting the secondary node

Answer Page  
b) To replicate data from the primary and provide redundancy  
b) It stops replicating and must be manually resynced  
a) By setting the readPreference to secondary  
a) A secondary node applies updates with a set delay  
a) By running rs.stepUp()

**7.4 Identify uses for read preference.**  
Multiple Choice Questions  
1\. What is the purpose of read preference in MongoDB?  
a) To specify how queries should be distributed among replica set members  
b) To enforce strict write consistency  
c) To optimize indexing performance  
d) To prioritize primary node elections

2\. What is the default read preference in MongoDB?  
a) primaryPreferred  
b) nearest  
c) primary  
d) secondary

3\. Which read preference allows reading from secondary nodes when the primary is unavailable?  
a) primaryOnly  
b) secondaryPreferred  
c) nearest  
d) primaryPreferred

4\. What happens if a query with nearest read preference is executed?  
a) It always reads from the primary node  
b) It selects the node with the lowest network latency, regardless of type  
c) It waits for all secondaries before reading data  
d) It reads only from secondaries

5\. When should secondaryPreferred be used?  
a) When strong consistency is required  
b) When high availability and reduced load on the primary is needed  
c) When the primary node should be used exclusively  
d) When the query needs to execute atomic operations

Answer Page  
a) To specify how queries should be distributed among replica set members  
c) primary  
d) primaryPreferred  
b) It selects the node with the lowest network latency, regardless of type  
b) When high availability and reduced load on the primary is needed

**7.5 Identify the information that can be found in the output of rs.status.**  
Multiple Choice Questions  
1\. What command is used to check the status of a replica set?  
a) db.replicationStatus()  
b) rs.status()  
c) replica.getStatus()  
d) db.replicaSetStatus()

2\. Which of the following is NOT included in the output of rs.status()?  
a) The oplog size  
b) The current primary node  
c) The health of each replica set member  
d) The election timestamp

3\. What does a stateStr value of SECONDARY indicate in rs.status() output?  
a) The node is eligible to become primary  
b) The node is currently unavailable  
c) The node is replicating from the primary  
d) The node is in recovery mode

4\. If rs.status() shows "health": 0 for a node, what does it mean?  
a) The node is online and fully operational  
b) The node is unhealthy or unreachable  
c) The node has become the new primary  
d) The node has the highest priority in elections

5\. What field in rs.status() output shows the time when the last heartbeat was received?  
a) lastPingMs  
b) uptime  
c) heartbeatTime  
d) lastHeartbeatRecv

Answer Page  
b) rs.status()  
a) The oplog size  
c) The node is replicating from the primary  
b) The node is unhealthy or unreachable  
d) lastHeartbeatRecv

**7.6 Identify the purpose of setting write concern.**  
Multiple Choice Questions  
1\. What is the purpose of write concern in MongoDB?  
a) To specify how long writes should take  
b) To ensure durability and acknowledgment of write operations  
c) To limit the size of write operations  
d) To enforce schema validation

2\. What is the default write concern in MongoDB?  
a) { w: "majority" }  
b) { w: 1 }  
c) { w: 0 }  
d) { w: 2 }

3\. What does { w: "majority" } mean in write concern?  
a) The write must be acknowledged by all members  
b) The write is acknowledged after being written to the primary only  
c) The write is acknowledged by a majority of the replica set members  
d) The write is immediately acknowledged without replication

4\. How does { j: true } affect write concern behavior?  
a) Ensures the write is written to the journal before acknowledgment  
b) Increases the write speed  
c) Reduces durability guarantees  
d) Forces a secondary node to become primary

5\. What happens if a write concern level is higher than the number of available nodes?  
a) The write fails  
b) The write is retried indefinitely  
c) The write succeeds but with a delay  
d) The primary node shuts down

Answer Page  
b) To ensure durability and acknowledgment of write operations  
b) { w: "majority" }  
c) The write is acknowledged by a majority of the replica set members  
a) Ensures the write is written to the journal before acknowledgment  
a) The write fails

**7.7 Identify the purpose of an election.**  
Multiple Choice Questions  
1\. What is the purpose of an election in a MongoDB replica set?  
a) To determine the next primary node  
b) To assign new indexes to documents  
c) To resync secondary nodes  
d) To delete outdated replicas

2\. When does an election occur in a MongoDB replica set?  
a) When the primary node is shut down or becomes unavailable  
b) When an administrator triggers it manually  
c) When the secondary nodes reach a size limit  
d) At fixed time intervals

3\. What determines which secondary node is elected as the new primary?  
a) The highest priority setting and most up-to-date replication state  
b) The node with the lowest latency  
c) The first node to request an election  
d) A random selection process

4\. What role does the priority setting play in elections?  
a) Nodes with a higher priority are more likely to be elected as primary  
b) Priority settings only affect secondary nodes  
c) Priority settings control replication speed  
d) Priority settings do not affect elections

5\. Which command forces an election manually?  
a) rs.stepDown()  
b) rs.reconfig()  
c) rs.electionForce()  
d) rs.stepUp()

Answer Page  
a) To determine the next primary node  
a) When the primary node is shut down or becomes unavailable  
a) The highest priority setting and most up-to-date replication state  
a) Nodes with a higher priority are more likely to be elected as primary  
a) rs.stepDown()

**7.8 Given a replica set and the primary fails, identify what will occur.**  
Multiple Choice Questions  
1\. What happens if a primary node in a replica set fails?  
a) A new primary is elected automatically  
b) The replica set stops working  
c) All data is lost  
d) The secondaries delete their data

2\. What triggers the election process when a primary fails?  
a) A majority of nodes detect that the primary is unreachable  
b) An administrator manually starts an election  
c) The secondaries merge into a single node  
d) The oplog size reaches zero

3\. What is a potential risk when a primary fails and an election occurs?  
a) A temporary period where writes are not accepted  
b) A new secondary is created automatically  
c) The primary deletes all its data before failing  
d) The secondary nodes stop responding

4\. How can an administrator check if an election has occurred?  
a) By checking rs.status() for election timestamps  
b) By running db.primaryElection()  
c) By running db.replicaStatus()  
d) By querying the oplog

5\. What happens if a secondary node is promoted to primary and the old primary comes back online?  
a) The old primary steps down to secondary  
b) The old primary reclaims its role  
c) The replica set splits  
d) The old primary shuts down

Answer Page  
a) A new primary is elected automatically  
a) A majority of nodes detect that the primary is unreachable  
a) A temporary period where writes are not accepted  
a) By checking rs.status() for election timestamps  
a) The old primary steps down to secondary  
**7.9 Identify the purpose of oplog.**  
Multiple Choice Questions  
1\. What is the purpose of the oplog in MongoDB?  
a) To store backup copies of documents  
b) To log all operations that modify data for replication  
c) To store authentication logs  
d) To optimize queries

2\. Where is the oplog stored?  
a) In the admin database  
b) In a capped collection in the local database  
c) In an external log file  
d) In the replication database

3\. What happens if the oplog size is too small?  
a) Replication performance improves  
b) Old operations are overwritten before secondaries can apply them  
c) Secondaries perform better  
d) The primary node fails

4\. How can an administrator check the oplog size?  
a) rs.oplogSize()  
b) db.oplog.rs.stats()  
c) db.checkOplogSize()  
d) rs.status()

5\. What is a potential risk if the oplog is full before secondaries can replicate?  
a) Secondaries stop working and require a full resync  
b) The primary shuts down  
c) Writes are blocked  
d) Queries become slower

Answer Page  
b) To log all operations that modify data for replication  
b) In a capped collection in the local database  
b) Old operations are overwritten before secondaries can apply them  
b) db.oplog.rs.stats()  
a) Secondaries stop working and require a full resync

**8.1 Identify how to create a backup of a replica set.**  
Multiple Choice Questions  
\*\*1. What is the recommended method to back up a MongoDB replica set?  
a) Copying the data files from the primary node while it is running  
b) Using mongodump to back up from a secondary node  
c) Shutting down all nodes and manually copying the oplog  
d) Using rs.backup() command

2\. Why is it recommended to back up from a secondary node instead of the primary?  
a) The secondary contains a full backup of all databases  
b) It reduces the impact on the primary node’s performance  
c) The primary node does not allow backups  
d) Secondaries always have the most up-to-date data

3\. What additional option should be used with mongodump to ensure point-in-time consistency in a replica set backup?  
a) \--archive  
b) \--oplog  
c) \--snapshot  
d) \--journal

4\. Which method ensures the most reliable backup with minimal downtime for a large replica set?  
a) Taking a filesystem snapshot of a secondary node  
b) Running mongodump on the primary node  
c) Exporting all collections manually using mongoexport  
d) Restarting the replica set in read-only mode before backing up

5\. How can an administrator restore a backup of a replica set?  
a) By running mongorestore and specifying the backup directory  
b) By restarting MongoDB with the \--restore flag  
c) By directly copying the backup files into the data directory  
d) By executing rs.restore() on the primary node

Answer Page  
b) Using mongodump to back up from a secondary node  
b) It reduces the impact on the primary node’s performance  
b) \--oplog  
a) Taking a filesystem snapshot of a secondary node  
a) By running mongorestore and specifying the backup directory