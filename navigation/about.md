---
layout: post
title: About
permalink: /about/
comments: true
---

## About Me

<comment>
Some pictures of me:
</comment>
<div class="image-gallery">
  <img src="{{site.baseurl}}/images/Pics/me_and_beach.jpg" alt="Image 1">
  <img src="{{site.baseurl}}/images/Pics/me_and_cat.jpg" alt="Image 2">
  <img src="{{site.baseurl}}/images/Pics/me_at_convention.jpg" alt="Image 3">
  <img src="{{site.baseurl}}/images/Pics/me_in_india.jpg" alt="Image 4">
  <img src="{{site.baseurl}}/images/Pics/me_watermelon.jpg" alt="Image 5">
</div>
<br>
- Age: 14
- Birthday: June 1st
- Favorite Color: Red

### Locations

I've lived in California my whole life: I was born in Los Angeles and moved to San Diego. I visit India a lot, since some of my family members live there!

Some other places I've visited:
- Mexico (Cancun, Puerto Vallarta, Cabo San Lucas)
- Puerto Rico
- Costa Rica

<style>
    /* Style looks pretty compact, 
       - grid-container and grid-item are referenced the code 
    */
    .grid-container {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(150px, 1fr)); /* Dynamic columns */
        gap: 10px;
    }
    .grid-item {
        text-align: center;
    }
    .grid-item img {
        width: 100%;
        height: 100px; /* Fixed height for uniformity */
        object-fit: contain; /* Ensure the image fits within the fixed height */
    }
    .grid-item p {
        margin: 5px 0; /* Add some margin for spacing */
    }

    .image-gallery {
        display: flex;
        flex-wrap: nowrap;
        overflow-x: auto;
        gap: 10px;
        }

    .image-gallery img {
        max-height: 150px;
        object-fit: cover;
        border-radius: 5px;
    }
</style>

<!-- This grid_container class is used by CSS styling and the id is used by JavaScript connection -->
<div class="grid-container" id="grid_container">
    <!-- content will be added here by JavaScript -->
</div>

<script>
    // 1. Make a connection to the HTML container defined in the HTML div
    var container = document.getElementById("grid_container"); // This container connects to the HTML div

    // 2. Define a JavaScript object for our http source and our data rows for the Living in the World grid
    var http_source = "https://upload.wikimedia.org/wikipedia/commons/";
    var living_in_the_world = [
        {"flag": "0/01/Flag_of_California.svg", "greeting": "born in Los Angeles", "description": "California - forever"},
        {"flag": "4/41/Flag_of_India.svg", "greeting": "nationality: Indian", "description": "India 🇮🇳"},
        {"flag": "f/fc/Flag_of_Mexico.svg", "greeting": "visited Mexico", "description": "Mexico 🇲🇽"},
        {"flag": "2/28/Flag_of_Puerto_Rico.svg", "greeting": "visited Puerto Rico", "description": "Puerto Rico 🇵🇷"},
        {"flag": "f/f2/Flag_of_Costa_Rica.svg", "greeting": "visited Costa Rica", "description": "Costa Rica 🇨🇷"}
    ];

    // 3a. Consider how to update style count for size of container
    // The grid-template-columns has been defined as dynamic with auto-fill and minmax

    // 3b. Build grid items inside of our container for each row of data
    for (const location of living_in_the_world) {
        // Create a "div" with "class grid-item" for each row
        var gridItem = document.createElement("div");
        gridItem.className = "grid-item";  // This class name connects the gridItem to the CSS style elements
        // Add "img" HTML tag for the flag
        var img = document.createElement("img");
        img.src = http_source + location.flag; // concatenate the source and flag
        img.alt = location.flag + " Flag"; // add alt text for accessibility

        // Add "p" HTML tag for the description
        var description = document.createElement("p");
        description.textContent = location.description; // extract the description

        // Add "p" HTML tag for the greeting
        var greeting = document.createElement("p");
        greeting.textContent = location.greeting;  // extract the greeting

        // Append img and p HTML tags to the grid item DIV
        gridItem.appendChild(img);
        gridItem.appendChild(description);
        gridItem.appendChild(greeting);

        // Append the grid item DIV to the container DIV
        container.appendChild(gridItem);
    }
</script>

### Journey through Life

Education:

- 🏫 Elementary Schools: Peninsula Montessori in LA, Willow Grove Elementary School in SD
- 🏫 Middle School: Oak Valley Middle School
- 🏫 High School: Del Norte High School (currently a Freshman)

### Family

- There are 3 people in my family: my and my parents
- I have no siblings but LOTS of cousins!
- I own a pet lovebird named Mango
- I love spending time with my family!


<comment>
Pictures of My Family, scroll to the right for more ...
</comment>
<div class="image-gallery">
  <img src="{{site.baseurl}}/images/Pics/IMG_8239.jpg" alt="Image 1">
  <img src="{{site.baseurl}}/images/Pics/IMG_5760.jpg" alt="Image 2">
  <img src="{{site.baseurl}}/images/Pics/IMG_5463.jpg" alt="Image 3">
  <img src="{{site.baseurl}}/images/Pics/IMG_3700.jpg" alt="Image 4">
  <img src="{{site.baseurl}}/images/Pics/IMG_3447.jpg" alt="Image 5">
  <img src="{{site.baseurl}}/images/Pics/IMG_9623.jpg" alt="Image 6">

</div>

### Hobbies and Interests

- STEM-oriented: love participating in extracurriculars like Science Olympiad and cybersecurity
- I have been playing the piano since I was 5 🎹
- I like to read and write in my spare time (I am currently revising a draft of my very own novel!)
- Rollerblading w/ friends 🛼
- Currently obsessed with Stray Kids, EPIC: The Musical, and Formula 1


