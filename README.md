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
gallery.html
```
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Image Gallery</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <nav>
            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#gallery">Gallery</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <main id="gallery">
        <div class="gallery-container">
            <img src="c:\Users\admin\AppData\Local\Packages\5319275A.WhatsAppDesktop_cv1g1gvanyjgm\TempState\243C74A16947D5D9D7ED8937AC3D2656\WhatsApp Image 2024-11-06 at 21.32.45_031c0865.jpg" alt="Image 1">
            <img src="c:\Users\admin\AppData\Local\Packages\5319275A.WhatsAppDesktop_cv1g1gvanyjgm\TempState\4CADFA5FF153FB1C686F5F7535A23DC6\WhatsApp Image 2024-11-06 at 21.34.13_bdbf1b06.jpg" alt="Image 2">
            <img src="c:\Users\admin\AppData\Local\Packages\5319275A.WhatsAppDesktop_cv1g1gvanyjgm\TempState\60BC551CA678C042256508C5A0F46689\WhatsApp Image 2024-11-06 at 21.37.51_98cf2f95.jpg" alt="Image 4">
            <img src="c:\Users\admin\AppData\Local\Packages\5319275A.WhatsAppDesktop_cv1g1gvanyjgm\TempState\ACC4BA4EEC87758E9B2CA94782C41BB9\WhatsApp Image 2024-11-06 at 21.38.23_d7e75077.jpg" alt="Image 5">
            <img src="c:\Users\admin\AppData\Local\Packages\5319275A.WhatsAppDesktop_cv1g1gvanyjgm\TempState\670F33F3CFB5217BCF008786165F1DC7\WhatsApp Image 2024-11-06 at 21.40.00_7a2baef8.jpg" alt="Image 6">
            <img src="c:\Users\admin\AppData\Local\Packages\5319275A.WhatsAppDesktop_cv1g1gvanyjgm\TempState\9ABBBDA872050C52F250190578B0C178\WhatsApp Image 2024-11-06 at 21.42.19_986458be.jpg" alt="Image 7">
            <img src="c:\Users\admin\AppData\Local\Packages\5319275A.WhatsAppDesktop_cv1g1gvanyjgm\TempState\F4FB3AD46ED38E0582C16FB84B610897\WhatsApp Image 2024-11-06 at 21.46.23_3cd35854.jpg" alt="Image 8">
            <!-- Add more images as needed -->
        </div>
    </main>

    <footer>
        <p>&copy; 2024 Your Website</p>
    </footer>
</body>
</html>

```

models.py
```
class Image(models.Model):
    title = models.CharField(max_length=50)
    image = models.ImageField(upload_to='images/')

    def __str__(self):
        return self.title
```

settings.py
```
ALLOWED_HOSTS = ['*']
```

style.css
```
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
}

header {
    background-color: #333;
    color: white;
    padding: 13px 0;
}

nav ul {
    list-style: none;
    padding: 0;
    display: flex;
    justify-content: center;
}

nav ul li {
    margin: 0 13px;
}

nav ul li a {
    color: white;
    text-decoration: none;
}

.gallery-container {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 16px;
    padding: 20px;
}

.gallery-container img {
    width: 50%;
    height: 900;
    border-radius: 10px;
}

footer {
    text-align: center;
    padding: 10px 0;
    background-color: #f1f1f1;
    margin-top: 20px;
}
```

urls.py
```
from .views import gallery_view

urlpatterns = [
    path('', gallery_view, name='gallery'),
]
```

views.py
```
from .models import Image

def gallery_view(request):
    images = Image.objects.all()
    return render(request, 'gallery/gallery.html', {'images': images})
```

## OUTPUT


## RESULT
  The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
