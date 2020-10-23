# SQL commands cheatsheet

## CRUD en SQL

**CRUD : Create - Read - Update - Delete**

<p>Liste des commandes: 

<ul>Create = `INSERT`</ul>
<ul>Read = `SELECT`</ul>
<ul>Update = `UPDATE`</ul>
<ul>Delete = `DELETE`</ul>

</p>

## Utilisation des TABLES

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

**Accéder aux élements de la TABLE**

<p>Lire l'ensemble de la table users</p>

```SQL
SELECT * FROM users;
```

<p>Créer un nouvel users dans ma base de donnée:</p>

```SQL
INSERT INTO users (first_name, last_name, age) VALUES ('Prénom', 'NomdeFamille', 27);
```

<p>Selectionner des éléments en particulier:</p>

```SQL
SELECT * FROM users WHERE age = 27;
```

<p>Mettre à jour un paramètre:</p>

```SQL
UPDATE users SET age = 25 WHERE id = 1;
```

<p>Supprimer un élément:</p>  

```SQL
DELETE FROM users WHERE id = 1;
```





