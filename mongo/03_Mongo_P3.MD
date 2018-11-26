Mongo Part 3

Something that sets MongoDB apart from relation database that it is possible for document in same collection to have different schemas
And we take advantage of this in various ways. This is an important difference from relational database tables in which all records must have 
exactly the same set of columns. One of the simplest ways in which we use this is in mongodb is that for document which for have do data for 
fields, we dont need to include field at all.  
Going a bit further many movies have not recieved awards, The flexibility of MongoDB's data model allows us to easily model awards for 
just that movies that have them without creating a second table or a collection that we must than join together in queries in order to get
all necessary data for a movie

If we need to update a record on MongoDB for exampel for a movie Martian which has now awards
The method is for a single movie updateOne. UpdateOne update document which first match.

db.collection.updateOn(
{json},  --filter
{$set:{  --update part
	json
}}
)

For update operations, update operators specify how to modify specific fields in documents matching a filter. Fields may be added, deleted, or have their value changed in some way.
Update operators define what modifications to make with respect to one or more fields in matching documents.

Update many has same functionality but for all records which matches criteria.

Upsert  insert data if it is not exist. it is actually and arguments for update
db.collection.updateOne({criteria},{set},{upsert:true}) 
Upsert first query filter if exist update it otherwise it will insert it.

UpdateOne update entire document rather than updates some fields. 


Similiar to update we can use deleteOne, deleteMany with only filter.








