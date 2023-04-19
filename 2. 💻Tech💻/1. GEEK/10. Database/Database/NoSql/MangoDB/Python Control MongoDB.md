#MangoDB #python #database 
# Config
```jsx
myclient = pymongo.MongoClient("localhost:27017")
```

# Database
## Create
```jsx
mydb = myclient["name"]
```

# Collection
## Create
```jsx
mycol = mydb["customer"]
```
## Insert
```jsx
data = {"name" : "lol", "address" : "olo street"}
mycol.insert_one(data) // there is also inert_many to insert more datas
```
## Update
```jsx
myquery = { "address": "Valley 345" }  
newvalues = { "$set": { "address": "Canyon 123" } }  
  
mycol.update_one(myquery, newvalues)
```
## Delete
```jsx
myquery = { "address": "Mountain 21" }  
  
mycol.delete_one(myquery)
```