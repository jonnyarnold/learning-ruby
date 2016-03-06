# Chapter 3: Let's Get LOUD!

Last chapter we made a number guessing game. We learned how to tell the computer to make decisions using `if` and `else`. We also learned about `loop`, which runs a set of instructions forever.

In this chapter we will build a tool that will take a file and CHANGE ALL THE LETTERS TO CAPITALS, SO IT LOOKS LIKE YOU'RE SHOUTING!

## Computer Files

Computers keep stuff in files. You can think of a file like a piece of paper: you can *write* something into a file, and the computer will remember it. Whenever you want to know what's on in the file, you can *read* it.

If you're using a computer and you want to find out what's in a file, you will usually click on it and the file will open. Ruby doesn't know how to click on files, so we have to teach it how to read and write.

## Teaching Ruby to Read and Write

Go on the Internet and go to:

> https://repl.it/languages/ruby

Using Ruby instructions, we can get Ruby to *write* a file. Type the following into the **blue** box:

```ruby
File.write "introduction", "Hello!"
```

When you have typed it in, press *Enter* on the keyboard.

You might be disappointed, because it doesn't do anything! It looks something like this:

```
> File.write "introduction", "Hello!"
=> 6
>
```

Did it work? We don't know yet. To find out, we need to *read* the file we have just written. Type this onto the next line of your **blue** box:

```ruby
File.read "introduction"
```

This should be more interesting:

```
> File.write "introduction", "Hello!"
=> 6
> File.read "introduction"
=> "Hello!"
```

Great, it worked! So what did we do?

`File.write` tells Ruby to write a new file. Straight after, we have to tell Ruby two things:

1. What's the name of the file? In the code above, we said the file was called `"introduction"`.
2. What's in the file? We put `Hello!` into the file.

Don't forget the comma `,` between the words! If you get everything right, your file will be written.

What happens when we want to read it? We just write `File.read`, followed by the name of the file. If you get that right, you'll get whatever you put in the file!

**Challenges**

- What happens when you try and read a file that you haven't written yet? Try it with `File.read "abc"`.
- Write a file called `sheep` that contains the words `baa baa baa`, and read it again. Have you got your quotes `"` in the right places?

## In. LOUD. Out.

We're nearly ready to make our SHOUTING FILE! There's one last thing we need to learn. Type this into your **blue** box:

```ruby
"hello".upcase
```

What do you get back? Hopefully this:

```
> "hello".upcase
=> "HELLO"
```

Wow! `upcase` tells Ruby to make all of the letters of your word capital letters. 

Let's add together everything we've learned so far:

```ruby
File.write "words", "make this loud!"
words = File.read "words"
uppercase_words = words.upcase
puts uppercase_words
```

What do you think will happen? Read each line carefully, and write down or say what each line does. We're using things from previous projects, so don't be afraid to go back and look at them if you get stuck.
 
To help, I've written down step-by-step what is happening here:

```ruby
File.write "words", "make this loud!" # Put "make this loud" into a file called "words"
words = File.read "words"             # Read the file "words" and put its contents into a variable called words.
uppercase_words = words.upcase        # Change all the letters to capitals and save it as the variable uppercase_words.
puts uppercase_words                  # Print out uppercase_words.
```

If you've typed everything correctly, you should see this when you press the *Run* button:

```
>
MAKE THIS LOUD!
=> nil
>
```

If you did, well done! You are now a file reading master!

**Challenges**

- If you use `downcase` instead of `upcase`, you will change all letters to lowercase. See if you can make `"MAKE THIS QUIET!"` quieter!
- Can you write the program above *without* using `File.read` or `File.write`? *(Hint: Can you set `words` to the words you want to capitalise without using a file?)*
