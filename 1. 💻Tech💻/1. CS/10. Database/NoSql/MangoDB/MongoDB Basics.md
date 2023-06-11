#MangoDB #database  
# Database
## Create a Database
```jsx
use blog
```
# Collection
## Create a Collection
```jsx
db.CreateCollection("Name")
```
## Insert into a Collection

```jsx
db.posts.insertOne({
  title: "Post Title 1",
  body: "Body of post.",
  category: "News",
  likes: 1,
  tags: ["news", "events"],
  date: Date()
})
```

```jsx
db.posts.insertMany([  
  {
    title: "Post Title 2",
    body: "Body of post.",
    category: "Event",
    likes: 2,
    tags: ["news", "events"],
    date: Date()
  },
  {
    title: "Post Title 3",
    body: "Body of post.",
    category: "Technology",
    likes: 3,
    tags: ["news", "events"],
    date: Date()
  },
  {
    title: "Post Title 4",
    body: "Body of post.",
    category: "Event",
    likes: 4,
    tags: ["news", "events"],
    date: Date()
  }
])
```

## find
```jsx
db.CollectionName.find( {category: "News"} )

db.CollectionName.find( {}, {"name"} ) // same as select name from CollectionName
```

## Update($set)

```jsx
db.posts.updateOne( { title: "Post Title 1" }, { $set: { likes: 2 } } ) 
```