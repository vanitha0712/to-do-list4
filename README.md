
# Ex03 To-Do List using JavaScript
## Date:17.11.2026

## AIM
To create a To-do Application with all features using JavaScript.

## ALGORITHM
### STEP 1
Build the HTML structure (index.html).

### STEP 2
Style the App (style.css).

### STEP 3
Plan the features the To-Do App should have.

### STEP 4
Create a To-do application using Javascript.

### STEP 5
Add functionalities.

### STEP 6
Test the App.

### STEP 7
Open the HTML file in a browser to check layout and functionality.

### STEP 8
Fix styling issues and refine content placement.

### STEP 9
Deploy the website.

### STEP 10
Upload to GitHub Pages for free hosting.

## PROGRAM

```
<!DOCTYPE html>
<html>
<head>
    <title>To-Do List</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <div class="container">
        <h1>My To-Do List</h1>

        <input type="text" id="taskInput"
        placeholder="Enter your task">

        <button onclick="addTask()">Add Task</button>

        <ul id="taskList"></ul>
    </div>

    <script src="script.js"></script>
</body>
</html>
```
```
body {
    font-family: Arial;
    background-color: lightblue;
    text-align: center;
}

.container {
    background-color: white;
    width: 350px;
    margin: 100px auto;
    padding: 20px;
    border-radius: 10px;
}

input {
    padding: 10px;
    width: 60%;
}

button {
    padding: 10px;
    background-color: green;
    color: white;
    border: none;
    cursor: pointer;
}

li {
    list-style: none;
    background-color: lightgray;
    margin: 10px;
    padding: 10px;
}

.delete {
    background-color: red;
    margin-left: 10px;
}
```
```

function addTask() {
    let input = document.getElementById("taskInput");
    let task = input.value;

    if (task === "") {
        alert("Please enter a task!");
        return;
    }

    let li = document.createElement("li");
    li.textContent = task;

    let btn = document.createElement("button");
    btn.textContent = "Delete";
    btn.className = "delete";

    btn.onclick = function() {
        li.remove();
    };

    li.appendChild(btn);

    document.getElementById("taskList")
    .appendChild(li);

    input.value = "";
}
```

## OUTPUT
![alt text](<Screenshot 2026-11-17 172303.png>)

## RESULT
The program for creating To-do list using JavaScript is executed successfully.
