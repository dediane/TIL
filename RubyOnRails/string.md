# String manipulation in Ruby

**.delete("")**

delete the letters you give in input from the original string

example 
`remove all vowels:`  
`string = "hello world" `    
`string.delete("aeiou") => hll wrld`    
`string = "heLLO World"`   
`string.delete("aeiouAEIOU" => hLL Wrld`  

-----------------------------

**.count "x"**

count how many times you can find the letters given in input throught quotes

 example
`counting vowels:`  
`string = "hello world"`   
`string.count "aeiou" => 3`  

--------------------------------

**.strip**

enlève les espaces au début et à la fin 

--------------------------------

**.reverse**

inverse un String.

exemple: 
`str = "hello"`
`str.reverse => "olleh"`

--------------------------------

**.upcase**

Transforme le String en majuscule.

exemple: 
`str = "hello"`
`str.reverse => "HELLO"`

--------------------------------

**.downcase**

Transforme le String en minuscule.

exemple: 
`str = "HELLO"`
`str.reverse => "hello"`

-------------------------------

**.chars**

Transforme la string en array de Characters.

exemple:
`str = "hello"   
str.chars = ["h", "e", "l", "l", "o"]`


