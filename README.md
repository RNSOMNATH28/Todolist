# Ex03 To-Do List using JavaScript
## Date: 20.11.2026

## Name : R N SOMNATH
## Reg.No : 212224240158

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

### index.html
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>to do list web</title>
    <link rel="stylesheet" href="todo.css">
</head>
<body>
    <h1>to do list </h1>
    <div class="task-container" id="taskcontainer">
        <div class="tasks-box">
            <h2>sample task</h2>
            <p>task description</p>
            <button class="delete-btn" onclick="deletetask(this)">delete</button>
        </div>
    </div>

    <div class="add-task-form" id="addtaskform">
        <input type="text" placeholder="enter the task" id="tasktitle">
        <input type="text" placeholder="enter the task description" id="taskdesc">
        <button class="add-btn" onclick="addtask()">Add</button>
    </div>

    <button class="add-task-btn" onclick="showaddtaskform()">+</button>
</body>
<script src="todo.js"></script>
</html>
```

### style.css
```
body{
    margin: 0;
    padding: 0;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    background-color: salmon;
    display: flex;
    flex-direction: column;
    align-items: center;
    min-height:  100vh; ;
}
h1{
    text-align: center;
    color: bisque;
}
.task-container{
    
    width: 90%;
    max-width: 650px;
    margin-top: 25px;
}
.tasks-box{
    box-shadow: 0 4px 8px rgba(192, 5, 5, 0);
    padding: 18px;
    background-color: orange;
    border-radius: 10px;
    position: relative;
    margin-top: 10px;
}
.tasks-box h2{
    margin: 0 0 10px;
}
.tasks-box p{
    margin: 0 0 10px;
}
.delete-btn{
    position: absolute;
    top: 40px;
    right: 15px;
    padding: 5px 10px;
    border-radius: 10px ;
    border: 1px solid;
}
 .add-task-form{
    display: none;
    flex-direction: column;
    border: 2px solid;
    border-radius: 10px;
    padding: 18px;
    width: 90%;
    max-width: 650px;
    margin-top: 20px;
    background-color: rgb(79, 4, 154);
 }
 .add-task-form input{
    width: 90%;
    display: block;
    margin-top: 9px;
    padding: 9px;
    border: 1px solid;
    border-radius: 8px;
    font-size: 18px;
    font-weight: 500px;
 }
 .add-btn{
    background-color: rgb(39, 13, 104);
    color: bisque;
    border: 9px;
    border-radius: 10px solid ;
    width: 93%;
    height: 30px;
    margin-top: 10px;
 }
 .add-task-btn{
    position: fixed;
    bottom: 20px;
    left: 20px;
    background-color: cornflowerblue;
    color: black;
    width: 60px;
    height: 60px;
    font-size: 35px;
    border-radius: 50%;
    cursor: pointer;
    border: none;
 }
```

### script.js
```
const addtaskform=document.getElementById("addtaskform")
const taskscontainer=document.getElementById("taskcontainer")

function showaddtaskform(){
    addtaskform.style.display='flex'
}


function addtask(){
    const title=document.getElementById('tasktitle').value.trim()
    const desc=document.getElementById('taskdesc').value.trim()
    if(title ===''|| desc ===''){
        alert('please fill out both header and description')
        return;
    }
    const taskbox=document.createElement('div')
        taskbox.className='tasks-box'

        taskbox.innerHTML=`
         <h2>${title}</h2>
            <p>${desc}</p>
            <button class="delete-btn" onclick="deletetask(this)">delete</button>
        `
        taskscontainer.appendChild(taskbox)   

        document.getElementById('tasktitle').value='';
        document.getElementById('taskdesc').value='';

        addtaskform.style.display= 'none'
}
function deletetask(button){
    const taskbox=button.parentElement
    taskscontainer.removeChild(taskbox)
}
```

## OUTPUT
<img width="1901" height="1097" alt="image" src="https://github.com/user-attachments/assets/106b6f97-5439-4367-93d8-bc6c4da5dce2" />

<img width="1917" height="1097" alt="image" src="https://github.com/user-attachments/assets/1512bee5-c541-4705-babd-cd585cae092b" />


<img width="1910" height="1097" alt="image" src="https://github.com/user-attachments/assets/5cc98c25-a034-4664-8754-79147c35aa96" />



## RESULT
The program for creating To-do list using JavaScript is executed successfully.
