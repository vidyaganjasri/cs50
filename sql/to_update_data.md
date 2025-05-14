to update 
prev: 
id  origin    destination  duration
--  --------  -----------  --------
1   New York  london       415
2   Shangai   Paris        760
3   Istanbul  Tokyo        700
4   New York  Paris        435
5   Moscow    Paris        245
6   Lima      New York     455

sqlite> UPDATE flights
   ...> SET duration = 430
   ...> WHERE origin = 'New York' AND destination='london';


sqlite> SELECT * FROM flights;
id  origin    destination  duration
--  --------  -----------  --------
1   New York  london       430
2   Shangai   Paris        760
3   Istanbul  Tokyo        700
4   New York  Paris        435
5   Moscow    Paris        245
6   Lima      New York     455
