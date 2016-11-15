# Optimization-Project
Optimization Project For Front End Nanodegree Program
## Website Performance Optimization portfolio project

###Running the Application
- Clone the repository or download the zip file
- To inspect the site on your phone, you can run a local server

  ```bash
  $> cd /path/to/your-project-folder
  $> python -m SimpleHTTPServer 8080
  ```
- Open a browser and visit localhost:8080
- Open the webpage remotely using GitHub Pages URL: https://prasanna4617.github.io/Optimization-Project/
- Copy the URL and paste it in the Pagespeed Insights to analyse the pagespeed
- To check the framerate:
    - Go to timeline menu in the developer tools
    - Hit record button and scroll through the page and stop it
- To check the computational effiency, click on the console menu in the dev tools

### Optimization Made
#### Part 1: Optimize PageSpeed Insights score for index.html
- Minify CSS
- **Optimized images** in index.html
- Moved JS and CSS files to the end of the html file
- Made JS **async** to avoid blocking

#### Part 2: Optimize Frames per Second in pizza.html
To optimize views/pizza.html, you will need to modify views/js/main.js until your frames per second rate is 60 fps or higher.
- Changes made in **UpdatePosition** function in main.js
- Used CSS transitions(translate and transform) 
- Included **backface-visibility: hidden** to the .mover class so it would generate seperate layers for the background pizzas

#### Part 3: Check the Computional Efficiency
- Changes made in **ChangePizzaSizes** function in main.js
- RandomPizza variable is created outside of the _for_ loop to avoid forced synchronous layout
   
