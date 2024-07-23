# Deploy HTML File in Nginx Container

This guide will help you deploy an HTML file in an Nginx container using Docker.

## Steps

### 1. Pull Nginx Server Container

Open your terminal and pull the Nginx image from Docker Hub:
```sh
docker pull nginx

### Step 2: Create HTML File

Create a simple HTML file. For example, you can create a file named `index.html` with the following content:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Nginx Server</title>
</head>
<body>
    <h1>Hello from Nginx!</h1>
</body>
</html>
