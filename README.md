Program1 : Simple SQL Queries

create table class(Name varchar(50), age int);
insert into class (Name,age)
    -> values("Sailesh",20);
update class set age = 30 where name = "Sailesh";
delete from class where age = 30;
drop table class;

Program2 :Create and Insert in Mongo

Use college
db.createCollection(“College”)
db.college.insertOne({Name:”Sailesh”,Class:”DS”})

Program3 :Query Document

Use college
db.createCollection(“College”)
db.college.insertOne({Name:”Sailesh”,Class:”DS”})
 db.college.find({Age: {$gt:20}}).pretty()
db.college.find({Age: {$lt:20}}).pretty()
db.college.find({Age: {$lte:20}}).pretty()
db.college.find().pretty()

Program4: Query Manipulation

db.college.updateOne({Name:”Sailesh”},{$set:{Class:”III DS”}})
db.college.replaceOne({}, {Name:”Someone”,Class”III DS”})
db.college.deleteOne({Name:”Sailesh”})
db.college.deleteMany({Class:”III DS”})


Program5: Table Cloning

Export the file to JSON Format 
db.createCollection(“MoviesCopy”) 
Click on ADD DATA and load the JSON File 

Program6: JSON File

Use notepad and copy it and export in mongodb compass

  [{ "Name": "riyan", "Age": 50, "Mark": 450 }, 
{ "Name": "Siruthai", "Age": 15, "Mark": 300 }]


Program7: Search the Text

db.college.createIndex({Name:”text”, Description:”text”})
db.college.find({$text:{$search:"Sailesh"}})


Program8: Regular Expression

Add one more name with full Name with all small case
db.college.find({Name:{$regex:"Sailesh",$options:"i"}}).pretty()

Program9: Basic Operation in Mongo

db.createCollection("Records") 
db.Records.insertOne({Name:"Someone",Reason:"Something"}) 
db.Records.updateOne({Name: "Someone"}, {$set:{Name: "Tamu"}}) 
db.Records.deleteOne({Name: "Someone"}) 
db.Records.find() 

Program10: Replication

Mam will take the responsibility 

Program11: Indexing

db.college.createIndex({ Name : 1}) 
db.college.createIndex({ Class: 1}) 
db.college.getIndexes()


