## sample sql commands

Test the sql commands out > https://www.w3schools.com/Sql/tryit.asp?filename=trysql_select_top

- select customerName, city, country from Customers
- select customerName, country, city from Customers
- (select CustomerID as id, CustomerName, ContactName from Customers) is the same as (select CustomerID id, CustomerName, ContactName from Customers)
- select [first name] from People > (how to handle column names with spaces)
- Using a clause:

  - SELECT CustomerID as Id, CustomerName as Name, ContactName FROM Customers order by contactName
  - SELECT CustomerID as Id, country, city FROM Customers order by country, city
  - SELECT CustomerID as Id, country, city FROM Customers order by country desc, city desc

  wildcards in SQLite = \* >> all, '\_' >> exactly one letter, % >> wildcard operator in a string for example

  - SELECT country, city, customerID as id, customerName name, contactName FROM Customers where city like '\_er%' order by city;

  will return list of cities with exactly one letter before cities followed by er followed by anything

adding more than one param for filter example

- SELECT \* FROM Customers where city not in ('Berlin', 'London');

// ====================================
// 1/15/19 notes
// ====================================

- insert into customers (Country, CustomerName, ContactName, Address, City, PostalCode) values ('USA', 'Lambda School', 'Ben Tsao', '1 Lambda Court', 'Provo', '84444')

- select * from customers
    update customers set Address = 92
    where customerId = 93