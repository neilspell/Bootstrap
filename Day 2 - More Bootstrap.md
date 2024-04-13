# Day 2 - More Bootstrap 
![image](https://github.com/ross-bish/Bootstrap/assets/83789503/ce5b5616-1e22-4f51-a2bc-d7eb701fab8c)

![image](https://github.com/ross-bish/Bootstrap/assets/83789503/4634393c-bedf-448f-89ef-f19616c9d12d)


Today we are going to explore some more features that Bootstrap offers us for web design.

## Getting started 👨🏽‍💻
1. I want you to click into [Trinket](https://trinket.io/).
2. Now click on the blue button, select **HTML** and create a new file called **Day 2 - Bootstrap**.

Now we need to add our boiler plate code again, just like last week.

### How Do You Use Bootstrap?
To use Bootstrap, you include its `CSS` and `JavaScript` files in your HTML document. 

- Remember to add these lines of code inside your `<head>` tags.
- This gives you access to all the pre-made styles and interactive features.

````html

<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>ISS Website</title>

<!-- Bootstrap CSS -->
<link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css">

<!-- Include Bootstrap JavaScript -->
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
````

Next, you need to add this line of code just above your closing body tag `</body>`.

````html
<!-- Bootstrap JS and dependencies -->
<script src="https://code.jquery.com/jquery-3.5.1.slim.min.js"></script>
<script src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.5.4/dist/umd/popper.min.js"></script>
<script src="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/js/bootstrap.min.js"></script>

````

## Challenges ⚔️
Working together with your classmates, I want you to try to complete the following challenges. Where possible, type up the code yourself, don't just copy and paste it into your editor.

### 💡Note: 
You must include _**comments**_ with your code, explaining what each section `<div>` does.


### Task 1 - Bootstrap Cards
Type up the following code to create Bootsrap Cards. 

These can be used in your _ISS - Website_ to display information about current / past crew members. 

````html
<!-- Crew Section with Bootstrap Cards -->
<div class="container mt-5">
  <h2>Current Crew Members</h2>
  <div class="row">

    <div class="col-md-4">
      <div class="card">
        <img src="crew_member1.jpg" class="card-img-top" alt="Crew Member 1">
        <div class="card-body">
          <h5 class="card-title">Neil Armstrong </h5>
          <p class="card-text">Mission Specialist</p>
          <!-- Add more details as needed -->
        </div>
      </div>
    </div>

    <div class="col-md-4">
      <div class="card">
        <img src="crew_member1.jpg" class="card-img-top" alt="Crew Member 1">
        <div class="card-body">
          <h5 class="card-title">Buzz Aldrin </h5>
          <p class="card-text">Mission Specialist</p>
          <!-- Add more details as needed -->
        </div>
      </div>
    </div>
    <!-- Repeat the card structure for other crew members -->

  </div>
</div>
````

### Task 2 - Timeline Cards & Modal Windows
Type up the following code to create a timeline card, which could be used to display key dates or mission milestones that occurred onboard the ISS. 🛰️ 

````html
<!-- Timeline Component with Bootstrap Cards -->
<div class="container mt-5">
  <div class="timeline-entry">
    <div class="card">
      <div class="card-body">
        <h5 class="card-title">2000</h5>
        <p class="card-text">Construction of the ISS begins with the launch of the first module, Zarya.</p>
        <!-- Add more details as needed -->
        <button type="button" class="btn btn-primary" data-bs-toggle="modal" data-bs-target="#modal2000">
          View Details
        </button>
      </div>
    </div>
  </div>
````
#### Modals
Let's add a little more style to our cards using a **Modal Windows**.

- A _modal window_ is a graphical control element subordinate to an application's main window. 
- A _modal window_ creates a mode that disables user interaction with the main window but keeps it visible, with the modal window as a child window in front of it.

````html
<!-- Modals for more Detailed Information -->
<div class="modal fade" id="modal2000" tabindex="-1" aria-labelledby="modal2000Label" aria-hidden="true">
  <div class="modal-dialog">
    <div class="modal-content">
      <div class="modal-header">
        <h5 class="modal-title" id="modal2000Label">Year 2000: Construction Begins</h5>
        <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
      </div>
      <div class="modal-body">
        <p>Detailed information about the construction of the ISS in the year 2000...</p>
      </div>
    </div>
  </div>
</div>
````

### Task 3 - Alerts
Now let's see if we can add a little more interaction to our page using alert boxes.

Type up the following code to create a **Success** alert box.
````html
    <div class="container mt-3">
    <h2>Alerts</h2>
    <p>The button with class="btn-close" and data-bs-dismiss="alert" is used to close the alert box.</p>
    
    
    <div class="alert alert-success alert-dismissible">
      <button type="button" class="btn-close" data-bs-dismiss="alert"></button>
      <strong>Success!</strong> This alert box could indicate a successful or positive action.
    </div> 
````

Now using the sample code shown below, create some more alert boxes, can you spot how the colour of the alerts changes??

**Info Alert**
````html
    <div class="alert alert-info alert-dismissible">
      <button type="button" class="btn-close" data-bs-dismiss="alert"></button>
      <strong>Info!</strong> This alert box could indicate a neutral informative change or action.
    </div>
````

**Warning Alert**
````html
    <div class="alert alert-warning alert-dismissible">
      <button type="button" class="btn-close" data-bs-dismiss="alert"></button>
      <strong>Warning!</strong> This alert box could indicate a warning that might need attention.
    </div>
````

**Danger Alert**
````html
    <div class="alert alert-danger alert-dismissible">
      <button type="button" class="btn-close" data-bs-dismiss="alert"></button>
      <strong>Danger!</strong> This alert box could indicate a dangerous or potentially negative action.
    </div>
````


### Task 4 - Progress Bar (with label)
If we created a website with multiple pages, to inform the user of how far they have navigated, we could use the following feature.

````html
  <div class="container mt-3">
    <h2>Progress Bar With Label</h2>
    <div class="progress">
      <div class="progress-bar" style="width:20%">20%</div>
    </div>
  </div>
````

👨🏽‍💻 Experiment with the code and see if you can create different progress bars with varying degrees of _progress_.


### Task 5 - Pagination
To accompany this progress bar, perhaps we want to include page numbers on our website, this can be done using **pagination.**

**Basic Pagination**
````html
<div class="container mt-3">
    <h2>Pagination</h2>
    <p>To create a basic pagination, add the .pagination class to an ul element. Then add the .page-item to each li
      element and a .page-link class to each link inside li:</p>
    <ul class="pagination">
      <li class="page-item"><a class="page-link" href="#">Previous</a></li>
      <li class="page-item"><a class="page-link" href="#">1</a></li>
      <li class="page-item"><a class="page-link" href="#">2</a></li>
      <li class="page-item"><a class="page-link" href="#">3</a></li>
      <li class="page-item"><a class="page-link" href="#">Next</a></li>
    </ul>
</div>
````

**Pagination - Active State**
````html
<div class="container mt-3">
    <h2>Pagination - Active State</h2>
    <p>Add class .active to let the user know which page he/she is on:</p>
    <ul class="pagination">
      <li class="page-item"><a class="page-link" href="#">Previous</a></li>
      <li class="page-item"><a class="page-link" href="#">1</a></li>
      <li class="page-item active"><a class="page-link" href="#">2</a></li>
      <li class="page-item"><a class="page-link" href="#">3</a></li>
      <li class="page-item"><a class="page-link" href="#">Next</a></li>
    </ul>
</div>
````

### Task 6 - Breadcrumbs
Perhaps you'd prefer to leave a trail of the users' navigation behind, rather than a page number. 

In that case, we can use **breadcrumbs**.

````html
<div class="container mt-3">
    <h2>Breadcrumbs</h2>
    <p>The .breadcrumb class indicates the current page's location within a navigational hierarchy:</p>
    <ul class="breadcrumb">
      <li class="breadcrumb-item"><a href="#">Photos</a></li>
      <li class="breadcrumb-item"><a href="#">Summer 2017</a></li>
      <li class="breadcrumb-item"><a href="#">Italy</a></li>
      <li class="breadcrumb-item active">Rome</li>
    </ul>
</div>
````

### Task 7 - Navigation Bar
Instead of using **_pagination_** or **_breadcrumbs_** (or perhaps in conjunction with one of them), we can add a **_Navigation Bar_** to the top of our webpage.

Add the following code just beneath your **Jumbotron** `<div>` at the top of your code.

````html
<nav class="navbar navbar-expand-lg navbar-dark bg-dark">
  <a class="navbar-brand" href="#">Space Mission</a>
  <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
    <span class="navbar-toggler-icon"></span>
  </button>

  <div class="collapse navbar-collapse" id="navbarSupportedContent">
    <ul class="navbar-nav mr-auto">
      <li class="nav-item active">
        <a class="nav-link" href="#">Home <span class="sr-only">(current)</span></a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="#">Past Missions</a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="#">Astro Pi</a>
      </li>
    </ul>
  </div>
</nav>
````
👨🏽‍💻 Experiment with some of the classes in the code to see if you can change the appearance, or add more _items_.

### Task 8 - Photo Carousel 📸
A Photo Carousel allows the user to view various photos related to one another, this can be on a _click-command_ or _automated_.
The following example shows how to create a basic carousel with indicators and controls.

1. Add the following code inside your `<body>` tags, try to pick a suitable place that will make the webpage look good.😎

````html
<div id="carouselExampleIndicators" class="carousel slide" data-ride="carousel">
  <ol class="carousel-indicators">
    <li data-target="#carouselExampleIndicators" data-slide-to="0" class="active"></li>
    <li data-target="#carouselExampleIndicators" data-slide-to="1"></li>
    <li data-target="#carouselExampleIndicators" data-slide-to="2"></li>
  </ol>
  <div class="carousel-inner">
    <div class="carousel-item active">
      <img class="d-block w-100" src="insert URL here" alt="First slide">
    </div>
    <div class="carousel-item">
      <img class="d-block w-100" src="insert URL here" alt="Second slide">
    </div>
    <div class="carousel-item">
      <img class="d-block w-100" src="insert URL here" alt="Third slide">
    </div>
  </div>
  <a class="carousel-control-prev" href="#carouselExampleIndicators" role="button" data-slide="prev">
    <span class="carousel-control-prev-icon" aria-hidden="true"></span>
    <span class="sr-only">Previous</span>
  </a>
  <a class="carousel-control-next" href="#carouselExampleIndicators" role="button" data-slide="next">
    <span class="carousel-control-next-icon" aria-hidden="true"></span>
    <span class="sr-only">Next</span>
  </a>
</div>
````
2. You will now have to find _**3 photographs**_ and copy & paste their URLs into the `src="insert URL here"` code above.

- Work together with your classmates to see if you can get this feature to work.
- Can you remember how we add photos to a webpage?

3. Perhaps you have noticed that the **Photo Carousel** is the full width of our webpage.

   This may be a feature you wish to keep, if not, we can add a little piece of `CSS` code inside our `<head>` tags and then add one final `<div>` just above our main Carousel code in the `<body>`.

   Add the following code inside your `<head>` tags.

````html

   <style>
    /* Custom style for limiting carousel width */
    .custom-carousel-container {
      width: 70%;
      margin: 0 auto; /* Center the container */
    }
  </style>

````
4. Now add this line of code at the top of the **Photo Carousel** `<div>`.

````html
<!-- Carousel with limited width -->
<div class="custom-carousel-container">
````

💡**Remember:** We then need to close this at the end of the code block using a `</div>` tag.

Now our Photo Carousel should take up ``70%`` of our screen. 

👨🏽‍💻 Experiment with these values to see which setting you prefer.
