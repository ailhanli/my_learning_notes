Mongo Part 4

Query operators
comparasion operators: they compare field value based on operator. for example: $gt, $gte, $lt, $lte, $eq, $ne, $in, $nin
       not: in mongodb we are not presenting rather than setting null value for the field which hasnt value. it is quite 	often.
       if we use x:null it will match both nullable and nonexsiting fields.
$exists has two value these are true or false. it means field exist or not.
$type has value as type. which is for field which has this type for example $type:"double". Mongo db has flexiable data models. so one field can have many types
logical operators: $and, $or, $not, $nor. value of this operators are array or selectors. selector is a simple boolean result expression. using $and or directly define in filter for two fields result same but sometime we want to use one field for different values
       Key in a json document is unique so you cannot get correct result from find({xfield:{$get:100}, {xfield:                   {$ne:null}}}) only the last one will be evaluated. so you have to define like 
       find($and:[{xfield:{$get:100}, {xfield:	{$ne:null}}}])

	find($and:[{xfield:{$eq:null}, {$exists:{$ne:true}}}]): which document has field and it is value is null.
Querying Arrays
$all: take array as parameter order is not important and check field which has these all array elements.
$size: compare element size which is an array within integer value
$ elemMatch: this operator need in case of arrays of document for seaching something. it takes selector which is boolean comparasion expression as parameter.

       Because mongo shell is javascript evulator we can write any javascript what we need.
       For example: delete x.y : it is deleting y field from x element.
				      x.push("something")-> pushes new element end of array
Querying Regex
$regex: this takes reqular expression as parameter. for example /^Won.*/ mean which field value start with Won

note that if we use only db.collection.find({},{_id=true}) all _id will be listed.

