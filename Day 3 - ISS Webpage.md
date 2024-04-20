# International Space Station

![image](https://github.com/ross-bish/Bootstrap/assets/83789503/4c005cc9-f3cf-42c2-9e4a-49dc47d7e1f5)

## Assignment - Design a Webpage 📚👨🏽‍💻

Building on the Bootstrap skills you have learned, you are asked to create a Bootstrap webpage about the ISS (International Space Station) and your Astro Pi - Mission Zero project.

### Getting started 👨🏽‍💻
1. I want you to click into [Trinket](https://trinket.io/).
2. Now click on the blue button, select **HTML** and create a new file called **Day 3 - ISS Webpage**.

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


## Assignment ⚔️
You can use some / all of the suggestions below to create your webpage.

However, your webpage must have the following **3 sections**:

1. Information Hub
2. Timeline: Chronological Information Display
3. Astro Pi - Mission Zero Project

<br>

## 1. Information Hub
Header and Introduction:
   - Use a Jumbotron to create an eye-catching header with a background image of the ISS or space.
   - Include a welcoming message, such as "Explore the International Space Station," to set the tone.

Grid System for Sections:
   - Divide the webpage into sections using Bootstrap's grid system (container, rows, and columns).
   - Create a "General Information" section with facts about the ISS, its purpose, and key specifications.
   - Add a "Crew" section with Bootstrap cards displaying information about the current crew members.
   - Include a "Mission Updates" section using Bootstrap alerts to highlight recent developments or news.

Card Components for Crew Members:
   - In the "Crew" section, use Bootstrap cards to present individual crew members.
   - Include an image, name, position, and a brief description for each crew member within the card.
   - Use the card layout to keep information organized and visually appealing.

Alerts for Mission Updates:
   - Implement Bootstrap alerts within the "Mission Updates" section to notify users about recent events.
   - Include a mix of success alerts for positive updates and danger alerts for critical announcements.
   - Enhance the alerts with relevant icons and colors to catch the user's attention.

Image Gallery:
   - Create a gallery section using Bootstrap's card component to showcase images of the International Space Station.
   - Add responsive images and captions to provide context for each image.
   - Use the grid system to arrange the gallery in an aesthetically pleasing layout.


## 2. Timeline: Chronological Information Display
Timeline Component:
   - Create a timeline using Bootstrap's grid system, arranging events chronologically.
   - Each timeline entry can be a Bootstrap card, containing information about a specific event in the history of the ISS.
   - Include images, dates, and concise descriptions for each event.

 Button Navigation:
   - Implement Bootstrap buttons to allow users to navigate to different time periods within the timeline.
   - Each button can represent a significant era or phase in the history of the ISS.
   - Add smooth scrolling functionality to enhance the user experience when jumping to different sections.

Modals for Detailed Information:
   - Use Bootstrap modals to display detailed information when users click on a specific timeline entry.
   - Include additional images, videos, or links related to the event within the modal.
   - Ensure that the modals are visually appealing and provide a seamless transition from the timeline.



## 3. Astro Pi - Mission Zero Project
Mission Zero Description
   - Explain the mission brief and purpose of Astro Pi - Mission Zero

What did you create?
   - Describe what you created _(flora / fauna display)_.
   - Include a _**code window**_ showing the Python code you submitted.

````python

# Import the libraries
from sense_hat import SenseHat
from time import sleep

# Set up the Sense HAT
sense = SenseHat()
sense.set_rotation(270)

# Set up the colour sensor
sense.color.gain = 60 # Set the sensitivity of the sensor
sense.color.integration_cycles = 64 # The interval at which the reading will be taken

# Add colour variables and image

c = (0, 0, 0) # Black
m = (34, 139, 34) # ForestGreen
q = (255, 255, 0) # Yellow
t = (255, 140, 0) # DarkOrange
y = (255, 20, 147) # DeepPink

for i in range(28):
  rgb = sense.color # get the colour from the sensor
  c = (rgb.red, rgb.green, rgb.blue)

  image = [
    c, c, y, y, y, y, c, c,
    c, y, y, t, t, y, y, c,
    y, y, t, q, q, t, y, y,
    c, y, y, t, t, y, y, c,
    c, c, y, y, y, y, c, c,
    m, c, c, m, m, c, c, m,
    c, m, m, m, m, m, m, c,
    c, c, c, m, m, c, c, c]

  # Display the image

  sense.set_pixels(image)
  sleep(1)

x = (178, 34, 34)  # choose your own red, green, blue values between 0 - 255
sense.clear(x)

````
Include an image of the display you created.
   - For example - Fauna or Flora

![image](https://github.com/ross-bish/Bootstrap/assets/83789503/4a83c4b2-6b19-47f0-a846-2ecf0f6acab2)

![image](https://github.com/ross-bish/Bootstrap/assets/83789503/2ff1fc27-08d3-48c6-b262-d0e102b600e8)

