Mongo Part 1

Database is a namespace for collections
Collections store individual records called documents
Similar items groups in collections.
Collections require for the same application within same database

we can also establish security policies that authorize users 
with different roles and different levels of access at the database or
collection level.mongodb does not support authorization settings spesific to 
individual documents.

each database and collection combination define a namespace.
ex: city.neighbours

we use compass interface to navigate databases in cluster.
collections contains variety of types of data and arrange of datamodals.
schema view provides a list of fields found in the documents within collection.

Data types
in the schema view of compass we can see
number of fields (name,type,graph that reflects range of values for field and what fraction of documents hold spesific values)
when you hover type you can see fraction of type for the field used in document.

types: string, int32, double, date, decimal, null
field can be in several data type compass show us rate of value type. for example for double field it can be some records are integer some 
is undefined. undefined means null.

valued fields: array valued fields(Array), document valued fields(Object)
mongodb supports nesting documents as the value of a field within another document.
it is important to modeling data using document and it is required to work in application.
you can nest documents two or more levels deep.
mongodb support filtering database based on value of fields in nested documents.

in addition to nested documents mongodb support array values for fields
mongodb has flexible data modal and all docs dont have to contain exactly the same fields. 
we can filter documents base on fields which contains spesific data.

mongodb supports natively geospatial data.
mongodb provides far reaching support for geospatial data, enabling you to store variety of shapes calculate the distance bw point,
filter for documents that are within a specified radious of another point and perform number of other operations.

Much of interaction will be through JSON documents of one type to another.



