# SQL commands cheatsheet

**Creation de table 'user' example**

<p>Avec la commande <b>AUTOINCREMENT</b>, on laisse la base de données s'occuper de l'incrémentation automatique de l'id : à chaque fois qu'une entrée sera créée dans la table user, elle portera un nouvel id (égal au dernier id + 1). </p>

```SQL
CREATE TABLE `user` (
`id` INTEGER PRIMARY KEY AUTOINCREMENT, 
`first_name` TEXT,
`last_name`TEXT,
`age` INTEGER
);
```

## CRUD en SQL

**CRUD : Create - Read - Update - Delete**

<p>Liste des commandes: 

<ul>Create = `INSERT`</ul>
<ul>Read = `SELECT`</ul>
<ul>Update = `UPDATE`</ul>
<ul>Delete = `DELETE`</ul>

</p>

## Accéder aux élements de la TABLE

<p>Lire l'ensemble de la table user</p>

```SQL
SELECT * FROM user;
```

<p>Créer un nouvel user dans ma base de donnée:</p>

```SQL
INSERT INTO user (first_name, last_name, age) VALUES ('Prénom', 'NomdeFamille', 27);
```




