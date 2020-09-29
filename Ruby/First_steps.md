# Ruby Basic language syntax

<br>

**puts** : put a string on the output with a line break

ex: ```puts "Hello world!"```

<br>

**print** : put a string without line break

ex: ```print "Hello"
print "World"```

<br>

**gets.chomp** : get user input (like scanf) - it can be a specified type with:
gets.chomp.to_i (integer) // gets.chomp.to_s (string) // gets.chomp.to_f (float)

ex: ```name = gets.chomp```
ex: ```year = gets.chomp.to_i``` -> gets integer from the user input

<br>

**.chop** : remove last caracter of the string

ex: ```name = gets.chop```
ex: ```name.chop = dian```
<br>

## Loops in Ruby

incremented variable |i|

ex ```5.times do |i|
puts i  
end```

```0
1
2
3
4
