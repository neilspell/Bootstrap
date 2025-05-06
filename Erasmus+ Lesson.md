# Bootstrap & HTML/CSS Lesson Template

## Introduction

Welcome to our web development workshop! In this lesson, you'll work in pairs (Czech and Irish students) to create a webpage documenting the Czech students' stay in Galway. You'll learn how to use HTML, CSS, and Bootstrap to create responsive, attractive web pages with various interactive elements.

## Project Overview

You will create a small website with **3 pages**:
1. **Home** - Introduction and overview of the visit
2. **Gallery** - Photos from the visit
3. **Experiences** - Stories and highlights

## Setup

1. Create a folder for your project
2. Create three HTML files: `index.html`, `gallery.html`, and `experiences.html`
3. Link Bootstrap to your HTML by adding this to the `<head>` of each file:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Our Galway Adventure</title>
    <!-- Bootstrap CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/css/bootstrap.min.css" rel="stylesheet">
    <!-- Optional custom CSS file -->
    <link href="style.css" rel="stylesheet">
</head>
<body>
    <!-- Content goes here -->

    <!-- Bootstrap JS Bundle with Popper -->
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
```

## 1. Navigation Bar

A navigation bar (navbar) helps users navigate between pages. Add this code after the opening `<body>` tag in each HTML file:

```html
<nav class="navbar navbar-expand-lg navbar-dark bg-primary">
  <div class="container">
    <a class="navbar-brand" href="index.html">Galway Adventure</a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNav">
      <ul class="navbar-nav">
        <li class="nav-item">
          <a class="nav-link" href="index.html">Home</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="gallery.html">Gallery</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="experiences.html">Experiences</a>
        </li>
      </ul>
    </div>
  </div>
</nav>
```

**Explanation:**
- The navbar uses Bootstrap classes for styling and responsiveness
- It collapses into a hamburger menu on smaller screens
- The active page can be highlighted by adding `active` class to the corresponding nav-item

## 2. Jumbotron (Hero Section)

A jumbotron is a large banner section that grabs attention. While Bootstrap 5 no longer has a specific "jumbotron" component, we can create one using other Bootstrap classes:

```html
<div class="container mt-4">
  <div class="p-5 mb-4 bg-light rounded-3">
    <div class="container-fluid py-5">
      <h1 class="display-5 fw-bold">Welcome to Our Galway Adventure!</h1>
      <p class="col-md-8 fs-4">Documenting the amazing experience of Czech students visiting Galway, Ireland through the Erasmus+ exchange program.</p>
      <button class="btn btn-primary btn-lg" type="button" data-bs-toggle="modal" data-bs-target="#welcomeModal">Learn More</button>
    </div>
  </div>
</div>
```

## 3. Bootstrap Grid System and Spans

Bootstrap's grid system divides the screen into 12 columns, allowing for responsive layouts. Columns are defined within rows, and you specify how many columns each element should span.

```html
<div class="container mt-4">
  <h2>About Our Exchange</h2>
  <div class="row">
    <!-- This column spans 4 out of 12 columns on medium screens and larger -->
    <div class="col-md-4">
      <h3>Czech Republic</h3>
      <p>Information about the visiting students and their school.</p>
    </div>
    <!-- This column spans 4 out of 12 columns on medium screens and larger -->
    <div class="col-md-4">
      <h3>Ireland</h3>
      <p>Information about the host school and Galway.</p>
    </div>
    <!-- This column spans 4 out of 12 columns on medium screens and larger -->
    <div class="col-md-4">
      <h3>Erasmus+</h3>
      <p>Information about the Erasmus+ program.</p>
    </div>
  </div>
</div>
```

**Explanation of Bootstrap Spans:**
- `col-md-4` means "on medium screens and larger, span 4 out of 12 columns"
- Common prefixes:
  - `col-` (extra small screens, <576px)
  - `col-sm-` (small screens, ≥576px)
  - `col-md-` (medium screens, ≥768px)
  - `col-lg-` (large screens, ≥992px)
  - `col-xl-` (extra large screens, ≥1200px)
- Example: `col-sm-6 col-md-4` means "span 6 columns on small screens, but 4 columns on medium screens and up"

## 4. Bootstrap Cards

Cards are flexible containers for displaying content. Add this to your page:

```html
<div class="container mt-4">
  <h2>Highlights of Our Visit</h2>
  <div class="row">
    <div class="col-md-4 mb-4">
      <div class="card">
        <img src="https://via.placeholder.com/300x200" class="card-img-top" alt="Placeholder Image">
        <div class="card-body">
          <h5 class="card-title">Aran Islands</h5>
          <p class="card-text">Our amazing trip to see the spectacular Aran Islands on the west coast of Ireland.</p>
          <a href="#" class="btn btn-primary">View Details</a>
        </div>
      </div>
    </div>
    
    <div class="col-md-4 mb-4">
      <div class="card">
        <img src="https://via.placeholder.com/300x200" class="card-img-top" alt="Placeholder Image">
        <div class="card-body">
          <h5 class="card-title">Galway City</h5>
          <p class="card-text">Exploring the vibrant streets and culture of Galway city center.</p>
          <a href="#" class="btn btn-primary">View Details</a>
        </div>
      </div>
    </div>
    
    <div class="col-md-4 mb-4">
      <div class="card">
        <img src="https://via.placeholder.com/300x200" class="card-img-top" alt="Placeholder Image">
        <div class="card-body">
          <h5 class="card-title">School Activities</h5>
          <p class="card-text">Collaborative projects and activities at the host school.</p>
          <a href="#" class="btn btn-primary">View Details</a>
        </div>
      </div>
    </div>
  </div>
</div>
```

**Note:** Replace the placeholder images with actual photos from your visit.

## 5. Modal Windows

Modals are popup dialogs that can display additional information. Add this code before the closing `</body>` tag:

```html
<!-- Modal -->
<div class="modal fade" id="welcomeModal" tabindex="-1" aria-labelledby="welcomeModalLabel" aria-hidden="true">
  <div class="modal-dialog">
    <div class="modal-content">
      <div class="modal-header">
        <h5 class="modal-title" id="welcomeModalLabel">About Our Exchange Program</h5>
        <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
      </div>
      <div class="modal-body">
        <p>This exchange program between Ostrava (Czech Republic) and Galway (Ireland) is part of the Erasmus+ initiative, promoting cultural exchange and international cooperation in education.</p>
        <p>During this 4 day visit, students are collaborating on projects, exploring Irish culture, and forming lasting friendships.</p>
      </div>
      <div class="modal-footer">
        <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Close</button>
        <button type="button" class="btn btn-primary">Learn More</button>
      </div>
    </div>
  </div>
</div>
```

**To trigger the modal:** Use a button with `data-bs-toggle="modal" data-bs-target="#welcomeModal"` as shown in the jumbotron section.

## 6. Photo Carousel

A carousel is a slideshow for cycling through images. Add this to your Gallery page:

```html
<div class="container mt-4">
  <h2>Photo Gallery</h2>
  <div id="photoCarousel" class="carousel slide" data-bs-ride="carousel">
    <div class="carousel-indicators">
      <button type="button" data-bs-target="#photoCarousel" data-bs-slide-to="0" class="active" aria-current="true" aria-label="Slide 1"></button>
      <button type="button" data-bs-target="#photoCarousel" data-bs-slide-to="1" aria-label="Slide 2"></button>
      <button type="button" data-bs-target="#photoCarousel" data-bs-slide-to="2" aria-label="Slide 3"></button>
    </div>
    <div class="carousel-inner">
      <div class="carousel-item active">
        <img src="https://via.placeholder.com/800x400" class="d-block w-100" alt="Placeholder Image 1">
        <div class="carousel-caption d-none d-md-block">
          <h5>Galway Bay</h5>
          <p>Beautiful views of Galway Bay during our boat trip.</p>
        </div>
      </div>
      <div class="carousel-item">
        <img src="https://via.placeholder.com/800x400" class="d-block w-100" alt="Placeholder Image 2">
        <div class="carousel-caption d-none d-md-block">
          <h5>Traditional Music Session</h5>
          <p>Enjoying traditional Irish music in a local pub.</p>
        </div>
      </div>
      <div class="carousel-item">
        <img src="https://via.placeholder.com/800x400" class="d-block w-100" alt="Placeholder Image 3">
        <div class="carousel-caption d-none d-md-block">
          <h5>Classroom Activities</h5>
          <p>Working together on collaborative projects.</p>
        </div>
      </div>
    </div>
    <button class="carousel-control-prev" type="button" data-bs-target="#photoCarousel" data-bs-slide="prev">
      <span class="carousel-control-prev-icon" aria-hidden="true"></span>
      <span class="visually-hidden">Previous</span>
    </button>
    <button class="carousel-control-next" type="button" data-bs-target="#photoCarousel" data-bs-slide="next">
      <span class="carousel-control-next-icon" aria-hidden="true"></span>
      <span class="visually-hidden">Next</span>
    </button>
  </div>
</div>
```

**Note:** Replace the placeholder images with your actual photos.

## 7. Multiple Pages

Create separate HTML files for each page with similar structure:

### index.html (Home Page)
Contains:
- Navigation bar
- Jumbotron
- Grid section about the exchange
- Cards with highlights
- Modal window

### gallery.html (Gallery Page)
Contains:
- Navigation bar
- Photo carousel
- Additional photo grid (optional)

### experiences.html (Experiences Page)
Contains:
- Navigation bar
- Student testimonials/stories
- Timeline of activities

## Creating a Common Footer

Add this before the closing `</body>` tag on each page:

```html
<footer class="bg-dark text-white mt-5 py-4">
  <div class="container">
    <div class="row">
      <div class="col-md-6">
        <h5>Erasmus+ Exchange Program</h5>
        <p>A collaboration between schools in the Czech Republic and Ireland.</p>
      </div>
      <div class="col-md-6 text-md-end">
        <h5>Contact</h5>
        <p>Email: exchange@school.edu<br>
        Phone: +353 1 234 5678</p>
      </div>
    </div>
    <div class="row">
      <div class="col text-center mt-3">
        <p>&copy; 2025 Student Exchange Project</p>
      </div>
    </div>
  </div>
</footer>
```

## Custom CSS (Optional)

Create a file named `style.css` for additional customization:

```css
/* Custom styles */
body {
  font-family: 'Arial', sans-serif;
}

.carousel-item img {
  height: 400px;
  object-fit: cover;
}

.card:hover {
  box-shadow: 0 4px 8px rgba(0,0,0,0.2);
  transform: translateY(-5px);
  transition: all 0.3s ease;
}

/* Add Czech and Irish flag colors as accent colors */
.czech-accent {
  color: #11457E; /* Blue from Czech flag */
}

.irish-accent {
  color: #169B62; /* Green from Irish flag */
}
```

## Challenge Tasks for Students

1. Add a contact form to the website
2. Create a timeline of events using Bootstrap components
3. Add a map showing locations visited in Galway
4. Implement a language switcher between English and Czech
5. Add animated counters showing statistics about the exchange

## Tips for Success

1. Start with the basic structure of all three pages
2. Use placeholder images until you have your own photos
3. Test your website on different devices to ensure it's responsive
4. Collaborate by dividing tasks between partners
5. Be creative with content and design!

## Resources

- [Bootstrap Documentation](https://getbootstrap.com/docs/)
- [W3Schools HTML Tutorial](https://www.w3schools.com/html/)
- [W3Schools CSS Tutorial](https://www.w3schools.com/css/)
- [Font Awesome Icons](https://fontawesome.com/) (optional for adding icons)
