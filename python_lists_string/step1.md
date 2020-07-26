Inspired from <a href = "https://www.codecademy.com/learn/paths/build-python-web-apps-flask/tracks/flask-python-data-structures-loops/modules/learn-python3-lists/cheatsheet" target="_blank">here</a>.
Before we begin click `Python`{{execute}} to start the interactive Python shell.

## Lists

In Python, lists are ordered collections of items that allow for easy use of a set of data.

List values are placed in between square brackets <code>[ ]</code>, separated by commas. It is good practice to put a space between the comma and the next value. The values in a list do not need to be unique (the same value can be repeated).

<pre class="file" data-filename="lists.py" data-target="append">
breakfast = ["bread", "butter", "milk"]
</pre>

```
import lists as l
l.shopping_list
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

```
import lists as l
l.shopping_list
```{{execute}}

Note: This will not work for adding a single item to the list, as in: <code><s>shopping_list = shopping_list + "cookies"</s></code>. To do this, either use the <code>append()</code> method or use the plus symbol to add a new list with a single value:

<pre class="file" data-filename="lists.py" data-target="append">
shopping_list.append("cookies")
shopping_list = shopping_list + ["peanuts"] # (or better: shopping_list += ["peanuts"])
# Result: ["bread", "butter", "milk", "apples", "cherries", "cookies", "peanuts"]
</pre>

```
import lists as l
l.shopping_list
```{{execute}}

## Accessing list items with indices

```
print(l.shopping_list[0]) # Result: bread
print(l.shopping_list[2]) # Result: milk

# All items from index 1 to 3 inclusive
print(l.shopping_list[1:4])
# Result: ["butter", "milk", "bread"]
# First 2 items
print(l.shopping_list[:2])
# Items from index 4 to the end
print(l.shopping_list[4:])
```{{execute}}


<pre class="file" data-filename="lists.py" data-target="append">

</pre>