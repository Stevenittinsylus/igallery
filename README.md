# Ex.08 Design of Interactive Image Gallery
## Date:23/12/24

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
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Interactive Image Gallery</title>
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: #f4f4f4;
      display: flex;
      flex-direction: column;
      align-items: center;
    }
    .gallery {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
      gap: 10px;
      padding: 20px;
      max-width: 1200px;
      width: 100%;
    }
    .gallery-item {
      position: relative;
      overflow: hidden;
      cursor: pointer;
    }
    .gallery-item img {
      width:80%;
      height: auto;
      display: block;
      transition: transform 0.3s ease;
    }
    .gallery-item:hover img {
      transform: scale(1.1);
    }
    /* Modal styles */
    .modal {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 00%;
      background: rgba(0, 0, 0, 0.8);
      display: flex;
      justify-content: center;
      align-items: center;
      opacity: 0;
      visibility: hidden;
      transition: opacity 0.3s ease, visibility 0.3s ease;
    }
    .modal.active {
      opacity: 1;
      visibility: visible;
    }
    .modal img {
      max-width: 90%;
      max-height: 80%;
      border-radius: 10px;
    }
    .modal-close {
      position: absolute;
      top: 20px;
      right: 20px;
      font-size: 24px;
      color: #fff;
      cursor: pointer;
      user-select: none;
    }
  </style>
</head>
<body>
  <h1>Interactive Image Gallery</h1>
  <div class="gallery">
    <div class="gallery-item" onclick="openModal('image1.jpg')">
      <img src="image1.jpg" alt="Image 1">
    </div>
    <div class="gallery-item" onclick="openModal('image2.jpg')">
      <img src="image2.jpg" alt="Image 2">
    </div>
    <div class="gallery-item" onclick="openModal('image3.jpg')">
      <img src="image3.jpg" alt="Image 3">
    </div>
    <div class="gallery-item" onclick="openModal('image4.jpg')">
      <img src="image4.jpg" alt="Image 4">
    </div>
    <div class="gallery-item" onclick="openModal('image5.jpg')">
      <img src="image5.jpg" alt="Image 5">
    </div>
  </div>

  <!-- Modal -->
  <div class="modal" id="modal">
    <span class="modal-close" onclick="closeModal()">&times;</span>
    <img id="modalImage" src="" alt="Modal Image">
  </div>

  <script>
    const modal = document.getElementById('modal');
    const modalImage = document.getElementById('modalImage');

    function openModal(imageSrc) {
      modalImage.src = imageSrc;
      modal.classList.add('active');
    }

    function closeModal() {
      modal.classList.remove('active');
    }
  </script>
</body>
</html>

```

## OUTPUT:
![image](https://github.com/user-attachments/assets/1f9ecacc-7f9f-4908-ab5e-95c75c483039)


## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
