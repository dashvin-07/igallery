# Ex.08 Design of Interactive Image Gallery
## Date:10/12/24

## AIM:
To design a web application for an inteactive image gallery with minimum five images.

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

## PROGRAM :
~~~
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Responsive Image Gallery</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f0f0f0;
        }

        h1 {
            text-align: center;
            margin: 20px 0;
            color: #333;
        }

        .gallery {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 15px;
            padding: 20px;
        }

        .gallery-item {
            position: relative;
            overflow: hidden;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
            transition: transform 0.3s;
        }

        .gallery-item:hover {
            transform: scale(1.05);
        }

        .gallery-item img {
            width: 100%;
            height: 200px;
            object-fit: cover;
            border-radius: 10px;
            transition: opacity 0.3s;
        }

        .overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.8);
            display: flex;
            justify-content: center;
            align-items: center;
            z-index: 1000;
            opacity: 0;
            transition: opacity 0.3s;
        }

        .overlay img {
            max-width: 90%;
            max-height: 90%;
            border-radius: 10px;
            box-shadow: 0 0 15px rgba(0, 0, 0, 0.5);
        }

        .close {
            position: absolute;
            top: 20px;
            right: 30px;
            font-size: 30px;
            color: white;
            cursor: pointer;
            transition: color 0.3s;
        }

        .close:hover {
            color: #ff4081;
        }
    </style>
</head>
<body>
    <h1>Image Gallery</h1>
    <div class="gallery">
        <div class="gallery-item">
            <img src="sec5.jpg" alt="Image 1">
            <center><h2>MEDICAL COLLEGE</h2></center>
        </div>
        <div class="gallery-item">
            <img src="sec 2.jpg" alt="Image 2">
            <center><h2>LINES HALL</h2></center>
        </div>
        <div class="gallery-item">
            <img src="sec3.jpg" alt="Image 3">
            <center><h2>SEC</h2></center>
        </div>
        <div class="gallery-item">
            <img src="sec4.jpg" alt="Image 4">
           <center> <h2>ARTS COLLEGE</h2></center>
        </div>
       
    </div>
<img style="height: 1500;width: 1500px;" src="sec1.jpg" alt="">
<center><h2>SAVEETHA INSTITUTE OF MEDICAL AND TECHNICAL SCIENCE</h2></center>
    <div class="overlay" id="overlay">
        <span class="close" id="close">&times;</span>
        <img id="overlayImage" src="" alt="Overlay Image">
    </div>

    <script>
        const galleryItems = document.querySelectorAll('.gallery-item img');
        const overlay = document.getElementById('overlay');
        const overlayImage = document.getElementById('overlayImage');
        const closeBtn = document.getElementById('close');

        galleryItems.forEach(item => {
            item.addEventListener('click', () => {
                overlayImage.src = item.src;
                overlay.style.opacity = '1';
                overlay.style.pointerEvents = 'auto';
            });
        });

        closeBtn.addEventListener('click', () => {
            overlay.style.opacity = '0';
            overlay.style.pointerEvents = 'none';
        });

        overlay.addEventListener('click', (e) => {
            if (e.target === overlay) {
                overlay.style.opacity = '0';
                overlay.style.pointerEvents = 'none';
            }
        });
    </script>
</body>
</html>
~~~

## OUTPUT:
![Screenshot (4)](https://github.com/user-attachments/assets/a367d1d8-2b87-463f-a2f2-8cb911645dd8)
![Screenshot 2024-12-13 180432](https://github.com/user-attachments/assets/4525c0cd-e821-4c8f-897b-ed07239208ad)




## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
