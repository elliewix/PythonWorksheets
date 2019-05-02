## Worksheet on for loops to repeat a task in Python

Information from Elizabeth Wickes' [lecture on for loops](https://github.com/elliewix/IS-452-Spring2019/blob/master/Lectures/Week-02-ExpressionsAndLoops.ipynb)

**Goals for this worksheet**  
This worksheet will provide guided and independent practice on 'for' loops that repeat a task.

**Concept**
Much of the action driven in Python is done so by loops. Loops tell the program to repeat things. Having a computer repeat a calculation or just keep trying something through a series of values is the power of computing. We're going to be focused on looping through a set of known values.

**The 'for' loop for repeating a task - the unpacking loop**
While there is a single syntax rule for for loop, there are many types. This worksheet focuses on
a 'for' loop that will repeat something however many times you need. This is valuable when you've
done something once, and now want to do the same thing many times, for instance printing out each thing
in a list, or renaming a lot of files.

**Core syntax reference**
What does this for loop look like?

``` python
for iterable_variable in sequence:
    do this stuff
```

This will loop over the sequence you provide, unpacking each value into the iterable_variable. This variable will hold an individual value, one at a time, for each loop through.

Some important notes:

- the iterable variable name can be literally any valid variable name and does not need to be declared previously
- the colon at the end of the for line block is required and indicates that the declaration line is done
- the in keyword separates the iterable variable name from the sequence
- this case has the sequence literal in the declaration line, but could also be a variable

**Setting up a 'for' loop**

There are three steps for setting up a for loop. We'll be going through all of these in much more detail as we work through examples. This section is just to set up your thought process.

1. Determine what kind of pattern you'll be executing.
  - This is a thinking stage, where you need to think through what kind of pattern will move your program forward.
2. Identify your sequence.
  - Once you know the kind of pattern you want, this will help you determine the kind of sequence. There are times when the sequence will be very clear to you, and others where you'll be crafting one (for example in a reference loop) to generate the values you need.
3. Give your iterable variable a good name.
  - You can technically call it kitten, but that isn't helpful. Think about what it is and try to name it, being sure that you are matching the plural correctly. For example, if you are working over a sequence of numbers, you might want to call it num, or if it's a string you could call it character.
  - Be very careful not to repeat any of your previous variable names, as their previous values will be erased for the iterable variable's value. You may end up blowing away your data and weird things happen.
  - This name must also be different from the sequence's variable name (if it has one), because it might word and end up with really strange results.

  ### Guided Practice

We have the word, 'alphabet'. We want to print out each letter, one at a time, from this word.

**Practice 1**
``` python
for letter in "alphabet":
  print(letter)
```
That gives us:  
'a'  
'l'  
'p'  
'h'  
'a'  
'b'  
'e'  
't'

**Question:** If we want to print out the word 'alligator', how would we change the above 'for' loop?

**Practice 2**

Now instead of putting the word right into the loop, we can use a variable instead.
First we create the variable we want to use. We can call it anything we want! Here we'll call the variable 'loopword'

``` python
loopword = "alphabet"
```

Now we'll use that variable in the loop.

``` python
for letter in loopword:
  print(letter)
```
Here again we get:  
'a'  
'l'  
'p'  
'h'  
'a'  
'b'  
'e'  
't'

**Question:** If we wanted to instead print out the letters from 'alligator', what would we change above?

**Practice 3**

Now we want to add something to the beginning of each thing that we print. Instead of just printing out the
letter, we want to write "This is the letter:" ahead of it. Then we can do:

``` python
loopword = "alphabet"
for letter in loopword:
  print("This is the letter: ", + letter)
```

- The part in quotes "This is the letter:", gets printed out just like it is.
- The '+' means to add what's after the '+' to what's in front of it. You can put as many of these together as you want. Each thing is also separated by a comma.

This prints:  

'This is the letter: a'  
'This is the letter: l'  
'This is the letter: p'  
'This is the letter: h'  
'This is the letter: a'  
'This is the letter: b'  
'This is the letter: e'  
'This is the letter: t'

**Question:** If we changed the variable *loopword* to 'telephone', what would get printed out?

**Question:** If we wanted to instead at the beginning say "Here is the letter: ", what would we change above?

**Question:** If we wanted to print 'the end' after we print out the letter, what would we change above? What would print out if the *loopword* was 'telephone'?

**Practice 4**

Now let's loop over a set of numbers instead. We can create a list of numbers.

numlist = [1,2,3,4,5]

``` Python
for num in numlist:
  print(num)
```
That gives us:  
1
2
3
4
5

**Question:** If we wanted to print out 1-8 instead, what would we change?

**Question:** If we wanted to add "This is a number:" before we printed the number, how would we change the loop?


  ### Independent Practice

**Practice 4**  

**Question:** Write a for loop that prints out each letter in the word 'awesome'.

**Question:** Write the same loop, but now use a variable in the loop. Use a different name for the variable than what
was used in the Guided Practice questions.

**Practice 5**  

**Question:** Print out the numbers 20 to 30.

**Question:** Before each number, when it's printed out add "My favorite number is ".
