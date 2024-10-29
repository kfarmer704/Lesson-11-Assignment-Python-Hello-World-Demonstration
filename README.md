file:///C:/Users/user/Downloads/simplewebpage1.html


# Lesson-11-Assignment-Python-Hello-World-Demonstration
Lesson 11 Assignment: Python Hello World Demonstration
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Simple HTML and Python Example</title>
  <link rel="stylesheet" href="https://pyscript.net/latest/pyscript.css" />
  <script defer src="https://pyscript.net/latest/pyscript.js"></script>
</head>
<body>

<h1>Simple HTML and Python Example</h1>

<input id="inputNumber" type="number" placeholder="Enter a number">
<input id="inputMultiplier" type="number" placeholder="Enter a multiplier">
<button id="submitButton">Submit</button>

<div id="output">The output will appear here...</div>

<py-script>
def process_input(event=None):
    input_value = Element('inputNumber').value
    input_multiplier = Element('inputMultiplier').value

    if input_value and input_multiplier:
        product = float(input_value) * float(input_multiplier)
        Element('output').write(f"You entered: {input_value} and multiplier: {input_multiplier}. Product: {product}")
    else:
        Element('output').write("Please enter both numbers.")

# Assign the function to the button's onclick event after PyScript is ready
from js import document

document.getElementById('submitButton').onclick = process_input
</py-script>

</body>
</html>
