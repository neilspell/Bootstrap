# Day 1 - Introduction to Bootstrap

![image](https://github.com/ross-bish/Bootstrap/assets/83789503/ce5b5616-1e22-4f51-a2bc-d7eb701fab8c)

Today we are going to explore and learn how to create a bunch of different features for our webpage using Bootstrap.

## Getting started 👨🏽‍💻
First I want you to click into `Replit` and open the **Introduction to Bootstrap** file.

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
You must include `comments` with your code, explaining what each section `<div>` does.

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

### Task 3 - Adding Columns of Text
Next we are going to create columns of text across our webpage. 

- Bootstrap's grid system allows up to 12 columns across the page.
- If you do not want to use all 12 column individually, you can group the columns together to create wider columns:
![image](https://github.com/ross-bish/Bootstrap/assets/83789503/7dab612e-d402-4696-ae0e-0285b8c8e077)


Bootstrap uses 12 columns across the page, so to make 3 equal columns, we will make each section 4 columns wide.

You can find more information on Bootstrap Grid System here [Bootstrap Grid System](https://www.w3schools.com/bootstrap/bootstrap_grid_system.asp).
