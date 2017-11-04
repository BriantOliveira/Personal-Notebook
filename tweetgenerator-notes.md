# Tweet Generator 

---

#### Getting random data:



Using the random method you can get random values in a list or dictionary, usually this method is just used to get random data and only a data within a list or dictionary, this method is never used for security.

```
import random
```

The random method only generates numbers between 0&gt;1.

```
import random 


value = random.random()
print(value)

>>> 0.98239298270925740982
```

So every time you run this, it will generate a number within 0 &gt; 1, this method is rarely used because usually you want to get a number within a certain range.

If you want a random floating value within a certain range, you can use the uniform method.  

```
import random 


value = random.uniform(1, 10)
print(value)

>>> 6.892734070942759

```

In case if you want to generate random integers you can use randint method

```
import random 


value = random.randint(1,6)
print(value)

>>> 3
```

The choice method picks a value within a list of values 

```
import random 

greetings = ["Hello", "Hi", "Hey", "Howdy", "Hola"]


value = random.choice(greetings)
print(value + ', Elliot!')

>>> Hey, Elliot!
```



It's also possible to get multiple values of a random list, but to do so you gotta use the method choices.

Let's create a roulette example...

```
import random 

colors = ['red', 'black', 'green']

results = random.choices(colors, k=4)

print(results)

>>>['red', 'green', 'red', 'black']
```

k=\# determines how many times we want to pick a random value. In the roulette game there is only 18 reds, 18 blacks and only 2 greens. In order to add that probability you can add weight. 

```
import random 

colors = ['red', 'black', 'green']

results = random.choices(colors,weights=[18, 18, 2], k=4)

print(results)
```

If you want to shuffle a list of values 

```
import random 

deck = list(range(1, 53))

random.shuffle(deck)
print(deck)
```

If you want get unique numbers you can use the sample method 

```
import random 

deck = list(range(1, 53))

hand = random.sample(deck, k=4)

print(results)

>>> [34, 23, 10, 37]
```

So now it only will return 4 unique numbers on the sequence .

If you want to generate a fake data using random you can do this

```
import random 

first_name = ['John', 'Michael','Chris', 'Elliot']

last_name = ['Smith', 'Doe', 'Jackson', 'Blackwell']

street_names = ['Main', 'High' 'Pear', 'Powell']

cities = ['Miami', 'Brooklyn', 'Fort Lauderdale', 'Nob hill'] 

states = ['FL', 'NY', 'CH', 'CA']

for num in range(10)
    first = random.choice(first_name)
    last = random.choice(last_name)
    
    phone = f'{random.randint(100, 999)-555-(random.randint(1000,9999)}'
    
    street_num = random.randint(100, 999)
    street = random.choice(street_names)
    city = random.choice(cities)
    zip_code = random.randint(10000, 99999)
    address = f'{street_num} {street} St., {city} {state} {zip_code}'
    
    email = first.lower() + last.lower() + '@gmail.com'
    
    print(f'{first} {last}\n{phone}\n{address}\n{email}\n')

```



