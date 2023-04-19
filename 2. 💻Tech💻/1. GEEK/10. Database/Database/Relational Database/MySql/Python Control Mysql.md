#mysql #database #python 

The things that goes in to the excecute() is the same as [[Mysql Basics]]

# Config
```python
import mysql.connector

  

# Config

mydb = mysql.connector.connect(

  host="localhost",

  user="root",

  password="11223320050822qazWSX!!",

  database="python"

)

mycursor = mydb.cursor()
```

# Select
```python
def select():

  mycursor.execute("SELECT * FROM customers")

  myresult = mycursor.fetchall()

  for x in myresult:

    print(x)

```

# Table

## Insert Table
```python

  

def InsertTable():

  sql = ("Insert into customers (name, address) values (%s, %s)")

  val = [

  ('Peter', 'Lowstreet 4'),

  ('Amy', 'Apple st 652'),

  ('Hannah', 'Mountain 21'),

  ('Michael', 'Valley 345'),

  ('Sandy', 'Ocean blvd 2'),

  ('Betty', 'Green Grass 1'),

  ('Richard', 'Sky st 331'),

  ('Susan', 'One way 98'),

  ('Vicky', 'Yellow Garden 2'),

  ('Ben', 'Park Lane 38'),

  ('William', 'Central st 954'),

  ('Chuck', 'Main Road 989'),

  ('Viola', 'Sideway 1633')

]

 # when insert many data, then excecutemany, when only one, then only execute
  mycursor.executemany(sql, val)

  mydb.commit()

  

```

## Show Table

```python
def ShowTables():

  mycursor.execute("Show Tables")

  for x in mycursor:

    print(x)

  ```
## Create Table

```python
def CreateTable():

  mycursor.execute("CREATE TABLE customers (name VARCHAR(255), address VARCHAR(255))")

  
```
# Database
```python
def ShowDatabases():

  mycursor.execute("Show Databases")

  for x in mycursor:

    print(x)

  

def CreateDatabase(name):

  mycursor.execute("Create Database " + name)
```