---
title: Hashes
length: 90
tags: ruby, hashes, data structures
---

## Learning Goals

* Understand that there are multiple types of collections
* Develop a mental model to understand hashes
* Gain some familiarity with common hash methods

## Structure

* 5 - WarmUp
* 25 - Together - Building a Hash
* 5 - Break
* 15 - Group Exercise
* 5 - WrapUp

## WarmUp
Make a T-Chart of the collections you are familiar with. Fill in what you know about each collection type you listed.

## Hashes

### Supplies

For this section, we'll walk through performing some common Hash operations both in code using IRB and in a physical model using some basic supplies.

You'll need these supplies:

1. 1 Black Velvet Bag
2. Piece of paper
3. 6 Beads
4. 6 Bead Labels  
   You'll need the following labels: blue, green, purple, red, orange, warm  

### Intro - Hash Properties

Hashes are the second most important data structure in Ruby. Like an Array, a Hash is a data structure used for representing a _collection_ of things. But whereas an Array generally represents a **list** of things (ordered, identified by numeric position), we use a Hash to represent a collection of *named* values. In a Hash, we can insert data by assigning it to a name and later retrieving it using the same name.

Some languages call their Hashes *dictionaries, map, associative array* for this reason -- you look up a word (the label) to retrieve its definition (the data or value with which the label was associated).

Key ideas:

* Ordered vs. Unordered
* Pairs
* Determinism and uniqueness
* Choosing a hash vs an array
* Performance characteristics

### Working a Hash

Now let's model some of the common hash operations in the physical space alongside an IRB session. As we go, we'll look at these common methods:

* `[]`     element reference
* `[]=`    element assignment
* `keys`   can be any object type
* `values` can be any object type 

Follow along with the instructor as you walk through the following operations:

1. Create a new hash `data = {}` or 'data = Hash.new`
   * Write data on your paper, this is your variable assigned to the hash we are making. Put your bag on your paper, this is your hash.  
2. Assign the key `blue`: `data["blue"] = Bead.new`
   * Using your blue tag, attach it to a bead. Put the bead into the bag leaving the blue tag/key hanging out.   
3. Read the value: `data["blue"]`
   * Pull the 'blue' tag. Blue is your key, bead is your value.
4. Store a second pair: `data["green"] = Bead.new`
   * Using your "green" tag, attach it to a bead. Put the bead into your hash/bag, leaving they key/tag hanging out.
5. Reuse a key: `data["blue"] = Bead.new`
   * Change what kind of blue bead you want. Take the blue tag off and re-attach it to a new bead.   
   * Note in IRB that the object ID is different for the first blue bead and the second blue bead.   
6. Create a key for nothing: `data["purple"] = nil`
   * Hang a purple tag/key from your bag/hash, with no bead attached. 
7. Retrieving a list of `keys` from the hash: I can see what is in my bag/hash by calling data, it returns the whole hash.
   * Grab all the tags, pull them all out
8. What if I want to do something with my keys, maybe I just want to see what keys are there. Use data.keys, note it returns an array of your keys. 
   *  Spread out your key/tags and look at what keys you have. 
8. Retrieving a list of `values` from the hash.  data.values
   * Returns just the values, as an array - looking in the bag? 
9. Get a little weird: We said you can have any object type as a value, perhaps an array - `data["red"] = [Bead.new, Bead.new]` perhaps a collection of all my red beads. 
10. Get more weird: You can also have a hash as a value (nested hashes) `data["warm"] = {"orange" => Bead.new, "red" => Bead.new}`  
    * This would be if you have a tag/key that is attached to your neighbor's hash/bag which had a orange and red bead in it.
11. Consider the key `"red"` and how it does and doesn't exist twice. What is different about the ways I need to access each of these reds?
12. Mess up your brain: `data["spinning top"] = data`

## Group Exercise

For this exercise you'll work in threes.

* Person `A` is in charge of reading the instructions
* Person `B` is in charge of the physical model - you'll need 3 more tags
* Person `C` is in charge of working in IRB (in such a way that the others can see!)

Start with an empty `data` hash in both the physical space and IRB.

For the IRB person, recall that you can create a simple `Bead` model like this:

```ruby
class Bead
end
```

### Steps

1. Insert a "blue" bead `data["blue"] = Bead.new`
2. Find the value attached to the key `"blue"`
3. Find the value attached to the key `"green"`
4. Add a new bead referenced by the key `"green"`
5. Add a new bead referenced by the key `"purple"`
6. What are the `keys`? What kind of object does that method return?
7. What are the `values`? What kind of object does that method return?
8. What's interesting about the order of the return value of both `keys` and `values`?
9. Add a new bead referenced by the key `"green"`
10. How has `keys` changed after the last step? How has `values` changed? What was lost?
11. As a group update your data collection T-Chart to include new Hash info.


## WrapUp  
Create a Venn Diagram of Arrays and Hashes
