# Ex.07 Design of Interactive Image Gallery
## Date:26.12.2025

## AIM:
To design a web application for an inteactive image gallery for a minimum five images with next and previous buttons.

## DESIGN STEPS:

### Step 1:
Clone the github repository and create Django admin interface.

### Step 2:
Change settings.py file to allow request from all hosts.

### Step 3:
Use CSS for positioning and styling.

### Step 4:
Write JavaScript program for implementing interactivity.

### Step 5:
Validate the HTML and CSS code.

### Step 6:
Publish the website in the given URL.

## PROGRAM:
```
gallery.html

<head>
    <title>Interactive Image Gallery</title>
    <link href="styles.css" rel="stylesheet">
</head>
<body>
    <header class="header">
        <h1>Image Gallery</h1>
    </header>

    <div class="container">
        <div class="card">
            <img id="galleryImage" src="coldcoffe.jpg"alt="Gallery Image">
            <p class="caption" id="caption">Cold Coffee</p>

            <div class="buttons">
                <button onclick="prevImage()">Previous</button>
                <button onclick="nextImage()">Next</button>
            </div>
        </div>
    </div>

    <footer class="footer">
        Daffodil Irene.S(25002685)
    </footer>

    <script>
        let gallery = [
            { src: "coldcoffe.jpg", text: "Cold Coffee" },
            { src: "cp.jpeg", text: "Cappuccino" },
            { src: "filter.jpg", text: "Filter Coffee" },
            { src: "ice.jpg", text: "Americano" },
            { src: "blackcoffe.jpg", text: "Black Coffee" }
        ];
        let index = 0;
        function nextImage() {
            index++;
            if (index >= gallery.length) {
                index = 0;
            }
            updateImage();
        }
        function prevImage() {
            index--;
            if (index < 0) {
                index = gallery.length - 1;
            }
            updateImage();
        }
        function updateImage() {
            document.getElementById("galleryImage").src = gallery[index].src;
            document.getElementById("caption").innerText = gallery[index].text;
        }
    </script>
</body>
</html>


styles.css


* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    background-image:url(bgcf.jpg);
    background-repeat: no-repeat;
    background-size: cover;
    background-position:center;
    display: flex;
    flex-direction: column;
    min-height: 100vh;
}

.header {
    background-color: rgba(101, 16, 16, 0.679);
    color: white;
    text-align: center;
    padding: 15px;
}

.container {
    flex: 1;
    display: flex;
    justify-content: center;
    align-items: center;
}

.card {
    background-color: rgb(91, 48, 9);
    padding: 15px;
    border-radius: 12px;
    box-shadow: 0 10px 25px rgba(0,0,0,0.15);
    text-align: center;
    width: 300px;
}

.card img {
    width: 220px;
    height: 220px;
    object-fit: cover;
    border-radius: 10px;
    margin-bottom: 10px;
}

.caption {
    margin: 15px 0;
    font-size: 16px;
    font-weight: bold;
}

.buttons {
    display: flex;
    justify-content: center;
    gap: 15px;
}

.buttons button {
    background-color: rgb(81, 8, 8);
    color: rgba(255, 255, 255, 0.773);
    border: none;
    padding: 10px 18px;
    border-radius: 8px;
    cursor: pointer;
}

.buttons button:hover {
    background-color: rgba(128, 39, 39, 0.875);
}

.footer {
    background-color: rgba(129, 23, 23, 0.693);
    color: white;
    text-align: center;
    padding: 12px;
}


















```

## OUTPUT:
![alt text](<Screenshot (37).png>)

## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
