# Ruby Basic language syntax

## Create an app with rails and postgresql

**Pour selectionner la version de Rails**
```shell
rails _5.2.3_ new -d postgresql NomDeAppli
```
**Version de Rails par default**
```shell
rails new -d postgresql NomDeAppli
```
--------------

<br>

**.inspect** == cat -e

--------------

**.downto**

--------------

**.upto**

--------------

**puts** : put a string on the output with a line break

ex: ```puts "Hello world!"```

---------------

**print** : put a string without line break

ex: ```print "Hello"
print "World"```

----------------

**gets.chomp** : get user input (like scanf) - it can be a specified type with:
gets.chomp.to_i (integer) // gets.chomp.to_s (string) // gets.chomp.to_f (float)

ex: ```name = gets.chomp```
ex: ```year = gets.chomp.to_i``` -> gets integer from the user input

----------------

**.chop** : remove last caracter of the string

ex: ```name = gets.chop```
ex: ```name.chop = dian```

-----------------

**.ord**

Convert a character to his ASCII value

------------------

**.chr**

Convert an ASCII value to his character

## Class is Ruby

```
"Hello".class<br>
=> String<br>

14000.class<br>
=> Integer<br>

3.5.class<br>
=> Float<br>

true.class<br>
=> TrueClass<br>

false.class<br>
=> FalseClass<br>
```

------------------

**.positive**

number > 0 == number.positive?

**.negative**

number < 0 == number.negative?