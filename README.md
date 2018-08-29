
Create table Directors(
Director_ID int NOT NULL identity(1,1) PRIMARY KEY,
FirstName_Director varchar (200),
LastName_Director varchar (200),
Nationality_Director varchar (100),
Birth char (10)
)

Create table Movies(
Movie_ID int NOT NULL identity(1,1) PRIMARY KEY,
Director_ID int REFERENCES Directors(Director_ID),
Title varchar(200),
ReleaseYear char(4) CHECK (ReleaseYear BETWEEN 1800 AND 2025),
Plot varchar(200),
MovieLength time,
Rating int CHECK (Rating<=100)
)
SELECT * FROM Movies

Create table Actors(
Actor_ID int NOT NULL identity(1,1) PRIMARY KEY,
FirstName_Actors varchar (200),
LastName_Actors varchar (200),
Nationality_Actor varchar (100),
Birth char (10)
)

Create table MovieActor(
MovieActor_ID int NOT NULL identity(1,1) PRIMARY KEY,
Movie_ID int REFERENCES Movies(Movie_ID),
Actor_ID int REFERENCES Actors(Actor_ID)
)

Create table Genres(
Genre_ID int NOT NULL identity(1,1) PRIMARY KEY,
Genre_Name varchar(150)
)

Create table MovieGenres(
MovieGenres_ID int NOT NULL identity(1,1) PRIMARY KEY,
Movie_ID int REFERENCES Movies(Movie_ID),
Genre_ID int REFERENCES Genres(Genre_ID)
)

insert into Genres (Genre_Name) values ('Комедия')
insert into Genres (Genre_Name) values ('Мелодрама')
insert into Genres (Genre_Name) values ('Триллер')
insert into Genres (Genre_Name) values ('Фэнтези')

insert into Directors (FirstName_Director,LastName_Director,Nationality_Director,Birth) values ('Herc', 'Corbin','Афроамериканец', '8/29/1975')
insert into Directors (FirstName_Director,LastName_Director,Nationality_Director,Birth) values ('Hermia', 'Perez','Татарка','5/19/1984' )
insert into Directors (FirstName_Director,LastName_Director,Nationality_Director,Birth) values('Ferdinand', 'Setford','Русский','1/9/1969' )
insert into Directors (FirstName_Director,LastName_Director,Nationality_Director,Birth) values ('Augusta', 'Southers','Украинец','9/17/1971' )
insert into Directors (FirstName_Director,LastName_Director,Nationality_Director,Birth) values ('Marla', 'Trounson','Белорус','11/20/1966' )
insert into Directors (FirstName_Director,LastName_Director,Nationality_Director,Birth) values ('Buck', 'Kinlock','Казах','5/5/1965' )
select * from Directors

/* - 2 - */
insert into Movies (Director_ID,Title,ReleaseYear,Plot,MovieLength,Rating) values (1,'Medac Pharma, Inc',1995,'1565', '01:40',100);
insert into Movies (Director_ID,Title,ReleaseYear,Plot,MovieLength,Rating) values (2,'HOMEOLAB USA INC',2001,'3245', '01:30',90);
insert into Movies (Director_ID,Title,ReleaseYear,Plot,MovieLength,Rating) values (3,'Publix Super Markets Inc',2005,'6784', '01:29',80);
insert into Movies (Director_ID,Title,ReleaseYear,Plot,MovieLength,Rating) values (4,'NATURE REPUBLIC CO., LTD.',2002,'6783', '01:10',80);
insert into Movies (Director_ID,Title,ReleaseYear,Plot,MovieLength,Rating) values (5,'Meijer Distribution Inc',2006,'5278', '01:15',70);
insert into Movies (Director_ID,Title,ReleaseYear,Plot,MovieLength,Rating) values (6,'DZA Brands LLC',2011,'27485', '01:35',50);
insert into Movies (Director_ID,Title,ReleaseYear,Plot,MovieLength,Rating) values (1,'Claris Lifesciences Inc.',2000,'3783', '01:34',60);
insert into Movies (Director_ID,Title,ReleaseYear,Plot,MovieLength,Rating) values (2,'Deseret Biologicals, Inc.',2015,'2786', '01:36',80);
insert into Movies (Director_ID,Title,ReleaseYear,Plot,MovieLength,Rating) values (3,'ALK-Abello, Inc.',2016,'6783', '01:11',90);
insert into Movies (Director_ID,Title,ReleaseYear,Plot,MovieLength,Rating) values (4,'PD-Rx Pharmaceuticals, Inc.',2017,'6783', '01:15',90);
insert into Movies (Director_ID,Title,ReleaseYear,Plot,MovieLength,Rating) values (5,'STOP HAIR PTY LTD',2005,'6786', '01:34',80);
insert into Movies (Director_ID,Title,ReleaseYear,Plot,MovieLength,Rating) values (6,'Cardinal Health',1998,'6767', '02:10',100);
insert into Movies (Director_ID,Title,ReleaseYear,Plot,MovieLength,Rating) values (1,'REMEDYREPACK INC.',2010,'5763', '01:34',70);
insert into Movies (Director_ID,Title,ReleaseYear,Plot,MovieLength,Rating) values (2,'Colgate-Palmolive Company',2018,'6347', '01:37',60);
insert into Movies (Director_ID,Title,ReleaseYear,Plot,MovieLength,Rating) values (3,'C.F.E.B. Sisley',2017,'3783', '01:40',50);
insert into Movies (Director_ID,Title,ReleaseYear,Plot,MovieLength,Rating) values (4,'Henry Schein, Inc.',2001,'6786', '01:38',40);
insert into Movies (Director_ID,Title,ReleaseYear,Plot,MovieLength,Rating) values (5,'Schryver Medical Sales and Marketing, Inc.',2003,'4654', '01:27',60);
insert into Movies (Director_ID,Title,ReleaseYear,Plot,MovieLength,Rating) values (6,'Clinigen Healthcare Ltd.',2010,'6767', '01:21',80);
insert into Movies (Director_ID,Title,ReleaseYear,Plot,MovieLength,Rating) values (1,'Mylan Pharmaceuticals Inc.',2012,'2732', '01:11',80);
insert into Movies (Director_ID,Title,ReleaseYear,Plot,MovieLength,Rating) values (2,'Lake Erie Medical & Surgical Supply DBA Quality Care Products LLC',2013,'2743', '01:38',90);
insert into Movies (Director_ID,Title,ReleaseYear,Plot,MovieLength,Rating) values (3,'3M Health Care',2017,'9846', '01:23',100);
SELECT * FROM Movies

insert into MovieGenres(Movie_ID,Genre_ID) values (1,2);
insert into MovieGenres(Movie_ID,Genre_ID) values (2,1);
insert into MovieGenres(Movie_ID,Genre_ID) values (3,3);
insert into MovieGenres(Movie_ID,Genre_ID) values (4,4);
insert into MovieGenres(Movie_ID,Genre_ID) values (5,1);
insert into MovieGenres(Movie_ID,Genre_ID) values (6,3);
insert into MovieGenres(Movie_ID,Genre_ID) values (7,2);
insert into MovieGenres(Movie_ID,Genre_ID) values (8,4);
insert into MovieGenres(Movie_ID,Genre_ID) values (9,1);
insert into MovieGenres(Movie_ID,Genre_ID) values (10,3);
insert into MovieGenres(Movie_ID,Genre_ID) values (11,3);
insert into MovieGenres(Movie_ID,Genre_ID) values (12,2);
insert into MovieGenres(Movie_ID,Genre_ID) values (13,1);
insert into MovieGenres(Movie_ID,Genre_ID) values (14,4);
insert into MovieGenres(Movie_ID,Genre_ID) values (15,2);
insert into MovieGenres(Movie_ID,Genre_ID) values (16,1);
insert into MovieGenres(Movie_ID,Genre_ID) values (17,3);
insert into MovieGenres(Movie_ID,Genre_ID) values (18,4);
insert into MovieGenres(Movie_ID,Genre_ID) values (19,1);
insert into MovieGenres(Movie_ID,Genre_ID) values (20,3);
insert into MovieGenres(Movie_ID,Genre_ID) values (21,2);

insert into Actors (FirstName_Actors,LastName_Actors,Nationality_Actor,Birth) values ('Janina', 'Puttergill','Афроамериканец', '1/15/1970')
insert into Actors (FirstName_Actors,LastName_Actors,Nationality_Actor,Birth) values ('Kamila', 'Dauncey','Американец','12/9/1975' )
insert into Actors (FirstName_Actors,LastName_Actors,Nationality_Actor,Birth) values('Gordan', 'Danes','Русский','6/19/1984' )
insert into Actors (FirstName_Actors,LastName_Actors,Nationality_Actor,Birth) values ('Fons', 'Pennacci','Украинец','7/28/1985' )
insert into Actors (FirstName_Actors,LastName_Actors,Nationality_Actor,Birth) values ('Felicio', 'Nise','Чуваш','1/1/1968' )
insert into Actors (FirstName_Actors,LastName_Actors,Nationality_Actor,Birth) values ('Madalyn', 'Abramovitz','Казах','3/12/1980' )
insert into Actors (FirstName_Actors,LastName_Actors,Nationality_Actor,Birth) values ('Piggy', 'Sokill','Узбек','4/19/1986' )
insert into Actors (FirstName_Actors,LastName_Actors,Nationality_Actor,Birth) values ('Marybelle', 'Matijasevic','Киргиз','8/25/1990' )

insert into MovieActor(Movie_ID,Actor_ID) values (1,1);
insert into MovieActor(Movie_ID,Actor_ID) values (2,2);
insert into MovieActor(Movie_ID,Actor_ID) values (3,3);
insert into MovieActor(Movie_ID,Actor_ID) values (4,4);
insert into MovieActor(Movie_ID,Actor_ID) values (5,5);
insert into MovieActor(Movie_ID,Actor_ID) values (6,6);
insert into MovieActor(Movie_ID,Actor_ID) values (7,1);
insert into MovieActor(Movie_ID,Actor_ID) values (8,2);
insert into MovieActor(Movie_ID,Actor_ID) values (9,3);
insert into MovieActor(Movie_ID,Actor_ID) values (10,4);
insert into MovieActor(Movie_ID,Actor_ID) values (11,5);
insert into MovieActor(Movie_ID,Actor_ID) values (12,6);
insert into MovieActor(Movie_ID,Actor_ID) values (13,1);
insert into MovieActor(Movie_ID,Actor_ID) values (14,2);
insert into MovieActor(Movie_ID,Actor_ID) values (15,3);
insert into MovieActor(Movie_ID,Actor_ID) values (16,4);
insert into MovieActor(Movie_ID,Actor_ID) values (17,5);
insert into MovieActor(Movie_ID,Actor_ID) values (18,6);
insert into MovieActor(Movie_ID,Actor_ID) values (19,1);
insert into MovieActor(Movie_ID,Actor_ID) values (20,2);
insert into MovieActor(Movie_ID,Actor_ID) values (21,3);
insert into MovieActor(Movie_ID,Actor_ID) values (2,3);
SELECT * FROM MovieActor

/* - 3 - */
/*Выбрать все фильмы одного жанра.*/
SELECT Title,Genre_Name From MovieGenres,Movies,Genres WHERE Genres.Genre_ID=1 AND Genres.Genre_ID=MovieGenres.Genre_ID AND MovieGenres.Movie_ID=Movies.Movie_ID

/* - 4 - */
/*Выбрать все фильмы, в которых снимались актеры, чьи имена начинаются на ‘F’.*/
SELECT FirstName_Actors,LastName_Actors,Title FROM Movies,Actors,MovieActor WHERE FirstName_Actors LIKE 'F%' AND MovieActor.Actor_ID=Actors.Actor_ID AND MovieActor.Movie_ID=Movies.Movie_ID

/* - 5 - */
/*Сделать выборку из таблицы Movies с отображением колонок Title, GenreName, DirectorFirstName+DirectorLastName, Rating с сортировкой по убыванию*/
SELECT M.Title,G.Genre_Name,D.FirstName_Director+' '+D.LastName_Director AS Name_Actor,M.Rating 
FROM Movies M, Genres G, Directors D ,MovieGenres MG
WHERE MG.Movie_ID=M.Movie_ID AND MG.Genre_ID=G.Genre_ID AND M.Director_ID=D.Director_ID
ORDER BY m.Rating DESC

/* - 6 - */
/*Удалить определенный фильм*/
DELETE from MovieActor WHERE MovieActor.Movie_ID=1
DELETE from MovieGenres WHERE MovieGenres.Movie_ID=1
Delete from Movies WHERE Movies.Movie_ID=1
SELECT * FROM Movies

/* - 7 - */
/*Добавить нового актера в таблицу «Actors».*/
insert into Actors (FirstName_Actors,LastName_Actors,Nationality_Actor,Birth) values ('Afafa', 'Abramfafafovitz','fasfa','3/12/1970' )

/* - 8 - */
/*Изменить дату рождения определенного режиссера.*/
Update Directors SET Birth='4/11/1971' WHERE Director_ID=3

/* - 9 - */
/* Выбрать всех актеров, снимавшихся в определенном фильме.*/
SELECT A.FirstName_Actors+' '+A.LastName_Actors AS NAME_ACTOR, M.Title 
FROM Actors A,MovieActor MA,Movies M
WHERE A.Actor_ID=MA.Actor_ID AND M.Movie_ID= MA.Movie_ID AND M.Movie_ID =2

/* - 10 - */
/* Выбрать список фильмов, выпущенных в текущем году */
SELECT M.Title,M.ReleaseYear FROM Movies M WHERE M.ReleaseYear= 2017

/* - 11 - */
SELECT G.Genre_Name , COUNT (M.Movie_ID) AS 'Quantity'
FROM Movies M,Genres G,MovieGenres MG
WHERE m.Movie_ID=mg.Movie_ID AND G.Genre_ID=MG.Genre_ID
GROUP BY G.Genre_Name

/* - 12 - */
SELECT G.Genre_Name , COUNT (M.Movie_ID) AS 'Quantity',AVG(Rating) AS 'AVG'
FROM Movies M,Genres G,MovieGenres MG
WHERE m.Movie_ID=mg.Movie_ID AND G.Genre_ID=MG.Genre_ID
GROUP BY G.Genre_Name

/* - 13 - */
SELECT A.FirstName_Actors+' '+a.LastName_Actors AS 'Name_Actor', COUNT(Title) AS 'Quantity'
FROM Movies M,MovieActor MA,Actors A
WHERE m.Movie_ID=ma.Movie_ID AND ma.Actor_ID=a.Actor_ID
GROUP BY A.FirstName_Actors+' '+a.LastName_Actors

/* - 14 - */
SELECT D.FirstName_Director+' '+D.LastName_Director AS 'Name_Dir', COUNT(Title) AS 'Quantity'
FROM Movies M,Directors D
WHERE M.Director_ID=D.Director_ID
GROUP BY D.FirstName_Director+' '+D.LastName_Director

/* - 15 - */
SELECT TOP 1 M.Title, MIN(M.MovieLength) AS 'MIN TIME' FROM Movies M GROUP BY M.Title, M.MovieLength

SELECT M.Title,m.MovieLength FROM Movies M WHERE M.MovieLength=(SELECT min(MovieLength)FROM Movies)
