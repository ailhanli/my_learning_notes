Mongo Part 2

Mongo shell is fully functional javascriptor interpreter.

Every document in collection must have unique _id which is primary key for each document.

in order to load data to mongo db collection. dir to location and then use load("sample.js") command

select statement
db.collection.find(json).pretty()    --> returns cursor
db.collection.findOne(json).pretty()   --->first document matches filter returns indiviual document

insert statement
db.collection.insertOne(json)

insertMany
db.collection.insertMany([jsons])
InsertMany is by default ordered. if there is an error during the insert it error out and stop execution of insert. because there is no transactional behaviour in nosql db before errors all record will be inserted successfully
if we define ordered=false as second argument, insertMany will continue inserting documents in case of error

Query more
for nested json 
db.collection.find(x.y.x=2).pretty()
--if we want to query nested json. we use dot notation to access inner json. if we use shell we need to spesify key in double quotas. in compass you dont need double quotas.

for counting
simply calls count() method on find

for array fields(exact match)
db.movieCollections.find({cast:["tim robbins", "alice cartoons"]}) : 			this is exact match. it means only the document who has onlt rim robbins and alice cartoons
db.movieCollections.find({cast:["tim robbins"]}): 		document which has tim robbins in cast array. it is not exact match

db.movieCollections.find({"cast.0":["tim robbins"]}):		which document has tim robbins it array first element

Cursor
If there too many records, we can iterate over the records use it as command.

Projections
Reduce network overhead and processing requirements by limiting the fields that are returned in documents. By default mongo db returnes all fields all matching documents for queries.
You can define projection as a second argument to the find method.
db.collection.find(json, {fieldname:1 or 0}): 1 for include, 0 for exclude