To enter a database
C:\Users\GANJA SRIVIDYA\Desktop\database>sqlite3 vidyadb   

Creation of tables
sqlite> CREATE TABLE flights(
(x1...> id INTEGER PRIMARY KEY AUTOINCREMENT,
(x1...> origin TEXT NOT NULL,
(x1...> destination TEXT NOT NULL,
(x1...> duration INTEGER NOT NULL
(x1...> );

To view the tables
sqlite> .tables
flights


to get the schem of it 
sqlite> .schema flights
CREATE TABLE flights(
id INTEGER PRIMARY KEY AUTOINCREMENT,
origin TEXT NOT NULL,
destination TEXT NOT NULL,
duration INTEGER NOT NULL
);

to enter details 
sqlite> INSERT INTO flights(origin, destination, duration) VALUES ('New York', 'london', 415);
for string values use only single quotes, doubel quotes will result in error

To view the details
sqlite> SELECT * FROM flights;
1|New York|london|415

to have a proper representatoin of the data 
sqlite> .mode columns
sqlite> .headers yes

sqlite> SELECT * FROM flights;
id  origin    destination  duration
--  --------  -----------  --------
1   New York  london       415
2   Shangai   Paris        760
3   Istanbul  Tokyo        700
4   New York  Paris        435
5   Moscow    Paris        245
6   Lima      New York     455


to get only required data instead of getting all of the flights
sqlite> SELECT * FROM flights WHERE origin='New York';
id  origin    destination  duration
--  --------  -----------  --------
1   New York  london       415
4   New York  Paris        435


have multiple constraints 
sqlite> select * from flights where duration>500 and destination = 'Paris';
id  origin   destination  duration
--  -------  -----------  --------
2   Shangai  Paris        760


if you want any of the constraints to be satisfied 
sqlite> select * from flights where duration>500 or destination = 'Paris';
id  origin    destination  duration
--  --------  -----------  --------
2   Shangai   Paris        760
3   Istanbul  Tokyo        700
4   New York  Paris        435
5   Moscow    Paris        245

we are looking for a row where a particular col val has some no of char maybe 0 or maybe more followed by a and then other no of characters
sqlite> SELECT * FROM flights WHERE origin LIKE '%a%';
id  origin    destination  duration
--  --------  -----------  --------
2   Shangai   Paris        760
3   Istanbul  Tokyo        700
6   Lima      New York     455

also have built-in functions
1.average
2.count
3.max
4.min
5.sum


