## Some common pitfalls

Before we begin click `python`{{execute}} to start the interactive Python shell.

The following function is supposed to print all square numbers smaller than 100. It is not working proberly though. Can you fix it?

<pre class="file" data-filename="fix_the_code.py" data-target="append">
def print_squares():
  for num in range(10):
    print(num * num)
    num += 1
</pre>

```
import fix_the_code as f
print_squares()
```{{execute}}

Hint: The for loop increments the iterator variable (<code>num</code> here) automatically. No need to increment it yourself.

```
import importlib
def reload():
  importlib.reload(f)
    
reload()
```{{execute}}

<pre class="file" data-filename="fix_the_code.py" data-target="append">
def swap(first, second):
  first = second
  second = first
  print(f'First variable after swap: {first}')
  print(f'Second variable after swap: {second}')
</pre>

```
reload()
f.swap("I'm first", "I'm second")
```{{execute}}


<pre class="file" data-filename="fix_the_code.py" data-target="append">
def sum_1_to_n(n):
  return sum(range(n))
</pre>

```
reload()
f.sum_1_to_5(10) # should be 15 
```{{execute}}

<pre class="file" data-filename="fix_the_code.py" data-target="append">
def away(minutes):
  while(minutes):
    print("I'm away! Be back soon...")
  print("I'm back!")
</pre>

```
reload()
f.away(6)
```{{execute}}

<pre class="file" data-filename="fix_the_code.py" data-target="append">

</pre>

```
reload()

```{{execute}}
