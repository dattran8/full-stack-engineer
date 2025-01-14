# Welcome to Python Data Structures and Loops

Let’s look ahead to see what’s coming up in the Python Data Structures
and Loops section of the skill path.

Welcome to the section of the skill path focused on Python Data
Structures and Loops. In this section, you will learn how to organize
and iterate through data in Python.

Additionally, you will dive into the foundations of object-oriented
programming, a foundational component of computer science that will help
you in creating your own web applications.

Let’s get started!

# Introduction to Lists

## What is a List?

In programming, it is common to want to work with collections of data.
In Python, a *list* is one of the many built-in
<a href="https://en.wikipedia.org/wiki/Data_structure"
class="e14vpv2g1 gamut-xro1w8-ResetElement-Anchor-AnchorBase e1bhhzie0"
target="_blank" rel="noopener">data structures</a> that allows us to
work with a collection of data in sequential order.

Suppose we want to make a list of the heights of students in a class:

-   Noelle is 61 inches tall
-   Ava is 70 inches tall
-   Sam is 67 inches tall
-   Mia is 64 inches tall

In Python, we can create a variable called `heights` to store these
integers into a <a
href="https://www.codecademy.com/resources/docs/python/lists?page_req=catalog"
class="e14vpv2g1 gamut-xro1w8-ResetElement-Anchor-AnchorBase e1bhhzie0"
target="_blank"><em>list</em></a>:

``` python
heights = [61, 70, 67, 64]
```

Notice that:

1.  A list begins and ends with square brackets (`[` and `]`).
2.  Each item (i.e., `67` or `70`) is separated by a comma (`,`)
3.  It’s considered good practice to insert a space () after each comma,
    but your code will run just fine if you forget the space.

Let’s write our own list!



**1.**

Examine the existing list `heights` in your code editor.

A new student just joined the class!

-   Chloe is 65 inches tall

Add Chloe’s height to the end of the list `heights`.

**2.**

Remove the `#` in front of the definition of the list `broken_heights`.
If you run this code, you’ll get an error in your terminal:

``` python
SyntaxError: invalid syntax
```

Add commas (`,`) to `broken_heights` so that it runs without errors.



``` python
heights = [61, 70, 67, 64, 65]

broken_heights = [65, 71, 59, 62]
```

## What can a List contain?

Lists can contain more than just numbers.

Let’s revisit our classroom example with heights:

-   Noelle is 61 inches tall
-   Ava is 70 inches tall
-   Sam is 67 inches tall
-   Mia is 64 inches tall

Instead of storing each student’s height, we can make a list that
contains their names:

``` python
names = ["Noelle", "Ava", "Sam", "Mia"]
```

We can even combine multiple <a
href="https://www.codecademy.com/resources/docs/python/data-types?page_ref=catalog"
class="e14vpv2g1 gamut-xro1w8-ResetElement-Anchor-AnchorBase e1bhhzie0"
target="_blank">data types</a> in one list. For example, this list
contains both a <a
href="https://www.codecademy.com/resources/docs/python/strings?page_req=catalog"
class="e14vpv2g1 gamut-xro1w8-ResetElement-Anchor-AnchorBase e1bhhzie0"
target="_blank">string</a> and an integer:

``` python
mixed_list_string_number = ["Noelle", 61]
```

Lists can contain any data type in Python! For example, this list
contains a string, integer, boolean, and float.

``` python
mixed_list_common = ["Mia", 27, False, 0.5]
```

Let’s experiment with different data types in our own lists!



**1.**

Add any additional string to the end of the list `ints_and_strings`.

**2.**

Create a new list called `sam_height_and_testscore` that contains:

1.  The string `"Sam"` (to represent Sam’s name)
2.  The number `67` (to represent Sam’s height)
3.  The float `85.5` (to represent Sam’s score)
4.  The boolean `True` (to represent Sam passing the test)

Make sure to write the elements in exact order.



``` python
ints_and_strings = [1, 2, 3, "four", "five", "Six"]

sam_height_and_testscore = ["Sam", 67, 85.5, True]
```

## Empty Lists

A list doesn’t have to contain anything. You can create an empty list
like this:

``` python
empty_list = []
```

Why would we create an empty list?

Usually, it’s because we’re planning on filling it up later based on
some other input. We’ll talk about two ways of filling up a list in the
next exercise.

Let’s practice writing an empty list!



**1.**

Create an empty list and call it `my_empty_list`. Don’t put anything in
the list just yet.



``` python
my_empty_list = []
```

## List Methods

As we start exploring lists further in the next exercises, we will
encounter the concept of a *method*.

In Python, for any specific data-type ( strings, booleans, lists, etc. )
there is built-in functionality that we can use to create, manipulate,
and even delete our data. We call this built-in functionality a method.

For lists, methods will follow the form of `list_name.method()`. Some
methods will require an input value that will go between the parenthesis
of the method `( )`.

An example of a popular list method is <a
href="https://www.codecademy.com/resources/docs/python/lists/append?page_req=catalog"
class="e14vpv2g1 gamut-xro1w8-ResetElement-Anchor-AnchorBase e1bhhzie0"
target="_blank"><code
class="code__2rdF32qjRVp7mMVBHuPwDS">.append()</code></a>, which allows
us to add an element to the end of a list.

``` python
append_example = [ 'This', 'is', 'an', 'example']
append_example.append('list')
 
print(append_example)
```

Will output:

``` python
['This', 'is', 'an', 'example', 'list']
```



We will be exploring `.append()` and many other methods in the upcoming
exercises but for now take a second to examine and play around with the
code for two common list methods.



``` python
example_list = [1, 2, 3, 4]

#Using Append
example_list.append(5)
# print(example_list)

#Using Remove
example_list.remove(5)
# print(example_list)
```

## Growing a List: Append

We can add a single element to a list using the `.append()` Python
method.

Suppose we have an empty list called `garden`:

``` python
garden = []
```

We can add the element `"Tomatoes"` by using the `.append()` method:

``` python
garden.append("Tomatoes")
 
print(garden)
```

Will output:

``` python
['Tomatoes']
```

We see that `garden` now contains `"Tomatoes"`!

When we use `.append()` on a list that already has elements, our new
element is added to the **end** of the list:

``` python
# Create a list
garden = ["Tomatoes", "Grapes", "Cauliflower"]
 
# Append a new element
garden.append("Green Beans")
print(garden)
```

Will output:

``` python
['Tomatoes', 'Grapes', 'Cauliflower', 'Green Beans']
```

Let’s use the `.append()` method to manipulate a list.



**1.**

Jiho works for a gardening store called Petal Power. Jiho keeps a record
of orders in a list called `orders`.

Use `print` to inspect the orders he has received today.

**2.**

Jiho just received a new order for `"tulips"`. Use `append` to add this
string to `orders`.

**3.**

Another order has come in! Use `append` to add `"roses"` to `orders`.

**4.**

Use `print` to inspect the `orders` Jiho has received today.



``` python
orders = ["daisies", "periwinkle"]
print(orders)

orders.append("tulips")
orders.append("roses")

print(orders)
```

    ## ['daisies', 'periwinkle']

    ## ['daisies', 'periwinkle', 'tulips', 'roses']

## Growing a List: Plus (+)

When we want to add multiple items to a list, we can use `+` to combine
two lists (this is also known as concatenation).

Below, we have a list of items sold at a bakery called `items_sold`:

``` python
items_sold = ["cake", "cookie", "bread"]
```

Suppose the bakery wants to start selling `"biscuit"` and `"tart"`:

``` python
items_sold_new = items_sold + ["biscuit", "tart"]
print(items_sold_new)
```

Would output:

``` python
['cake', 'cookie', 'bread', 'biscuit', 'tart']
```

In this example, we created a new variable, `items_sold_new`, which
contained both the original items sold, and the new items. We can
inspect the original `items_sold` and see that it did not change:

``` python
print(items_sold)
```

Would output:

``` python
['cake', 'cookie', 'bread']
```

We can only use `+` with other lists. If we type in this code:

``` python
my_list = [1, 2, 3]
my_list + 4
```

we will get the following error:

``` python
TypeError: can only concatenate list (not "int") to list
```

If we want to add a single element using `+`, we have to put it into a
list with brackets (`[]`):

``` python
my_list + [4]
```

Let’s use `+` to practice combining two lists!



**1.**

Jiho is updating a list of `orders`. He just received orders for
`"lilac"` and `"iris"`.

Create a list called `new_orders` that contains our new orders.

**2.**

Use `+` to create a new list called `orders_combined` that combines
`orders` with `new_orders`.

**3.**

Remove the `#` and whitespace in front of the list `broken_prices`. If
you run this code, you’ll get an error:

``` python
TypeError: can only concatenate list (not "int") to list
```

Fix the command by inserting brackets (`[` and `]`) so that it will run
without errors.



``` python
orders = ["daisy", "buttercup", "snapdragon", "gardenia", "lily"]

# Create new orders here:
new_orders = ["lilac", "iris"]

orders_combined = orders + new_orders

broken_prices = [5, 3, 4, 5, 4] + [4]
```

## Accessing List Elements

We are interviewing candidates for a job. We will call each candidate in
order, represented by a Python list:

``` python
calls = ["Juan", "Zofia", "Amare", "Ezio", "Ananya"]
```

First, we’ll call `"Juan"`, then `"Zofia"`, etc.

In Python, we call the location of an element in a list its *index*.

Python lists are *zero-indexed*. This means that the first element in a
list has index `0`, rather than `1`.

Here are the index numbers for the list `calls`:

| Element    | Index |
|------------|-------|
| `"Juan"`   | `0`   |
| `"Zofia"`  | `1`   |
| `"Amare"`  | `2`   |
| `"Ezio"`   | `3`   |
| `"Ananya"` | `4`   |

In this example, the element with *index* `2` is `"Amare"`.

We can select a single element from a list by using square brackets
(`[]`) and the index of the list item. If we wanted to select the third
element from the list, we’d use `calls[2]`:

``` python
print(calls[2])
```

Will output:

``` python
Amare
```

**Note:** When accessing elements of a list, you *must* use an `int` as
the index. If you use a `float`, you will get an error. This can be
especially tricky when using division. For example `print(calls[4/2])`
will result in an error, because `4/2` gets evaluated to the `float`
`2.0`.

To solve this problem, you can force the result of your division to be
an `int` by using the `int()` function. `int()` takes a number and cuts
off the decimal point. For example, `int(5.9)` and `int(5.0)` will both
become `5`. Therefore, `calls[int(4/2)]` will result in the same value
as `calls[2]`, whereas `calls[4/2]` will result in an error.



**1.**

Use square brackets (`[` and `]`) to select the 4th employee from the
list `employees`. Save it to the variable `employee_four`.

**2.**

Paste the following code into **script.py**:

``` python
print(employees[8])
```

What happens? Why?

**3.**

Selecting an element that does not exist produces an `IndexError`.

In the line of code that you pasted, change `8` to an index that exists
so that you don’t get an `IndexError`.

Run your code again!



``` python
employees = ["Michael", "Dwight", "Jim", "Pam", "Ryan", "Andy", "Robert"]

employee_four = employees[3]
print(employees[4])
```

    ## Ryan

## Accessing List Elements: Negative Index

What if we want to select the last element of a list?

We can use the index `-1` to select the last item of a list, even when
we don’t know how many elements are in a list.

Consider the following list with 6 elements:

``` python
pancake_recipe = ["eggs", "flour", "butter", "milk", "sugar", "love"]
```

If we select the `-1` index, we get the final element, `"love"`.

``` python
print(pancake_recipe[-1])
```

Would output:

``` python
love
```

This is equivalent to selecting the element with index `5`:

``` python
print(pancake_recipe[5])
```

Would output:

``` python
love
```

Here are the negative index numbers for our list:

| Element    | Index |
|------------|-------|
| `"eggs"`   | `-6`  |
| `"flour"`  | `-5`  |
| `"butter"` | `-4`  |
| `"milk"`   | `-3`  |
| `"sugar"`  | `-2`  |
| `"love"`   | `-1`  |



**1.**

Create a variable called `last_element`.

Assign the last element in `shopping_list` to the variable
`last_element` using a negative index.

**2.**

Now select the element with index `5` and save it to the variable
`index5_element`.

**3.**

Use `print` to display both `index5_element` and `last_element`.

Note that they are equal to `"cereal"`!



``` python
shopping_list = ["eggs", "butter", "milk", "cucumbers", "juice", "cereal"]

last_element = shopping_list[-1]

index5_element = shopping_list[5]

print(last_element)
print(index5_element)
```

    ## cereal

    ## cereal

## Modifying List Elements

Let’s return to our garden.

``` python
garden = ["Tomatoes", "Green Beans", "Cauliflower", "Grapes"]
```

Unfortunately, we forgot to water our cauliflower and we don’t think it
is going to recover.

Thankfully our friend Jiho from Petal Power came to the rescue. Jiho
gifted us some strawberry seeds. We will replace the cauliflower with
our new seeds.

We will need to modify the list to accommodate the change to our
`garden` list. To change a value in a list, reassign the value using the
specific index.

``` python
garden[2] = "Strawberries"
 
print(garden)
```

Will output:

``` python
["Tomatoes", "Green Beans", "Strawberries", "Grapes"]
```

Negative indices will work as well.

``` python
garden[-1] = "Raspberries"
 
print(garden)
```

Will output:

``` python
["Tomatoes", "Green Beans", "Strawberries", "Raspberries"]
```



**1.**

We have decided to start selling some of our garden produce. Word around
our town has spread and people are interested in getting some of our
delicious vegetables and fruit.

We decided to create a waitlist to make sure we can sell to all of our
new customers!

Define a list called `garden_waitlist` and set the value to contain our
customers (in order): `"Jiho"`, `"Adam"`, `"Sonny"`, and `"Alisha"`.

**2.**

`"Adam"` decided his fridge is too full at the moment and asked us to
remove him from the waitlist and make space for one of our other
townsfolk.

Replace `"Adam"` with our other interested customer `"Calla"` using the
index method we used in the narrative.

Print `garden_waitlist` to see the change!

**3.**

`Alisha` realized she was already stocked with all the items we are
selling. She asked us to replace her with her friend `Alex` who just ran
out.

Replace `Alisha` with `Alex` ***using a negative index***.

Print `garden_waitlist` again to see the change!



``` python
# Your code below:
garden_waitlist = ["Jiho", "Adam", "Sonny", "Alisha"]

garden_waitlist[1] = "Calla"

print(garden_waitlist)

garden_waitlist[-1] = "Alex"

print(garden_waitlist)
```

    ## ['Jiho', 'Calla', 'Sonny', 'Alisha']

    ## ['Jiho', 'Calla', 'Sonny', 'Alex']

## Shrinking a List: Remove

We can remove elements in a list using the <a
href="https://www.codecademy.com/resources/docs/python/lists/remove?page_req=catalog"
class="e14vpv2g1 gamut-xro1w8-ResetElement-Anchor-AnchorBase e1bhhzie0"
target="_blank"><code
class="code__2rdF32qjRVp7mMVBHuPwDS">.remove()</code></a> Python method.

Suppose we have a filled list called `shopping_line` that represents a
line at a grocery store:

``` python
shopping_line = ["Cole", "Kip", "Chris", "Sylvana"]
```

We could remove `"Chris"` by using the `.remove()` method:

``` python
shopping_line.remove("Chris")
 
print(shopping_line)
```

If we examine `shopping_line`, we can see that it now doesn’t contain
`"Chris"`:

``` python
["Cole", "Kip", "Sylvana"]
```

We can also use `.remove()` on a list that has duplicate elements.

Only the first instance of the matching element is removed:

``` python
# Create a list
shopping_line = ["Cole", "Kip", "Chris", "Sylvana", "Chris"]
 
# Remove a element
shopping_line.remove("Chris")
print(shopping_line)
```

Will output:

``` python
["Cole", "Kip", "Sylvana", "Chris"]
```

Let’s practice using the `.remove()` method to remove elements from a
list.



**1.**

We have decided to get into the grocery store business. Our manager
Calla has decided to store all the inventory purchases in a list to help
track what products need to be ordered.

Let’s create a list called `order_list` with the following values (in
this particular order):

`"Celery"`, `"Orange Juice"`, `"Orange"`, `"Flatbread"`

Print `order_list` to see the current list.

**2.**

We are in luck! We actually found a spare case of `"Flatbread"` in our
back storage. We won’t need to order it anymore. Let’s remove it from
`order_list` using the `.remove()` method.

Print `order_list` to see the current list.

**3.**

Our store has grown to be a huge success! We decided to open a second
store and require a new order list. Calla has done us the favor of
putting one together.

Create a new list called `new_store_order_list` and assign it the
following values (in order):

`"Orange"`, `"Apple"`, `"Mango"`, `"Broccoli"`, `"Mango"`

**Note**: Our second store is going to need two orders of mangos so the
value is duplicated.

Print `new_store_order_list` to see the current list.

**4.**

We are in luck again! We actually found a spare case of `"Mango"` in our
back storage.

We won’t be needing to place two orders anymore.

Let’s remove it from `new_store_order_list` using the `.remove()`
method.

Print `new_store_order_list` to see the current list.

**5.**

Calla ran to tell us some important news! She asked us to remove
`"Onions"` from our new `new_store_order_list`. If we double-check our
list, we will notice we don’t have `"Onions"` on our list.

Let’s see what happens when we try to remove an item that does not
exist.

Call the `.remove()` method with the value of `"Onions"` on our
`new_store_order_list` list.



``` python
#Your code below: 

# Checkpoint 1
order_list = ["Celery", "Orange Juice", "Orange", "Flatbread"]
print(order_list)

# Checkpoint 2
order_list.remove("Flatbread")
print(order_list)

# Checkpoint 3
new_store_order_list = ["Orange", "Apple", "Mango", "Broccoli", "Mango"]
print(new_store_order_list)

# Checkpoint 4
new_store_order_list.remove("Mango")
print(new_store_order_list)

# Checkpoint 5
new_store_order_list.remove("Onions")
```

    ## ['Celery', 'Orange Juice', 'Orange', 'Flatbread']

    ## ['Celery', 'Orange Juice', 'Orange']

    ## ['Orange', 'Apple', 'Mango', 'Broccoli', 'Mango']

    ## ['Orange', 'Apple', 'Broccoli', 'Mango']

    ## ValueError: list.remove(x): x not in list

## Two-Dimensional (2D) Lists

We’ve seen that the items in a list can be numbers or strings. Lists can
contain other lists! We will commonly refer to these as *two-dimensional
(2D)* lists.

Once more, let’s look at a class height example:

-   Noelle is 61 inches tall
-   Ava is 70 inches tall
-   Sam is 67 inches tall
-   Mia is 64 inches tall

Previously, we saw that we could create a list representing both
Noelle’s name and height:

``` python
noelle = ["Noelle", 61]
```

We can put several of these lists into one list, such that each entry in
the list represents a student and their height:

``` python
heights = [["Noelle", 61], ["Ava", 70], ["Sam", 67], ["Mia", 64]]
```

We will often find that a two-dimensional list is a very good structure
for representing grids such as games like tic-tac-toe.

``` python
#A 2d list with three lists in each of the indices. 
tic_tac_toe = [
            ["X","O","X"], 
            ["O","X","O"], 
            ["O","O","X"]
]
```

Let’s practice creating our own 2D list!



**1.**

A new student named `"Vik"` has joined our class. Vik is `68` inches
tall. Add a sublist to the end of the `heights` list that represents Vik
and his height.

**2.**

Create a two-dimensional list called `ages` where each sublist contains
a student’s name and their age. Use the following data:

-   `"Aaron"` is `15`
-   `"Dhruti"` is `16`



``` python
heights = [["Jenny", 61], ["Alexus", 70], ["Sam", 67], ["Grace", 64], ["Vik", 68]]

ages = [["Aaron", 15], ["Dhruti", 16]]
```

## Accessing 2D Lists

Let’s return to our classroom heights example:

``` python
heights = [["Noelle", 61], ["Ali", 70], ["Sam", 67]]
```

Two-dimensional lists can be accessed similar to their one-dimensional
counterpart. Instead of providing a single pair of brackets `[ ]` we
will use an additional set for each dimension past the first.

If we wanted to access `"Noelle"`’s height:

``` python
#Access the sublist at index 0, and then access the 1st index of that sublist. 
noelles_height = heights[0][1] 
print(noelles_height)
```

Would output:

``` python
61
```

Here are the index numbers to access data for the list `heights`:

| Element    | Index           |
|------------|-----------------|
| `"Noelle"` | `heights[0][0]` |
| `61`       | `heights[0][1]` |
| `"Ali"`    | `heights[1][0]` |
| `70`       | `heights[1][1]` |
| `"Sam"`    | `heights[2][0]` |
| `67`       | `heights[2][1]` |

Let’s practice accessing data in a two-dimensional list.



**1.**

We want to have a way to store all of our classroom test score data.

Using the provided table, create a two-dimensional list called
`class_name_test` to represent the data. Each sublist in
`class_name_test` should have one student’s name and their associated
score.

| Name       | Test Score |
|------------|------------|
| `"Jenny"`  | `90`       |
| `"Alexus"` | `85.5`     |
| `"Sam"`    | `83`       |
| `"Ellie"`  | `101.5`    |

Print `class_name_test` to see the result.

**2.**

Use double square brackets (`[][]`) to select `Sam`’s test score from
the list `class_name_test`.

Save it to the variable `sams_score`.

Print the variable `sams_score` to see the result.

**3.**

Use double square brackets (`[][]`) to select `Ellie`s test score from
the list `class_name_test`. ***This time only use negative indices!***

Save it to the variable `ellies_score`.

Print the variable `ellies_score` to see the result.



``` python
#Your code below: 

#Checkpoint 1
class_name_test = [["Jenny", 90], ["Alexus", 85.5], ["Sam", 83], ["Ellie", 101.5]]
print(class_name_test)

#Checkpoint 2
sams_score = class_name_test[2][1]
print(sams_score)

#Checkpoint 3
ellies_score = class_name_test[-1][-1]
print(ellies_score)
```

    ## [['Jenny', 90], ['Alexus', 85.5], ['Sam', 83], ['Ellie', 101.5]]

    ## 83

    ## 101.5

## Modifying 2D Lists

Now that we know how to access two-dimensional lists, modifying the
elements should come naturally.

Let’s return to a classroom example, but now instead of heights or test
scores, our list stores the student’s favorite hobby!

``` python
class_name_hobbies = [["Jenny", "Breakdancing"], ["Alexus", "Photography"], ["Grace", "Soccer"]]
```

`"Jenny"` changed their mind and is now more interested in
`"Meditation"`.

We will need to modify the list to accommodate the change to our
`class_name_hobbies` list. To change a value in a two-dimensional list,
reassign the value using the specific index.

``` python
# The list of Jenny is at index 0. The hobby is at index 1. 
class_name_hobbies[0][1] = "Meditation"
print(class_name_hobbies)
```

Would output:

``` python
[["Jenny", "Meditation"], ["Alexus", "Photography"], ["Grace", "Soccer"]]
```

Negative indices will work as well.

``` python
# The list of Grace is the last entry. The hobby is the last element. 
class_name_hobbies[-1][-1] = "Football"
print(class_name_hobbies)
```

Would output:

``` python
[["Jenny", "Meditation"], ["Alexus", "Photography"], ["Grace", "Football"]]
```



**1.**

Our school is expanding! We are welcoming a new set of students today
from all over the world.

Using the provided table, create a two-dimensional list called
`incoming_class` to represent the data. Each sublist in `incoming_class`
should contain the name, nationality, and grade for a single student.

| Name        | Nationality   | Grade Level |
|-------------|---------------|-------------|
| `"Kenny"`   | `"American"`  | 9           |
| `"Tanya"`   | `"Ukrainian"` | 9           |
| `"Madison"` | `"Indian"`    | 7           |

Print `incoming_class` to see our list.

**2.**

`"Madison"` passed an exam to advance a grade. She will be pushed into
8th grade rather than her current 7th in our list.

Modify the list using double brackets `[][]` to make the change. ***Use
positive indices***.

Print `incoming_class` to see our change.

**3.**

`"Kenny"` likes to be called by his nickname `"Ken"`. Modify the list
using double brackets `[][]` to accommodate the change but ***only using
negative indices***.

Print `incoming_class` to see our change.



``` python
#Checkpoint 1
incoming_class = [["Kenny", "American", 9], ["Tanya", "Ukrainian", 9], ["Madison", "Indian", 7]]
print(incoming_class)

#Checkpoint 2
incoming_class[2][2] = 8
print(incoming_class)

#Checkpoint 3
incoming_class[-3][-3] = "Ken"
print(incoming_class)
```

    ## [['Kenny', 'American', 9], ['Tanya', 'Ukrainian', 9], ['Madison', 'Indian', 7]]

    ## [['Kenny', 'American', 9], ['Tanya', 'Ukrainian', 9], ['Madison', 'Indian', 8]]

    ## [['Ken', 'American', 9], ['Tanya', 'Ukrainian', 9], ['Madison', 'Indian', 8]]

## Review

So far, we have learned:

-   How to create a list
-   How to access, add, remove, and modify list elements
-   How to create a two-dimensional list
-   How to access and modify two-dimensional list elements

Let’s practice these skills.



**1.**

Maria is entering customer data for her web store business. We’re going
to help her organize her data.

Start by turning this list of customer first names into a list called
`first_names`. Make sure to enter the names in this order:

-   Ainsley
-   Ben
-   Chani
-   Depak

**2.**

Maria wants to track all customer’s preferred sizes for her clothing.
Create a list called `preferred_size`.

Fill our new list `preferred_size` with the following data, containing
the preferred sizes for Ainsley, Ben, and Chani:

``` python
["Small", "Large", "Medium"]
```

**3.**

Oh no! We forgot to add Depak’s size.

Depak’s size is `"Medium"`. Use `.append()` to add `"Medium"` to the
`preferred_size` list.

Print `preferred_size` to see our change.

**4.**

Maria is having a hard time visualizing which customer is associated
with each size. Let’s restructure our two lists into a two-dimensional
list to help Maria.

In addition to our already available data, Maria is adding a third value
for each customer that reflects if they want expedited shipping on their
orders.

This will be reflected using a boolean value (`True` for expedited,
`False` for regular)

Create a two-dimensional list called `customer_data` using the following
table as a reference for the data. Each sublist should contain a name,
size, and expedited shipping option for a single person.

| Name        | Size       | Expedited Shipping |
|-------------|------------|--------------------|
| `"Ainsley"` | `"Small"`  | True               |
| `"Ben"`     | `"Large"`  | False              |
| `"Chani"`   | `"Medium"` | True               |
| `"Depak"`   | `"Medium"` | False              |

Print `customer_data` to see the data.

**5.**

`"Chani"` reached out to Maria. She requested to switch to regular
shipping to save some money.

Change the data value for `"Chani"`’s shipping preference to `False` in
our two-dimensional list to reflect the change.

**6.**

`"Ben"` reached out to Maria asking to remove his shipping option
because he is not sure what type he wants.

Use the `.remove()` method to delete the shipping value from the sublist
that contains ben’s data.

***Note:*** We never explicitly went over how to use the `.remove()`
method on a 2d list together. If you feel like you are struggling, take
a look at the hint for some guidance.

**7.**

Great job making it this far! One last thing, Maria received new
customers, `"Amit"` and `"Karim"`, the following 2d list contains their
data:

``` python
[["Amit", "Large", True], ["Karim", "X-Large", False]]
```

Create a new variable `customer_data_final`. Combine our existing list
`customer_data` with our new customer 2d list using `+` by adding it to
the end of `customer_data`.

Print `customer_data_final` to see our final result.



``` python
# Your code below: 

# Checkpoint 1
first_names = ["Ainsley", "Ben", "Chani", "Depak"]

# Checkpoint 2
preferred_size = ["Small", "Large", "Medium"]

# Checkpoint 3
preferred_size.append("Medium")
print(preferred_size)

# Checkpoint 4
customer_data = [["Ainsley", "Small", True ], ["Ben", "Large", False ], ["Chani", "Medium", True ], ["Depak", "Medium", False ]]
print(customer_data)

# Checkpoint 5
customer_data[2][2] = False

# Checkpoint 6
customer_data[1].remove(False)

# Checkpoint 7
customer_data_final = customer_data + [["Amit", "Large", True], ["Karim", "X-Large", False]]
print(customer_data_final)
```

    ## ['Small', 'Large', 'Medium', 'Medium']

    ## [['Ainsley', 'Small', True], ['Ben', 'Large', False], ['Chani', 'Medium', True], ['Depak', 'Medium', False]]

    ## [['Ainsley', 'Small', True], ['Ben', 'Large'], ['Chani', 'Medium', False], ['Depak', 'Medium', False], ['Amit', 'Large', True], ['Karim', 'X-Large', False]]

# Gradebook

You are a student and you are trying to organize your subjects and
grades using Python. Let’s explore what we’ve learned about lists to
organize your subjects and scores.

## Instructions

Mark the tasks as complete by checking them off

### Create Some Lists:

1\.

Create a list called `subjects` and fill it with the classes you are
taking:

-   `"physics"`
-   `"calculus"`
-   `"poetry"`
-   `"history"`

2\.

Create a list called `grades` and fill it with your scores:

-   `98`
-   `97`
-   `85`
-   `88`

3\.

Manually (without any methods) create a two-dimensional list to combine
`subjects` and `grades`. Use the table below as a reference to
associated values.

| Name         | Test Score |
|--------------|------------|
| `"physics"`  | `98`       |
| `"calculus"` | `97`       |
| `"poetry"`   | `85`       |
| `"history"`  | `88`       |

Assign the value into a variable called `gradebook`.

4\.

Print `gradebook`.

Does it look how you expected it would?

### Add More Subjects:

5\.

Your grade for your computer science class just came in! You got a
perfect score, `100`!

Use the `.append()` method to add a list with the values of
`"computer science"` and an associated grade value of `100` to our
two-dimensional list of `gradebook`.

6\.

Your grade for `"visual arts"` just came in! You got a 93!

Use `append` to add `["visual arts", 93]` to `gradebook`.

### Modify The Gradebook:

7\.

Our instructor just told us they made a mistake grading and are
rewarding an extra 5 points for our visual arts class.

Access the index of the grade for your visual arts class and modify it
to be 5 points greater.

8\.

You decided to switch from a numerical grade value to a Pass/Fail option
for your poetry class.

Find the grade value in your `gradebook` for your poetry class and use
the `.remove()` method to delete it.

9\.

Use the `.append()` method to then add a new `"Pass"` value to the
sublist where your poetry class is located.

### One Big Gradebook!

10\.

You also have your grades from last semester, stored in
`last_semester_gradebook`.

Create a new variable `full_gradebook` that combines both
`last_semester_gradebook` and `gradebook` using `+` to have one complete
grade book.

Print `full_gradebook` to see our completed list.

## Solution

``` python
last_semester_gradebook = [["politics", 80], ["latin", 96], ["dance", 97], ["architecture", 65]]

# Your code below: 
subjects = ["physics", "calculus", "poetry", "history"]

grades = [98, 97, 85, 88]

gradebook = [["physics", 98], ["calculus", 97], ["poetry", 85], ["history", 88]]

print(gradebook)

gradebook.append(["computer science", 100])

gradebook.append(["visual arts", 93])

gradebook[-1][1] = 98

gradebook[2].remove(85)

gradebook[2].append("Pass")

full_gradebook = last_semester_gradebook + gradebook
print(full_gradebook)
```

    ## [['physics', 98], ['calculus', 97], ['poetry', 85], ['history', 88]]

    ## [['politics', 80], ['latin', 96], ['dance', 97], ['architecture', 65], ['physics', 98], ['calculus', 97], ['poetry', 'Pass'], ['history', 88], ['computer science', 100], ['visual arts', 98]]

# Working with Lists in Python

## Working with Lists

Now that we know how to create and access list data, we can start to
explore additional ways of working with lists.

In this lesson, you’ll learn how to:

-   Add and remove items from a list using a specific index.
-   Create lists with continuous values.
-   Get the length of a list.
-   Select portions of a list (called *slicing*).
-   Count the number of times that an element appears in a list.
-   Sort a list of items.

**Note:** In some of the exercises, we will be using <a
href="https://www.codecademy.com/resources/docs/python/built-in-functions?page_req=catalog"
class="e14vpv2g1 gamut-xro1w8-ResetElement-Anchor-AnchorBase e1bhhzie0"
target="_blank">built-in functions</a> in Python. If you haven’t yet
explored the concept of a function, it may look a bit new. Below we
compare it to the method syntax we learned in the earlier lesson.

Here is a preview:

``` python
# Example syntax for methods
list.method(input)
 
# Example syntax for a built-in function 
builtinfuncion(input)
```



Take a second to preview some of the things we will be learning by
examining the graphic of common list methods and built-in functions.

When you’re ready, continue to the next exercise.



<img src="https://static-assets.codecademy.com/Courses/CS101-Intro-to-Programming/ListsLessonDiagrams_v2-0622.svg" alt=".count() is a list method to count the number of occurrences of an element in a list.
.insert() is a list method to insert an element into a specific index of a list.
.pop() is a list method to remove and element from a specific index or from the end of a list. 
range() is a built-in Python function to create sequence of integers. 
len() is a built-in Python function to get the length of a list.
.sort() or sorted() is a method and a built-in function to sort a list." class="gamut-1h2re45-imageStyles-imageStyles e1xtjyf0">

## Adding by Index: Insert

The Python list method `.insert()` allows us to add an element to a
specific index in a list.

The <a
href="https://www.codecademy.com/resources/docs/python/lists/insert?page_ref=catalog"
class="e14vpv2g1 gamut-xro1w8-ResetElement-Anchor-AnchorBase e1bhhzie0"
target="_blank"><code
class="code__2rdF32qjRVp7mMVBHuPwDS">.insert()</code></a> method takes
in two inputs:

1.  The index you want to insert into.
2.  The element you want to insert at the specified index.

The `.insert()` method will handle shifting over elements and can be
used with negative indices.

To see it in action let’s imagine we have a list representing a line at
a store:

``` python
store_line = ["Karla", "Maxium", "Martim", "Isabella"]
```

`"Maxium"` saved a spot for his friend `"Vikor"` and we need to adjust
the list to add him into the line right behind `"Maxium"`.

For this example, we can assume that `"Karla"` is the front of the line
and the rest of the elements are behind her.

Here is how we would use the `.insert()` method to insert `"Vikor"` :

``` python
store_line.insert(2, "Vikor")
print(store_line) 
```

Would output:

``` python
 ['Karla', 'Maxium', 'Vikor', 'Martim', 'Isabella']
```

Some important things to note:

1.  The order and number of the inputs is important. The `.insert()`
    method expects two inputs, the first being a numerical index,
    followed by any value as the second input.

2.  When we insert an element into a list, all elements from the
    specified index and up to the last index are shifted one index to
    the right. This does not apply to inserting an element to the very
    end of a list as it will simply add an additional index and no other
    elements will need to shift.

Let’s practice using `.insert()`!



**1.**

We are helping out a popular grocery store called Jiho’s Produce.

Every week the store has to choose the order in which it displays some
of its popular items on sale in the front window to attract customers.

Jiho, the store owner, likes to store the items for the display in a
list.

Check out the current display list in our code editor. Click **Run** to
print out the list.

**2.**

Jiho found out some great news! `"Pineapple"` is back in stock.

Jiho would like to put `"Pineapple"` in the front of the list so it is
the first item customers see in the display window.

Use `.insert()` to add `"Pineapple"` to the front of the list.

Print the resulting list to see the change.

***Note***: For this list, the front will be the element at index `0`



``` python
front_display_list = ["Mango", "Filet Mignon", "Chocolate Milk"]
print(front_display_list)

# Your code below: 

# Checkpoint 2
front_display_list.insert(0, "Pineapple")
print(front_display_list)
```

    ## ['Mango', 'Filet Mignon', 'Chocolate Milk']

    ## ['Pineapple', 'Mango', 'Filet Mignon', 'Chocolate Milk']

## Removing by Index: Pop

Just as we learned to insert elements at specific indices, Python gives
us a method to remove elements at a specific index using a method called
`.pop()`.

The <a
href="https://www.codecademy.com/resources/docs/python/lists/pop?page_req=catalog"
class="e14vpv2g1 gamut-xro1w8-ResetElement-Anchor-AnchorBase e1bhhzie0"
target="_blank"><code
class="code__2rdF32qjRVp7mMVBHuPwDS">.pop()</code></a> method takes an
optional single input:

1.  The index for the element you want to remove.

To see it in action, let’s consider a list called `cs_topics` that
stores a collection of topics one might study in a computer science
program.

``` python
cs_topics = ["Python", "Data Structures", "Balloon Making", "Algorithms", "Clowns 101"]
```

Two of these topics don’t look like they belong, let’s see how we remove
them using `.pop()`.

First let’s remove `"Clowns 101"`:

``` python
removed_element = cs_topics.pop()
print(cs_topics)
print(removed_element)
```

Would output:

``` python
['Python', 'Data Structures', 'Balloon Making', 'Algorithms']
'Clowns 101'
```

Notice two things about this example:

1.  The method can be called without a specific index. Using `.pop()`
    without an index will remove whatever the last element of the list
    is. In our case `"Clowns 101"` gets removed.

2.  `.pop()` is unique in that it will *return* the value that was
    removed. If we wanted to know what element was deleted, simply
    assign a variable to the call of the `.pop()` method. In this case,
    we assigned it to `removed_element`.

Lastly let’s remove `"Balloon Making"`:

``` python
cs_topics.pop(2)
print(cs_topics)
```

Would output:

``` python
['Python', 'Data Structures', 'Algorithms']
```

Notice two things about this example:

1.  The method can be called with an optional specific index to remove.
    In our case, the index `2` removes the value of `"Balloon Making"`.
2.  We don’t have to save the removed value to any variable if we don’t
    care to use it later.

***Note:*** Passing in an index that does not exist or calling `.pop()`
on an empty list will both result in an `IndexError`.

Let’s apply what we learned about the `.pop()` method.



**1.**

We have decided to pursue the study of data science in addition to our
computer science coursework. We signed up for an online school that
would help us become proficient.

Check out the current list of topics we will be studying in our code
editor.

Click ***Run*** to print out the list.

**2.**

It looks like we have an overlap with our computer science curriculum
for the topic of `"Python 3"`.

Let’s remove the topic from the list of `data_science_topics` using our
newly learned `.pop()` method.

Print `data_science_topics` to see your result.

**3.**

Looks like there is overlap on the `"Algorithms"` topic as well. Let’s
use `.pop()` to remove it as well.

Print `data_science_topics` to see the changes.



``` python
data_science_topics = ["Machine Learning", "SQL", "Pandas", "Algorithms", "Statistics", "Python 3"]
print(data_science_topics)

# Your code below: 

# Checkpoint 2
data_science_topics.pop()
print(data_science_topics)

# Checkpoint 3
data_science_topics.pop(3)
print(data_science_topics)
```

    ## ['Machine Learning', 'SQL', 'Pandas', 'Algorithms', 'Statistics', 'Python 3']

    ## 'Python 3'

    ## ['Machine Learning', 'SQL', 'Pandas', 'Algorithms', 'Statistics']

    ## 'Algorithms'

    ## ['Machine Learning', 'SQL', 'Pandas', 'Statistics']

## Consecutive Lists: Range

Often, we want to create a list of consecutive numbers in our programs.
For example, suppose we want a list containing the numbers 0 through 9:

``` python
my_list = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
```

Typing out all of those numbers takes time and the more numbers we type,
the more likely it is that we have a typo that can cause an error.

Python gives us an easy way of creating these types of lists using a
built-in function called <a
href="https://www.codecademy.com/resources/docs/python/built-in-functions/range?page_req=catalog"
class="e14vpv2g1 gamut-xro1w8-ResetElement-Anchor-AnchorBase e1bhhzie0"
target="_blank"><code
class="code__2rdF32qjRVp7mMVBHuPwDS">range()</code></a>.

The function `range()` takes a single input, and generates numbers
starting at `0` and ending at the number **before** the input.

So, if we want the numbers from `0` through `9`, we use `range(10)`
because `10` is 1 greater than `9`:

``` python
my_range = range(10)
print(my_range)
```

Would output:

``` python
range(0, 10)
```

Notice something different? The `range()` function is unique in that it
creates a *range object*. It is not a typical list like the ones we have
been working with.

In order to use this object as a list, we have to first convert it using
another built-in function called <a
href="https://www.codecademy.com/resources/docs/python/built-in-functions/list?page_ref=catalog"
class="e14vpv2g1 gamut-xro1w8-ResetElement-Anchor-AnchorBase e1bhhzie0"
target="_blank"><code
class="code__2rdF32qjRVp7mMVBHuPwDS">list()</code></a>.

The `list()` function takes in a single input for the object you want to
convert.

We use the `list()` function on our range object like this:

``` python
print(list(my_range))
```

Would output:

``` python
[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
```

Let’s try out using `range()`!



**1.**

Modify `number_list` so that it is a range containing numbers starting
at 0 and up to, but not including, 9.

**2.**

Create a range called `zero_to_seven` with the numbers 0 through 7.

Print the result in list form.



``` python
# Checkpoint 1
number_list = range(9)
print(list(number_list))

# Checkpoint 2
zero_to_seven = range(8)
print(list(zero_to_seven))
```

    ## [0, 1, 2, 3, 4, 5, 6, 7, 8]

    ## [0, 1, 2, 3, 4, 5, 6, 7]

## The Power of Range!

By default, `range()` creates a list starting at `0`. However, if we
call `range()` with two inputs, we can create a list that starts at a
different number.

For example, `range(2, 9)` would generate numbers starting at `2` and
ending at `8` (just before `9`):

``` python
my_list = range(2, 9)
print(list(my_list))
```

Would output:

``` python
[2, 3, 4, 5, 6, 7, 8]
```

If we use a third input, we can create a list that “skips” numbers.

For example, `range(2, 9, 2)` will give us a list where each number is
`2` greater than the previous number:

``` python
my_range2 = range(2, 9, 2)
print(list(my_range2))
```

Would output:

``` python
[2, 4, 6, 8]
```

We can skip as many numbers as we want!

For example, we’ll start at `1` and skip in increments of `10` between
each number until we get to `99` (one before `100`):

``` python
my_range3 = range(1, 100, 10)
print(list(my_range3))
```

Would output:

``` python
[1, 11, 21, 31, 41, 51, 61, 71, 81, 91]
```

Our list stops at `91` because the next number in the sequence would be
`101`, which is greater than or equal to `100` (our stopping point).

Let’s experiment with our additional `range()` inputs!



**1.**

Modify the `range()` function that created the range `range_five_three`
such that it:

-   Starts at `5`
-   Has a difference of `3` between each item
-   Ends **before** `15`

**2.**

Create a range called `range_diff_five` that:

-   Starts at `0`
-   Has a difference of `5` between each item
-   Ends **before** `40`



``` python
#Checkpoint 1
range_five_three = range(5, 15, 3)

#Checkpoint 2
range_diff_five = range(0,40,5)
```

## Length

Often, we’ll need to find the number of items in a list, usually called
its *length*.

We can do this using a built-in function called <a
href="https://www.codecademy.com/resources/docs/python/built-in-functions/len?page_ref=catalog"
class="e14vpv2g1 gamut-xro1w8-ResetElement-Anchor-AnchorBase e1bhhzie0"
target="_blank"><code
class="code__2rdF32qjRVp7mMVBHuPwDS">len()</code></a>.

When we apply `len()` to a list, we get the number of elements in that
list:

``` python
my_list = [1, 2, 3, 4, 5]
 
print(len(my_list))
```

Would output:

``` python
5
```

Let’s find the length of various lists!



**1.**

Calculate the length of `long_list` and save it to the variable
`long_list_len`.

**2.**

Use `print()` to examine `long_list_len`.

**3.**

We have provided a completed `range()` function for the variable
`big_range`.

Calculate its length using the function `len()` and save it to a
variable called `big_range_length`.

***Note:*** Range objects do not need to be converted to lists in order
to determine their length

**4.**

Use `print()` to examine `big_range_length`.

**5.**

Change the `range()` function that generates `big_range` so that it
skips `100` instead of `10` steps between items.

How does this change `big_range_length`?



``` python
long_list = [1, 5, 6, 7, -23, 69.5, True, "very", "long", "list", "that", "keeps", "going.", "Let's", "practice", "getting", "the", "length"]

big_range = range(2, 3000, 10)

# Your code below: 

# Checkpoint 1 & 2
long_list_len = len(long_list)
print(long_list_len)

# Checkpoint 3 & 4
big_range_length = len(big_range)
print(big_range_length)

# Checkpoint 5
# Change range_list to be equal to range(2, 3000, 100)
```

    ## 18

    ## 300

## Slicing Lists I

In Python, often we want to extract only a portion of a list. Dividing a
list in such a manner is referred to as *slicing*.

Lets assume we have a list of `letters`:

``` python
letters = ["a", "b", "c", "d", "e", "f", "g"]
```

Suppose we want to select from `"b"` through `"f"`.

We can do this using the following syntax: `letters[start:end]`, where:

-   `start` is the index of the first element that we want to include in
    our selection. In this case, we want to start at `"b"`, which has
    index `1`.
-   `end` is the index of *one more than* the last index that we want to
    include. The last element we want is `"f"`, which has index `5`, so
    `end` needs to be `6`.

``` python
sliced_list = letters[1:6]
print(sliced_list)
```

Would output:

``` python
["b", "c", "d", "e", "f"]
```

Notice that the element at index `6` (which is `"g"`) is *not* included
in our selection.



**1.**

Use `print()` to examine the variable `beginning`.

Before hitting ***Run*** think about what elements `beginning` will
contain?

**2.**

Modify `beginning`, so that it selects the first 2 elements of
`suitcase`.

**3.**

Create a new list called `middle` that contains the middle two items (
`["pants", "pants"]` ) from `suitcase`.

Print `middle` to see the slice!



``` python
suitcase = ["shirt", "shirt", "pants", "pants", "pajamas", "books"]

beginning = suitcase[0:4]

# Your code below: 
print(beginning)

# Checkpoint 2 
beginning = suitcase[0:2]

# Checkpoint 3
middle = suitcase[2:4]
print(middle)
```

    ## ['shirt', 'shirt', 'pants', 'pants']

    ## ['pants', 'pants']

## Slicing Lists II

Slicing syntax in Python is very flexible. Let’s look at a few more
problems we can tackle with slicing.

Take the list `fruits` as our example:

``` python
fruits = ["apple", "cherry", "pineapple", "orange", "mango"]
```

If we want to select the *first `n` elements* of a list, we could use
the following code:

``` python
fruits[:n]
```

For our `fruits` list, suppose we wanted to slice the first three
elements.

The following code would start slicing from index `0` and up to index
`3`. Note that the fruit at index `3` (`orange`) is not included in the
results.

``` python
print(fruits[:3])
```

Would output:

``` python
['apple', 'cherry', 'pineapple']
```

We can do something similar when we want to slice the *last `n`
elements* in a list:

``` python
fruits[-n:]
```

For our `fruits` list, suppose we wanted to slice the last two elements.

This code slices from the element at index `-2` up through the last
index.

``` python
print(fruits[-2:])
```

Would output:

``` python
['orange', 'mango']
```

Negative indices can also accomplish taking *all but n last elements* of
a list.

``` python
fruits[:-n]
```

For our `fruits` example, suppose we wanted to slice all but the last
element from the list.

This example starts counting from the `0` index up to the element at
index `-1`.

``` python
print(fruits[:-1])
```

Would output:

``` python
['apple', 'cherry', 'pineapple', 'orange']
```

Let’s practice some of these extra slicing techniques!



**1.**

Create a new list called `last_two_elements` containing the final two
elements of `suitcase`.

Print `last_two_elements` to see your result.

**2.**

Create a new list called `slice_off_last_three` containing all but the
last three elements.

Print `slice_off_last_three` to see your result.



``` python
suitcase = ["shirt", "shirt", "pants", "pants", "pajamas", "books"]

# Your code below: 

# Checkpoint 1
last_two_elements = suitcase[-2:]
print(last_two_elements)

# Checkpoint 2
slice_off_last_three = suitcase[:-3]
print(slice_off_last_three)
```

    ## ['pajamas', 'books']

    ## ['shirt', 'shirt', 'pants']

## Counting in a List

In Python, it is common to want to count occurrences of an item in a
list.

Suppose we have a list called `letters` that represents the letters in
the word “Mississippi”:

``` python
letters = ["m", "i", "s", "s", "i", "s", "s", "i", "p", "p", "i"]
```

If we want to know how many times `i` appears in this word, we can use
the list method called <a
href="https://www.codecademy.com/resources/docs/python/lists/count?page_req=catalog"
class="e14vpv2g1 gamut-xro1w8-ResetElement-Anchor-AnchorBase e1bhhzie0"
target="_blank"><code
class="code__2rdF32qjRVp7mMVBHuPwDS">.count()</code></a>:

``` python
num_i = letters.count("i")
print(num_i)
```

Would output:

``` python
4
```

Notice that since `.count()` *returns* a value, we can assign it to a
variable to use it.

We can even use `.count()` to count element appearances in a
two-dimensional list.

Let’s use the list `number_collection` as an example:

``` python
number_collection = [[100, 200], [100, 200], [475, 29], [34, 34]]
```

If we wanted to know how often the sublist `[100, 200]` appears:

``` python
num_pairs = number_collection.count([100, 200])
print(num_pairs)
```

Would output:

``` python
2
```

Let’s count some list items using the `.count()` method!



**1.**

Mrs. Wilson’s class is voting for class president. She has saved each
student’s vote into the list `votes`.

Use `.count()` to determine how many students voted for `"Jake"` and
save the value to a variable called `jake_votes`.

**2.**

Use `print()` to examine `jake_votes`.



``` python
votes = ["Jake", "Jake", "Laurie", "Laurie", "Laurie", "Jake", "Jake", "Jake", "Laurie", "Cassie", "Cassie", "Jake", "Jake", "Cassie", "Laurie", "Cassie", "Jake", "Jake", "Cassie", "Laurie"]

# Your code below: 

# Checkpoint 1
jake_votes = votes.count("Jake")

# Checkpoint 2
print(jake_votes)
```

    ## 9

## Sorting Lists I

Often, we will want to sort a list in either numerical (1, 2, 3, …) or
alphabetical (a, b, c, …) order.

We can sort a list using the method <a
href="https://www.codecademy.com/resources/docs/python/lists/sort?page_req=catalog"
class="e14vpv2g1 gamut-xro1w8-ResetElement-Anchor-AnchorBase e1bhhzie0"
target="_blank"><code
class="code__2rdF32qjRVp7mMVBHuPwDS">.sort()</code></a>.

Suppose that we have a list of names:

``` python
names = ["Xander", "Buffy", "Angel", "Willow", "Giles"]
```

Let’s see what happens when we apply `.sort()`:

``` python
names.sort()
print(names)
```

Would output:

``` python
['Angel', 'Buffy', 'Giles', 'Willow', 'Xander']
```

As we can see, the `.sort()` method sorted our list of `names` in
alphabetical order.

`.sort()` also provides us the option to go in reverse. Instead of
sorting in ascending order like we just saw, we can do so in descending
order.

``` python
names.sort(reverse=True)
print(names)
```

Would output:

``` python
['Xander', 'Willow', 'Giles', 'Buffy', 'Angel']
```

**Note:** The `.sort()` method does not return any value and thus does
not need to be assigned to a variable since it modifies the list
directly. If we do assign the result of the method, it would assign the
value of `None` to the variable.

Let’s experiment sorting various lists!



**1.**

Use `.sort()` to sort `addresses`.

**2.**

Use `print()` to see how `addresses` changed.

**3.**

Remove the `#` and whitespace in front of the line `sort(names)`. Edit
this line so that it runs without producing a `NameError`.

**4.**

Use `print` to examine `sorted_cities`. Why is it not the sorted version
of `cities`?

**5.**

Edit the `.sort()` call on `cities` such that it sorts the cities in
reverse order (descending).

Print `cities` to see the result.



``` python
# Checkpoint 1 & 2
addresses = ["221 B Baker St.", "42 Wallaby Way", "12 Grimmauld Place", "742 Evergreen Terrace", "1600 Pennsylvania Ave", "10 Downing St."]
addresses.sort()
print(addresses)


# Checkpoint 3
names = ["Ron", "Hermione", "Harry", "Albus", "Sirius"]
names.sort()


# Checkpoint 4 & 5
cities = ["London", "Paris", "Rome", "Los Angeles", "New York"]
sorted_cities = cities.sort(reverse=True)
print(sorted_cities)
print(cities)
```

    ## ['10 Downing St.', '12 Grimmauld Place', '1600 Pennsylvania Ave', '221 B Baker St.', '42 Wallaby Way', '742 Evergreen Terrace']

    ## None

    ## ['Rome', 'Paris', 'New York', 'Los Angeles', 'London']

## Sorting Lists II

A second way of sorting a list in Python is to use the built-in function
`sorted()`.

The <a
href="https://www.codecademy.com/resources/docs/python/built-in-functions/sorted?page_req=catalog"
class="e14vpv2g1 gamut-xro1w8-ResetElement-Anchor-AnchorBase e1bhhzie0"
target="_blank"><code
class="code__2rdF32qjRVp7mMVBHuPwDS">sorted()</code></a> function is
different from the `.sort()` method in two ways:

1.  It comes *before* a list, instead of after as all built-in functions
    do.
2.  It generates a new list rather than modifying the one that already
    exists.

Let’s return to our list of names:

``` python
names = ["Xander", "Buffy", "Angel", "Willow", "Giles"]
```

Using `sorted()`, we can create a new list, called `sorted_names`:

``` python
sorted_names = sorted(names)
print(sorted_names)
```

This yields the list sorted alphabetically:

``` python
['Angel', 'Buffy', 'Giles', 'Willow', 'Xander']
```

Note that using `sorted` did not change `names`:

``` python
print(names)
```

Would output:

``` python
['Xander', 'Buffy', 'Angel', 'Willow', 'Giles']
```



**1.**

Use `sorted()` to order `games` and create a new list called
`games_sorted`.

**2.**

Print both `games` and `games_sorted`. How are they different?



``` python
games = ["Portal", "Minecraft", "Pacman", "Tetris", "The Sims", "Pokemon"]

# Your code below:
# Checkpoint 1
games_sorted = sorted(games)

# Checkpoint 2
print(games)
print(games_sorted)
```

    ## ['Portal', 'Minecraft', 'Pacman', 'Tetris', 'The Sims', 'Pokemon']

    ## ['Minecraft', 'Pacman', 'Pokemon', 'Portal', 'Tetris', 'The Sims']

## Review

In this lesson, we learned how to:

-   Add elements to a list by index using the `.insert()` method.
-   Remove elements from a list by index using the `.pop()` method.
-   Generate a list using the `range()` function.
-   Get the length of a list using the `len()` function.
-   Select portions of a list using slicing syntax.
-   Count the number of times that an element appears in a list using
    the `.count()` method.
-   Sort a list of items using either the `.sort()` method or `sorted()`
    function.

As you go through the exercises, feel free to use `print()` to see
changes when not explicitly asked to do so.



**1.**

Our friend Jiho has been so successful in both the flower and grocery
business that she has decided to open a furniture store.

Jiho has compiled a list of inventory items into a list called
`inventory` and wants to know a few facts about it.

First, how many items are in the warehouse?

Save the answer to a variable called `inventory_len`.

**2.**

Select the first element in `inventory`. Save it to a variable called
`first`.

**3.**

Select the last element from `inventory`. Save it to a variable called
`last`.

**4.**

Select items from the `inventory` starting at index `2` and up to, but
not including, index `6`.

Save your answer to a variable called `inventory_2_6`.

**5.**

Select the first 3 items of `inventory`. Save it to a variable called
`first_3`.

**6.**

How many `'twin bed'`s are in `inventory`? Save your answer to a
variable called `twin_beds`.

**7.**

Remove the 5th element in the inventory. Save the value to a variable
called `removed_item`.

**8.**

There was a new item added to our inventory called
`"19th Century Bed Frame"`.

Use the `.insert()` method to place the new item as the 11th element in
our inventory.

**9.**

Sort `inventory` using the `.sort()` method or the `sorted()` function.

Remember, the `sorted()` function doesn’t change the original list — it
creates a new list with the elements properly sorted. If you use
`sorted()` you’ll have to set `inventory` equal to the value returned by
`sorted()`.

Print `inventory` to see the result.



``` python
inventory = ["twin bed", "twin bed", "headboard", "queen bed", "king bed", "dresser", "dresser", "table", "table", "nightstand", "nightstand", "king bed", "king bed", "twin bed", "twin bed", "sheets", "sheets", "pillow", "pillow"]

# Checkpoint 1
inventory_len = len(inventory)

# Checkpoint 2
first = inventory[0]

# Checkpoint 3
last = inventory[-1]

# Checkpoint 4
inventory_2_6 = inventory[2:6]

# Checkpoint 5
first_3 = inventory[:3]

# Checkpoint 6
twin_beds = inventory.count("twin bed")

# Checkpoint 7
removed_item = inventory.pop(4)

# Checkpoint 8
inventory.insert(10, "19th Century Bed Frame")

#Checkpoint 9
inventory.sort()
print(inventory)
```

    ## ['19th Century Bed Frame', 'dresser', 'dresser', 'headboard', 'king bed', 'king bed', 'nightstand', 'nightstand', 'pillow', 'pillow', 'queen bed', 'sheets', 'sheets', 'table', 'table', 'twin bed', 'twin bed', 'twin bed', 'twin bed']

# Len’s Slice

You work at Len’s Slice, a new pizza joint in the neighborhood. You are
going to use your knowledge of Python lists to organize some of your
sales data.

## Instructions

Mark the tasks as complete by checking them off

### Make Some Pizzas

1\.

To keep track of the kinds of pizzas you sell, create a list called
`toppings` that holds the following:

-   `"pepperoni"`
-   `"pineapple"`
-   `"cheese"`
-   `"sausage"`
-   `"olives"`
-   `"anchovies"`
-   `"mushrooms"`

2\.

To keep track of how much each kind of pizza slice costs, create a list
called `prices` that holds the following integer values:

-   `2`
-   `6`
-   `1`
-   `3`
-   `2`
-   `7`
-   `2`

3\.

Your boss wants you to do some research on $2 slices.

Count the number of occurrences of `2` in the `prices` list, and store
the result in a variable called `num_two_dollar_slices`. Print it out.

4\.

Find the length of the `toppings` list and store it in a variable called
`num_pizzas`.

5\.

Print the string `We sell [num_pizzas] different kinds of pizza!`, where
`[num_pizzas]` represents the value of our variable `num_pizzas`.

6\.

Use the existing data about the pizza toppings and prices to create a
new two-dimensional list called `pizza_and_prices`.

Each sublist in `pizza_and_prices` should have one pizza topping and an
associated price.

| Price | Topping       |
|-------|---------------|
| `2`   | `"pepperoni"` |
| `6`   | `"pineapple"` |
| `1`   | `"cheese"`    |
| `3`   | `"sausage"`   |
| `2`   | `"olives"`    |
| `7`   | `"anchovies"` |
| `2`   | `"mushrooms"` |

For this new list make sure the prices come before the topping name like
so:

``` python
[price, topping_name]
```

Note: You don’t need to use your original `toppings` and `prices` lists
in this exercise. Create a new two-dimensional list from scratch.

7\.

Print `pizza_and_prices`.

Does it look the way you expect?

### Sorting and Slicing Pizzas

8\.

Sort `pizza_and_prices` so that the pizzas are in the order of
increasing price (ascending).

9\.

Store the first element of `pizza_and_prices` in a variable called
`cheapest_pizza`.

10\.

A man walks into the pizza store and shouts “I will have your MOST
EXPENSIVE pizza!”

Get the last item of the `pizza_and_prices` list and store it in a
variable called `priciest_pizza`.

11\.

It looks like the most expensive pizza from the previous step was our
very last `"anchovies"` slice. Remove it from our `pizza_and_prices`
list since the man bought the last slice.

12\.

Since there is no longer an `"anchovies"` pizza, you want to add a new
topping called `"peppers"` to keep your customers excited about new
toppings. Here is what your new topping looks like:

``` python
[2.5, "peppers"]
```

Add the new peppers pizza topping to our list `pizza_and_prices`.

**Note:** Make sure to position it relative to the rest of the sorted
data in `pizza_and_prices`, otherwise our data will not be correctly
sorted anymore!

13\.

Three mice walk into the store. They don’t have much money (they’re
mice), but they do each want different pizzas.

Slice the `pizza_and_prices` list and store the 3 lowest cost pizzas in
a list called `three_cheapest`.

14\.

Great job! The mice are very pleased and will be leaving you a 5-star
review.

Print the `three_cheapest` list.

## Solution

``` python
# Your code below:
toppings = ["pepperoni", "pineapple", "cheese", "sausage", "olives", "anchovies", "mushrooms"]

prices = [2, 6, 1, 3, 2, 7, 2]

num_two_dollar_slices = prices.count(2)

num_pizzas = len(toppings)

print("We Sell", num_pizzas, "different kinds of pizza!")

pizza_and_prices = list(zip(prices, toppings))

pizza_and_prices.sort()

cheapest_pizza = pizza_and_prices[0]

priciest_pizza = pizza_and_prices[-1]

pizza_and_prices.pop()

priciest_pizza = pizza_and_prices[-1]

three_cheapest = pizza_and_prices[:3]

print(three_cheapest)
```

    ## We Sell 7 different kinds of pizza!

    ## (7, 'anchovies')

    ## [(1, 'cheese'), (2, 'mushrooms'), (2, 'olives')]

# Learn Python: Tuples

[Python Walkthrough Tuples In
Python](https://www.youtube.com/watch?v=yDvRR8nWMNI)

# Combining Lists: The Zip Function

Learn about a popular Python built-in function called zip().

In Python, we have an assortment of built-in functions that allow us to
build our programs faster and cleaner. One of those functions is
`zip()`.

The `zip()` function allows us to quickly combine associated data-sets
without needing to rely on multi-dimensional lists. While `zip()` can
work with many different scenarios, we are going to explore only a
single one in this article.

Let’s use a list of student names and associated heights as our example
data set:

-   Jenny is 61 inches tall
-   Alexus is 70 inches tall
-   Sam is 67 inches tall
-   Grace is 64 inches tall

Suppose that we already had a list of names and a list of heights:

``` python
names = ["Jenny", "Alexus", "Sam", "Grace"]
heights = [61, 70, 67, 64]
```

If we wanted to create a nested list that paired each name with a
height, we could use the built-in function `zip()`.

The `zip()` function takes two (or more) lists as inputs and returns an
*object* that contains a list of pairs. Each pair contains one element
from each of the inputs. This is how we would do it for our `names` and
`heights` lists:

``` python
names_and_heights = zip(names, heights)
```

If we were to then examine this new variable `names_and_heights`, we
would find it looks a bit strange:

``` python
print(names_and_heights)
```

Would output:

``` python
<zip object at 0x7f1631e86b48>
```

This *zip object* contains the location of this variable in our
computer’s memory. Don’t worry though, it is fairly simple to convert
this object into a useable list by using the built-in function `list()`:

``` python
converted_list = list(names_and_heights)
print(converted_list)
```

Outputs:

``` python
[('Jenny', 61), ('Alexus', 70), ('Sam', 67), ('Grace', 64)]
```

Notice two things:

1.  Our data set has been converted from a zip memory object to an
    actual list (denoted by `[ ]`)

2.  Our inner lists don’t use square brackets `[ ]` around the values.
    This is because they have been converted into <a
    href="https://docs.python.org/3/tutorial/datastructures.html#tuples-and-sequences"
    class="e14vpv2g1 gamut-xro1w8-ResetElement-Anchor-AnchorBase e1bhhzie0"
    target="_blank" rel="noopener">tuples</a> (an immutable type of
    list).

Let’s practice using `zip()`!

Use `zip()` to create a new variable called `names_and_dogs_names` that
combines `owners` and `dogs_names` lists into a zip object.

Then, create a new variable named `list_of_names_and_dogs_names` by
calling the `list()` function on `names_and_dogs_names`.

Print `list_of_names_and_dogs_names`.

``` python
owners = ["Jenny", "Alexus", "Sam", "Grace"]
dogs_names = ["Elphonse", "Dr. Doggy DDS", "Carter", "Ralph"]
names_and_dogs_names = zip(owners, dogs_names)
list_of_names_and_dogs_names = list(names_and_dogs_names)
print(list_of_names_and_dogs_names)
```

    ## [('Jenny', 'Elphonse'), ('Alexus', 'Dr. Doggy DDS'), ('Sam', 'Carter'), ('Grace', 'Ralph')]

# Loops

## What are Loops?

In our everyday lives, we tend to repeat a lot of processes without
noticing.

For instance, if we want to cook a delicious recipe, we might have to
prepare our ingredients by chopping them up. We chop and chop and chop
until all of our ingredients are the right size. At this point, we stop
chopping.

If we break down our chopping task into a series of three smaller steps,
we have:

1.  An initialization: We’re ready to cook and have a collection of
    ingredients we want to chop. We will start at the first ingredient.

2.  A repetition: We’re chopping away. We are performing the action of
    chopping over and over on each of our ingredients, one ingredient at
    a time.

3.  An end condition: We see that we have run out of ingredients to chop
    and so we stop.

In programming, this process of using an initialization, repetitions,
and an ending condition is called a <a
href="https://www.codecademy.com/resources/docs/python/loops?page_ref=catalog"
class="e14vpv2g1 gamut-xro1w8-ResetElement-Anchor-AnchorBase e1bhhzie0"
target="_blank"><em>loop</em></a>. In a loop, we perform a process of
*iteration* (repeating tasks).

Programming languages like Python implement two types of iteration:

1.  *Indefinite iteration*, where the number of times the loop is
    executed depends on how many times a condition is met.

2.  *Definite iteration*, where the number of times the loop will be
    executed is defined in advance (usually based on the collection
    size).

Typically we will find loops being used to iterate a collection of
items. In the above example, we can think of our ingredients we want to
chop as our collection. This is a form of definite iteration since we
know how long our collection is in advance and thus know how many times
we need to iterate over the collection of ingredients.

Some collections might be small — like a short string, while other
collections might be massive like a range of numbers from 1 to
10,000,000! But don’t worry, loops give us the ability to masterfully
handle both ends of the spectrum. This simple, but powerful, concept
saves us a lot of time and makes it easier for us to work with large
amounts of data.

In this lesson, we’ll learn how to use Python to implement both definite
and indefinite iteration in our own programs.



Look over (and over) the provided diagram. Then, go to the next exercise
to get looped in!



<img src="https://content.codecademy.com/courses/learn-swift/loops/ChalkboardLoop.svg" alt="Chalkboard filled with from top to bottom with the sentence &quot;I will not write smelly code&quot; with a visibly annoyed person standing next to it." class="gamut-1h2re45-imageStyles-imageStyles e1xtjyf0">

## Why Loops?

Before we get to writing our own loops, let’s explore what programming
would be like if we couldn’t use loops.

Let’s say we have a list of `ingredients` and we want to print every
element in the list:

``` python
ingredients = ["milk", "sugar", "vanilla extract", "dough", "chocolate"]
```

If we only use `print()`, our program might look like this:

``` python
print(ingredients[0])
print(ingredients[1])
print(ingredients[2])
print(ingredients[3])
print(ingredients[4])
```

The output would be:

``` python
milk
sugar
vanilla extract
dough
chocolate
```

That’s still manageable, We’re writing 5 `print()` statements (or
copying and pasting a few times). Now imagine if we come back to this
program and our list had 10, or 24601, or … 100,000,000 elements? It
would take an extremely long time and by the end, we could still end up
with inconsistencies and mistakes.

Don’t dwell too long on this tedious scenario — we’ll learn how loops
can help us out in the next exercise. For now, let’s gain an
appreciation for loops.



**1.**

Using 10 `print()` statements, print out:
`"This can be so much easier with loops!"`.



``` python
# Write 10 print() statements below! 

print("This can be so much easier with loops!")
print("This can be so much easier with loops!")
print("This can be so much easier with loops!")
print("This can be so much easier with loops!")
print("This can be so much easier with loops!")
print("This can be so much easier with loops!")
print("This can be so much easier with loops!")
print("This can be so much easier with loops!")
print("This can be so much easier with loops!")
print("This can be so much easier with loops!")
```

    ## This can be so much easier with loops!

    ## This can be so much easier with loops!

    ## This can be so much easier with loops!

    ## This can be so much easier with loops!

    ## This can be so much easier with loops!

    ## This can be so much easier with loops!

    ## This can be so much easier with loops!

    ## This can be so much easier with loops!

    ## This can be so much easier with loops!

    ## This can be so much easier with loops!

## For Loops: Introduction

Now that we can appreciate what loops do for us, let’s start with your
first type of loop, a `for` loop, a type of definite iteration.

In a `for` loop, we will know in advance how many times the loop will
need to iterate because we will be working on a collection with a
predefined length. In our examples, we will be using Python lists as our
collection of elements.

With `for` loops, on each iteration, we will be able to perform an
action on each element of the collection.

Before we work with any collection, let’s examine the general structure
of a `for` loop:

``` python
for <temporary variable> in <collection>:
  <action>
```

Let’s break down each of these components:

1.  A `for` keyword indicates the start of a `for` loop.
2.  A `<temporary variable>` that is used to represent the value of the
    element in the collection the loop is currently on.
3.  An `in` keyword separates the temporary variable from the collection
    used for iteration.
4.  A `<collection>` to loop over. In our examples, we will be using a
    list.
5.  An `<action>` to do anything on each iteration of the loop.

Let’s link these concepts back to our `ingredients` example. This `for`
loop prints each `ingredient` in `ingredients`:

``` python
ingredients = ["milk", "sugar", "vanilla extract", "dough", "chocolate"]
 
for ingredient in ingredients:
  print(ingredient)
```

In this example:

1.  `ingredient` is the `<temporary variable>`.
2.  `ingredients` is our `<collection>`.
3.  `print(ingredient)` was the `<action>` performed on every iteration
    using the temporary variable of `ingredient`.

This code outputs:

``` python
milk
sugar
vanilla extract
dough
chocolate
```

Some things to note about `for` loops:

-   **Temporary Variables:**

    A temporary variable’s name is arbitrary and does not need to be
    defined beforehand. Both of the following code snippets do the exact
    same thing as our above example:

    ``` python
    for i in ingredients:
      print(i)
    ```

    ``` python
    for item in ingredients:
     print(item)
    ```

    Programming best practices suggest we make our temporary variables
    as descriptive as possible. Since each iteration (step) of our loop
    is accessing an ingredient it makes more sense to call our temporary
    variable `ingredient` rather than `i` or `item`.

<!-- -->

-   **Indentation:**

    Notice that in all of these examples the `print` statement is
    indented. Everything at the same level of indentation after the
    `for` loop declaration is included in the loop body and is run on
    every iteration of the loop.

    ``` python
    for ingredient in ingredients:
      # Any code at this level of indentation 
      # will run on each iteration of the loop
      print(ingredient)
    ```

    If we ever forget to indent, we’ll get an `IndentationError` or
    unexpected behavior.

<!-- -->

-   **Elegant loops:**

    Python loves to help us write elegant code so it allows us to write
    simple `for` loops in one-line. In order to see the below example as
    one line, you may need to expand your narrative window. Here is the
    previous example in a single line:

    ``` python
    for ingredient in ingredients: print(ingredient)
    ```

    **Note**: One-line `for` loops are useful for simple programs. It is
    not recommended you write one-line loops for any loop that has to
    perform multiple complex actions on each iteration. Doing so will
    hurt the readability of your code and may ultimately lead to buggier
    code.

Let’s practice writing our own `for` loop!



**1.**

Run the code.

We should get an `IndentationError` because the `print(game)` line is
not indented.

**2.**

Indent (2 spaces or tab) line 6 so that we don’t get an
`IndentationError` when you run the code.

Run the code again!

**3.**

Write a `for` loop that prints each sport in the list `sport_games`.



``` python
board_games = ["Settlers of Catan", "Carcassone", "Power Grid", "Agricola", "Scrabble"]

sport_games = ["football", "hockey", "baseball", "cricket"]

for game in board_games:
  print(game)

for sport in sport_games:
  print(sport)
```

    ## Settlers of Catan
    ## Carcassone
    ## Power Grid
    ## Agricola
    ## Scrabble

    ## football
    ## hockey
    ## baseball
    ## cricket

## For Loops: Using Range

Often we won’t be iterating through a specific list (or any collection),
but rather only want to perform a certain action multiple times.

For example, if we wanted to print out a `"Learning Loops!"` message six
times using a `for` loop, we would follow this structure:

``` python
for <temporary variable> in <list of length 6>:
  print("Learning Loops!")
```

Notice that we need to iterate through a list with a length of six, but
we don’t necessarily care what is inside of the list.

To create arbitrary collections of any length, we can pair our `for`
loops with the trusty <a
href="https://www.codecademy.com/resources/docs/python/built-in-functions/range?page_ref=catalog"
class="e14vpv2g1 gamut-xro1w8-ResetElement-Anchor-AnchorBase e1bhhzie0"
target="_blank">Python built-in function <code
class="code__2rdF32qjRVp7mMVBHuPwDS">range()</code></a>.

An example of how the `range()` function works, this code generates a
collection of 6 integer elements from `0` to `5`:

``` python
six_steps = range(6)
 
# six_steps is now a collection with 6 elements:
# 0, 1, 2, 3, 4, 5
```

We can then use the range directly in our `for` loops as the collection
to perform a six-step iteration:

``` python
for temp in range(6):
  print("Learning Loops!")
```

Would output:

``` python
Learning Loops!
Learning Loops!
Learning Loops!
Learning Loops!
Learning Loops!
Learning Loops!
```

Something to note is we are not using `temp` anywhere inside of the loop
body. If we are curious about which loop iteration (step) we are on, we
can use `temp` to track it. Since our range starts at `0`, we will add
`+ 1` to our `temp` to represent how many iterations (steps) our loop
takes more accurately.

``` python
for temp in range(6):
  print("Loop is on iteration number " + str(temp + 1))
```

Would output:

``` python
Loop is on iteration number 1
Loop is on iteration number 2
Loop is on iteration number 3
Loop is on iteration number 4
Loop is on iteration number 5
Loop is on iteration number 6
```

Let’s try out using a range in a `for` loop!



**1.**

Use the `range()` function in a `for` loop to `print()` out the provided
`promise` variable five times.



``` python
promise = "I will finish the python loops module!"

for temp in range(5): 
  print(promise)
```

    ## I will finish the python loops module!
    ## I will finish the python loops module!
    ## I will finish the python loops module!
    ## I will finish the python loops module!
    ## I will finish the python loops module!

## While Loops: Introduction

In Python, `for` loops are not the only type of loops we can use.
Another type of loop is called a `while` loop and is a form of
indefinite iteration.

A `while` loop performs a set of instructions as long as a given
condition is true.

The structure follows this pattern:

``` python
while <conditional statement>:
  <action>
```

Let’s examine this example, where we print the integers `0` through `3`:

``` python
count = 0
while count <= 3:
  # Loop Body
  print(count)
  count += 1
```

Let’s break the loop down:

1.  `count` is initially defined with the value of `0`. The conditional
    statement in the `while` loop is `count <= 3`, which is true at the
    initial iteration of the loop, so the loop body executes.

    Inside the loop body, `count` is printed and then incremented by
    `1`.

2.  When the first iteration of the loop has finished, Python returns to
    the top of the loop and checks the conditional again. After the
    first iteration, `count` would be equal to `1` so the conditional
    still evaluates to `True` and so the loop continues.

3.  This continues until the `count` variable becomes `4`. At that
    point, when the conditional is tested it will no longer be `True`
    and the loop will stop.

The output would be:

``` python
0
1
2
3
```

Note the following about `while` loops before we write our own:

-   **Indentation:**

    Notice that in our example the code under the loop declaration is
    indented. Similar to a `for` loop, everything at the same level of
    indentation after the `while` loop declaration is run on every
    iteration of the loop while the condition is true.

    ``` python
    while count <= 3:
      # Loop Body
      print(count)
      count += 1
      # Any other code at this level of indentation will
      # run on each iteration
    ```

    If we ever forget to indent, we’ll get an `IndentationError` or
    unexpected behavior.

-   **Elegant loops:**

    Similar to `for` loops, Python allows us to write elegant one-line
    `while` loops. Here is our previous example in a single line:

    ``` python
    count = 0
    while count <= 3: print(count); count += 1
    ```

    **Note**: Here we separate each statement with a `;` to denote a
    separate line of code.

Let’s practice writing a `while` loop!



**1.**

Examine the `while` loop from the narrative in your code editor. There
are additional `print()` statements to help visualize the iterations.

Run the code to see what happens on each iteration of the loop. When you
are finished, comment out the example to make space for the rest of the
checkpoints.

To quickly comment out the code, use your cursor or mouse to highlight
all the code and press <span class="kbd">command ⌘</span> +
<span class="kbd">/</span> on a Mac or <span class="kbd">CTRL</span> +
<span class="kbd">/</span> on a Windows machine.

**2.**

Let’s write a `while` loop that counts down from `10` to `0`(inclusive).
Once our loop is finished we will commemorate our accomplishment by
printing `"We have liftoff!"`.

As we saw in the narrative, our key components will be:

1.  A variable to keep track of the count, and also help our loop
    eventually stop.

2.  A condition that our `while` loop will check on each iteration.

3.  Several code statements to execute on each iteration of the loop.

Let’s tackle the first component!

Create a variable named `countdown` and set the value to `10`.

**3.**

Now let’s tackle the actual `while` loop. Define a `while` loop that
will run while our `countdown` variable is greater than or equal to
zero.

On each iteration:

1.  We should `print()` the value of the `countdown` variable.
2.  We should decrease the value of the `countdown` variable by `1`

Make sure to *only* print the value of `countdown`.

If you notice the **Run** button spinning continuously or a “Lost
connection to Codecademy” message in an exercise, you may have an
infinite loop! If the stop condition for our loop is never met, we will
create an infinite loop which stops our program from running anything
else. To exit out of an infinite loop in an exercise, refresh the page —
then fix the code for your loop.

**4.**

Now that we have built our loop, let’s commemorate our success by
printing `"We have liftoff!"` after the `while` loop.



``` python
# While Loop Walkthrough
# count = 0
# print("Starting While Loop")
# while count <= 3:
#   # Loop Body
#   # Print if the condition is still true
#   print("Loop Iteration - count <= 3 is still true")
#   # Print the current value of count 
#   print("Count is currently " + str(count))
#   # Increment count
#   count += 1
#   print(" ----- ")
# print("While Loop ended")

# Your code below: 
countdown = 10
while countdown >= 0: 
  print(countdown)
  countdown -= 1 
print("We have liftoff!")
```

    ## 10
    ## 9
    ## 8
    ## 7
    ## 6
    ## 5
    ## 4
    ## 3
    ## 2
    ## 1
    ## 0

    ## We have liftoff!

## While Loops: Lists

A `while` loop isn’t only good for counting! Similar to how we saw `for`
loops working with lists, we can use `while` loops to iterate through a
<a
href="https://www.codecademy.com/resources/docs/python/lists?page_ref=catalog"
class="e14vpv2g1 gamut-xro1w8-ResetElement-Anchor-AnchorBase e1bhhzie0"
target="_blank">list</a> as well.

Let’s return to our ingredient list:

``` python
ingredients = ["milk", "sugar", "vanilla extract", "dough", "chocolate"]
```

We know that `while` loops require some form of a variable to track the
condition of the loop to start and stop.

Take some time to think about what we would use to track whether we need
to start/stop the loop if we want to iterate through `ingredients` and
print every element.

Click here to find out!

We know that a list has a predetermined length. If we use the length of
the list as the basis for how long our `while` loop needs to run, we can
iterate the exact length of the list.

We can use the <a
href="https://www.codecademy.com/resources/docs/python/built-in-functions/len?page_ref=catalog"
class="e14vpv2g1 gamut-xro1w8-ResetElement-Anchor-AnchorBase e1bhhzie0"
target="_blank">built-in Python <code
class="code__2rdF32qjRVp7mMVBHuPwDS">len()</code> function</a> to
accomplish this:

``` python
# Length would be equal to 5
length = len(ingredients)
```

We can then use this `length` in addition to another variable to
construct the `while` loop:

``` python
length = len(ingredients)
index = 0
 
while index < length:
  print(ingredients[index])
  index += 1
```

Let’s break this down:

``` python
# Length will be 5 in this case
length = len(ingredients)
```

Explanation

As mentioned, we need a way to know how many times we need our loop to
iterate based on the size of the collection.

This comes in the form of our `length` variable which stores the value
of the length of the list.

``` python
# Index starts at zero
index = 0
```

Explanation

We still need an additional variable that will be used to compare
against our `length`.

``` python
while index < length:
```

Explanation

In our `while` loop conditional, we will compare the `index` variable to
the length of our list stored inside of the `length` variable.

On the first iteration, we will be comparing the equivalent of `0 < 5`
which will evaluate to `True`, and start the execution of our loop body.

``` python
# The first iteration will print ingredients[0]
print(ingredients[index])
```

Explanation

Inside of our loop body, we can use the `index` variable to access our
`ingredients` list and print the value at the current iteration.

Since our `index` starts at zero, our first iteration will print the
value of the element at the zeroth index of our `ingredients` list, then
the next iteration will print the value of the element at the first
index, and so on.

``` python
# Increment index to access the next element in ingredients
# Each iteration gets closer to making the conditional no longer true
index += 1
```

Explanation

On each iteration of our `while` loop, we need to also increment the
value of `index` to make sure our loop can stop once the `index` value
is no longer smaller than the `length` value.

This increment also helps us access the next value of the `ingredients`
list on the next iteration.

Our final output would be:

``` python
milk
sugar
vanilla extract
dough
chocolate
```

Let’s use a `while` loop to iterate through some lists!



**1.**

We are going to write a `while` loop to iterate over the provided list
`python_topics`.

First, we will need a variable to represent the length of the list. This
will help us know how many times our `while` loop needs to iterate.

Create a variable `length` and set its value to be the length of the
list of `python_topics`.

**2.**

Next, we will require a variable to compare to our length variable to
make sure we are able to implement a condition that eventually allows
the loop to stop.

Create a variable called `index` and initialize the value to be `0`.

**3.**

Let’s now build our loop. We want our loop to iterate over the list of
`python_topics` and on each iteration print
`"I am learning about <element from python_topics>"`. For this loop we
will need the following components:

1.  A condition for our `while` loop
2.  A statement in the loop body to print from our condition
3.  A statement in the loop body to increment our index forward.

The end result should output:

``` python
I am learning about variables
I am learning about control flow
I am learning about loops
I am learning about modules
I am learning about classes
```

If you notice the **Run** button spinning continuously or a “Lost
connection to Codecademy” message in an exercise, you may have an
infinite loop! If the stop condition for our loop is never met, we will
create an infinite loop which stops our program from running anything
else. To exit out of an infinite loop in an exercise, refresh the page —
then fix the code for your loop.



``` python
python_topics = ["variables", "control flow", "loops", "modules", "classes"]

length = len(python_topics)
index = 0

while index < length:
  print("I am learning about " + python_topics[index])
  index += 1
```

    ## I am learning about variables
    ## I am learning about control flow
    ## I am learning about loops
    ## I am learning about modules
    ## I am learning about classes

## Infinite Loops

We’ve iterated through lists that have a discrete beginning and end.
However, let’s consider this example:

``` python
my_favorite_numbers = [4, 8, 15, 16, 42]
 
for number in my_favorite_numbers:
  my_favorite_numbers.append(1)
```

Take some time to ponder what happens with this code.

Click to see what would happen!

Every time we enter the loop, we add a `1` to the end of the list that
we are iterating through. As a result, we never make it to the end of
the list. It keeps growing forever!

A loop that never terminates is called an *infinite loop*. These are
very dangerous for our code because they will make our program run
forever and thus consume all of your computer’s resources.

A program that hits an infinite loop often becomes completely unusable.
The best course of action is to avoid writing an infinite loop.

**Note**: If you accidentally stumble into an infinite loop while
developing on your own machine, you can end the loop by using
<span class="kbd">control</span> + <span class="kbd">c</span> to
terminate the program. If you’re writing code in our online editor,
you’ll need to **refresh the page** to get out of an infinite loop.

Let’s fix an infinite loop to see it in action.



Suppose we have two lists of students, `students_period_A` and
`students_period_B`. We want to combine all students into
`students_period_B`.

In your code editor, we have provided you a loop. Go ahead and uncomment
line 5 and ***before you run the code*** ponder why this code would
cause an infinite loop.

When you are ready, run this code. What do you notice happens? Over the
run button, notice the loading circle is continuing without anything
happening.

This is an infinite loop! To end this program we must ***refresh the
page***. (Note: The reason this loop is infinite is that we’re adding
each student in `students_period_A` to `students_period_A` which would
create a never-ending list of all the student names.)

Open this after you refresh the page

Delete the line causing the infinite loop and fix it to accomplish the
original goal of combining all students from `students_period_A` into
`students_period_B`.



``` python
students_period_A = ["Alex", "Briana", "Cheri", "Daniele"]
students_period_B = ["Dora", "Minerva", "Alexa", "Obie"]

for student in students_period_A:
  students_period_B.append(student)
  print(student)
```

    ## Alex
    ## Briana
    ## Cheri
    ## Daniele

## Loop Control: Break

Loops in Python are very versatile. Python provides a set of control
statements that we can use to get even more control out of our loops.

Let’s take a look at a common scenario that we may encounter to see a
use case for *loop control statements*.

Take the following list `items_on_sale` as our example:

``` python
items_on_sale = ["blue shirt", "striped socks", "knit dress", "red headband", "dinosaur onesie"]
```

It’s often the case that we want to search a list to check if a specific
value exists. What does our loop look like if we want to search for the
value of `"knit dress"` and print out `"Found it"` if it did exist?

It would look something like this:

``` python
for item in items_on_sale:
  if item == "knit dress":
    print("Found it")
```

This code goes through each `item` in `items_on_sale` and checks for a
match. This is all fine and dandy but what’s the downside?

Once `"knit_dress"` is found in the list `items_on_sale`, we don’t need
to go through the rest of the `items_on_sale` list. Unfortunately, our
loop will keep running until we reach the end of the list.

Since it’s only 5 elements long, iterating through the entire list is
not a big deal in this case but what if `items_on_sale` had 1000 items?
What if it had 100,000 items? This would be a huge waste of time for our
program!

Thankfully you can stop iteration from inside the loop by using `break`
loop control statement.

When the program hits a `break` statement it immediately terminates a
loop. For example:

``` python
items_on_sale = ["blue shirt", "striped socks", "knit dress", "red headband", "dinosaur onesie"]
 
print("Checking the sale list!")
 
for item in items_on_sale:
  print(item)
  if item == "knit dress":
    break
 
print("End of search!")
```

This would produce the output:

``` python
Checking the sale list!
blue shirt
striped socks
knit dress
End of search!
```

When the loop entered the `if` statement and saw the `break` it
immediately ended the loop. We didn’t need to check the elements of
`"red headband"` or `"dinosaur onesie"` at all.

Now let’s `break` some loops!



**1.**

You have a list of dog breeds you can adopt,
`dog_breeds_available_for_adoption`.

Using a `for` loop, iterate through the
`dog_breeds_available_for_adoption` list and `print()` out each dog
breed.

Use the `<temporary variable>` name of `dog_breed` in your loop
declaration.

**2.**

Inside your for loop, after you print each dog breed, check if the
current element inside `dog_breed` is equal to `dog_breed_I_want`. If
so, print `"They have the dog I want!"`

**3.**

Add a `break` statement when your loop has found `dog_breed_I_want` so
that the rest of the list does not need to be checked once we have found
our breed.



``` python
dog_breeds_available_for_adoption = ["french_bulldog", "dalmatian", "shihtzu", "poodle", "collie"]
dog_breed_I_want = "dalmatian"

for dog_breed in dog_breeds_available_for_adoption:
  print(dog_breed)
  if dog_breed == dog_breed_I_want:
    print("They have the dog I want!")
    break
```

    ## french_bulldog
    ## dalmatian
    ## They have the dog I want!

## Loop Control: Continue

While the `break` control statement will come in handy, there are other
situations where we don’t want to end the loop entirely. What if we only
want to skip the current iteration of the loop?

Let’s take this list of integers as our example:

``` python
big_number_list = [1, 2, -1, 4, -5, 5, 2, -9]
```

What if we want to print out all of the numbers in a list, but only if
they are positive integers. We can use another common loop control
statement called `continue`.

``` python
for i in big_number_list:
  if i <= 0:
    continue
  print(i)
```

This would produce the output:

``` python
1
2
4
5
2
```

Notice a few things:

1.  Similar to when we were using the `break` control statement, our
    `continue` control statement is usually paired with some form of a
    conditional (`if`/`elif`/`else`).
2.  When our loop first encountered an element (`-1`) that met the
    conditions of the `if` statement, it checked the code inside the
    block and saw the `continue`. When the loop then encounters a
    `continue` statement it immediately skips the current iteration and
    moves onto the next element in the list (`4`).
3.  The output of the list only printed positive integers in the list
    because every time our loop entered the `if` statement and saw the
    `continue` statement it simply moved to the next iteration of the
    list and thus never reached the `print` statement.

Let’s `continue` learning about control statements with some exercises!



**1.**

Your computer is the doorman at a bar in a country where the drinking
age is 21.

Loop through the `ages` list. If an entry is less than `21`, skip it and
move to the next entry. Otherwise, `print()` the age.



``` python
ages = [12, 38, 34, 26, 21, 19, 67, 41, 17]

for age in ages:
  if age < 21:
    continue
  print(age)
```

    ## 38
    ## 34
    ## 26
    ## 21
    ## 67
    ## 41

## Nested Loops

Loops can be nested in Python, as they can with other programming
languages. We will find certain situations that require nested loops.

Suppose we are in charge of a science class, that is split into three
project teams:

``` python
project_teams = [["Ava", "Samantha", "James"], ["Lucille", "Zed"], ["Edgar", "Gabriel"]]
```

Using a for or while loop can be useful here to get each team:

``` python
for team in project_teams:
  print(team)
```

Would output:

``` python
["Ava", "Samantha", "James"]
["Lucille", "Zed"]
["Edgar", "Gabriel"]
```

But what if we wanted to print each individual student? In this case, we
would actually need to *nest* our loops to be able to loop through each
sub-list. Here is what it would look like:

``` python
# Loop through each sublist
for team in project_teams:
  # Loop elements in each sublist
  for student in team:
    print(student)
```

This would output:

``` python
Ava
Samantha
James
Lucille
Zed
Edgar
Gabriel
```

Let’s practice writing a nested loop!



**1.**

We have provided the list `sales_data` that shows the number of scoops
sold for different flavors of ice cream at three different locations:
Scoopcademy, Gilberts Creamery, and Manny’s Scoop Shop.

We want to sum up the total number of scoops sold across all three
locations. Start by defining a variable `scoops_sold` and set it to
zero.

**2.**

Loop through the `sales_data` list using the following guidelines:

1.  For our temporary variable of the for loop, call it `location`.
2.  `print()` out each `location` list.

**3.**

Within our `sales_data` loop, nest a secondary loop to go through each
`location` sublist element and add the element value to `scoops_sold`.

By the end, you should have the sum of every number in the `sales_data`
nested list.

**4.**

Print out the value of `scoops_sold` outside of the nested loop.



``` python
sales_data = [[12, 17, 22], [2, 10, 3], [5, 12, 13]]

scoops_sold = 0

for location in sales_data:
  print(location)
  for element in location:
    scoops_sold += element
    
print(scoops_sold)
```

    ## [12, 17, 22]
    ## [2, 10, 3]
    ## [5, 12, 13]

    ## 96

## List Comprehensions: Introduction

So far we have seen many of the ideas about using loops in our code.
Python prides itself on allowing programmers to write clean and elegant
code. We have already seen this with Python giving us the ability to
write `while` and `for` loops in a single line.

In this exercise, we are going to examine another way we can write
elegant loops in our programs using *list comprehensions*.

To start, let’s say we had a list of integers and wanted to create a
list where each element is doubled. We could accomplish this using a
`for` loop and a new list called `doubled`:

``` python
numbers = [2, -1, 79, 33, -45]
doubled = []
 
for number in numbers:
  doubled.append(number * 2)
 
print(doubled)
```

Would output:

``` python
[4, -2, 158, 66, -90]
```

Let’s see how we can use the power of list comprehensions to solve these
types of problems in one line. Here is our same problem but now written
as a list comprehension:

``` python
numbers = [2, -1, 79, 33, -45]
doubled = [num * 2 for num in numbers]
print(doubled)
```

Let’s break down our example in a more general way:

``` python
new_list = [<expression> for <element> in <collection>]
```

In our `doubled` example, our list comprehension:

1.  Takes an element in the list `numbers`
2.  Assigns that element to a variable called `num` (our `<element>`)
3.  Applies the `<expression>` on the element stored in `num` and adds
    the result to a new list called `doubled`
4.  Repeats steps 1-3 for every other element in the `numbers` list (our
    `<collection>`)

Our result would be the same:

``` python
[4, -2, 158, 66, -90]
```



**1.**

We have been provided a list of `grades` in a physics class. Using a
list comprehension, create a new list called `scaled_grades` that scales
the class grades based on the highest score.

Since the highest score was a `90` we simply want to add `10` points to
all the grades in the list.

**2.**

Print `scaled_grades`.



``` python
grades = [90, 88, 62, 76, 74, 89, 48, 57]

scaled_grades = [grade + 10 for grade in grades]

print(scaled_grades)
```

    ## [100, 98, 72, 86, 84, 99, 58, 67]

## List Comprehensions: Conditionals

List Comprehensions are very flexible. We even can expand our examples
to incorporate conditional logic.

Suppose we wanted to double only our negative numbers from our previous
`numbers` list.

We will start by using a `for` loop and a list `only_negative_doubled`:

``` python
numbers = [2, -1, 79, 33, -45]
only_negative_doubled = []
 
for num in numbers:
  if num < 0: 
    only_negative_doubled.append(num * 2)
 
print(only_negative_doubled) 
```

Would output:

``` python
[-2, -90]
```

Now, here is what our code would look like using a list comprehension:

``` python
numbers = [2, -1, 79, 33, -45]
negative_doubled = [num * 2 for num in numbers if num < 0]
print(negative_doubled)
```

Would output the same result:

``` python
[-2, -90]
```

In our `negative_doubled` example, our list comprehension:

1.  Takes an element in the list `numbers`.
2.  Assigns that element to a variable called `num`.
3.  Checks if the condition `num < 0` is met by the element stored in
    `num`. If so, it goes to step 4, otherwise it skips it and goes to
    the next element in the list.
4.  Applies the expression `num * 2` on the element stored in `num` and
    adds the result to a new list called `negative_doubled`
5.  Repeats steps 1-3 (and sometimes 4) for each remaining element in
    the `numbers` list.

We can also use If-Else conditions directly in our comprehensions. For
example, let’s say we wanted to double every negative number but triple
all positive numbers. Here is what our code might look like:

``` python
numbers = [2, -1, 79, 33, -45]
doubled = [num * 2 if num < 0 else num * 3 for num in numbers ]
print(doubled)
```

Would output:

``` python
[6, -2, 237, 99, -90]
```

**NOTE**: This is a bit different than our previous comprehension since
the conditional `if num < 0 else num * 3` comes after the expression
`num * 2` but before our `for` keyword. The placement of the conditional
expression within the comprehension is dependent on whether or not an
`else` clause is used. When an `if` statement is used without `else`,
the conditional must go after `for <element> in <collection>`. If the
conditional expression includes an `else` clause, the conditional must
go before `for`. Attempting to write the expressions in any other order
will result in a `SyntaxError`.

Here are a few list comprehensions in a single block. Take a moment to
compare how the syntax must change depending on whether or not an `else`
clause is included:

``` python
numbers = [2, -1, 79, 33, -45]
 
no_if   = [num * 2 for num in numbers]
if_only = [num * 2 for num in numbers if num < 0]
if_else = [num * 2 if num < 0 else num * 3 for num in numbers]
```

Now, let’s write our own list comprehensions with conditionals!



**1.**

We have defined a list `heights` of visitors to a theme park. In order
to ride the Topsy Turvy Tumbletron roller coaster, you need to be above
161 centimeters.

Using a list comprehension, create a new list called `can_ride_coaster`
that has every element from `heights` that is greater than `161`.

**2.**

Print `can_ride_coaster`.



``` python
heights = [161, 164, 156, 144, 158, 170, 163, 163, 157]

can_ride_coaster = [height for height in heights if height > 161]

print(can_ride_coaster)
```

    ## [164, 170, 163, 163]

## Review

Good job! In this lesson, you learned

-   How to write a `for` loop.
-   How to use `range` in a loop.
-   How to write a `while` loop.
-   What infinite loops are and how to avoid them.
-   How to control loops using `break` and `continue`.
-   How to write elegant loops as list comprehensions.

Let’s get some more practice with these concepts!



**1.**

Create a list called `single_digits` that consists of the numbers 0-9
(inclusive).

**2.**

Create a for loop that goes through `single_digits` and prints out each
one.

**3.**

Before the loop, create a list called `squares`. Assign it to be an
empty list to begin with.

**4.**

Inside the loop that iterates through `single_digits`, append the
squared value of each element of `single_digits` to the list `squares`.
You can do this before or after printing the element.

**5.**

After the for loop, print out `squares`.

**6.**

Create the list `cubes` using a list comprehension on the
`single_digits` list. Each element of `cubes` should be an element of
`single_digits` taken to the third power.

**7.**

Print `cubes`.

Good job!



``` python
single_digits = range(10)
squares = []

for item in single_digits:
  print(item)
  squares.append(item**2)
  
print(squares)
  
cubes = [item**3 for item in single_digits]
print(cubes)
```

    ## 0
    ## 1
    ## 2
    ## 3
    ## 4
    ## 5
    ## 6
    ## 7
    ## 8
    ## 9

    ## [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]

    ## [0, 1, 8, 27, 64, 125, 216, 343, 512, 729]

# Carly’s Clippers

You are the Data Analyst at Carly’s Clippers, the newest hair salon on
the block. Your job is to go through the lists of data that have been
collected in the past couple of weeks. You will be calculating some
important metrics that Carly can use to plan out the operation of the
business for the rest of the month.

You have been provided with three lists:

-   `hairstyles`: the names of the cuts offered at Carly’s Clippers.
-   `prices`: the price of each hairstyle in the `hairstyles` list.
-   `last_week`: the number of purchases for each hairstyle type in the
    last week.

Each index in `hairstyles` corresponds to an associated index in
`prices` and `last_week`.

For example, The hairstyle `"bouffant"` has an associated price of `30`
from the `prices` list, and was purchased `2` times in the last week as
shown in the `last_week` list. Each of these elements are in the first
index of their respective lists.

Let’s get started!

If you get stuck during this project or would like to see an experienced
developer work through it, click “**Get Unstuck**“ to see a **project
walkthrough video**.

## Instructions

Mark the tasks as complete by checking them off

### Prices and Cuts:

1\.

Carly wants to be able to market her low prices. We want to find out
what the average price of a cut is.

First, let’s sum up all the prices of haircuts. Create a variable
`total_price`, and set it to `0`.

2\.

Loop through the `prices` list and add each price to the variable
`total_price`.

3\.

After your loop, create a variable called `average_price` that is the
`total_price` divided by the number of prices.

You can get the number of prices by using the `len()` function.

4\.

Print the value of `average_price` so the output looks like:

``` python
Average Haircut Price: <average_price>
```

5\.

That average price is more expensive than Carly thought it would be! She
wants to cut all prices by 5 dollars.

Use a list comprehension to make a list called `new_prices`, which has
each element in `prices` minus `5`.

6\.

Print `new_prices`.

### Revenue:

7\.

Carly really wants to make sure that Carly’s Clippers is a profitable
endeavor. She first wants to know how much revenue was brought in last
week.

Create a variable called `total_revenue` and set it to `0`.

8\.

Use a `for` loop to create a variable `i` that goes from `0` to
`len(hairstyles)`

Hint: You can use `range()` to do this!

9\.

Add the product of `prices[i]` (the price of the haircut at position
`i`) and `last_week[i]` (the number of people who got the haircut at
position `i`) to `total_revenue` at each step.

10\.

After your loop, print the value of `total_revenue`, so the output looks
like:

``` python
Total Revenue: <total_revenue>
```

11\.

Find the average daily revenue by dividing `total_revenue` by 7. Call
this number `average_daily_revenue` and print it out.

12\.

Carly thinks she can bring in more customers by advertising all of the
haircuts she has that are under `30` dollars.

Use a list comprehension to create a list called `cuts_under_30` that
has the entry `hairstyles[i]` for each `i` for which `new_prices[i]` is
less than `30`.

You can use `range()` in your list comprehension to make `i` go from `0`
to `len(new_prices) - 1`.

13\.

Print `cuts_under_30`.

## Solution

``` python
hairstyles = ["bouffant", "pixie", "dreadlocks", "crew", "bowl", "bob", "mohawk", "flattop"]

prices = [30, 25, 40, 20, 20, 35, 50, 35]

last_week = [2, 3, 5, 8, 4, 4, 6, 2]

total_price = 0

for price in prices:
  total_price += price

average_price = total_price/len(prices)

print('Average Haircut Price: ' + str(average_price))

new_prices = [price - 5 for price in prices]

print(new_prices)

total_revenue = 0

for i in range(len(hairstyles)):
  total_revenue += prices[i] * last_week[i]

print('Total Revenue: ' + str(total_revenue))

average_daily_revenue = total_revenue/7
print(average_daily_revenue)

cuts_under_30 = [hairstyles[i] for i in range(len(hairstyles)) if new_prices[i] < 30]
print(cuts_under_30)
```

    ## Average Haircut Price: 31.875

    ## [25, 20, 35, 15, 15, 30, 45, 30]

    ## Total Revenue: 1085

    ## 155.0

    ## ['bouffant', 'pixie', 'crew', 'bowl']

# Creating Dictionaries

## Introduction to Python Dictionaries

A <a
href="https://www.codecademy.com/resources/docs/python/dictionaries?page_ref=catalog"
class="e14vpv2g1 gamut-xro1w8-ResetElement-Anchor-AnchorBase e1bhhzie0"
target="_blank"><em>dictionary</em></a> is an unordered set of
`key: value` pairs.

It provides us with a way to map pieces of data to each other so that we
can quickly find values that are associated with one another.

Suppose we want to store the prices of various items sold at a cafe:

-   Avocado Toast is 6 dollars
-   Carrot Juice is 5 dollars
-   Blueberry Muffin is 2 dollars

In Python, we can create a dictionary called `menu` to store this data:

``` python
menu = {"avocado toast": 6, "carrot juice": 5, "blueberry muffin": 2}
```

Notice that:

1.  A dictionary begins and ends with curly braces `{` and `}`.
2.  Each item consists of a key (`"avocado toast"`) and a value (`6`).
3.  Each `key: value` pair is separated by a comma.

It’s considered good practice to insert a space () after each comma, but
our code will still run without the space.



**1.**

Suppose we have a dictionary of temperature sensors in the house and
what temperatures they read. We’ve just added a sensor to the
`"pantry"`, and it reads 22 degrees.

Add this pair to the dictionary on line 1.

**2.**

Remove the `#` in front of the definition of the dictionary
`num_cameras`, which represents the number of cameras in each area
around the house.

If you run this code, you’ll get an error:

``` python
SyntaxError: invalid syntax
```

Try to find and fix the syntax error to make this code run.



``` python
sensors =  {"living room": 21, "kitchen": 23, "bedroom": 20, "pantry": 22}
num_cameras = {"backyard": 6,  "garage": 2, "driveway": 1}

print(sensors)
```

    ## {'living room': 21, 'kitchen': 23, 'bedroom': 20, 'pantry': 22}

## Make a Dictionary

In the previous exercise, we saw a dictionary that maps strings to
numbers (i.e., `"avocado toast": 6`). However, the keys can be numbers
as well.

For example, if we were mapping restaurant bill subtotals to the bill
total after tip, a dictionary could look like:

``` python
subtotal_to_total = {20: 24, 10: 12, 5: 6, 15: 18}
```

Values can be of any <a
href="https://www.codecademy.com/resources/docs/python/data-types?page_ref=catalog"
class="e14vpv2g1 gamut-xro1w8-ResetElement-Anchor-AnchorBase e1bhhzie0"
target="_blank">type</a>. We can use a string, a number, a list, or even
another dictionary as the value associated with a key!

For example:

``` python
students_in_classes = {"software design": ["Aaron", "Delila", "Samson"], "cartography": ["Christopher", "Juan", "Marco"], "philosophy": ["Frederica", "Manuel"]}
```

The list `["Aaron", "Delila", "Samson"]`, which is the value for the key
`"software design"`, represents the students in that class.

We can also mix and match key and value types. For example:

``` python
person = {"name": "Shuri", "age": 18, "family": ["T'Chaka", "Ramonda"]}
```



**1.**

Create a dictionary called `translations` that maps the following words
in English to their definitions in Sindarin (the language of the elves):

| English  | Sindarin |
|----------|----------|
| mountain | orod     |
| bread    | bass     |
| friend   | mellon   |
| horse    | roch     |



``` python
translations = {"mountain": "orod", "bread": "bass", "friend": "mellon", "horse": "roch"}
```

## Invalid Keys

We can have a list or a dictionary as a *value* of an item in a
dictionary, but we cannot use these data types as keys of the
dictionary. If we try to, we will get a `TypeError`.

For example:

``` python
powers = {[1, 2, 4, 8, 16]: 2, [1, 3, 9, 27, 81]: 3}
```

This code will yield:

``` python
TypeError: unhashable type: 'list'
```

The word “unhashable” in this context means that this ‘list’ is an
object that can be changed.

Dictionaries in Python rely on each key having a *hash value*, a
specific identifier for the key. If the key can change, that hash value
would not be reliable. So the keys must always be unchangeable, hashable
data types, like numbers or strings.



**1.**

Run the code inside **script.py**. You should get an error:

``` python
TypeError: unhashable type
```

Make the code run without errors by flipping the items in the dictionary
so that the strings are the keys and the lists are the values



``` python
children = {"von Trapp":["Johannes", "Rosmarie", "Eleonore"] , "Corleone":["Sonny", "Fredo", "Michael"]}
```

## Empty Dictionary

A dictionary doesn’t have to contain anything. Sometimes we need to
create an empty dictionary when we plan to fill it later based on some
other input.

We can create an empty dictionary like this:

``` python
empty_dict = {}
```

We will explore ways to fill a dictionary in the next exercise.



**1.**

Create an empty dictionary called `my_empty_dictionary`.



``` python
my_empty_dictionary = {}
```

## Add A Key

To add a single `key: value` pair to a dictionary, we can use the
syntax:

``` python
dictionary[key] = value
```

For example, if we had our `menu` dictionary from the first exercise:

``` python
menu = {"oatmeal": 3, "avocado toast": 6, "carrot juice": 5, "blueberry muffin": 2}
```

And we wanted to add a new item, `"cheesecake"` for `8` dollars, we
could use:

``` python
menu["cheesecake"] = 8
```

Now, `menu` looks like:

``` python
{"oatmeal": 3, "avocado toast": 6, "carrot juice": 5, "blueberry muffin": 2, "cheesecake": 8}
```



**1.**

Create an empty dictionary called `animals_in_zoo`.

**2.**

Walking around the zoo, you see 8 zebras. Add `"zebras"` to
`animals_in_zoo` as a key with a value of `8`.

**3.**

The primate house was bananas! Add `"monkeys"` to `animals_in_zoo` as a
key with a value of `12`.

**4.**

As you leave the zoo, you are saddened that you did not see any
dinosaurs. Add `"dinosaurs"` to `animals_in_zoo` as a key with a value
of `0`.

**5.**

Print `animals_in_zoo`.



``` python
animals_in_zoo = {}
animals_in_zoo['zebras'] = 8
animals_in_zoo['monkeys'] = 12
animals_in_zoo['dinosaurs'] = 0
print(animals_in_zoo)
```

    ## {'zebras': 8, 'monkeys': 12, 'dinosaurs': 0}

## Add Multiple Keys

If we wanted to add multiple key : value pairs to a dictionary at once,
we can use the <a
href="https://www.codecademy.com/resources/docs/python/dictionaries/update?page_ref=catalog"
class="e14vpv2g1 gamut-xro1w8-ResetElement-Anchor-AnchorBase e1bhhzie0"
target="_blank"><code
class="code__2rdF32qjRVp7mMVBHuPwDS">.update()</code></a> method.

Looking at our `sensors` object from a previous exercise:

``` python
sensors = {"living room": 21, "kitchen": 23, "bedroom": 20}
```

If we wanted to add 3 new rooms, we could use:

``` python
sensors.update({"pantry": 22, "guest room": 25, "patio": 34})
```

This would add all three items to the `sensors` dictionary.

Now, `sensors` looks like:

``` python
{"living room": 21, "kitchen": 23, "bedroom": 20, "pantry": 22, "guest room": 25, "patio": 34}
```



**1.**

In one line of code, add two new users to the `user_ids` dictionary:

-   `theLooper`, with an id of 138475
-   `stringQueen`, with an id of 85739

**2.**

Print `user_ids`.



``` python
user_ids = {"teraCoder": 9018293, "proProgrammer": 119238}
user_ids.update({"theLooper": 138475, "stringQueen": 85739})
print(user_ids)
```

    ## {'teraCoder': 9018293, 'proProgrammer': 119238, 'theLooper': 138475, 'stringQueen': 85739}

## Overwrite Values

We know that we can add a key by using the following syntax:

``` python
menu["banana"] = 3
```

This will create a key `"banana"` and set its value to `3`. But what if
we used a key that already has an entry in the `menu` dictionary?

In that case, our value assignment would overwrite the existing value
attached to that key. We can overwrite the value of `"oatmeal"` like
this:

``` python
menu = {"oatmeal": 3, "avocado toast": 6, "carrot juice": 5, "blueberry muffin": 2}
menu["oatmeal"] = 5
print(menu)
```

This would yield:

``` python
{"oatmeal": 5, "avocado toast": 6, "carrot juice": 5, "blueberry muffin": 2}
```

Notice the value of `"oatmeal"` has now changed to `5`.



**1.**

Add the key `"Supporting Actress"` and set the value to `"Viola Davis"`.

**2.**

Without changing the definition of the dictionary `oscar_winners`,
change the value associated with the key `"Best Picture"` to
`"Moonlight"`.



``` python
oscar_winners = {"Best Picture": "La La Land", "Best Actor": "Casey Affleck", "Best Actress": "Emma Stone", "Animated Feature": "Zootopia"}

oscar_winners["Supporting Actress"] = "Viola Davis"
oscar_winners["Best Picture"] = "Moonlight"
```

## Dict Comprehensions

Let’s say we have two lists that we want to combine into a dictionary,
like a list of students and a list of their heights, in inches:

``` python
names = ['Jenny', 'Alexus', 'Sam', 'Grace']
heights = [61, 70, 67, 64]
```

Python allows you to create a dictionary using a dict comprehension,
with this syntax:

``` python
students = {key:value for key, value in zip(names, heights)}
#students is now {'Jenny': 61, 'Alexus': 70, 'Sam': 67, 'Grace': 64}
```

Remember that <a
href="https://www.codecademy.com/resources/docs/python/built-in-functions/zip?page_ref=catalog"
class="e14vpv2g1 gamut-xro1w8-ResetElement-Anchor-AnchorBase e1bhhzie0"
target="_blank"><code
class="code__2rdF32qjRVp7mMVBHuPwDS">zip()</code></a> combines two lists
into an iterator of tuples with the list elements paired together. This
dict comprehension:

1.  Takes a pair from the iterator of tuples
2.  Names the elements in the pair `key` (the one originally from the
    `names` list) and `value` (the one originally from the `heights`
    list)
3.  Creates a `key` : `value` item in the `students` dictionary
4.  Repeats steps 1-3 for the entire iterator of pairs



**1.**

You have two lists, representing some drinks sold at a coffee shop and
the milligrams of caffeine in each. First, create a variable called
`zipped_drinks` that is an iterator of pairs between the `drinks` list
and the `caffeine` list.

**2.**

Create a dictionary called `drinks_to_caffeine` by using a dict
comprehension that goes through the `zipped_drinks` iterator and turns
each tuple pair into a key:value item.



``` python
drinks = ["espresso", "chai", "decaf", "drip"]
caffeine = [64, 40, 0, 120]
zipped_drinks = zip(drinks, caffeine)
drinks_to_caffeine = {key: value for key, value in zipped_drinks}
```

## Review

So far we have learned:

-   How to create a dictionary
-   How to add elements to a dictionary
-   How to update elements in a dictionary
-   How to use a dict comprehension to create a dictionary from two
    lists

Let’s practice these skills!



**1.**

We are building a music streaming service. We have provided two lists,
representing songs in a user’s library and the amount of times each song
has been played.

Using a dict comprehension, create a dictionary called `plays` that goes
through `zip(songs, playcounts)` and creates a `song`:`playcount` pair
for each `song` in `songs` and each `playcount` in `playcounts`.

**2.**

Print `plays`.

**3.**

After printing `plays`, add a new entry to it. The entry should be for
the song `"Purple Haze"` and the playcount is `1`.

**4.**

This user has caught Aretha Franklin fever and listened to “Respect” 5
more times. Update the value for `"Respect"` to be 94 in the `plays`
dictionary.

**5.**

Create a dictionary called `library` that has two key: value pairs:

-   key `"The Best Songs"` with a value of `plays`, the dictionary you
    created
-   key `"Sunday Feelings"` with a value of an empty dictionary

**6.**

Print `library`.



``` python
songs = ["Like a Rolling Stone", "Satisfaction", "Imagine", "What's Going On", "Respect", "Good Vibrations"]
playcounts = [78, 29, 44, 21, 89, 5]

plays = {song:playcount for [song, playcount] in zip(songs, playcounts)}

plays["Respect"] = 94
plays["Purple Haze"] = 1

library = {"The Best Songs": plays, "Sunday Feelings": {}}

print(library)
```

    ## {'The Best Songs': {'Like a Rolling Stone': 78, 'Satisfaction': 29, 'Imagine': 44, "What's Going On": 21, 'Respect': 94, 'Good Vibrations': 5, 'Purple Haze': 1}, 'Sunday Feelings': {}}

# Using Dictionaries

## Using Dictionaries

Now that we know how to create a dictionary, we can start using already
created dictionaries to solve problems.

In this lesson, you’ll learn how to:

-   Use a key to get a value from a dictionary
-   Check for existence of keys
-   Iterate through keys and values in dictionaries

## Get A Key

Once you have a dictionary, you can access the values in it by providing
the key. For example, let’s imagine we have a dictionary that maps
buildings to their heights, in meters:

``` python
building_heights = {"Burj Khalifa": 828, "Shanghai Tower": 632, "Abraj Al Bait": 601, "Ping An": 599, "Lotte World Tower": 554.5, "One World Trade": 541.3}
```

Then we can access the data in it like this:

``` python
>>> building_heights["Burj Khalifa"]
828
>>> building_heights["Ping An"]
599
```



**1.**

We have provided a dictionary that maps the elements of astrology to the
zodiac signs. Print out the list of zodiac signs associated with the
`"earth"` element.

**2.**

Print out the list of the `"fire"` signs.



``` python
zodiac_elements = {"water": ["Cancer", "Scorpio", "Pisces"], "fire": ["Aries", "Leo", "Sagittarius"], "earth": ["Taurus", "Virgo", "Capricorn"], "air":["Gemini", "Libra", "Aquarius"]}

print(zodiac_elements['earth'])
print(zodiac_elements['fire'])
```

    ## ['Taurus', 'Virgo', 'Capricorn']

    ## ['Aries', 'Leo', 'Sagittarius']

## Get an Invalid Key

Let’s say we have our dictionary of building heights from the last
exercise:

``` python
building_heights = {"Burj Khalifa": 828, "Shanghai Tower": 632, "Abraj Al Bait": 601, "Ping An": 599, "Lotte World Tower": 554.5, "One World Trade": 541.3}
```

What if we wanted to know the height of the Landmark 81 in Ho Chi Minh
City? We could try:

``` python
print(building_heights["Landmark 81"])
```

But `"Landmark 81"` does not exist as a key in the `building_heights`
dictionary! So this will throw a KeyError:

``` python
KeyError: 'Landmark 81'
```

One way to avoid this error is to first check if the key exists in the
dictionary:

``` python
key_to_check = "Landmark 81"
 
if key_to_check in building_heights:
  print(building_heights["Landmark 81"])
```

This will not throw an error, because `key_to_check in building_heights`
will return `False`, and so we never try to access the key.



**1.**

Review the code in the editor and predict what the output will be. Run
the code to see if you are correct!

**2.**

Because `"energy"` is not a key in `zodiac_elements`, a `KeyError` is
thrown in the terminal!

Using an `if` statement, check if `"energy"` is a key in
`zodiac_elements`. Nest the existing `print()` statement within the `if`
statement so that it will only execute if `"energy"` is a key.

Run your code again. This time, there should be no errors in the
terminal!

**3.**

Add the key `"energy"` to the `zodiac_elements`. It should map to a
value of `"Not a Zodiac element"`. Run the code. Since `"energy"` is now
a key, its value prints to the terminal!



``` python
zodiac_elements = {"water": ["Cancer", "Scorpio", "Pisces"], "fire": ["Aries", "Leo", "Sagittarius"], "earth": ["Taurus", "Virgo", "Capricorn"], "air":["Gemini", "Libra", "Aquarius"]}

zodiac_elements["energy"] = "Not a Zodiac element"

if "energy" in zodiac_elements:
  print(zodiac_elements["energy"])
```

    ## Not a Zodiac element

## Safely Get a Key

We saw in the last exercise that we had to add a key:value pair to a
dictionary in order to avoid a KeyError. This solution is not
sustainable. We can’t predict every key a user may call and add all of
those placeholder values to our dictionary!

Dictionaries have a `.get()` method to search for a value instead of the
`my_dict[key]` notation we have been using. If the key you are trying to
`.get()` does not exist, it will return `None` by default:

``` python
building_heights = {"Burj Khalifa": 828, "Shanghai Tower": 632, "Abraj Al Bait": 601, "Ping An": 599, "Lotte World Tower": 554.5, "One World Trade": 541.3}
 
#this line will return 632:
building_heights.get("Shanghai Tower")
 
#this line will return None:
building_heights.get("My House")
```

You can also specify a value to return if the key doesn’t exist. For
example, we might want to return a building height of 0 if our desired
building is not in the dictionary:

``` python
>>> building_heights.get('Shanghai Tower', 0)
632
>>> building_heights.get('Mt Olympus', 0)
0
>>> building_heights.get('Kilimanjaro', 'No Value')
'No Value'
```



**1.**

Use `.get()` to get the value of `"teraCoder"`’s user ID, with `100000`
as a default value if the user doesn’t exist. Store it in a variable
called `tc_id`. Print `tc_id` to the console.

**2.**

Use `.get()` to get the value of `"superStackSmash"`’s user ID, with
`100000` as a default value if the user doesn’t exist. Store it in a
variable called `stack_id`. Print `stack_id` to the console.



``` python
user_ids = {"teraCoder": 100019, "pythonGuy": 182921, "samTheJavaMaam": 123112, "lyleLoop": 102931, "keysmithKeith": 129384}

tc_id = user_ids.get("teraCoder", 100000)
stack_id = user_ids.get("superStackSmash", 100000)

print(tc_id)
print(stack_id)
```

    ## 100019

    ## 100000

## Delete a Key

Sometimes we want to get a key and remove it from the dictionary.
Imagine we were running a raffle, and we have this dictionary mapping
ticket numbers to prizes:

``` python
raffle = {223842: "Teddy Bear", 872921: "Concert Tickets", 320291: "Gift Basket", 412123: "Necklace", 298787: "Pasta Maker"}
```

When we get a ticket number, we want to return the prize and also remove
that pair from the dictionary, since the prize has been given away. We
can use `.pop()` to do this. Just like with `.get()`, we can provide a
default value to return if the key does not exist in the dictionary:

``` python
>>> raffle.pop(320291, "No Prize")
"Gift Basket"
>>> raffle
{223842: "Teddy Bear", 872921: "Concert Tickets", 412123: "Necklace", 298787: "Pasta Maker"}
>>> raffle.pop(100000, "No Prize")
"No Prize"
>>> raffle
{223842: "Teddy Bear", 872921: "Concert Tickets", 412123: "Necklace", 298787: "Pasta Maker"}
>>> raffle.pop(872921, "No Prize")
"Concert Tickets"
>>> raffle
{223842: "Teddy Bear", 412123: "Necklace", 298787: "Pasta Maker"}
```

`.pop()` works to delete items from a dictionary, when you know the key
value.



**1.**

You are designing the video game Big Rock Adventure. We have provided a
dictionary of items that are in the player’s inventory which add points
to their health meter. In one line, add the corresponding value of the
key `"stamina grains"` to the `health_points` variable and remove the
item `"stamina grains"` from the dictionary. If the key does not exist,
add 0 to `health_points`.

**2.**

In one line, add the value of `"power stew"` to `health_points` and
remove the item from the dictionary. If the key does not exist, add 0 to
`health_points`.

**3.**

In one line, add the value of `"mystic bread"` to `health_points` and
remove the item from the dictionary. If the key does not exist, add 0 to
`health_points`.

**4.**

Print `available_items` and `health_points`.



``` python
available_items = {"health potion": 10, "cake of the cure": 5, "green elixir": 20, "strength sandwich": 25, "stamina grains": 15, "power stew": 30}
health_points = 20

health_points += available_items.pop("stamina grains", 0)
health_points += available_items.pop("power stew", 0)
health_points += available_items.pop("mystic bread", 0)

print(available_items)
print(health_points)
```

    ## {'health potion': 10, 'cake of the cure': 5, 'green elixir': 20, 'strength sandwich': 25}

    ## 65

## Get All Keys

Sometimes we want to operate on all of the keys in a dictionary. For
example, if we have a dictionary of students in a math class and their
grades:

``` python
test_scores = {"Grace":[80, 72, 90], "Jeffrey":[88, 68, 81], "Sylvia":[80, 82, 84], "Pedro":[98, 96, 95], "Martin":[78, 80, 78], "Dina":[64, 60, 75]}
```

We want to get a roster of the students in the class, without including
their grades. We can do this with the built-in `list()` function:

``` python
>>> list(test_scores)
["Grace", "Jeffrey", "Sylvia", "Pedro", "Martin", "Dina"]
```

Dictionaries also have a `.keys()` method that returns a `dict_keys`
object. A `dict_keys` object is a *view* object, which provides a look
at the current state of the dictionary, without the user being able to
modify anything. The `dict_keys` object returned by `.keys()` is a set
of the keys in the dictionary. You cannot add or remove elements from a
`dict_keys` object, but it can be used in the place of a list for
iteration:

``` python
for student in test_scores.keys():
  print(student)
```

will yield:

``` python
Grace
Jeffrey
Sylvia
Pedro
Martin
Dina
```



**1.**

Create a variable called `users` and assign it to be a `dict_keys`
object of all of the keys of the `user_ids` dictionary.

**2.**

Create a variable called `lessons` and assign it to be a `dict_keys`
object of all of the keys of the `num_exercises` dictionary.

**3.**

Print `users` to the console.

**4.**

Print `lessons` to the console.



``` python
user_ids = {"teraCoder": 100019, "pythonGuy": 182921, "samTheJavaMaam": 123112, "lyleLoop": 102931, "keysmithKeith": 129384}
num_exercises = {"functions": 10, "syntax": 13, "control flow": 15, "loops": 22, "lists": 19, "classes": 18, "dictionaries": 18}

users = user_ids.keys()
lessons = num_exercises.keys()

print(users)
print(lessons)
```

    ## dict_keys(['teraCoder', 'pythonGuy', 'samTheJavaMaam', 'lyleLoop', 'keysmithKeith'])

    ## dict_keys(['functions', 'syntax', 'control flow', 'loops', 'lists', 'classes', 'dictionaries'])

## Get All Values

Dictionaries have a `.values()` method that returns a `dict_values`
object (just like a `dict_keys` object but for values!) with all of the
values in the dictionary. It can be used in the place of a list for
iteration:

``` python
test_scores = {"Grace":[80, 72, 90], "Jeffrey":[88, 68, 81], "Sylvia":[80, 82, 84], "Pedro":[98, 96, 95], "Martin":[78, 80, 78], "Dina":[64, 60, 75]}
 
for score_list in test_scores.values():
  print(score_list)
```

will yield:

``` python
[80, 72, 90]
[88, 68, 81]
[80, 82, 84]
[98, 96, 95]
[78, 80, 78]
[64, 60, 75]
```

There is no built-in function to get all of the values as a list, but if
you *really* want to, you can use:

``` python
list(test_scores.values())
```

However, for most purposes, the `dict_values` object will act the way
you want a list to act.



**1.**

Create a variable called `total_exercises` and set it equal to 0.

**2.**

Iterate through the values in the `num_exercises` list and add each
value to the `total_exercises` variable.

**3.**

Print the `total_exercises` variable to the console.



``` python
num_exercises = {"functions": 10, "syntax": 13, "control flow": 15, "loops": 22, "lists": 19, "classes": 18, "dictionaries": 18}

total_exercises = 0

for exercises in num_exercises.values():
  total_exercises += exercises
print(total_exercises)
```

    ## 115

## Get All Items

You can get both the keys and the values with the `.items()` method.
Like `.keys()` and `.values()`, it returns a `dict_list` object. Each
element of the `dict_list` returned by `.items()` is a tuple consisting
of:

``` python
(key, value)
```

so to iterate through, you can use this syntax:

``` python
biggest_brands = {"Apple": 184, "Google": 141.7, "Microsoft": 80, "Coca-Cola": 69.7, "Amazon": 64.8}
 
for company, value in biggest_brands.items():
  print(company + " has a value of " + str(value) + " billion dollars. ")
```

which would yield this output:

``` python
Apple has a value of 184 billion dollars.
Google has a value of 141.7 billion dollars.
Microsoft has a value of 80 billion dollars.
Coca-Cola has a value of 69.7 billion dollars.
Amazon has a value of 64.8 billion dollars.
```



**1.**

Use a for loop to iterate through the items of
`pct_women_in_occupation`. For each key : value pair, print out a string
that looks like:

``` python
Women make up [value] percent of [key]s.
```



``` python
pct_women_in_occupation = {"CEO": 28, "Engineering Manager": 9, "Pharmacist": 58, "Physician": 40, "Lawyer": 37, "Aerospace Engineer": 9}

for occupation, percentage in pct_women_in_occupation.items():
  print("Women make up " + str(percentage) + " percent of " + occupation + "s.") 
```

    ## Women make up 28 percent of CEOs.
    ## Women make up 9 percent of Engineering Managers.
    ## Women make up 58 percent of Pharmacists.
    ## Women make up 40 percent of Physicians.
    ## Women make up 37 percent of Lawyers.
    ## Women make up 9 percent of Aerospace Engineers.

## Review

In this lesson, you’ve learned how to go through dictionaries and access
keys and values in different ways. Specifically, you have seen how to:

-   Use a key to get a value from a dictionary
-   Check for existence of keys
-   Remove a key: value pair from a dictionary
-   Iterate through keys and values in dictionaries



**1.**

We have provided a pack of tarot cards, `tarot`. You are going to do a
three card spread of your past, present, and future.

Create an empty dictionary called `spread`.

**2.**

The first card you draw is card 13. Pop the value assigned to the key
`13` out of the `tarot` dictionary and assign it as the value of the
`"past"` key of `spread`.

**3.**

The second card you draw is card 22. Pop the value assigned to the key
`22` out of the `tarot` dictionary and assign it as the value of the
`"present"` key of `spread`.

**4.**

The third card you draw is card 10. Pop the value assigned to the key
`10` out of the `tarot` dictionary and assign it as the value of the
`"future"` key of `spread`.

**5.**

Iterate through the items in the `spread` dictionary and for each key:
value pair, print out a string that says:

``` python
Your {key} is the {value} card.
```

**6.**

Congratulations! You have learned about how to modify and use
dictionaries.  
Hit the `Run` button one more time when you are ready to continue.



``` python
tarot = { 1:    "The Magician", 2:  "The High Priestess", 3:    "The Empress", 4:   "The Emperor", 5:   "The Hierophant", 6:    "The Lovers", 7:    "The Chariot", 8:   "Strength", 9:  "The Hermit", 10:   "Wheel of Fortune", 11: "Justice", 12:  "The Hanged Man", 13:   "Death", 14:    "Temperance", 15:   "The Devil", 16:    "The Tower", 17:    "The Star", 18: "The Moon", 19: "The Sun", 20:  "Judgement", 21:    "The World", 22: "The Fool"}

spread = {}

spread["past"] = tarot.pop(13)
spread["present"] = tarot.pop(22)
spread["future"] = tarot.pop(10)

for key, value in spread.items():
  print("Your "+key+" is the "+value+" card. ")
```

    ## Your past is the Death card. 
    ## Your present is the The Fool card. 
    ## Your future is the Wheel of Fortune card.

# Scrabble

In this project, you will process some data from a group of friends
playing scrabble. You will use dictionaries to organize players, words,
and points.

There are many ways you can extend this project on your own if you
finish and want to get more practice!

If you get stuck during this project or would like to see an experienced
developer work through it, click “**Get Unstuck**“ to see a **project
walkthrough video**.

## Instructions

Mark the tasks as complete by checking them off

### Build your Point Dictionary

1\.

We have provided you with two lists, `letters` and `points`. We would
like to combine these two into a dictionary that would map a letter to
its point value.

Using a list comprehension and `zip`, create a dictionary called
`letter_to_points` that has the elements of `letters` as the keys and
the elements of `points` as the values.

2\.

Our `letters` list did not take into account blank tiles. Add an element
to the `letter_to_points` dictionary that has a key of `" "` and a point
value of `0`.

### Score a Word

3\.

We want to create a function that will take in a word and return how
many points that word is worth.

Define a function called `score_word` that takes in a parameter `word`.

4\.

Inside `score_word`, create a variable called `point_total` and set it
to `0`.

5\.

After defining `point_total`, create a for loop that goes through the
letters in `word` and adds the point value of each letter to
`point_total`.

You should get the point value from the `letter_to_points` dictionary.
If the letter you are checking for is not in `letter_to_points`, add 0
to the `point_total`.

6\.

After the for loop is finished, return `point_total`.

7\.

Let’s test this function! Create a variable called `brownie_points` and
set it equal to the value returned by the `score_word()` function with
an input of `"BROWNIE"`.

8\.

We expect the word BROWNIE to earn 15 points:

``` python
(B + R + O + W + N + I + E)
 
(3 + 1 + 1 + 4 + 4 + 1 + 1) = 15
```

Let’s print out `brownie_points` to make sure we got it right.

### Score a Game

9\.

Create a dictionary called `player_to_words` that maps players to a list
of the words they have played. This table represents the data to
transcribe into your dictionary:

| player1 | wordNerd | Lexi Con | Prof Reader |
|---------|----------|----------|-------------|
| BLUE    | EARTH    | ERASER   | ZAP         |
| TENNIS  | EYES     | BELLY    | COMA        |
| EXIT    | MACHINE  | HUSKY    | PERIOD      |

10\.

Create an empty dictionary called `player_to_points`.

11\.

Iterate through the items in `player_to_words`. Call each player
`player` and each list of words `words`.

Within your loop, create a variable called `player_points` and set it to
0.

12\.

Within the loop, create another loop that goes through each `word` in
`words` and adds the value of `score_word()` with `word` as an input.

13\.

After the inner loop ends, set the current `player` value to be a key of
`player_to_points`, with a value of `player_points`.

14\.

`player_to_points` should now contain the mapping of players to how many
points they’ve scored. Print this out to see the current standings for
this game!

If you’ve calculated correctly, wordNerd should be winning by 1 point.

### Ideas for Further Practice!

15\.

If you want extended practice, try to implement some of these ideas with
the Python you’ve learned:

-   `play_word()` — a function that would take in a player and a word,
    and add that word to the list of words they’ve played
-   `update_point_totals()` — turn your nested loops into a function
    that you can call any time a word is played
-   make your `letter_to_points` dictionary able to handle lowercase
    inputs as well

## Solution

``` python
letters = ["A", "B", "C", "D", "E", "F", "G", "H", "I", "J", "K", "L", "M", "N", "O", "P", "Q", "R", "S", "T", "U", "V", "W", "X", "Y", "Z"]
points = [1, 3, 3, 2, 1, 4, 2, 4, 1, 8, 5, 1, 3, 4, 1, 3, 10, 1, 1, 1, 1, 4, 4, 8, 4, 10]

letters_to_points = {
  key: value
  for key, value
  in zip(letters, points)
  }

letters_to_points[" "] = 0

def score_word(word):
  point_total = 0
  for letter in word.upper():
    point_total += letters_to_points.get(letter,0)
  return point_total

brownie_points = score_word("BROWNIE")
print(brownie_points)

player_to_words = {
  "player1" : ["BLUE", "TENNIS", "EXIT"],
  "wordNerd" : ["EARTH", "EYES", "MACHINE"],
  "Lexi Con" : ["ERASER", "BELLY", "HUSKY"],
  "Prof Reader": ["ZAP", "COMA", "PERIOD"]
}

player_to_points = {}

for player, words in player_to_words.items():
  player_points = 0
  for word in words:
    player_points += score_word(word)
  player_to_points[player]= player_points

print(player_to_points)
```

    ## 15

    ## {'player1': 29, 'wordNerd': 32, 'Lexi Con': 31, 'Prof Reader': 31}

# Off-Platform Project: Abruptly Goblins

In this off-platform project you will be the proprietor of a comic and
games store, the Sorcery Society, and you decide to host a game night to
play the hot new tabletop RPG Abruptly Goblins! You’ll be writing your
own Python functions and using dictionaries to provide a new service to
gaming attendees of your shop.

Your beloved clientele want to organize a game night at your comics
store! Create a system for organizing and tracking gamer’s availability.
Programmatically figure out the best day to host a game night and send
out emails to your attendees to let them know when to come. Follow the
steps below to get started with your project!

#### Working on Your Computer

1.  If you’ve never used the command line, we recommend taking the
    <a href="https://www.codecademy.com/learn/learn-the-command-line"
    class="e14vpv2g1 gamut-xro1w8-ResetElement-Anchor-AnchorBase e1bhhzie0"
    target="_blank">Learn the Command Line course</a>.

2.  Install Python by following the directions in this article on
    <a href="https://www.codecademy.com/articles/install-python3"
    class="e14vpv2g1 gamut-xro1w8-ResetElement-Anchor-AnchorBase e1bhhzie0"
    target="_blank">Installing Python</a>.

3.  Learn about <a
    href="https://www.codecademy.com/articles/how-to-use-jupyter-notebooks-py3"
    class="e14vpv2g1 gamut-xro1w8-ResetElement-Anchor-AnchorBase e1bhhzie0"
    target="_blank">Jupyter Notebooks</a>, a cool way of combining
    Python code with explanations or instruction in a web terminal.

4.  Download the <a
    href="https://content.codecademy.com/programs/programming-with-python/Abruptly%20Goblins.zip"
    class="e14vpv2g1 gamut-xro1w8-ResetElement-Anchor-AnchorBase e1bhhzie0"
    target="_blank" rel="noopener">Abruptly Goblins project</a>.

5.  Unzip it by double-clicking on it.

6.  In the terminal, navigate to the directory containing the project,
    and type:

    ``` bash
    jupyter notebook
    ```

    This should open a browser tab.

7.  Click on `Abruptly Goblins Planner.ipynb` in the browser tab. This
    will open up your Jupyter Notebook.

8.  Follow the steps in the Jupyter Notebook. If you get stuck, you can
    look at `Abruptly Goblins Planner (Solution).ipynb` for the answer.

# Introduction to Classes

## Types

Python equips us with many different ways to store data. A `float` is a
different kind of number from an `int`, and we store different data in a
`list` than we do in a `dict`. These are known as different *types*. We
can check the type of a Python variable using the <a
href="https://www.codecademy.com/resources/docs/python/built-in-functions/type?page_ref=catalog"
class="e14vpv2g1 gamut-xro1w8-ResetElement-Anchor-AnchorBase e1bhhzie0"
target="_blank"><code
class="code__2rdF32qjRVp7mMVBHuPwDS">type()</code></a> function.

``` python
a_string = "Cool String"
an_int = 12
 
print(type(a_string))
# prints "<class 'str'>"
 
print(type(an_int))
# prints "<class 'int'>"
```

Above, we defined two variables, and checked the `type` of these two
variables. A variable’s type determines what you can do with it and how
you can use it. You can’t `.get()` something from an integer, just as
you can’t add two dictionaries together using `+`. This is because those
operations are defined at the `type` level.



**1.**

Call `type()` on the integer `5` and print the results.

**2.**

Define a dictionary `my_dict`.

**3.**

Print out the `type()` of `my_dict`.

**4.**

Define a list called `my_list`.

**5.**

Print out the `type()` of `my_list`.



``` python
print(type(5))

my_dict = {}
print(type(my_dict))

my_list = []
print(type(my_list))
```

    ## <class 'int'>

    ## <class 'dict'>

    ## <class 'list'>

## Class

A <a
href="https://www.codecademy.com/resources/docs/python/classes?page_ref=catalog"
class="e14vpv2g1 gamut-xro1w8-ResetElement-Anchor-AnchorBase e1bhhzie0"
target="_blank"><em>class</em></a> is a template for a data type. It
describes the kinds of information that class will hold and how a
programmer will interact with that data. Define a class using the <a
href="https://www.codecademy.com/resources/docs/python/keywords/class?page_ref=catalog"
class="e14vpv2g1 gamut-xro1w8-ResetElement-Anchor-AnchorBase e1bhhzie0"
target="_blank"><code
class="code__2rdF32qjRVp7mMVBHuPwDS">class</code></a> keyword.
<a href="https://www.python.org/dev/peps/pep-0008/#class-names"
class="e14vpv2g1 gamut-xro1w8-ResetElement-Anchor-AnchorBase e1bhhzie0"
target="_blank" rel="noopener">PEP 8 Style Guide for Python Code</a>
recommends capitalizing the names of classes to make them easier to
identify.

``` python
class CoolClass:
  pass
```

In the above example we created a class and named it `CoolClass`. We
used the `pass` keyword in Python to indicate that the body of the class
was intentionally left blank so we don’t cause an `IndentationError`.
We’ll learn about all the things we can put in the body of a class in
the next few exercises.



**1.**

Define an empty class called `Facade`. We’ll chip away at it soon!



``` python
class Facade:
  pass
```

## Instantiation

A class doesn’t accomplish anything simply by being defined. A class
must be *instantiated*. In other words, we must create an *instance* of
the class, in order to breathe life into the schematic.

Instantiating a class looks a lot like calling a function. We would be
able to create an instance of our defined `CoolClass` as follows:

``` python
cool_instance = CoolClass()
```

Above, we created an object by adding parentheses to the name of the
class. We then assigned that new instance to the variable
`cool_instance` for safe-keeping so we can access our instance of
`CoolClass` at a later time.



**1.**

In **script.py** we see our `Facade` class from last exercise. Make a
`Facade` instance and save it to the variable `facade_1`.



``` python
class Facade:
  pass

facade_1 = Facade()
```

## Object-Oriented Programming

A class instance is also called an *object*. The pattern of defining
classes and creating objects to represent the responsibilities of a
program is known as <a
href="https://www.codecademy.com/resources/docs/general/programming-paradigms/object-oriented-programming?page_ref=catalog"
class="e14vpv2g1 gamut-xro1w8-ResetElement-Anchor-AnchorBase e1bhhzie0"
target="_blank"><em>Object Oriented Programming</em></a> or OOP.

Instantiation takes a class and turns it into an object, the `type()`
function does the opposite of that. When called with an object, it
returns the class that the object is an instance of.

``` python
print(type(cool_instance))
# prints "<class '__main__.CoolClass'>"
```

We then print out the `type() of cool_instance` and it shows us that
this object is of type `__main__.CoolClass`.

In Python `__main__` means “this current file that we’re running” and so
one could read the output from `type()` to mean “the class `CoolClass`
that was defined here, in the script you’re currently running.”



**1.**

In **script.py** we see `facade_1` from last exercise. Try calling
`type()` on `facade_1` and saving it to the variable `facade_1_type`.

**2.**

Print out `facade_1_type`.



``` python
class Facade:
  pass

facade_1 = Facade()

facade_1_type = type(facade_1)
print(facade_1_type)
```

    ## <class '__main__.Facade'>

## Class Variables

When we want the same data to be available to every instance of a class
we use a *class variable*. A class variable is a variable that’s the
same for every instance of the class.

You can define a class variable by including it in the indented part of
your class definition, and you can access all of an object’s class
variables with `object.variable` syntax.

``` python
class Musician:
  title = "Rockstar"
 
drummer = Musician()
print(drummer.title)
# prints "Rockstar"
```

Above we defined the class `Musician`, then instantiated `drummer` to be
an object of type `Musician`. We then printed out the drummer’s `.title`
attribute, which is a class variable that we defined as the string
“Rockstar”.

If we defined another musician, like `guitarist = Musician()` they would
have the same `.title` attribute.



**1.**

You are digitizing grades for *Jan van Eyck High School and
Conservatory*. At *Jan van High*, as the students call it, `65` is the
minimum passing grade.

Create a `Grade` class with a class attribute `minimum_passing` equal to
`65`.



``` python
class Grade:
  minimum_passing = 65
```

## Methods

*Methods* are functions that are defined as part of a class. The first
argument in a method is always the object that is calling the method.
Convention recommends that we name this first argument `self`. Methods
always have at least this one argument.

We define methods similarly to functions, except that they are indented
to be part of the class.

``` python
class Dog:
  dog_time_dilation = 7
 
  def time_explanation(self):
    print("Dogs experience {} years for every 1 human year.".format(self.dog_time_dilation))
 
pipi_pitbull = Dog()
pipi_pitbull.time_explanation()
# Prints "Dogs experience 7 years for every 1 human year."
```

Above we created a `Dog` class with a `time_explanation` method that
takes one argument, `self`, which refers to the object calling the
function. We created a `Dog` named `pipi_pitbull` and called the
`.time_explanation()` method on our new object for Pipi.

Notice we didn’t pass any arguments when we called
`.time_explanation()`, but were able to refer to `self` in the function
body. When you call a method it automatically passes the object calling
the method as the first argument.



**1.**

At *Jan van High*, the students are constantly calling the school rules
into question. Create a `Rules` class so that we can explain the rules.

In order for your code to run, you have to have *something* in your
class — you can’t have a defined class with no body like the following:

``` python
class exampleClass:
```

For now, make the body of your class `pass`. This will allow your code
to run without error.

**2.**

Give `Rules` a method `washing_brushes` that returns the string

``` python
"Point bristles towards the basin while washing your brushes."
```

Since we’ve now given this class a method, we can remove the `pass` that
we added in the previous step.



``` python
class Rules:
  def washing_brushes(self):
    return "Point bristles towards the basin while washing your brushes."
```

## Methods with Arguments

Methods can also take more arguments than just `self`:

``` python
class DistanceConverter:
  kms_in_a_mile = 1.609
  def how_many_kms(self, miles):
    return miles * self.kms_in_a_mile
 
converter = DistanceConverter()
kms_in_5_miles = converter.how_many_kms(5)
print(kms_in_5_miles)
# prints "8.045"
```

Above we defined a `DistanceConverter` class, instantiated it, and used
it to convert 5 miles into kilometers. Notice again that even though
`how_many_kms` takes two arguments in its definition, we only pass
`miles`, because `self` is implicitly passed (and refers to the object
`converter`).



**1.**

It’s March 14th (known in some places as **Pi day**) at *Jan van High*,
and you’re feeling awfully festive. You decide to create a program that
calculates the area of a circle.

Create a `Circle` class with class variable `pi`. Set `pi` to the
approximation `3.14`.

**2.**

Give `Circle` an `area` method that takes two parameters: `self` and
`radius`.

Return the area as given by this formula:

``` python
area = pi * radius ** 2
```

**3.**

Create an instance of `Circle`. Save it into the variable `circle`.

**4.**

You go to measure several circles you happen to find around.

-   A medium pizza that is 12 inches across.
-   Your teaching table which is 36 inches across.
-   The Round Room auditorium, which is 11,460 inches across.

You save the areas of these three things into `pizza_area`,
`teaching_table_area`, and `round_room_area`.

Remember that the `radius` of a circle is half the diameter. We gave
three diameters here, so halve them before you calculate the given
circle’s area.



``` python
class Circle:
  pi = 3.14
  
  def area(self, radius):
    return Circle.pi * radius ** 2
  
circle = Circle()
pizza_area = circle.area(12 / 2)
teaching_table_area = circle.area(36 / 2)
round_room_area = circle.area(11460 / 2)
```

## Constructors

There are several methods that we can define in a Python class that have
special behavior. These methods are sometimes called “magic,” because
they behave differently from regular methods. Another popular term is
*dunder methods*, so-named because they have two underscores
(double-underscore abbreviated to “dunder”) on either side of them.

The first dunder method we’re going to use is the `__init__()` method
(note the two underscores before and after the word “init”). This method
is used to *initialize* a newly created object. It is called every time
the class is instantiated.

Methods that are used to prepare an object being instantiated are called
*constructors*. The word “constructor” is used to describe similar
features in other object-oriented programming languages but programmers
who refer to a constructor in Python are usually talking about the
`__init__()` method.

``` python
class Shouter:
  def __init__(self):
    print("HELLO?!")
 
shout1 = Shouter()
# prints "HELLO?!"
 
shout2 = Shouter()
# prints "HELLO?!"
```

Above we created a class called `Shouter` and every time we create an
instance of `Shouter` the program prints out a shout. Don’t worry, this
doesn’t hurt the computer at all.

Pay careful attention to the instantiation syntax we use. `Shouter()`
looks a lot like a function call, doesn’t it? If it’s a function, can we
pass parameters to it? We absolutely can, and those parameters will be
received by the `__init__()` method.

``` python
class Shouter:
  def __init__(self, phrase):
    # make sure phrase is a string
    if type(phrase) == str:
 
      # then shout it out
      print(phrase.upper())
 
shout1 = Shouter("shout")
# prints "SHOUT"
 
shout2 = Shouter("shout")
# prints "SHOUT"
 
shout3 = Shouter("let it all out")
# prints "LET IT ALL OUT"
```

Above we’ve updated our `Shouter` class to take the additional parameter
`phrase`. When we created each of our objects we passed an argument to
the constructor. The constructor takes the argument `phrase` and, if
it’s a string, prints out the all-caps version of `phrase`.



**1.**

Add a constructor to our `Circle` class.

Since we seem more frequently to know the diameter of a circle, it
should take the argument `diameter`.

It doesn’t need to do anything yet, just write `pass` in the body of the
constructor.

**2.**

Now have the constructor print out the message
`"New circle with diameter: {diameter}"` when a new circle is created.

Create a circle `teaching_table` with diameter 36.



``` python
class Circle:
  pi = 3.14
  
  # Add constructor here:
  def __init__(self, diameter):
    print('New circle with diameter: {}'.format(diameter))
    
teaching_table = Circle(36)
```

    ## New circle with diameter: 36

## Instance Variables

We’ve learned so far that a class is a schematic for a data type and an
object is an instance of a class, but why is there such a strong need to
differentiate the two if each object can only have the methods and class
variables the class has? This is because each instance of a class can
hold different kinds of data.

The data held by an object is referred to as an *instance variable*.
Instance variables aren’t shared by all instances of a class — they are
variables that are specific to the object they are attached to.

Let’s say that we have the following class definition:

``` python
class FakeDict:
  pass
```

We can instantiate two different objects from this class, `fake_dict1`
and `fake_dict2`, and assign instance variables to these objects using
the same attribute notation that was used for accessing class variables.

``` python
fake_dict1 = FakeDict()
fake_dict2 = FakeDict()
 
fake_dict1.fake_key = "This works!"
fake_dict2.fake_key = "This too!"
 
# Let's join the two strings together!
working_string = "{} {}".format(fake_dict1.fake_key, fake_dict2.fake_key)
print(working_string)
# prints "This works! This too!"
```



**1.**

In **script.py** we have defined a `Store` class. Create two objects
from this store class, named `alternative_rocks` and `isabelles_ices`.

**2.**

Give them both instance attributes called `store_name`. Set
`alternative_rocks`’s `store_name` to `"Alternative Rocks"`. Set
`isabelles_ices`’s `store_name` to `"Isabelle's Ices"`.



``` python
class Store:
  pass

alternative_rocks = Store()
isabelles_ices = Store()

alternative_rocks.store_name = "Alternative Rocks"
isabelles_ices.store_name = "Isabelle's Ices"
```

## Attribute Functions

Instance variables and class variables are both accessed similarly in
Python. This is no mistake, they are both considered *attributes* of an
object. If we attempt to access an attribute that is neither a class
variable nor an instance variable of the object Python will throw an
`AttributeError`.

``` python
class NoCustomAttributes:
  pass
 
attributeless = NoCustomAttributes()
 
try:
  attributeless.fake_attribute
except AttributeError:
  print("This text gets printed!")
 
# prints "This text gets printed!"
```

What if we aren’t sure if an object has an attribute or not? `hasattr()`
will return `True` if an object has a given attribute and `False`
otherwise. If we want to get the actual value of the attribute,
`getattr()` is a Python function that will return the value of a given
object and attribute. In this function, we can also supply a third
argument that will be the default if the object does not have the given
attribute.

The syntax and parameters for these functions look like this:

`hasattr(object, “attribute”)` has two parameters:

-   *object* : the object we are testing to see if it has a certain
    attribute
-   *attribute* : name of attribute we want to see if it exists

`getattr(object, “attribute”, default)` has three parameters (one of
which is optional):

-   *object* : the object whose attribute we want to evaluate
-   *attribute* : name of attribute we want to evaluate
-   *default* : the value that is returned if the attribute does not
    exist (note: this parameter is **optional**)

Calling those functions looks like this:

``` python
hasattr(attributeless, "fake_attribute")
# returns False
 
getattr(attributeless, "other_fake_attribute", 800)
# returns 800, the default value
```

Above we checked if the `attributeless` object has the attribute
`fake_attribute`. Since it does not, `hasattr()` returned `False`. After
that, we used `getattr` to attempt to retrieve `other_fake_attribute`.
Since `other_fake_attribute` isn’t a real attribute on `attributeless`,
our call to `getattr()` returned the supplied default value `800`,
instead of throwing an `AttributeError`.



**1.**

In **script.py** we have a list of different data types: a dictionary, a
string, an integer, and a list all saved in the variable
`can_we_count_it`.

For every element in the list, check if the element has the attribute
`count` using the `hasattr()` function. If so, print the following line
of code:

``` python
print(str(type(element)) + " has the count attribute!")
```

**2.**

Now let’s add an `else` statement for the elements that do not have the
attribute `count`. In this `else` statement add the following line of
code:

``` python
print(str(type(element)) + " does not have the count attribute :(")
```

**3.**

Let’s go over the terminal output of the past two instructions. You
should see the following output in your terminal right now:

``` python
<class 'dict'> does not have the count attribute :(
<class 'str'> has the count attribute!
<class 'int'> does not have the count attribute :(
<class 'list'> has the count attribute!
```

This is because dictionaries and integers both do not have a `count`
attribute, while strings and lists do. In this exercise, we have
iterated through `can_we_count_it` and used `hasattr()` to determine
which elements have a `count` attribute. We never actually used the
count method, but you can read more about it
<a href="https://www.w3schools.com/python/ref_list_count.asp"
class="e14vpv2g1 gamut-xro1w8-ResetElement-Anchor-AnchorBase e1bhhzie0"
target="_blank" rel="noopener">here</a> if you are curious about what it
is.

Click run to move onto the next exercise!



``` python
can_we_count_it = [{'s': False}, "sassafrass", 18, ["a", "c", "s", "d", "s"]]

for element in can_we_count_it:
  if hasattr(element, "count"):
    print(str(type(element)) + " has the count attribute!")
  else:
    print(str(type(element)) + " does not have the count attribute :(")
```

    ## <class 'dict'> does not have the count attribute :(
    ## <class 'str'> has the count attribute!
    ## <class 'int'> does not have the count attribute :(
    ## <class 'list'> has the count attribute!

## Self

Since we can already use dictionaries to store key-value pairs, using
objects for that purpose is not really useful. Instance variables are
more powerful when you can guarantee a rigidity to the data the object
is holding.

This convenience is most apparent when the constructor creates the
instance variables, using the arguments passed in to it. If we were
creating a search engine, and we wanted to create classes for each
separate entry we could return. We’d do that like this:

``` python
class SearchEngineEntry:
  def __init__(self, url):
    self.url = url
 
codecademy = SearchEngineEntry("www.codecademy.com")
wikipedia = SearchEngineEntry("www.wikipedia.org")
 
print(codecademy.url)
# prints "www.codecademy.com"
 
print(wikipedia.url)
# prints "www.wikipedia.org"
```

Since the `self` keyword refers to the object and not the class being
called, we can define a `secure` method on the `SearchEngineEntry` class
that returns the secure link to an entry.

``` python
class SearchEngineEntry:
  secure_prefix = "https://"
  def __init__(self, url):
    self.url = url
 
  def secure(self):
    return "{prefix}{site}".format(prefix=self.secure_prefix, site=self.url)
 
codecademy = SearchEngineEntry("www.codecademy.com")
wikipedia = SearchEngineEntry("www.wikipedia.org")
 
print(codecademy.secure())
# prints "https://www.codecademy.com"
 
print(wikipedia.secure())
# prints "https://www.wikipedia.org"
```

Above we define our `secure()` method to take just the one required
argument, `self`. We access both the class variable `self.secure_prefix`
and the instance variable `self.url` to return a secure URL.

This is the strength of writing object-oriented programs. We can write
our classes to structure the data that we need and write methods that
will interact with that data in a meaningful way.



**1.**

In **script.py** you’ll find our familiar friend, the `Circle` class.

Even though we usually know the `diameter` beforehand, what we need for
most calculations is the `radius`.

In `Circle`’s constructor set the instance variable `self.radius` to
equal half the `diameter` that gets passed in.

**2.**

Define a new method `circumference` for your circle object that takes
only one argument, `self`, and returns the circumference of a circle
with the given radius by this formula:

``` python
circumference = 2 * pi * radius
```

**3.**

Define three `Circle`s with three different diameters.

-   A medium pizza, `medium_pizza`, that is 12 inches across.
-   Your teaching table, `teaching_table`, which is 36 inches across.
-   The Round Room auditorium, `round_room`, which is 11,460 inches
    across.

**4.**

Print out the circumferences of `medium_pizza`, `teaching_table`, and
`round_room`.



``` python
class Circle:
  pi = 3.14
  def __init__(self, diameter):
    print("Creating circle with diameter {d}".format(d=diameter))
    # Add assignment for self.radius here:
    
    self.radius = diameter / 2
    
  def circumference(self):
    return 2 * self.pi * self.radius
  
medium_pizza = Circle(12)
teaching_table = Circle(36)
round_room = Circle(11460)

print(medium_pizza.circumference())
print(teaching_table.circumference())
print(round_room.circumference())
```

    ## Creating circle with diameter 12

    ## Creating circle with diameter 36

    ## Creating circle with diameter 11460

    ## 37.68

    ## 113.04

    ## 35984.4

## Everything is an Object

Attributes can be added to user-defined objects after instantiation, so
it’s possible for an object to have some attributes that are not
explicitly defined in an object’s constructor. We can use the `dir()`
function to investigate an object’s attributes at runtime. `dir()` is
short for *directory* and offers an organized presentation of object
attributes.

``` python
class FakeDict:
  pass
 
fake_dict = FakeDict()
fake_dict.attribute = "Cool"
 
dir(fake_dict)
# Prints ['__class__', '__delattr__', '__dict__', '__dir__', '__doc__', '__eq__', '__format__', '__ge__', '__getattribute__', '__gt__', '__hash__', '__init__()', '__init_subclass__', '__le__', '__lt__', '__module__', '__ne__', '__new__', '__reduce__', '__reduce_ex__', '__repr__', '__setattr__', '__sizeof__', '__str__', '__subclasshook__', '__weakref__', 'attribute']
```

That’s certainly a lot more attributes than we defined! Python
automatically adds a number of attributes to all objects that get
created. These internal attributes are usually indicated by
double-underscores. But sure enough, `attribute` is in that list.

Do you remember being able to use `type()` on Python’s native data
types? This is because they are also objects in Python. Their classes
are `int`, `float`, `str`, `list`, and `dict`. These Python classes have
special syntax for their instantiation, `1`, `1.0`, `"hello"`, `[]`, and
`{}` specifically. But these instances are still full-blown objects to
Python.

``` python
fun_list = [10, "string", {'abc': True}]
 
type(fun_list)
# Prints <class 'list'>
 
dir(fun_list)
# Prints ['__add__', '__class__', [...], 'append', 'clear', 'copy', 'count', 'extend', 'index', 'insert', 'pop', 'remove', 'reverse', 'sort']
```

Above we define a new list. We check it’s type and see that’s an
instantiation of class `list`. We use `dir()` to explore its attributes,
and it gives us a large number of internal Python dunder attributes,
but, afterward, we get the usual list methods.



**1.**

Call `dir()` on the number `5`. Print out the results.

**2.**

Define a function called `this_function_is_an_object`. It can take any
parameters and return anything you’d like.

**3.**

Print out the result of calling `dir()` on `this_function_is_an_object`.

Functions are objects too!



``` python
print(dir(5))

def this_function_is_an_object(num):
  return "Cheese is {} times better than everything else".format(num)

print(dir(this_function_is_an_object))
```

    ## ['__abs__', '__add__', '__and__', '__bool__', '__ceil__', '__class__', '__delattr__', '__dir__', '__divmod__', '__doc__', '__eq__', '__float__', '__floor__', '__floordiv__', '__format__', '__ge__', '__getattribute__', '__getnewargs__', '__gt__', '__hash__', '__index__', '__init__', '__init_subclass__', '__int__', '__invert__', '__le__', '__lshift__', '__lt__', '__mod__', '__mul__', '__ne__', '__neg__', '__new__', '__or__', '__pos__', '__pow__', '__radd__', '__rand__', '__rdivmod__', '__reduce__', '__reduce_ex__', '__repr__', '__rfloordiv__', '__rlshift__', '__rmod__', '__rmul__', '__ror__', '__round__', '__rpow__', '__rrshift__', '__rshift__', '__rsub__', '__rtruediv__', '__rxor__', '__setattr__', '__sizeof__', '__str__', '__sub__', '__subclasshook__', '__truediv__', '__trunc__', '__xor__', 'as_integer_ratio', 'bit_length', 'conjugate', 'denominator', 'from_bytes', 'imag', 'numerator', 'real', 'to_bytes']

    ## ['__annotations__', '__call__', '__class__', '__closure__', '__code__', '__defaults__', '__delattr__', '__dict__', '__dir__', '__doc__', '__eq__', '__format__', '__ge__', '__get__', '__getattribute__', '__globals__', '__gt__', '__hash__', '__init__', '__init_subclass__', '__kwdefaults__', '__le__', '__lt__', '__module__', '__name__', '__ne__', '__new__', '__qualname__', '__reduce__', '__reduce_ex__', '__repr__', '__setattr__', '__sizeof__', '__str__', '__subclasshook__']

## String Representation

One of the first things we learn as programmers is how to print out
information that we need for debugging. Unfortunately, when we print out
an object we get a default representation that seems fairly useless.

``` python
class Employee():
  def __init__(self, name):
    self.name = name
 
argus = Employee("Argus Filch")
print(argus)
# prints "<__main__.Employee object at 0x104e88390>"
```

This default string representation gives us some information, like where
the class is defined and our computer’s memory address where this object
is stored, but is usually not useful information to have when we are
trying to debug our code.

We learned about the dunder method `__init__()`. Now, we will learn
another dunder method called `__repr__()`. This is a method we can use
to tell Python what we want the *string representation* of the class to
be. `__repr__()` can only have one parameter, `self`, and must return a
string.

In our `Employee` class above, we have an instance variable called
`name` that should be unique enough to be useful when we’re printing out
an instance of the `Employee` class.

``` python
class Employee():
  def __init__(self, name):
    self.name = name
 
  def __repr__(self):
    return self.name
 
argus = Employee("Argus Filch")
print(argus)
# prints "Argus Filch"
```

We implemented the `__repr__()` method and had it return the `.name`
attribute of the object. When we printed the object out it simply
printed the `.name` of the object! Cool!



**1.**

Add a `__repr__()` method to the `Circle` class that returns

``` python
Circle with radius {radius}
```

**2.**

Print out `medium_pizza`, `teaching_table`, and `round_room`.



``` python
class Circle:
  pi = 3.14
  
  def __init__(self, diameter):
    self.radius = diameter / 2
  
  def area(self):
    return self.pi * self.radius ** 2
  
  def circumference(self):
    return self.pi * 2 * self.radius
  
  def __repr__(self):
    return "Circle with radius {radius}".format(radius=self.radius)
  
  
medium_pizza = Circle(12)
teaching_table = Circle(36)
round_room = Circle(11460)

print(medium_pizza)
print(teaching_table)
print(round_room)
```

    ## Circle with radius 6.0

    ## Circle with radius 18.0

    ## Circle with radius 5730.0

## Review

So far we’ve covered what a data type actually is in Python. We explored
what the functionality of Python’s built-in types (also referred to as
*primitives*) are. We learned how to create our own data types using the
`class` keyword.

We explored the relationship between a class and an object — we create
objects when we instantiate a class, we find the class when we check the
`type()` of an object. We learned the difference between class variables
(the same for all objects of a class) and instance variables (unique for
each object).

We learned about how to define an object’s functionality with methods.
We created multiple objects from the same class, all with similar
functionality, but with different internal data. They all had the same
methods, but produced different output because they were different
instances.

Take a moment to congratulate yourself, object-oriented programming is a
complicated concept.



**1.**

Define a class named `Student` that will be our data model at *Jan van
Eyck High School and Conservatory*.

Add a constructor for `Student`. Have the constructor take in two
parameters: a `name` and a `year`. Save those two as attributes `.name`
and `.year`.

**2.**

Create three instances of the `Student` class:

-   Roger van der Weyden, year 10
-   Sandro Botticelli, year 12
-   Pieter Bruegel the Elder, year 8

Save them into the variables `roger`, `sandro`, and `pieter`.

**3.**

Create a `Grade` class, with `minimum_passing` as an attribute set to
`65`.

**4.**

Give `Grade` a constructor. Take in a parameter `score` and assign it to
`self.score`.

**5.**

In the body of the constructor for `Student`, declare `self.grades` as
an empty list.

**6.**

Add an `add_grade()` method to `Student` that takes a parameter,
`grade`.

`.add_grade()` should verify that `grade` is of type `Grade` and if so,
add it to the `Student`’s `.grades`.

If `grade` isn’t an instance of `Grade` then `.add_grade()` should do
nothing.

**7.**

Create a new `Grade` with a score of `100` and add it to `pieter`’s
`.grades` attribute using `.add_grade()`.

**8.**

Great job! You’ve created two classes and defined their interactions.
This is object-oriented programming! From here you could:

-   Write a `Grade` method `is_passing()` that returns whether a `Grade`
    has a passing `.score`.
-   Write a `Student` method `get_average()` that returns the student’s
    average score.
-   Add an instance variable to `Student` that is a dictionary called
    `.attendance`, with dates as keys and booleans as values that
    indicate whether the student attended school that day.
-   Write your own classes to do whatever logic you want!



``` python
class Student:
  def __init__(self, name, year):
    self.name = name
    self.year = year
    self.grades = []
  
  def add_grade(self, grade):
    if type(grade) is Grade:
      self.grades.append(grade)      

class Grade:
  minimum_passing = 65
  
  def __init__(self, score):
    self.score = score
    
roger = Student("Roger van der Weyden", 10)
sandro = Student("Sandro Botticelli", 12)
pieter = Student("Pieter Bruegel the Elder", 8)
pieter.add_grade(Grade(100))
```

# Basta Fazoolin’

You’ve started a position as the lead programmer for the family-style
Italian restaurant *Basta Fazoolin’ with My Heart*. The restaurant has
been doing fantastically and seen a lot of growth lately. You’ve been
hired to keep things organized.

If you get stuck during this project or would like to see an experienced
developer work through it, click “**Get Unstuck**“ to see a **project
walkthrough video**.

## Instructions

Mark the tasks as complete by checking them off

### Making the Menus

1\.

At *Basta Fazoolin’ with my Heart* our motto is simple: when you’re here
with family, that’s great! We have four different menus: brunch,
early-bird, dinner, and kids.

Create a `Menu` class .

2\.

Give `Menu` a constructor with the five parameters `self`, `name`,
`items`, `start_time`, and `end_time`.

3\.

Let’s create our first menu: `brunch`. Brunch is served from 11am to
4pm. The following items are sold during brunch:

``` python
{
  'pancakes': 7.50, 'waffles': 9.00, 'burger': 11.00, 'home fries': 4.50, 'coffee': 1.50, 'espresso': 3.00, 'tea': 1.00, 'mimosa': 10.50, 'orange juice': 3.50
}
```

4\.

Let’s create our second menu item `early_bird`. Early-bird Dinners are
served from 3pm to 6pm. The following items are available during the
early-bird menu:

``` python
{
  'salumeria plate': 8.00, 'salad and breadsticks (serves 2, no refills)': 14.00, 'pizza with quattro formaggi': 9.00, 'duck ragu': 17.50, 'mushroom ravioli (vegan)': 13.50, 'coffee': 1.50, 'espresso': 3.00,
}
```

5\.

Let’s create our third menu, `dinner`. Dinner is served from 5pm to
11pm. The following items are available for dinner:

``` python
{
  'crostini with eggplant caponata': 13.00, 'caesar salad': 16.00, 'pizza with quattro formaggi': 11.00, 'duck ragu': 19.50, 'mushroom ravioli (vegan)': 13.50, 'coffee': 2.00, 'espresso': 3.00,
}
```

6\.

And let’s create our last menu, `kids`. The kids menu is available from
11am until 9pm. The following items are available on the kids menu.

``` python
{
  'chicken nuggets': 6.50, 'fusilli with wild mushrooms': 12.00, 'apple juice': 3.00
}
```

7\.

Give our `Menu` class a string representation method that will tell you
the `name` of the menu. Also, indicate in this representation when the
menu is available.

8\.

Try out our string representation. If you call `print(brunch)` it should
print out something like the following:

``` python
brunch menu available from 11am to 4pm
```

9\.

Give `Menu` a method `.calculate_bill()` that has two parameters:
`self`, and `purchased_items`, a list of the names of purchased items.

Have `calculate_bill` return the total price of a purchase consisting of
all the items in `purchased_items`.

10\.

Test out `Menu.calculate_bill()`. We have a breakfast order for one
order of pancakes, one order of home fries, and one coffee. Pass that
into `brunch.calculate_bill()` and print out the price.

11\.

What about an early-bird purchase? Our last guests ordered the salumeria
plate and the vegan mushroom ravioli. Calculate the bill with
`.calculate_bill()`.

### Creating the Franchises

12\.

*Basta Fazoolin’ with my Heart* has seen tremendous success with the
family market, which is fantastic because when you’re at *Basta
Fazoolin’ with my Heart* with family, that’s great!

We’ve decided to create more than one restaurant to offer our fantastic
menus, services, and ambience around the country.

First, let’s create a `Franchise` class.

13\.

Give the `Franchise` class a constructor. Take in an `address`, and
assign it to `self.address`. Also take in a list of `menus` and assign
it to `self.menus`.

14\.

Let’s create our first two franchises! Our flagship store is located at
`"1232 West End Road"` and our new installment is located at
`"12 East Mulberry Street"`. Pass in all four menus along with these
addresses to define `flagship_store` and `new_installment`.

15\.

Give our `Franchise`s a string representation so that we’ll be able to
tell them apart. If we print out a `Franchise` it should tell us the
address of the restaurant.

16\.

Let’s tell our customers what they can order! Give `Franchise` an
`.available_menus()` method that takes in a `time` parameter and returns
a list of the `Menu` objects that are available at that time.

17\.

Let’s test out our `.available_menus()` method! Call it with 12 noon as
an argument and print out the results.

18\.

Let’s do another test! See what is printed if we call
`.available_menus()` with 5pm as an argument and print out the results.

### Creating Businesses!

19\.

Since we’ve been so successful building out a branded chain of
restaurants, we’ve decided to diversify. We’re going to create a
restaurant that sells arepas!

First let’s define a `Business` class.

20\.

Give `Business` a constructor. A `Business` needs a `name` and a list of
`franchises`.

21\.

Let’s create our first `Business`. The name is
`"Basta Fazoolin' with my Heart"` and the two franchises are
`flagship_store` and `new_installment`.

22\.

Before we create our new business, we’ll need a `Franchise` and before
our `Franchise` we’ll need a menu. The items for our *Take a’ Arepa*
available from 10am until 8pm are the following:

``` python
{
  'arepa pabellon': 7.00, 'pernil arepa': 8.50, 'guayanes arepa': 8.00, 'jamon arepa': 7.50
}
```

Save this to a variable called `arepas_menu`.

23\.

Next let’s create our first *Take a’ Arepa* franchise! Our new
restaurant is located at `"189 Fitzgerald Avenue"`. Save the `Franchise`
object to a variable called `arepas_place`.

24\.

Now let’s make our new `Business`! The business is called
`"Take a' Arepa"`!

25\.

Congrats! You created a system of classes that help structure your code
and perform all business requirements you need. Whenever we need a new
feature we’ll have the well-organized code required to make developing
and shipping it easy.

26\.

If you are stuck on the project or would like to see an experienced
developer work through the project, watch the following project
walkthrough video!

[Python Project Walkthrough Basta
Fazoolin’](https://www.youtube.com/watch?v=Dk-ePlxdmBU)

## Solution

``` python
class Business:
  def __init__(self, name, franchises):
    self.name = name
    self.franchises = franchises


class Franchise:
  def __init__(self, address, menus):
    self.address = address
    self.menus = menus
  
  def __repr__(self):
    return self.address

  def available_menus(self, time):
    available_menus = []
    for menu in self.menus:
      if time >= menu.start_time and time <= menu.end_time:
        available_menus.append(menu)
    return available_menus


class Menu:
  def __init__(self, name, items, start_time, end_time):
    self.name = name
    self.items = items
    self.start_time = start_time
    self.end_time = end_time

  def __repr__(self):
    return self.name + ' menu available from ' + str(self.start_time) + ' - ' + str(self.end_time)

  def calculate_bill(self, purchased_items):
    bill = 0
    for purchased_item in purchased_items:
      if purchased_item in self.items:
        bill += self.items[purchased_item]
    return bill


# Brunch Menu
brunch_items = {
  'pancakes': 7.50, 'waffles': 9.00, 'burger': 11.00, 'home fries': 4.50, 'coffee': 1.50, 'espresso': 3.00, 'tea': 1.00, 'mimosa': 10.50, 'orange juice': 3.50
}
brunch_menu = Menu('Brunch', brunch_items, 1100, 1600)

# Early Bird Menu
early_bird_items = {
  'salumeria plate': 8.00, 'salad and breadsticks (serves 2, no refills)': 14.00, 'pizza with quattro formaggi': 9.00, 'duck ragu': 17.50, 'mushroom ravioli (vegan)': 13.50, 'coffee': 1.50, 'espresso': 3.00,
}
early_bird_menu = Menu('Early Bird', early_bird_items, 1500, 1800)

# Dinner Menu
dinner_items = {
  'crostini with eggplant caponata': 13.00, 'ceaser salad': 16.00, 'pizza with quattro formaggi': 11.00, 'duck ragu': 19.50, 'mushroom ravioli (vegan)': 13.50, 'coffee': 2.00, 'espresso': 3.00,
}
dinner_menu = Menu('Dinner', dinner_items, 1700, 2300)

# Kids Menu
kids_items = {
  'chicken nuggets': 6.50, 'fusilli with wild mushrooms': 12.00, 'apple juice': 3.00
}
kids_menu = Menu('Kids', kids_items, 1100, 2100)

menus = [brunch_menu, early_bird_menu, dinner_menu, kids_menu]

flagship_store = Franchise('1232 West End Road', menus)
new_installment = Franchise('12 East Mulberry Street', menus)

basta = Business("Basta Fazoolin' with my Heart", [flagship_store, new_installment])


# Arepa
arepas_items = {
  'arepa pabellon': 7.00, 'pernil arepa': 8.50, 'guayanes arepa': 8.00, 'jamon arepa': 7.50
}
arepas_menu = Menu("Take a’ Arepa", arepas_items, 1000, 2000)

arepas_place = Franchise("189 Fitzgerald Avenue", arepas_menu)

arepas = Business("Take a' Arepa", arepas_place)
```

# Decorators

[What Are Decorators?](https://www.youtube.com/watch?v=WOHsHaaJ8VQ)
