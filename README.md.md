# &nbsp;MongoDB CRUD Operations – Class 10 Database



##### &nbsp; **Objective:**



###### To perform basic CRUD (Create, Read, Update, Delete) operations using MongoDB.

###### 

##### Tools Used



\* MongoDB Community Edition

\* MongoDB Shell (mongosh)

\* Windows OS



###### &nbsp;**Database Used**



Database Name: \*\*school\*\*



Collection Name: \*\*class10\*\*



###### CREATE Operation:



test> use school

switched to db school

school> db.class10.find()

\[

&nbsp; {

&nbsp;   \_id: ObjectId("698c747834fa3ba39ece0376"),

&nbsp;   name: 'vamsi',

&nbsp;   rollno: 1

&nbsp; },

&nbsp; {

&nbsp;   \_id: ObjectId("698c74b534fa3ba39ece0377"),

&nbsp;   name: 'shire',

&nbsp;   rollno: 2

&nbsp; },

&nbsp; { \_id: ObjectId("698c8f26a314f74d13eba561") },

&nbsp; { \_id: ObjectId("698c905ca314f74d13eba562"), name: 'suma' }

]

school> db.class10.insertOne({ name:"srinu", rollno:5,age:15})

{

&nbsp; acknowledged: true,

&nbsp; insertedId: ObjectId("69970054d6c97ca026b2094c")

}

school> db.class10.insertOne({ name:"naniii", rollno:10,age:15,marks:50})

{

&nbsp; acknowledged: true,

&nbsp; insertedId: ObjectId("699701b7d6c97ca026b2094d")

}

school> db.class10.insertOne({ name:"suma", rollno:12,age:21})

{

&nbsp; acknowledged: true,

&nbsp; insertedId: ObjectId("699701d2d6c97ca026b2094e")

}



###### &nbsp;READ Operation:

school> db.class10.find()

\[

&nbsp; {

&nbsp;   \_id: ObjectId("698c747834fa3ba39ece0376"),

&nbsp;   name: 'vamsi',

&nbsp;   rollno: 1

&nbsp; },

&nbsp; {

&nbsp;   \_id: ObjectId("698c74b534fa3ba39ece0377"),

&nbsp;   name: 'shire',

&nbsp;   rollno: 18

&nbsp; },

&nbsp; { \_id: ObjectId("698c8f26a314f74d13eba561") },

&nbsp; {

&nbsp;   \_id: ObjectId("69970054d6c97ca026b2094c"),

&nbsp;   name: 'srinu',

&nbsp;   rollno: 5,

&nbsp;   age: 15

&nbsp; },

&nbsp; {

&nbsp;   \_id: ObjectId("699701b7d6c97ca026b2094d"),

&nbsp;   name: 'naniii',

&nbsp;   rollno: 10,

&nbsp;   age: 15,

&nbsp;   marks: 50

&nbsp; },

&nbsp; {

&nbsp;   \_id: ObjectId("699701d2d6c97ca026b2094e"),

&nbsp;   name: 'suma',

&nbsp;   rollno: 12,

&nbsp;   age: 21

&nbsp; }

]



###### &nbsp;UPDATE Operation:



school>  db.class10.updateOne({name:"shire"},{$set :{rollno:18}})

{

&nbsp; acknowledged: true,

&nbsp; insertedId: null,

&nbsp; matchedCount: 1,

&nbsp; modifiedCount: 1,

&nbsp; upsertedCount: 0

}



###### &nbsp;DELETE Operation:



school> db.class10.deleteOne({name:"suma"})

{ acknowledged: true, deletedCount: 1 }



###### After Delection displaying all:



school> db.class10.find()

\[

&nbsp; {

&nbsp;   \_id: ObjectId("698c747834fa3ba39ece0376"),

&nbsp;   name: 'vamsi',

&nbsp;   rollno: 1

&nbsp; },

&nbsp; {

&nbsp;   \_id: ObjectId("698c74b534fa3ba39ece0377"),

&nbsp;   name: 'shire',

&nbsp;   rollno: 18

&nbsp; },

&nbsp; { \_id: ObjectId("698c8f26a314f74d13eba561") },

&nbsp; {

&nbsp;   \_id: ObjectId("69970054d6c97ca026b2094c"),

&nbsp;   name: 'srinu',

&nbsp;   rollno: 5,

&nbsp;   age: 15

&nbsp; },

&nbsp; {

&nbsp;   \_id: ObjectId("699701b7d6c97ca026b2094d"),

&nbsp;   name: 'naniii',

&nbsp;   rollno: 10,

&nbsp;   age: 15,

&nbsp;   marks: 50

&nbsp; },

&nbsp; {

&nbsp;   \_id: ObjectId("699701d2d6c97ca026b2094e"),

&nbsp;   name: 'suma',

&nbsp;   rollno: 12,

&nbsp;   age: 21

&nbsp; }

]

###### &nbsp; Result:



Successfully executed CRUD operations in MongoDB and verified using mongosh.



###### Learning Outcome:



\* Understood NoSQL database structure

\* Learned document-based storage

\* Performed real-time database manipulation



