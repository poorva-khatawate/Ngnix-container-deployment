# Deploy HTML File in Nginx Container

This guide will help you deploy an HTML file in an Nginx container using Docker.

## Steps

### 1. Pull Nginx Server Container

Open your terminal and pull the Nginx image from Docker Hub:
```sh
docker pull nginx
```
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
```


### Step 3: Run Your Nginx Container on Port 80

Run the Nginx container, mapping port 80 on your host to port 80 in the container:

```
docker run --name my-nginx -d -p 80:80 nginx
```

### Step 4: Check the Working of Nginx Container

Open your web browser and navigate to http://localhost. You should see the default Nginx welcome page.

### Step 5: Enter into the Container and Navigate to /usr/share/nginx/html

Use the following command to enter the running container:

```
docker exec -it my-nginx bash
```

Once inside the container, navigate to the /usr/share/nginx/html directory:
```
cd /usr/share/nginx/html
```

### Step 6: Load the HTML File into the Container

Exit the container by typing exit or pressing Ctrl + D, and copy your HTML file into the container's /usr/share/nginx/html directory from your host machine:

```
docker cp index.html my-nginx:/usr/share/nginx/html/index.html
```

### Step 7: Verify the HTML File Deployment

Open your web browser and navigate to http://localhost again. You should now see the content of your index.html file.
