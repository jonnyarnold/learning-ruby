# Chapter 2: Guess the Number

Last chapter we wrote a story about you, your friends, or anyone that you liked! We learned how to talk to computers with a language called Ruby. We learned how to make the computer say something with `puts` and how to ask for something with `gets.chomp`.

In this chapter we will make a guessing game. In the game, the computer will think of a number between 1 and 10, and you will have to guess what it is.

## Making Decisions

Computers are clever enough to make decisions! We can ask it to check something and decide whether it is true or false.

This will be very important in our game. Every time we guess, we need to check if the computer's secret number is the same as the guessed number. If the guess is right, we need to say well done!

If I was writing out a question in English I would write:

*If the guessed number is the same as the secret number say, "Well done!". If it isn't say, "Sorry, wrong!".*

In Ruby, we would write:

```ruby
if guessed_number == secret_number
  puts "Well done!"
else
  puts "Sorry, wrong!"
end
```

There are a lot of differences! Let's look at each *translation*:

- *if* stays the same!
- *the guessed number* turns into `guessed_number`. (The underline between the words is called an *underscore*.)
- *is the same as* turns into `==`, two equals signs.
- *the secret number* turns into `secret_number`.
- *say* turns into `puts`, which is an instruction we learned in Chapter 1.
- *if it isn't* turns into `else`.
- *say* turns into `puts` again.
- At the end of the instruction we have had to put `end`. This is to tell the computer that we have reached the end of the things to do for our decision.

Wow, that's a lot of changes! Don't worry if it's confusing, you just need some more practice!

**Challenges**
- What do you think would happen if we ran this code when:
  - `guessed_number` is 3 and `secret_number` is 6?
  - `guessed_number` is 3 and `secret_number` is 3?
- The way to say *not the same as* in Ruby is `!=`. Can you write the sentence *If the guessed number is not the same as the secret number* in Ruby?

## Guessing the (Not Very) Secret Number

Let's start writing some code! Go on the Internet and go to:

> https://repl.it/languages/ruby

Type out this code. Remember that all the symbols are important!

```ruby
secret_number = "3"

puts "Guess the number!"
guessed_number = gets.chomp

if guessed_number == secret_number
  puts "Well done!"
else
  puts "Sorry, wrong!"
end
```

When you have typed it in, press the *Play* button.

1. It should ask you to guess the secret number.
2. Enter a number in the blue box and press `Enter`.
3. If you get the secret number, you should see *Well done!*. If you didn't, you will see *Sorry, wrong!*.
4. Press the *Play* button to play again!

After you have played the game a few times, try to work out what each line in the code does. The answers are below:

- In Chapter 1, you saw `name = gets.chomp`. This instruction told the computer to remember what you typed and give it the label `name`. We use this twice here: `secret_number = "3"` and `guessed_number = gets.chomp` are remembering instructions. We give the labels `secret_number` and `guessed_number` a special name: *variables*.
- There are three `puts` instructions! Look back to Chapter 1 if you have forgotten what they do.
- The end of this code is the same code we saw earlier in this chapter. It is the same as the sentence: *If the guessed number is the same as the secret number say, "Well done!". If it isn't, say "Sorry, wrong!"*

Now after a few games you should be able to figure out what the secret number is. Give it to your friends, but change the secret number and hide it so they don't figure it out! See how many tries it takes before they get it.

## Too Many Bums!

Pressing the *Play* button every time we want to guess again is boring. I want to let the player keep guessing until they get it right.

We can tell the computer to *loop* forever in Ruby using `loop do`. Try this program:

```ruby
loop do
  puts "BUM"
end
```

Press the *Play* button.

**Oh no!** Your blue box will now be full of `BUMBUMBUMBUM`, and you won't be able to stop it! Whatever is between `loop do` and `end` will be done forever!

You will have to refresh the page to stop the `BUM`s. Sorry!

Luckily, Ruby has an instruction to stop doing things forever: `break`. When the computer reads `break`, it will stop the loop and carry on after the `end`.

If you trust me any more, type this program in and press *Play*:

```ruby
loop do
  puts "BUM"
  break
end
```

If you trusted me you will see only one `BUM` when you press *Play*. One bum is enough, I think.

## Guess Again!

Now that we know how to loop, let's put it into our program. I'm going to write it out in English and in Ruby.

```ruby
secret_number = "3"                  ## Set the secret number to 3
                                     ## 
puts "Guess the number!"             ## Say, "Guess the number!"
                                     ## 
loop do                              ## Do everything between here and the last "end" forever:
  guessed_number = gets.chomp        ##   Ask for a number and call it the guessed number
                                     ## 
  if guessed_number == secret_number ##   If the guessed number is the same as the secret number:
    puts "Well done!"                ##     Say "Well done!"
    break                            ##     Stop looping
  else                               ##   If it isn't:
    puts "Guess again!"              ##     Say "Guess again!"
  end                                ##   This is the end of the decision
end                                  ## This is the end of the loop
```

I won't make you write this code out: [click here](https://repl.it/BWNM/2) to get it in your white box. 

Press *Play* to play the game. You should try some wrong answers before you try the right answer. You should see that the computer will ask you to guess again if you give a wrong answer.

**Challenges**
- Change the first line of your code to: `secret_number = rand(10).to_s`. Can you guess the secret number now? Does it stay the same every time?
