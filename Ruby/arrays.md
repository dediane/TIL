# Arrays & Hashes in Ruby language 

### Declaration of an array in Ruby:

**Array.new**

 ex:```myArray = Array.new   # => []```

**.push**

 push dans un array
 
 ### puts two arrays in an hash 
 
 **array1** is an array of *keys*
 **array2** is an array of *values*
 
 ```hash= Hash[array1.zip(array2.map {|i|})]```
 
 ### Calculate the length of an array:
 
 ```myarray.length```
 or 
 ```myarray.size```
 
 ex : ```myarray = ["hello", "salut", "ciao"]
 myarray.size => 3```
 
 ### Select element in an array or an hash
 
 **.select**
 
 select elements in an array that we can stock in a new array or that we can display with "puts"
 
 example in a hash: ```array_tostock = myhash.select {|k,v| v == 0}```
 this line will stock the value equal to zero in the *array_tostock* from the hash *myhash*
 
 ### Sort 
 
 **.sort**
 
 sort element in an array by ascii index -> myarray.sort
 to sort alphabetical without case -> myarray.sort(&:casecmp)
 
 
 **.max & .min**
 
 .min and .max are 2 methods to find the max value and the min value in an array.
 ex: ```myarray = [1, 2, 3]
 myarray.min => 1
 myarray.max => 3```
 
 
**.delete**

supprime des éléments d'un array

**.include?**

permet de savoir si un array contient une valeur, renvoie True ou False

**.sample(n)**

permet de selectionner aléatoirement "n" objets de ton array.
 
