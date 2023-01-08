# subqueries

/*

1. 
select avg (scost)
from software
where developin = 'pascal'

2.
select pname, year (getdate ()) - year(dob) as age
from programmer

3.
select p.pname
from programmer as p
inner join studies as s on p.pname = s.pname
where course = 'dap'

4.
select pname, dob
from programmer
where month(dob) = 1

5.
select max(sold)
from software
group by developin

6.
select min (fee)
from studies

7.
select count (pname)
from studies
where course = 'pgdca'

8.
select sum (sold * scost)
from software
where developin = 'c'

9.
select *
from programmer
where pname = 'ramesh'

10.
select count(pname)
from programmer as p
inner join studies on p.pname = studies.pname
where iname = 'sabhari'

11.
select *
from software
where (scost * sold) > 2000

12.
select *
from software
where sum(scost * sold) > dcost

13.
select max(dcost)
from software
where developin = 'basic'

14.
select count (title)
from software
where technology = 'dbase'

15.
select count (programmer.pname)
from programmer
inner join studies on programmer.pname = studies.pname
where iname = 'pragathi'

16.
select count(programmer.pname)
from programmer
inner join studies on programmer.pname = studies.pname
where coursefee between 5000 and 10000

17.
select avg (coursefee)
from studies

18.
select *
from programmer
where prof1 = 'c' or prof2 = 'c'

19.
select count (pname)
from programmer
where prof1 in ('cobol', 'pascal') or prof2 in ('cobol', 'pascal')

20.
select count (pname)
from programmer
where prof1 not in ('c', 'pascal') and prof2 not in ('c', 'pascal')

21. How old is the Oldest Male Programmer. 

select max (year (getdate ()) - year(dob)) as oldestage
from programmer
where gender = 'M'

22.
select avg (year (getdate ()) - year(dob)) as avgage
from programmer
where gender = 'F'

23.
select year(year(getdate()) - year(doj)) , pname
from programmer
order by pname desc

24.
select pname
from programmer
where month(getdate ()) = month (dob)

25.
select count(pname)
from programmer
where gender = 'F'

26.
select course
from studies
inner join on programmer where programmer.pname = studies.pname
where gender = 'm'

27.
select avg (salary)
from programmer

28.
select count(pname)
from programmer
where salary between 2000 and 4000

29.
select *
from programmer
where prof1 not in ('pascal', 'cobol', 'clipper') or prof1 not in ('pascal', 'cobol', 'clipper')

30.
select pname, dcost
from software
group by pname

31.
select pname, sum (scost * sold)
from software
group by pname

32.
select pname, sold
from software
group by pname

33.
select pname, scost
from programmer
group by developin, pname

34.
select developin, avg (dcost), avg(scost), (select avg(scost * sold) from software group by developin)
from software
group by developin

35.
select pname, max(dcost), min (dcost)
from software
group by pname

36.
select iname, count(course), avg(coursefee)
from studies
group by iname

37.
select iname, count(pname)
from studies
group by iname

38.
select pname, gender
from programmer

39.
select pname, title
from software

40.
select count(package)
from software
where developin not in ('c', 'c++')

41.
select developin, count(title)
from software
where dcost < 1000
group by developin

42.
select title, avg ((scost) - (dcost))
from software
group by title

43.
select name, sum (scost), sum(dcost), sum (dcost) - sum(scost) as recoveryamount
from software
group by pname
where dcost > sum (sold * scost)

44.
 SELECT MAX(SALARY), MIN(SALARY), AVG(SALARY) 
 FROM PROGRAMMER 
 WHERE SALARY > 2000

 45.
 select pname
 from programmer
 where salary = (select max(salary) from programmer where prof1 = 'c' or prof2 = 'c') and (where prof1 = 'c' or where prof2 = 'c')

 46.
 select pname
 from programmer
 where salary = (select max(salary) from programmer where technology = 'cobol' and  gender = 'f')
 and (where prof1 = 'cobol' or where prof2 = 'cobol') and gender = 'f'

 47. 
 select pname, prof1
 from programmer
 where salary = (select max(salary) from programmer group by prof1)
 group by prof1
 union
 select pname, prof2
 from programmer
 where salary = (select max(salary) from programmer group by prof2)
 group by prof2

 48.
 select pname
 from programmer
 where DATEDIFF(day,doj, getdate()) = (select min (DATEDIFF(day,doj, getdate())) from programmer)

 49.
 select pname
 from programmer
 where skill = 'pascal' and DATEDIFF(day,doj, getdate()) = (select max (DATEDIFF(day,doj, getdate())) from programmer where prof1 = 'pascal' or prof2 = 'pascal')

 50.
 select prof1
 from programmer
 group by prof1
 having count(prof1) = 1
 union
 select prof2
 from programmer
 group by prof2
 having count(prof2) = 1

 51. select pname
     from programmer
	 where prof 1 in 
 (select prof1
 from programmer
 group by prof1
 having count(prof1) = 1)
     or prof2 in 
 (select prof2
 from programmer
 group by prof2
 having count(prof2) = 1)

 52.
 select pname
 from programmer
 where datediff(day, dob, getdate ()) =
 (
 select min (datediff(day, dob, getdate ())) 
 from programmer
 where technology = 'dbase'
 )
 and technology = 'dbase'

 53.
 select pname
 from programmer
 where salary > 3000 and gender = 'f' and prof1 not in ('c' , 'c++' , 'oracle' , 'dbase')
 union
 select pname
 from programmer
 where salary > 3000 and gender = 'f' and prof2 not in ('c' , 'c++' , 'oracle' , 'dbase')

 54.
 SELECT iname 
 FROM STUDIES 
 GROUP BY iname 
 HAVING  count (iname) = (select top 1 count (iname) from studies group by iname order by count(iname) desc)

 55.
 select course
 from studies
 where price = (select max(price) from studies)

 56.
 SELECT course
 FROM STUDIES 
 GROUP BY course
 HAVING  count (course) = (select top 1 count (course) from studies group by cname order by count(course) desc)

 57.
 select iname
 from studies
 where coursefee = (select max (coursefee) from studies)

 58.
 select iname, course
 from studies
 where coursefee < (select avg(coursefee) from studies)

 59.
 select course
 from studies
 where coursefee > (select 1000 - avg(coursefee) from studies) and coursefee < (select 1000 + avg(coursefee) from studies)

 60.
 select title
 from software
 where dcost = (select max (dcost) from software)

 61. select course
 from studies
 group by course
 having count (course) <
 (
 (select count (pname) from studies) / (select count (course) from studies)
 )

 62.
 select title
 from software
 where scost = (select min (scost) from software)

 63.
 select pname
 from software
 where sold = (select min(sold) from software)

 64.
 select developin
 from software
 where sold * scost = (select max (sold * scost) from software)

 65.
 select count (title)
 from software
 where (dcost - scost) = select min ((dcost - scost)) from software)

 66.
 select title
 from software
 where dcost = (select max (dcost) from software where developin = 'pascal') and developin  = 'pascal'

 67.
 select developin 
 from software
 group by developin 
 having count (developin) = (select top 1 count(developin) from software  group by developin  order by count(developin) desc)

 68.
 select pname
 from software
 group by pname
 having count (pname) = (select top 1 count(pname) from software group by pname order by count(pname) desc)

 69.
 select pname
 from software
 where dcost = (select max(dcost) from software)

 70.
 select title
 from software
 where sold < (select avg(sold) from software)

 71.
 select pname
 from software
 where sold * scost > 2 * dcost
 
 72.
 select pname, developin, title
 from software
 where dcost = (select min(dcost) from software group by developin)
 group by pname , developin

 73.
 select pname, developin
 from software
 where sold in (select max(sold) from software group by pname)
 group by pname
 union
 select pname, developin
 from software
 where sold in (select min(sold) from software group by pname)
 group by pname

 74.
 select pname
 from programmer
 where gender = 'm' 
 and datediff (day, dob, getdate()) = (select min (datediff (day, dob, getdate())) from programmer where year(dob) = 1965)
 and year (dob) = 1965

 75.
 select pname
 from programmer
 where gender = 'f' and datediff (day, dob, getdate()) = (select max (datediff (day, dob, getdate())) from programmer where year(doj) = 1992)
 and year(doj) = 1992

 76.
 select year(dob)
 from programmer
 group by year(dob)
 having count(year(dob)) = (select top 1 count(year(dob)) from programmer group by year(dob) order by count(year(dob)) desc)

 77.
 select month(doj)
 from programmer
 group by month(doj)
 having count(month(doj)) = (select top 1 count(month(doj)) from programmer group by month(doj) order by count(month(doj)) desc)

 78.
 select prof1
 from programmer
 group by prof1
 having count(prof1) > (select top 1 count(prof2) from programmer group by prof2 order by count(prof2) desc)
 union
 select prof2
 from programmer
 group by prof2
 having count(prof2) > (select top 1 count(prof1) from programmer group by prof1 order by count(prof1) desc)



 79.
 select pname
 from programmer
 where gender = 'M' and salary < (select avg(salary) from programmer where gender = 'f')

 80.
 select pname
 from programmer
 where gender = 'f' and salary > (select max(salary) from programmer where gender = 'm')

 81.
 select prof1
 from programmer
 group by prof1
 having count(prof1) > (select top 1 count(prof2) from programmer group by prof2 order by count(prof2) desc)
 union
 select prof2
 from programmer
 group by prof2
 having count(prof2) > (select top 1 count(prof1) from programmer group by prof1 order by count(prof1) desc)

 82.
 select pname, salary
 from programmer 
 where salary in 
 (
 select salary
 from programmer
 group by salary
 having count(salary) > 1
 )
 order by salary desc

 83.
 select *
 from programmer as p
 inner join software as s on p.id = s.id
 where salary > 3000 and gender = 'M'

 84.
 select title, scost, dcost, sold
 from programmer as p
 inner join software as s on p.id = s.id
 where developin = 'pascal' and gender = 'F'

 85.
 select *
 from programmer
 where year(doj) > 1990

 86.
 select title, scost, dcost, sold
 from software as s
 inner join programmer as p on p.id = s.id
 inner join studies as st on st.id = p.id
 where gender = 'f' and iname = 'pragathi'

 87.
 
 select count(package), sold, scost * sold , pname, iname
 from programmer as p
 inner join studies as s on s.id = p.id
 inner join software as so on so.id = p.id
 group by iname, pname

 88.
select title, pname, sold
from software as s
inner join studies as st on st.id = s.id
where iname =
(select iname
from studies
group by iname
having count(iname) = (select top 1 count (iname) from studies))
and developin = 'dbase' and gender = 'M'

89.

select title, developin, sold
from software as s
inner join programmer as p on p.pname = s.pname 
where gender = 'M' and year(dob) < 1965

union

select title, developin, sold
from software as s
inner join programmer as p on p.pname = s.pname
where gender = 'f' and year (dob) > 1975

90.
select *
from software as s
inner join programmer as p on p.pname = s.pname
where developin not in (select prof1 from programmer union select prof2 from programmer)

91.
select title, developin, sold
from software as s
inner join programmer as p on p.pname = s.pname
inner join studies as st on st.pname = s.pname
where gender = 'm' and iname = 'sabhari'

92.
select p.pname
from software as s
right join programmer as p on p.pname = s.pname
where title is null

93.
select sum (sold * scost)
from software
where developin = 'apple'

94.
select pname, doj
from programmer
where doj in
(
select doj
from programmer
group by doj
having count (doj) > 1
)
order by count(doj) desc

95.
select pname, prof2
from programmer
where prof2 in
(
select prof2
from programmer
group by prof2
having count (prof2) > 1
)
order by count (prof2) desc

96.
select sold * scost , iname
from software as s
inner join studies as st on s.pname = st.pname
group by iname

97.
select iname
from studies as st
inner join software as s on s.pname = st.pname
where dcost = (select max (dcost) from software)

98.
select prof1, prof2
from programmer as p
inner join software as s on s.name = p.name
where prof1 not in (select developin from software) or prof2 not in (select developin from software)

99.
select salary, course
from studies as st
inner join programmer as p on st.pname = p.pname
inner join software as s on s.pname = p.pname
where sold = (select max (sold) from software) 

100.
select avg (salary)
from programmer as p
inner join software as s on s.pname = p.pname
where (sold * scost) > 50000

101.
select count (title)
from software as s
inner join studies as st on st.pname = s.pname
where coursefee in (select min(coursefee) from studies)

102.
select count (title), iname
from software as s
inner join studies as st on st.pname = s.pname
where dcost = (select min (dcost) from software)
group by s.pname

103.
select count(package)
from software as s
inner join programmer as p on s.pname = p.pname
where gender = 'F' and salary > (select max (salary) from programmer where gender = 'M')

104.
select count (title)
from software as s
inner join studies as st on st.pname = s.pname
where datediff (day, doj, getdate ()) = 
(
select max(datediff (day, doj, getdate ()))
from programmer as p
inner join studies as s on p.pname = s.pname
where iname = 'bdps'
)
group by s.pname

105.
select s.pname, iname
from software as s
inner join studies as st on s.pname = st.pname

106.
select prof1 , count(s.pname), count(title)
from software as s
inner join programmer as p on s.pname = p.pname
group by prof1
union
select prof2 , count(s.pname), count(title)
from software as s
inner join programmer as p on s.pname = p.pname
group by prof2

107.
select p.pname, count (title)
from programmer as p
inner join software as s on s.pname = p.pname 
group by p.pname
