Inspired from [here](https://www.codecademy.com/learn/paths/build-python-web-apps-flask/tracks/flask-python-data-structures-loops/modules/learn-python3-lists/cheatsheet).
Before we begin click `python`{{execute}} to start the interactive Python shell.

# Lists

In Python, lists are ordered collections of items that allow for easy use of a set of data.

List values are placed in between square brackets `[ ]`, separated by commas. It is good practice to put a space between the comma and the next value. The values in a list do not need to be unique (the same value can be repeated). To make and empty list, use square brackets with no values in them:

<pre class="file" data-filename="lists.py" data-target="append">
breakfast = ["bread", "butter", "milk"]
shopping_list = [] # Empty for now
</pre>

Click on below to load our python file in the shell and print the "breakfast":

```python
import lists as l
l.breakfast
```{{execute}}


## Adding Lists Together

Lists can be added to each other using the plus symbol `+`. This will result in a new list containing the same items in the same order with the first list’s items coming first.

<pre class="file" data-filename="lists.py" data-target="append">
fruits = ["apples", "cherries"]
shopping_list = breakfast + fruits
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
shopping_list.append("honey")
shopping_list += ["peanuts"]
# (short form of: shopping_list = shopping_list + ["peanuts"])
</pre>


```python
reload()
# Result: ["bread", "butter", "milk", "apples", "cherries", "honey", "peanuts"]
l.shopping_list
```{{execute}}

## The length of the list
The Python `len()` function can be used to find the number of items in the list:

```python
len(l.shopping_list)
``` {{execute}}

## Accessing list items with indices
[Python list indexing](./assets/python-list.png)
Individual list items can be accessed using the syntax `list[index]`. Indices begin at zero and end at the length of the list minus one. So the first item is at index `0` and the last one at index `len(list) - 1`. You can select a range of items using the symbol `:`: e.g. `list[1:3]` gives you a new list with only the items at indices 1 and 2. When selecting a range, if you want to start from the first item, there is no need to specify the index `0`  before the `:`. Similarly, if you want to select a range ending with the last item, you don't need to specify an index after `:`:

```python
l.shopping_list[0] # bread
l.shopping_list[2] # milk

l.shopping_list[1:4] # items indices 1 to 3 inclusive
l.shopping_list[:2] # first 2 items
l.shopping_list[2:3] # milk
l.shopping_list[4:] # items indices 4 to the end
```{{execute}}


## Practice!

Inside `lists.py`, define a new list called `dinner`, with items "pasta" and "sausage", and add it to the shopping list. Then, define another list called `vegan_shopping_list`, and add all vegan items from the shopping list to it, using **only** the range subsetting and plus syntax. Test it by running:

```python
reload()
l.vegan_shopping_list
```{{execute}}

 This should result in: `["bread", "apples", "cherries", "peanuts", "pasta"]`
