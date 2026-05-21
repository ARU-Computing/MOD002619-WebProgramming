# Bill Splitter Worksheet

## Java Script Introduction - Week 2 Tasks

### Changing Text

A simple JavaScript function to change the text within a `<div>`

```javascript
function changeling(eid) {
    document.getElementById(eid).innerHTML = "<p>New text!</p>";
}
```

The function takes an element ID `eid` as a parameter, searches the document for an element with that ID and replaces the data within that element with the paragraph New text!
To call this function from an onclick event of a button you could use the following code in your HTML file.

```html
<button onclick="changeling('IDofDivToChange')">Change</button>
Ideally you would have your JavaScript function in an external file from your HTML file so you would need to reference it in your HTML file using code such as:
<script type="text/javascript" src="Changeling.js"></script>
```

### Using user input

This simple function takes a number inputted by a user and adds another number to it and prints the result to the page.

```javascript
function setValue(ineid, num, outeid) {
    var input = Number(document.getElementById(ineid).value);
    input += num;
    document.getElementById(outeid).innerHTML = input;
}
```

The parameter `ineid` is the element id of the user input and we access the data by searching the document for this element and returning its value. You should also note that the result of this is wrapped inside a call to the Number function to ensure that it is not treated as text.
You would need an input box in your HTML file – e.g.

```html
<input id="inputData" type="number" placeholder="Some number">
```

You could call it using an onclick event as above or using an anonymous function in your JavaScript file

```javascript
document.getElementById("calculate").onclick = function() {
    setValue("inputData", 10, "outputData");
};
```

In this instance “calculate” is the ID of the HTML button element this function is assigned to.

```html
<button type="button" id="calculate">
```

The advantage of using this approach is that your implementation details are somewhat hidden from the user – if they view your source HTML file they cannot see your function name so don’t get an insight into how your code works making things harder to hack.
There is a simple example of all this code put together on [Canvas](https://canvas.anglia.ac.uk/courses/39956/files/5147048?module_item_id=2241352)– `Changeling.html` & `Changeling.js`.

## Task 1

You are to create a new web page using external CSS that enables a user to enter:

- Total bill amount
- Tip rate as a percentage – select from 0%, 5%, 10%, 15%, 20%
- Number of people

The user should then be able to click a button that invokes some JavaScript defined in an external file that calculates the total bill amount with tip and the amount everyone should pay assuming it is split evenly – this should be displayed appropriately on your web page.

As you develop you code use the debugger to test for errors etc and capture evidence of this showing:

- Using a breakpoint
- Stepping through the code
- Inspecting a variable

Once working you should

- Check for valid numbers
- Inform the user which input items are not valid
- Use CSS to control the look of your error messages

## Task 2

Develop your web page to enable the user to add a series of menu items bought and the cost of each.
Remove the ability for a user to input the total bill amount and populate this the sum of all the items in your list once the user presses the button.

## Task 3

Create a web page that enables the user to create a simple ToDo list and then tick things that are completed. Note we are not expecting this to use persistent data, i.e., refreshing the page will clear it.

## Resources

- https://www.w3schools.com/js/
- https://www.tutorialspoint.com/javascript/
- https://codepen.io/cphemm/pen/reNwWd
- https://codepen.io/JohnPaulFich/pen/MXmzzM

[back](../README.md)