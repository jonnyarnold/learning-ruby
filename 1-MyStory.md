# Chapter 1: My Story

In this chapter we will write a story about you and your friends.

Even better, you will be able to change the names in the story. You can make the story about you, then make it about your friend, then make it about your family!

## Telling Computers What To Do

Before we can write our story, we need to learn how to tell a computer what to do.

If I wanted you to do 5 star jumps, I could write an *instruction* like "Do 5 star jumps" on a piece of paper and give it to you. When you read the paper, you'd start jumping up and down!

Talking to a computer is the same. We tell it what to do by writing instructions, then tell the computer to read these instructions and do what we say.

Computers don't read English like you and me. Instructions for computers use special words and you have to write sentences in a special way. This special way is called a *programming language*. There are lots of programming languages out there. We will be learning a programming language called Ruby.

## Making a Computer Say *BUM*

Let's start telling the computer what to do! Go on the Internet and go to:

> https://repl.it/languages/ruby

You should see something like this:

[!! Image of repl.it !!]

We will write our instructions in the white box, and the computer will talk to us in the blue box.

Type this into the white box:

```ruby
puts "BUM"
```

Make sure you type everything above. You can get a `"` by holding down `Shift` and pressing `2`.

Once you have done this, click the *Run* button (the triangle). If you typed the instruction right, you should see in the blue box:

```
>
BUM
=> nil
>
```

Well done! You made the computer shout *BUM* at you! Every time you press *Run*, the computer will say *BUM*. Try pressing *Run* a few more times to see!

When the computer sees `puts "BUM"`, it says whatever is between the `"` marks.

Why is it called `puts`? Because it **puts** the words that you say in the blue box.

**Challenges**
- Can you make the computer say *Good Morning* instead of *BUM*?
- Can you make the computer say your name?

## Remember My Name!

Let's make the computer remember your name and say it back to you. Type this into the white box:

```ruby
puts "What is your name?"
name = gets.chomp
puts "Hello #{name}!"
```

There are a few tricky things here:
- Can you find the `?` on your keyboard? Usually it's on the same key as `/`. You will need to hold `Shift` and press this key to get a `?`.
- The `#` is usually near the big `Enter` key.
- You will need to hold `Shift` to get `{` and `}` too. These keys are also near the big `Enter` key.

When you have typed it in, press the *Run* button.
1. It should ask you for your name!
2. Type your name in the blue box and press `Enter`.
3. The computer should say hello to you!

After you have finished, you should have something like this in the blue box:

```
>
What is your name?
 Jonny
Hello Jonny!
>
```

Try it again with a different name. See how it changes!

Let's look at each instruction:
- `puts "What is your name?"` makes the computer say *What is your name?*
- `name = gets.chomp` makes the computer wait until you have typed your name into the blue box and pressed `Enter`. It remembers what you typed as `name`.
- `puts "Hello #{name}!"` makes the computer say *Hello*, followed by the name you typed in.

**Challenges**
- Can you make the computer ask how old you are?
- Can you make the computer say "Hello Jonny, Age 9" if I say my name is Jonny and my age is 9?

## Your Story

It's time to write your story! Use a piece of paper or use a computer to write a story.

I've written a little story here. Your story will be better than this!

```
One day, Jonny and Sarah went to space! They saw stars and flew past the moon. Jonny played tennis with an alien and Sarah drove the spaceship back to Earth.
```

We want to be able to tell the computer the names of the people in the story when we press *Run*, so we need to replace the names in the story with *person1* and *person2*:

```
One day, person1 and person2 went to space! They saw stars and flew past the moon. person1 played tennis with an alien and person2 drove the spaceship back to Earth.
```

What does the computer need to do?
1. Ask for the names of the people in the story.
2. Write out the story with the names in it.

Let's go! There are a lot of things here, so make sure you type carefully!

```ruby
puts "What is the name of person 1?"
person1 = gets.chomp
puts "What is the name of person 2?"
person2 = gets.chomp
puts "One day, #{person1} and #{person2} went to space! They saw stars and flew past the moon. #{person1} played tennis with an alien and #{person2} drove the spaceship back to Earth."
```

Press *Run* and you should be able to see your story!

## Oops!

You might have made a mistake when typing out the code. If you did, you might get an error message like:

```
(repl):1: unterminated string meets end of file
```

Don't worry about this. The computer is very stupid and very picky, so you have to type *everything* right before it will work. That includes the quote marks, full stops and brackets!
