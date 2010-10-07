.. Objectives
.. ----------

.. A - Students and teachers from Science and engineering backgrounds
   B - Will learn what are tuples and why they are needed
       Will learn the various methods of accessing elements in tuples
   C - 
   D - 

.. Prerequisites
.. -------------

..   1. Getting started with lists
     
.. Author              : Nishanth Amuluru
   Internal Reviewer   : 
   External Reviewer   :
   Checklist OK?       : <put date stamp here, if OK> [2010-10-05]

Script
------

Hello friends and welcome to the tutorial on Sets

{{{ Show the slide containing title }}}

{{{ Show the slide containing the outline slide }}}

In this tutorial, we shall learn

 * sets
 * operations on sets

Sets are data structures which contain unique elements. In other words,
duplicates are not allowed in sets.

Lets look at how to input sets.
type
::
 
    a_list = [1, 2, 1, 4, 5, 6, 7]
    a = set(a_list)
    a
     
We can see that duplicates are removed and the set contains only unique
elements. 
::

    f10 = set([1, 2, 3, 5, 8])
    p10 = set([2, 3, 5, 7])

f10 is the set of fibonacci numbers from 1 to 10.
p10 is the set of prime numbers from 1 to 10.

Various operations that we do on sets are possible here also.
The | character stands for union
::

    f10 | p10

gives us the union of f10 and p10

The & character stands for intersection.
::

    f10 & p10

gives the intersection

similarly,
::

    f10 - p10

gives all the elements that are in f10 but not in p10

::

    f10 ^ p10

is all the elements in f10 union p10 but not in f10 intersection p10. In
mathematical terms, it gives the symmectric difference.

Sets also support checking of subsets.
::

    b = set([1, 2])
    b < f10

gives a True since b is a proper subset of f10.
Similarly,
::

    f10 < f10

gives a False since f10 is not a proper subset.
hence the right way to do would be
::

    f10 <= f10

and we get a True since every set is a subset of itself.

Sets can be iterated upon just like lists and tuples. 
::

    for i in f10:
        print i,

prints the elements of f10.

The length and containership check on sets is similar as in lists and tuples.
::

    len(f10)

shows 5. And
::
    
    1 in f10
    2 in f10

prints True and False respectively

The order in which elements are organised in a set is not to be relied upon 
since sets do not support indexing. Hence, slicing and striding are not valid
on sets.

{{{ Pause here and try out the following exercises }}}

%% 1 %% Given a list of marks, marks = [20, 23, 22, 23, 20, 21, 23] 
        list all the duplicates

{{{ continue from paused state }}}

Duplicates marks are the marks left out when we remove each element of the 
list exactly one time.

::

    marks = [20, 23, 22, 23, 20, 21, 23] 
    marks_set = set(marks)
    for mark in marks_set:
        marks.remove(mark)

    # we are now left with only duplicates in the list marks
    duplicates = set(marks)

{{{ Show summary slide }}}

This brings us to the end of the tutorial.
we have learnt

 * How to make sets from lists
 * How to input sets
 * How to perform union, intersection and symmectric difference operations
 * How to check if a set is a subset of other
 * The various similarities with lists like length and containership

{{{ Show the "sponsored by FOSSEE" slide }}}

#[Nishanth]: Will add this line after all of us fix on one.
This tutorial was created as a part of FOSSEE project, NME ICT, MHRD India

Hope you have enjoyed and found it useful.
Thankyou
