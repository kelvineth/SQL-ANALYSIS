# SQL-ANALYSIS

# SQL-ANALYSIS
#downloaded a education database from kaggle
#created a table to insecta data into it
# use sql to analysis the data
create table graduates(
`index` int not null auto_increment primary key,
major_code int null ,
major text null,
Major_Category text null,
total int null,
Men int null,
Women int null,
Employed int null,
Umemployment int null,
`umemployment rate` decimal(4,2) null

); 

insert into graduates (major_code,major,Major_Category,Total,Men,Women,Employed,Umemployment,`umemployment rate`)
 Values(2012,"Medicine","Health Sciences",40000,20000,20000,30000,10000,25.02);

#calcutating the total number of student admitted into each Major_Program grouping them into men and women
select Major_Category ,sum(Men) as Men,sum(Women) as Women,sum(total) as Total from `recent-grads`
 group by Major_category order by total desc;

 #selecting the Major_category with most women 
 select * from `recent-grads` order by Women desc limit 1;
 
