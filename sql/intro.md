sql allows to store data
ex: sql, postgreSQL,SQLite

each of these data has type, each dbms has its own type
## Data types
sql lite: text, numeric(date,boolean), integer, real ,blob(binary large object, audio files, imaegs)
Mysql: CHAR(size) if we know max length adn that is fixed,   VARCHAR(size) if something up to certain char, 
       SMALLINT, INT, BIGINT
       FLOAT, DOUBLE(helps us to be precise) ... 

# commands
## to create a table
CREATE TABLE flighta(
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    origin TEXT NOT NULL,
    destination TEXT NOT NULL, 
    duration INTEGER NOT NULL
);

## types
id is integer 
origin, destination, is text
duration is int(minutes)

## additional constraints
to acess a particualr flight uniquely we use primary key 
Not null to be able to say don't want that col to  ever be empty 
autoincrement giving a row next available id automatically sql gives it 

# constraints 
check      : to ensure that particular col values withing the range
default    : gives default value 
not null 
primary 
unique      : guarantees unique values, so that particular col doesn't have dup values

## Insert 
to insert data 
INSERT INTO flights
  (origin, destination, duration)
  values("new york", "london", 415)

leaving out id since it is auto increment


# to retriev the data 
## select query 
takes a table allows us to get data out of the table, not modies, but retruevs dat 

SELECT * FROM FLIGHTS;

*: indicates everything 


to select particular col 

SELECT origin, destination FROM flights; 



# to get a particluar row/rows
SELECT * FROM filghts WHERE id = 3;

SELECT * FROM flights WHERE origint="NEW YORK";



