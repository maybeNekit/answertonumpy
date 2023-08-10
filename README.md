# answers to the course!!!
_If you run out of ideas on how to solve it, then here are the answers)_

(introduction in python only Numpy)
## Your First NumPy Array
In this chapter, we're going to dive into the world of baseball. Along the way, you'll get comfortable with the basics of numpy, a powerful package to do data science.

A list baseball has already been defined in the Python script, representing the height of some baseball players in centimeters. Can you add some code here and there to create a numpy array from it?

- Import the numpy package as np, so that you can refer to numpy with np.
- Use np.array() to create a numpy array from baseball. Name this array np_baseball.
- Print out the type of np_baseball to check that you got it right.

```python
import numpy as np


# Create list baseball
baseball = [180, 215, 210, 210, 188, 176, 209, 200]

# Create a numpy array from baseball: np_baseball
np_baseball=np.array(baseball)

# Print out type of np_baseball
print(type(np_baseball))
```
## Baseball players' height
You are a huge baseball fan. You decide to call the MLB (Major League Baseball) and ask around for some more statistics on the height of the main players. They pass along data on more than a thousand players, which is stored as a regular Python list: height_in. The height is expressed in inches. Can you make a numpy array out of it and convert the units to meters?

height_in is already available and the numpy package is loaded, so you can start straight away (Source: stat.ucla.edu).

- Create a numpy array from height_in. Name this new array np_height_in.
- Print np_height_in.
- Multiply np_height_in with 0.0254 to convert all height measurements from inches to meters. Store the new values in a new array, np_height_m.
- Print out np_height_m and check if the output makes sense.

```python
# Import numpy
import numpy as np

# Create a numpy array from height_in: np_height_in
np_height_in=np.array(height_in)

# Print out np_height_in
print(np_height_in)

# Convert np_height_in to m: np_height_m
np_height_m=np_height_in * 0.0254

# Print np_height_m
print(np_height_m)
```
## Baseball player's BMI
The MLB also offers to let you analyze their weight data. Again, both are available as regular Python lists: height_in and weight_lb. height_in is in inches and weight_lb is in pounds.

It's now possible to calculate the BMI of each baseball player. Python code to convert height_in to a numpy array with the correct units is already available in the workspace. Follow the instructions step by step and finish the game! height_in and weight_lb are available as regular lists.

- Create a numpy array from the weight_lb list with the correct units. Multiply by 0.453592 to go from pounds to kilograms. Store the resulting numpy array as np_weight_kg.
- Use np_height_m and np_weight_kg to calculate the BMI of each player. Use the following equation: ***BMI=weight/height^2***
 
- Save the resulting numpy array as bmi.
- Print out bmi.

```python
# Import numpy
import numpy as np

# Create array from height_in with metric units: np_height_m
np_height_m = np.array(height_in) * 0.0254

# Create array from weight_lb with metric units: np_weight_kg
np_weight_kg=np.array(weight_lb) * 0.453592

# Calculate the BMI: bmi
bmi=np_weight_kg / np_height_m**2


# Print out bmi
print(bmi)
```
## Lightweight baseball players
To subset both regular Python lists and numpy arrays, you can use square brackets:
```
x = [4 , 9 , 6, 3, 1]
x[1]
import numpy as np
y = np.array(x)
y[1]
```
For numpy specifically, you can also use boolean numpy arrays:
```
high = y > 5
y[high]
```
The code that calculates the BMI of all baseball players is already included. Follow the instructions and reveal interesting things from the data! height_in and weight_lb are available as regular lists.

- Create a boolean numpy array: the element of the array should be True if the corresponding baseball player's BMI is below 21. You can use the < operator for this. Name the array light.
- Print the array light.
- Print out a numpy array with the BMIs of all baseball players whose BMI is below 21. Use light inside square brackets to do a selection on the bmi array.

```python
# Import numpy
import numpy as np

# Calculate the BMI: bmi
np_height_m = np.array(height_in) * 0.0254
np_weight_kg = np.array(weight_lb) * 0.453592
bmi = np_weight_kg / np_height_m ** 2

# Create the light array
light=bmi<21

# Print out light
print(light)

# Print out BMIs of all baseball players whose BMI is below 21
print(bmi[bmi<21])
```
