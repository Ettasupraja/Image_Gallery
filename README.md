# Ex.08 Design of Interactive Image Gallery

## AIM
  To design a web application for an inteactive image gallery with minimum five images.

## DESIGN STEPS

## Step 1:

Clone the github repository and create Django admin interface

## Step 2:

Change settings.py file to allow request from all hosts.

## Step 3:

Use CSS for positioning and styling.

## Step 4:

Write JavaScript program for implementing interactivit

## Step 5:

Validate the HTML and CSS code

## Step 6:

Publish the website in the given URL.

## PROGRAM

```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Interactive Image Gallery</title>
  <style>
    body {
  font-family: Arial, sans-serif;
  background-color: #f3f3f3;
  margin: 0;
  padding: 0;
}

.gallery {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
  padding: 20px;
  justify-content: center;
}

.gallery-item {
  width: 200px;
  height: auto;
  cursor: pointer;
  border: 2px solid #ddd;
  transition: transform 0.2s;
}

.gallery-item:hover {
  transform: scale(1.05);
}

.modal {
  display: none;
  position: fixed;
  z-index: 1;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.8);
  justify-content: center;
  align-items: center;
}

.modal-content {
  max-width: 80%;
  max-height: 80%;
}

.close {
  position: absolute;
  top: 20px;
  right: 30px;
  font-size: 30px;
  color: white;
  cursor: pointer;
}

  </style>
  <script>
    function openModal(image) {
  const modal = document.getElementById('imageModal');
  const modalImg = document.getElementById('modalImage');
  
  modal.style.display = "flex";
  modalImg.src = image.src;
}

function closeModal() {
  const modal = document.getElementById('imageModal');
  modal.style.display = "none";
}

  </script>
</head>
<body>
  <div class="gallery">
    <img src="c:\Users\admin\AppData\Local\Packages\5319275A.WhatsAppDesktop_cv1g1gvanyjgm\TempState\F6B192564928A1348DA491C4987E08C4\WhatsApp Image 2024-11-15 at 14.15.49_47e5013c.jpg" alt="Image 1" class="gallery-item" onclick="openModal(this)">
    <img src="c:\Users\admin\AppData\Local\Packages\5319275A.WhatsAppDesktop_cv1g1gvanyjgm\TempState\E30FAF2040DBB22E0C56D1FF3C95ED0C\WhatsApp Image 2024-11-15 at 14.16.51_04ab2fe4.jpg" alt="Image 2" class="gallery-item" onclick="openModal(this)">
    <img src="c:\Users\admin\AppData\Local\Packages\5319275A.WhatsAppDesktop_cv1g1gvanyjgm\TempState\4611B8FF403BEA67637C3F1911940668\WhatsApp Image 2024-11-15 at 14.17.27_c431161e.jpg" alt="Image 3" class="gallery-item" onclick="openModal(this)">
    <img src="c:\Users\admin\AppData\Local\Packages\5319275A.WhatsAppDesktop_cv1g1gvanyjgm\TempState\56F9E53C06985234D40A35145C1A919E\WhatsApp Image 2024-11-15 at 14.19.07_5763a3fc.jpg" alt="Image 4" class="gallery-item" onclick="openModal(this)">
    <img src="c:\Users\admin\AppData\Local\Packages\5319275A.WhatsAppDesktop_cv1g1gvanyjgm\TempState\E1A2719218AD9000036929229C99CD3A\WhatsApp Image 2024-11-15 at 14.20.05_6fd87f29.jpg" alt="Image 5" class="gallery-item" onclick="openModal(this)">
    <img src="c:\Users\admin\AppData\Local\Packages\5319275A.WhatsAppDesktop_cv1g1gvanyjgm\TempState\2C9F13441C3F36D9422D5DE661E57742\WhatsApp Image 2024-11-15 at 14.21.57_3452cd06.jpg" alt="Image 6" class="gallery-item" onclick="openModal(this)">
    <img src="c:\Users\admin\AppData\Local\Packages\5319275A.WhatsAppDesktop_cv1g1gvanyjgm\TempState\CF72E369BA89123691BCFAF253572530\WhatsApp Image 2024-11-15 at 14.23.56_63ed07ca.jpg" alt="Image 7" class="gallery-item" onclick="openModal(this)">
    <img src="c:\Users\admin\AppData\Local\Packages\5319275A.WhatsAppDesktop_cv1g1gvanyjgm\TempState\60FF2F34A3371413AEA763296E66B04A\WhatsApp Image 2024-11-15 at 14.24.27_956f5515.jpg" alt="Image 8" class="gallery-item" onclick="openModal(this)">
    
  </div>

  <!-- Modal -->
  <div id="imageModal" class="modal" onclick="closeModal()">
    <span class="close">&times;</span>
    <img class="modal-content" id="modalImage">
  </div>

  <script src="script.js"></script>
</body>
</html>
```



## OUTPUT

![WhatsApp Image 2024-11-15 at 14 31 16_2a027e21](https://github.com/user-attachments/assets/1830989c-c926-4f7b-a799-10237ed4279b)


## RESULT
  The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
