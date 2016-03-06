# Chapter 4: Writing Your Christmas List

I'm really sorry about all of the shouting in the last chapter. However, we learned how we can read and write to files with Ruby, which was pretty cool.

This chapter is all about building something that will make a Christmas list! 

Here's what we want to do:

- I want to start with an empty list.
- I want to put as many items as I want into it.
- When I'm done, I want to type "done". At that point, it should turn my list into a proper Christmas list.

Before we can do this, we need to figure out how to make lists in Ruby.

## Making a List

What's a list? This might sound like a weird question! A shopping list looks like this:

```
Shopping List
-------------

1. Milk
2. Bread
3. Chocolate

```

We have a *title*, and then we have *items*, one on every line. In the shopping list, we have given each of them a *number* as well.

How would we write a shopping list in Ruby? Well it would look like this:

```ruby
shopping_list = [
  "Milk", 
  "Bread", 
  "Chocolate",
]
```

The square brackets `[]` start and end a list. You put the items of the list between the square brackets, making sure you finish every line with a comma `,`.

Oh no! We've forgotten the toilet roll! Don't worry, we can put items on the list like this:

```ruby
shopping_list << "Toilet Roll"
```

If you follow the arrows `<<`, it looks like we're pushing the Toilet Roll into the shopping list! That's why this is called a *push*.

## Checking It Twice

What can we do with a list? Well, we can ask the list questions about the items.

Time to write some code! Go on the Internet and go to:

> https://repl.it/languages/ruby

Let's ask some questions about our shopping list. Put the following code in the white box:

```ruby
shopping_list = [
  "Milk", 
  "Bread", 
  "Chocolate",
]

shopping_list << "Toilet Roll"

# How long is the list?
puts shopping_list.length

# What's the first item in the list?
puts shopping_list.first

# What's the last item in the list?
puts shopping_list.last
```

Press the *Run* button. You should see this:

```
>
4
Milk
Toilet Roll
>
```

Cool! We asked the list 3 questions:

1. How long is the list? It answered: 4 items!
2. What's the first item in the list? It answered: Milk!
3. What's the last item in the list? It answered: Toilet Roll!

Ruby should get a prize for getting all those questions right!

**Challenges**

- What would these instructions do when you press *Run*? Have a guess and then try it!

```ruby
shopping_list = ["Sweets"]

puts shopping_list.length
puts shopping_list.first
puts shopping_list.last
```

- We can ask the question, "Is the list empty?" with the instruction `empty?`. Add it to the code above to ask whether the shopping list is empty. What do you get when you *Run* it?

## Going Through the List

What if we wanted to print out every item on the list? Well, we would need to go to each item in the list and `puts` it. In Ruby, that sentence looks like this (the English is next to it):

```ruby
shopping_list.each do |item| # Give me each item (call it `item`)...
  puts item                  # ...and print it!
end                          #
```

When Ruby sees this, it will run the instructions between `do` and `end` once for every item in the list. If we didn't have `each`, it would look like this:

```ruby
item = "Milk"
puts item

item = "Bread"
puts item

item = "Chocolate"
puts item
```

As you can see, `each` saves us a lot of code!

**Challenge**

Have a look at this code. What do you think will come out when you press *Run*? Have a guess, then see if you're right!

```ruby
numbers = [1, 2, 3]

numbers.each do |number|
  add_one = number + 1
  puts add_one
end
```

If this is hard, try writing it out without `each`, like we did earlier.

## Dear Santa...

If you've got this far, well done! You have everything you need to put together your Christmas list.

At the start of this chapter, I wrote down what we want our Christmas list maker to do:

- I want to start with an empty list.
- I want to put as many items as I want into it.
- When I'm done, I want to type "done". At that point, it should turn my list into a proper Christmas list.

That's a lot of things! Let's see what it looks like:

```ruby
christmas_list = [] # The Christmas List starts empty.
name = "Jonny"      # Put your name here!

                                    # This looks a lot like Guess The Number from Chapter 2!
                                    #
loop do                             # We want to keep asking for items until we're done.
  puts "Add an item, or type done." #
  item = gets.chomp                 # Ask for something from the Christmas list!
                                    #
  if item == 'done'                 # If we said 'done'...
    break                           # ...stop asking for items!
  else                              # ...otherwise...
    christmas_list << item          # ...put the item on the Christmas list. 
  end                               #
end                                 #

# Let's start our letter:
puts
puts "Dear Santa,"
puts
puts "I've been really good this year!"
puts "Could I have these #{christmas_list.length} things please?"

# Now we want to print out all of items:
christmas_list.each do |item|
  puts "- #{item}"
end

# Let's finish our letter!
puts
puts "Thank you!"
puts name
```

- If you've forgotten about `puts`, `gets.chomp` or `#{item}`, go back to Chapter 1.
- If you've forgotten about `loop`, `if` or `break`, go back to Chapter 2.
- We've seen `[]`, `<<` and `each` in this chapter. Go back and read this chapter again if you've forgotten what they do.

If you can type all of that out, press *Run* and see what happens. Here is what happened when I did it:

```
>
Add an item, or type done.
 A pony
Add an item, or type done.
 A race car
Add an item, or type done.
 done

Dear Santa,

I've been really good this year!
Could I have these 2 things please?
- A pony
- A race car

Thank you!
Jonny
=> nil
>
```

If you got that, well done: you're vey good at typing!

**Challenge**

Let's *really* understand what happens in our code. We're going to pretend to be the computer!

Get a big piece of paper and draw out this table:

```
Line Number | christmas_list | name | item | Next Line Number
------------+----------------+------+------+------------------
            |                |      |      |
```

Start at line 6 of the code. For each line, write down the line number and what the value of `christmas_list`, `name` and `item` are. When you get to line 8, you ask a question:

- The first time you get to line 8, pretend the answer was "A pony".
- The second time you get to line 8, pretend the answer was "done".

Stop when you get to line 15.

At the end of this challenge, you should have about 14 rows in your table. That's a lot of work! Luckily, the computer does this for you *really* quickly so you don't have to!
