# Ex03 To-Do List using JavaScript
## Date:26.03.25

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

##PROGRAM
```
<!DOCTYPE html>
<meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>To-Do List</title>
    <style>
        body {
          font-family: Arial, sans-serif;
          background: #000000;
          text-align: center;
          text-decoration: double;
        }
  
        .container {
          max-width: 600px;
          margin: 400px auto;
          padding: 30px;
          background: white;
          box-shadow: 0px 0px 10px rgb(4, 100, 155);
          border-radius: 10px;
        }
  
        h1 {
          color: #80013c;
        }
  
        .todo-input {
          display: flex;
          justify-content: space-between;
          margin-bottom: 10px;
        }
  
        .todo-input input {
          flex: 1;
          padding: 8px;
          border: 1px solid #ccc;
          border-radius: 5px;
        }
  
        .todo-input button {
          padding: 8px 12px;
          background: #28a745;
          color: white;
          border: none;
          cursor: pointer;
          margin-left: 5px;
          border-radius: 5px;
        }
  
        .todo-input button:hover {
          background: #218838;
        }
  
        ul {
          list-style: none;
          padding: 0;
        }
  
        li {
          padding: 10px;
          background: #f9f9f9;
          margin: 5px 0;
          display: flex;
          justify-content: space-between;
          border-radius: 5px;
        }
  
        li button {
          background: #dc3545;
          border: none;
          color: white;
          padding: 5px;
          cursor: pointer;
          border-radius: 5px;
        }
  
        li button:hover {
          background: #c82333;
        }

        footer {
            text-align: center;
            padding: 10px;
            
            background-color: #c2ced9;
            color: rgb(0, 0, 0);
            position: relative;
            width: 100%;
        }

      </style>    
      </head>
      <body>
        <div class="container">
          <h1>To-Do List</h1>
          <div class="todo-input">
            <input type="text" id="taskInput" placeholder="Add a new task..." />
            <button onclick="addTask()">Add</button>
          </div>
          <ul id="taskList"></ul>
        </div>
    
        <script>
          function addTask() {
            let taskInput = document.getElementById("taskInput");
            let taskValue = taskInput.value.trim();
    
            if (taskValue === "") {
              alert("Please enter a task!");
              return;
            }
    
            let taskList = document.getElementById("taskList");
    
            let li = document.createElement("li");
            li.innerHTML = `
              ${taskValue}
              <button onclick="removeTask(this)">Delete</button>
            `;
    
            taskList.appendChild(li);
            taskInput.value = "";
          }
    
          function removeTask(button) {
            let taskList = document.getElementById("taskList");
            let taskItem = button.parentElement;
            taskList.removeChild(taskItem);
          }
        </script>
        
        
        <footer>
          <p>SANDHIYA SREE(212223220093).</p>
      </footer>
  
      </body>
    </html>
```


## OUTPUT

![image](https://github.com/user-attachments/assets/106aa3e1-c94a-4c62-baf3-036c66596d85)




## RESULT
The program for creating To-do list using JavaScript is executed successfully.
