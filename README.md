# Install arc.io widget on Pterodactyl Panel
You must have an Arc.io account in order to do this.

## 1. Adding the service worker
```
cd /var/www/pterodactyl/public
nano arc-sw.js
```
Copy all text from https://arc.io/arc-sw.js and put it into the arc-sw.js file.
Use "Ctrl o" to save and "Ctrl x" to exit.

## 2. Adding the widget to pages
```
cd /var/www/pterodactyl/resources/views/templates
nano wrapper.blade.php
```
Put your widget script in the `<head>` element (in between `<head>` and `</head>`).
Your script should look something like `<script async src="https://arc.io/widget.min.js#MyArcScript"></script>`.

## 3. Adding the widget to admin area
```
cd /var/www/pterodactyl/resources/views/layouts
nano admin.blade.php
```
Put your widget script in the `<head>` element (in between `<head>` and `</head>`).
Your script should look something like `<script async src="https://arc.io/widget.min.js#MyArcScript"></script>`.
