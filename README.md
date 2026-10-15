# Northwind database


This is an extended version of the Northwind database  (from w3schools)

Use on a linuxcomputer folowing commands:

```bash
cd
```

```bash
git clone https://github.com/jmo2300/NorthwindDB2
```

```bash
cd NorthwindDB2
```




##  Database en tabellen aanmaken
Eerst als sudo:
```bash
sudo mysql -u root -p
```
Geef ons afgesproken paswoord (blind: je ziet geen characters verschijnen) 
Kopieer onderstaande code om de database aan te maken

```bash
CREATE DATABASE northwind;
USE northwind;
CREATE USER 'w3schools'@'localhost' IDENTIFIED BY 'w3schoolspw';
GRANT ALL PRIVILEGES ON northwind.* TO 'w3schools'@'localhost';
FLUSH PRIVILEGES;
QUIT;
```

Als gebruiker w3schools deze database laden:
```bash
mysql -u w3schools -p < NorthWindDB2.sql
```

Aanloggen als gebruiker w3schools aanloggen:
```bash
mysql -u w3schools -p
```

```bash
USE northwind;
SELECT * from Customers;
```

Vanaf nu kan je alle oefeningen (zowel lezen als schrijven, verwijderen) maken op deze database.
