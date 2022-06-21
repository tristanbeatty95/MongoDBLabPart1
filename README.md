# MongoDBLabPart1

 db.people.find()

 db.people.find().count()

 db.people.find({state: "Arizona"})

 db.people.find({state: "Arizona", gender: "Male"})

 db.people.find({$or: [{state: "Arizona"}, {state: "New Mexico"}]})

 db.people.find({age: {$lt: 40}})

 db.people.find({$and: [{state: "Florida"}, {gender: "Female"}, {$and: [{age: {$gte: 40}}, {age: {$lte: 45}}]}]})
	
 db.people.find({first_name: /^H/})

 db.people.find({state: "Michigan"}).sort({first_name: 1}) 

db.people.find({$or: [{state: "Virginia"}, {first_name: "Virginia"}, {last_name: "Virginia"}]})

db.people.find({age: {$lt: 30}}, {first_name: true, last_name: true})

db.people.find({state: "Montana"}, {age: false})

db.people.find({email: /.edu$/}, {email: true})
