to delete a file 
prev: 
sqlite> SELECT * FROM flights;
id  origin    destination  duration
--  --------  -----------  --------
1   New York  london       430
2   Shangai   Paris        760
3   Istanbul  Tokyo        700
4   New York  Paris        435
5   Moscow    Paris        245
6   Lima      New York     455


code: 
DELETE FROM flights WHERE destination='Tokyo';

sqlite> SELECT * FROM flights;
id  origin    destination  duration
--  --------  -----------  --------
1   New York  london       430
2   Shangai   Paris        760
4   New York  Paris        435
5   Moscow    Paris        245
6   Lima      New York     455
