# Day 1 - Introduction to Bootstrap

![image](https://github.com/ross-bish/Bootstrap/assets/83789503/ce5b5616-1e22-4f51-a2bc-d7eb701fab8c)

Today we are going to explore and learn how to create a bunch of different features for our webpage using Bootstrap.

## Getting started 👨🏽‍💻
1. I want you to click into [Trinket](https://trinket.io/) and set up an account.
2. Now click on the blue button, select **HTML** and create a file called **Introduction to Bootstrap**.

Now we need to add our boiler plate code shown below.

### 🤔 Question to make you think?
Can you remember what `<tags>` our HTML documents must always have?
Discuss this with yoru classmates for a moment and see what you can remember.

<details>
  <summary>👀Hint:</summary>
  
````html
  <html></html>
  <body></body>
  <head></head>
  <title></title>
  
````
</details>

### How Do You Use Bootstrap?
To use Bootstrap, you include its `CSS` and `JavaScript` files in your HTML document. 

- Remember to add these lines of code inside your `<head>` tags.
- This gives you access to all the pre-made styles and interactive features.

````html
<!-- Include Bootstrap CSS -->
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">

<!-- Include Bootstrap JavaScript -->
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
````

Next, you need to add this line of code just above your closing body tag `</body>`.

````html
<!-- Bootstrap Scripts -->
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
````

## Challenges ⚔️
Working together with your classmates, I want you to try to complete the following challenges. Where possible, type up the code yourself, don't just copy and paste it into your editor.

### 💡Note: 
You must include _**comments**_ with your code, explaining what each section `<div>` does.

  - Can you remember how to add comments into `HMTL`?

### Task 1 - Jumbotron
Type up the following code to add your first Bootstrap Container.
````html
  <!-- Header with Jumbotron -->
  <div class="container-fluid p-5 bg-primary text-white text-center">
    <h1>My First Bootstrap Page</h1>
    <p>Resize this responsive page to see the effect!</p>
  </div>
````

### Task 2 - General Information Section
Now we are going to create a general information section at the top of our webpage, beneath our Jumbotron Header.
````html
<!-- General Information Section -->
<div class="container mt-5">
  <div class="row">
    <div class="col-md-12">
      <h2>General Information</h2>
      <p>The International Space Station (ISS) is a habitable artificial satellite...</p>
      <!-- Add more content as needed -->
    </div>
  </div>
</div>
````
I've given you a little hint in this piece of code as to what your next assignment will be...can you figure it out? 🛰️

### Task 3 - Adding Columns of Text 🏛️
Next we are going to create columns of text across our webpage. 

- Bootstrap's grid system allows up to **12 columns** across the page.
- If you do not want to use all 12 columns individually, you can group the columns together to create wider columns:
![image](https://github.com/ross-bish/Bootstrap/assets/83789503/7dab612e-d402-4696-ae0e-0285b8c8e077)


Bootstrap uses 12 columns across the page, so to make 3 equal columns, we will make each section 4 columns wide.

- Please take your time typing this up.
- Try to use the <kbd>tab</kbd> button to format your code.
- Remember to add _**comments**_ to explain what your code does.

````html
  <div class="container mt-5">
    <div class="row">
      <div class="col-sm-4">
        <h3>Column 1</h3>
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit...</p>
        <p>Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris...</p>
      </div>
      <div class="col-sm-4">
        <h3>Column 2</h3>
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit...</p>
        <p>Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris...</p>
      </div>
      <div class="col-sm-4">
        <h3>Column 3</h3>
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit...</p>
        <p>Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris...</p>
      </div>
    </div>
  </div>
````

You can find more information on Bootstrap Grid System [here](https://www.w3schools.com/bootstrap/bootstrap_grid_system.asp).


### Task 4 - More Containers
What if we want to inlcude another heading or container in the middle of our page? 
We can use the code shown below, notice how the **font** and **background colour** are changed inside the first `<div>` tag.

````html
  <div class="container p-5 my-5 border">
    <h1>My First Bootstrap Page</h1>
    <p>This container has a border and some extra padding and margins.</p>
  </div>

  <div class="container p-5 my-5 bg-dark text-white">
    <h1>My First Bootstrap Page</h1>
    <p>This container has a dark background color and a white text, and some extra padding and margins.</p>
  </div>

  <div class="container p-5 my-5 bg-primary text-white">
    <h1>My First Bootstrap Page</h1>
    <p>This container has a blue background color and a white text, and some extra padding and margins.</p>
  </div>
````
Again, add _**comments**_ to explain what your code does.

### Task 5 - Headings and Secondary Text 
If you can think back to last year, `<h1>` tags made the largest headings, while `<h6>` tags made the smallest. 
Here's an example showing how we can add headings and also add smaller secondary text to our webpage.

````html
  <div class="container mt-3">
    <h1>Smaller, Secondary Text</h1>
    <p>The small element (and the .small class) is used to create a smaller, secondary text in any heading:</p>
    <h1>h1 heading <small>secondary text</small></h1>
    <h2>h2 heading <small>secondary text</small></h2>
    <h3>h3 heading <small>secondary text</small></h3>
    <h4>h4 heading <small>secondary text</small></h4>
    <h5>h5 heading <small>secondary text</small></h5>
    <h6>h6 heading <small>secondary text</small></h6>
  </div>
````

### Task 6 - Highlight Text
What if we wanted to highlight a piece of text within our webpage?
````html
<div class="container mt-3">
    <h1>Highlight Text</h1>
    <p>Use the mark element (or the .mark class) to <mark>highlight</mark> text.</p>
  </div>
````

### Task 7 - Keyboard Inputs ⌨️
Perhaps you wanted to create a gaming webpage showing which controls to use while playing the game, or simply give some keyboard commands, the following code could be useful.
````html
  <div class="container mt-3">
    <h1>Keyboard Inputs</h1>
    <p>To indicate input that is typically entered via the keyboard, use the kbd element:</p>
    <p>Use <kbd>ctrl + p</kbd> to open the Print dialog box.</p>
  </div>
````
Again, add _**comments**_ to explain what your code does.


### Task 8 - Set a background colour with contrasting foreground colour.🌈
Let's experiment again with background and text colours.

````html
<div class="container mt-3">
    <h2>Background Color with Contrasting Text Color</h2>
    <p class="text-bg-primary">This text is important.</p>
    <p class="text-bg-success">This text indicates success.</p>
    <p class="text-bg-info">This text represents some information.</p>
    <p class="text-bg-warning">This text represents a warning.</p>
    <p class="text-bg-danger">This text represents danger.</p>
    <p class="text-bg-secondary">Secondary background color.</p>
    <p class="text-bg-dark">Dark grey background color.</p>
    <p class="text-bg-light">Light grey background color.</p>
  </div>
````


### Task 9 - Tables 
We did a lot of work last year with `<table>` tags. 

Remember what we learned last year
- table rows `<tr>`go left to right.
- table columns (headings) `<th>` go top to bottom.

Also, while we type up our code from top to bottom, it appears in the table rows _left -> right._

Take a look at the following examples below.

#### Hover
````html
<div class="container mt-3">
    <h2>Hover Rows</h2>
    <p>The .table-hover class enables a hover state (grey background on mouse over) on table rows:</p>
    <table class="table table-hover">
      <thead>
        <tr>
          <th>Firstname</th>
          <th>Lastname</th>
          <th>Email</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>Ada</td>
          <td>Lovelace</td>
          <td>ada@example.com</td>
        </tr>
        <tr>
          <td>Alan</td>
          <td>Turing</td>
          <td>alan@example.com</td>
        </tr>
        <tr>
          <td>Tim</td>
          <td>Berners-Lee</td>
          <td>tim@example.com</td>
        </tr>
      </tbody>
    </table>
  </div>
````

#### Dark
````html
 <div class="container mt-3">
    <h2>Hoverable Dark Table</h2>
    <p>The .table-hover class adds a hover effect (grey background color) on table rows:</p>
    <table class="table table-dark table-hover">
      <thead>
        <tr>
          <th>Firstname</th>
          <th>Lastname</th>
          <th>Email</th>
        </tr>
      </thead>
     <tbody>
        <tr>
          <td>Ada</td>
          <td>Lovelace</td>
          <td>ada@example.com</td>
        </tr>
        <tr>
          <td>Alan</td>
          <td>Turing</td>
          <td>alan@example.com</td>
        </tr>
        <tr>
          <td>Tim</td>
          <td>Berners-Lee</td>
          <td>tim@example.com</td>
        </tr>
      </tbody>
    </table>
  </div>
````

### Buttons - 
Bootstrap includes several predefined button styles, each serving its own semantic purpose

Semantics is ...
