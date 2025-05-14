# LIMIT
to give us the top rows/ not every row frmo the db 
sqlite> SELECT * FROM flights;

id  origin    destination  duration
--  --------  -----------  --------
1   New York  london       430
2   Shangai   Paris        760
4   New York  Paris        435
5   Moscow    Paris        245
6   Lima      New York     455

sqlite> SELECT * FROM flights LIMIT 3;

id  origin    destination  duration
--  --------  -----------  --------
1   New York  london       430
2   Shangai   Paris        760
4   New York  Paris        435


# ORDER BY
to give in a particular order 

sqlite> SELECT * FROM flights ORDER BY duration;
id  origin    destination  duration
--  --------  -----------  --------
5   Moscow    Paris        245
1   New York  london       430
4   New York  Paris        435
6   Lima      New York     455
2   Shangai   Paris        760


sqlite> SELECT * FROM flights ORDER BY origin;
id  origin    destination  duration
--  --------  -----------  --------
6   Lima      New York     455
5   Moscow    Paris        245
1   New York  london       430
4   New York  Paris        435
2   Shangai   Paris        760


sqlite> SELECT * FROM flights ORDER BY destination;
id  origin    destination  duration
--  --------  -----------  --------
6   Lima      New York     455
2   Shangai   Paris        760
4   New York  Paris        435
5   Moscow    Paris        245
1   New York  london       430


# Group by 
groups the rows that have the same value in specified  columns

original: 
sqlite> SELECT * FROM flights;
id  origin    destination  duration
--  --------  -----------  --------
1   New York  london       430
2   Shangai   Paris        760
4   New York  Paris        435
5   Moscow    Paris        245
6   Lima      New York     455


sqlite> SELECT * FROM flights GROUP BY origin;
id  origin    destination  duration
--  --------  -----------  --------
6   Lima      New York     455
5   Moscow    Paris        245
1   New York  london       430
2   Shangai   Paris        760

sqlite> SELECT * FROM flights GROUP BY destination;
id  origin    destination  duration
--  --------  -----------  --------
6   Lima      New York     455
2   Shangai   Paris        760
1   New York  london       430


# Having 
having is basically a condition for group ur group them acc to specified col vals 
then ur giving a condition
to filter further 

sqlite> SELECT * FROM flights GROUP BY destination HAVING duration>500;
id  origin   destination  duration
--  -------  -----------  --------
2   Shangai  Paris        760
