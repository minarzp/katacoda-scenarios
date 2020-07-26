Inspired from <a href = "https://www.codecademy.com/learn/paths/build-python-web-apps-flask/tracks/flask-python-data-structures-loops/modules/learn-python3-lists/cheatsheet" target="_blank">here</a>.
Before we begin click `python`{{execute}} to start the interactive Python shell.

## Lists

In Python, lists are ordered collections of items that allow for easy use of a set of data.

List values are placed in between square brackets <code>[ ]</code>, separated by commas. It is good practice to put a space between the comma and the next value. The values in a list do not need to be unique (the same value can be repeated).

<pre class="file" data-filename="lists.py" data-target="append">
breakfast = ["bread", "butter", "milk"]
</pre>

Click on below to load our python file in the shell now and print the "breakfast":

```
import lists as l
l.breakfast
```{{execute}}

Empty lists do not contain any values within the square brackets.

<pre class="code">
empty_list=[]
</pre>

## Adding Lists Together

Lists can be added to each other using the plus symbol <code>+</code>. This will result in a new list containing the same items in the same order with the first list’s items coming first.

<pre class="file" data-filename="lists.py" data-target="append">
fruits = ["apples", "cherries"]
shopping_list = breakfast + fruits
# Result: ["bread", "butter", "milk", "apples", "cherries"]
</pre>

We need to reload our script everytime it changes:

```
import importlib
def reload():
  importlib.reload(l)
    
reload()

l.shopping_list
```{{execute}}

Note: This will not work for adding a single item to the list, as in: <code><s>shopping_list = shopping_list + "honey"</s></code>. To do this, either use the <code>append()</code> method or use the plus symbol to add a new list with a single value:

<pre class="file" data-filename="lists.py" data-target="append">
shopping_list.append("honey")
shopping_list = shopping_list + ["peanuts"] # (or better: shopping_list += ["peanuts"])
# Result: ["bread", "butter", "milk", "apples", "cherries", "honey", "peanuts"]
</pre>


```
reload()
l.shopping_list
```{{execute}}

## Accessing list items with indices

```
l.shopping_list[0] # Result: bread
l.shopping_list[2] # Result: milk

# All items from index 1 to 3 inclusive
l.shopping_list[1:4]
# First 2 items
l.shopping_list[:2]
# Items from index 4 to the end
l.shopping_list[4:]
```{{execute}}

## Practice!

Inside <code>lists.py</code>, define a new list called <code>dinner</code>, with items "pasta" and "sausage", and add it to the shopping list. Then, define a new list called <code>vegan_shopping_list</code>, and add all vegan items from the shopping list to it, using <strong>only</strong> the range subsetting and plus syntax. If you do this right, the following command should result in <code>["bread", "apples", "cherries", "pasta"]</code>.

```
reload()
l.vegan_shopping_list
```{{execute}}