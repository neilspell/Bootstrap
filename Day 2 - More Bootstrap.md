# Day 2 - More Bootstrap

![image](https://github.com/ross-bish/Bootstrap/assets/83789503/ce5b5616-1e22-4f51-a2bc-d7eb701fab8c)

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

### Task 1 - Timeline Cards & Modal Windows
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
Let's add a litte more style to our cards using a **Modal Windows**.

- A _modal window_ is a graphical control element subordinate to an application's main window. 
- A modal window creates a mode that disables user interaction with the main window but keeps it visible, with the modal window as a child window in front of it.

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
