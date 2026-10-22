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

Als gebruiker w3schools deze database laden (met paswoord w3schoolspw):
```bash
mysql -u w3schools -p < NorthWindDB2.sql
```

Aanloggen als gebruiker w3schools aanloggen:
```bash
mysql -u w3schools -p
```

Controlleer of er customers in de database zitten:
```bash
USE northwind;
SELECT * from customers;
```

Vanaf nu kan je alle oefeningen (zowel lezen als schrijven, verwijderen) maken op deze database.

---
## Aanloggen met w3schools op database "northwind"

Indien je in de volgende les opnieuw moet inloggen in deze "Northwind"-database, dan doe je dit enkel met volgende commando's.

Als gebruiker w3schools deze database laden:
```bash
mysql -u w3schools -p
```
het paswoord is   w3schoolspw

Met volgende commando's kan je kijken in SQL welke database er beschikbaar is (wanneer je ingelogd bent in SQL)
```bash
show databases;
```
Nu je hier ook de database "Northwind" ziet staan kan je deze gebruiken door:

Als gebruiker w3schools deze database laden:
```bash
use northwind;
```

Wil je de tabellen van deze database bekijken, dan doe je dit met:
Als gebruiker w3schools deze database laden:
```bash
show tables;
```
vanaf hier kan je alle SQL-commando's uit de les toepassen op deze database (zowel lezen, schrijven, aanpassen en verwijderen)
vb
Als gebruiker w3schools deze database laden:
```bash
select * from products;
```
