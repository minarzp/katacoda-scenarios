Inspired from [here]("https://www.codecademy.com/learn/paths/build-python-web-apps-flask/tracks/flask-python-data-structures-loops/modules/learn-python3-lists/cheatsheet).
Before we begin click `python`{{execute}} to start the interactive Python shell.

# Lists

In Python, lists are ordered collections of items that allow for easy use of a set of data.

List values are placed in between square brackets `[ ]`, separated by commas. It is good practice to put a space between the comma and the next value. The values in a list do not need to be unique (the same value can be repeated).

<pre class="file" data-filename="lists.py" data-target="append">
breakfast = ["bread", "butter", "milk"]
</pre>

Click on below to load our python file in the shell now and print the "breakfast":

```python
import lists as l
l.breakfast
```{{execute}}

Empty lists do not contain any values within the square brackets.

```python
empty_list=[]
```

## Adding Lists Together

Lists can be added to each other using the plus symbol `+`. This will result in a new list containing the same items in the same order with the first list’s items coming first.

<pre class="file" data-filename="lists.py" data-target="append">
```python
fruits = ["apples", "cherries"]
shopping_list = breakfast + fruits
```
</pre>

We need to reload our script everytime it changes:

```python
import importlib
def reload():
  importlib.reload(l)
    
reload()

# Result: ["bread", "butter", "milk", "apples", "cherries"]
l.shopping_list
```{{execute}}

Note: This will not work for adding a single item to the list, as in: <code><s>shopping_list = shopping_list + "cookies"</s></code>. To do this, either use the `append()` method or use the plus symbol to add a new list with a single value:

<pre class="file" data-filename="lists.py" data-target="append">
```python
shopping_list.append("honey")
shopping_list += ["peanuts"]
# (short form of: shopping_list = shopping_list + ["peanuts"])
```
</pre>


```python
reload()
# Result: ["bread", "butter", "milk", "apples", "cherries", "honey", "peanuts"]
l.shopping_list
```{{execute}}

## Accessing list items with indices

```python
l.shopping_list[0] # bread
l.shopping_list[2] # milk

l.shopping_list[1:4] # items indices 1 to 3 inclusive
l.shopping_list[:2] # first 2 items
l.shopping_list[2:3] # milk
l.shopping_list[4:] # items indices 4 to the end
```{{execute}}

## Practice!

Inside `lists.py`, define a new list called `dinner`, with items "pasta" and "sausage", and add it to the shopping list. Then, define another list called `vegan_shopping_list`, and add all vegan items from the shopping list to it, using **only** the range subsetting and plus syntax. If you do this right, the following command should result in `["bread", "apples", "cherries", "peanuts", "pasta"]`.

```python
reload()
l.vegan_shopping_list
```{{execute}}