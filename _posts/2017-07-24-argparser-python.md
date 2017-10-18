---
layout: post
title:  "Using argument parser for Python scripts"
date:   2017-07-24 10:00:38 -0500
categories: cs

---

It's often easy to run your Python scripts from the command line. Sometimes, your scripts may require a form of input to run- here's a two-minute recipe to use the ArgumentParser module in Python to allow you to enter these inputs like the following: 

````
$ python script.py --input <input>
# can use input in script
````  

And then using these inputs in your program. Easy/quick documentation for these things can be hard to come by, so I'm making some notes here for reference. 

1. First, install the [argparse module](https://pypi.python.org/pypi/argparse)- this is built in for most standard versions of Python, but run this to be sure you have it.   

````
$ pip install argparse
````  

2. Say we wanted to use argparse to input a string value of someone's name, for our Python script hello.py that says hello and happy birthday to an input person for an input age:  

{% highlight python %}
name = 'Monty'
print ('Happy ' + str(age) + 'th' + ' Birthday ' + name + '!')
# Ex: Happy 20th Birthday John!  for name = John, age = 20. 
{% endhighlight %}

3. First, we import the argparse model and instantiate an object: 

{% highlight python %}
import argparse 


ap = argparse.ArgumentParser(description='Greet the user')
# Optional: put in a description for your script 
{% endhighlight %}


4. Next, we add the argument, 'name', to our argparse object with the add_argument function with the following parameters:

{% highlight python %}

ap.add_argument("-n", "--name", type=str, default= "Shamikh",
        help= "Name of person to greet. ex: Shamikh")

ap.add_argument("-a", "--age", type=int, default= 19,
        help= "Age of person to greet. ex: 19")
{% endhighlight %}


- "-n" and "--name" serve the same function, that is, they will indicate the parameter the user is entering, which becomes important if we have multiple parameters. "-j" is simply the shorthand abbreviation that can also be used to indicate that the next value entered is the argument desired. 
- type: indicates the data type desired, will usually be string (str), float, integer (int) as needed 
- default: the default value of the input that is assumed if nothing is input by the user. So, if the user simply enters 'python script.py' in the command line, then the default values will be used to run the program. 
- help: the user can simply enter '--help' to see this helper string, along with the helper strings of all your inputs. Useful to explain requirements of the sought input here, and an example. 

If the user types  
````
python script.py --help 
````

They will see: 
````
usage: script.py [-h] [-n NAME] [-a AGE]

Script to greet and wish happy birthday.

optional arguments:
  -h, --help            show this help message and exit
  -n NAME, --name NAME  Name of person to greet. ex: Monty
  -a AGE, --age AGE     Age of person to greet. ex: 19
````
Sweet! Now how do we use these values into our program? If we use the parse_args() function, the entered inputs can be loaded into a python dictionary. 

{% highlight python %}
args = vars(ap.parse_args())

# we can now access the inputs with their reference: 
name = args['name']
age = args['age']
print ('Happy ' + str(age) + 'th' + ' Birthday ' + name + '!')
{% endhighlight %}


So, for a test run (here's the full code): 

{% highlight python %}
import argparse 


ap = argparse.ArgumentParser(description = 'Script to greet and wish happy birthday.')

ap.add_argument("-n", "--name", type=str, default= "Shamikh",
        help= "Name of person to greet. ex: Shamikh")

ap.add_argument("-a", "--age", type=int, default= 19,
        help= "Age of person to greet. ex: 19")

args = vars(ap.parse_args())

print ('Happy ' + str(args['age']) + 'th' + ' Birthday ' + args['name'] + '!')
{% endhighlight %}

And here's the output of running the script in Terminal: 

````
$ python script.py -name Monty -age 100
Happy 100th Birthday Monty!

````



