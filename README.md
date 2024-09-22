

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Homework 2 - Static Website</title>
    <link rel="stylesheet" href="css.css">
</head>
<body>
    <h1>Welcome to My Website </h1>

    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #0c9117;
        }

        img {
            max-width: 100%;
            height: auto;
        }

        h1 {
            color: #333;
        }

        #name-input {
            margin-top: 20px;
        }

        input[type="text"] {
            padding: 8px;
            font-size: 16px;
            width: 200px;
        }

        button {
            padding: 8px 16px;
            font-size: 16px;
            margin-left: 10px;
            cursor: pointer;
        }
        #greeting {
            margin-top: 20px;
            font-size: 18px;
            color: #0a0000;
        }
    </style>
</head>
<body>

    <img src="https://example.com/myimage.jpg" alt="Web Image">

    <div id="name-input">
        <label for="userName">Please enter your name:</label><br>
        <input type="text" id="userName" placeholder="">
        <button onclick="submitName()">Submit</button>
    </div>

    <p id="greeting"></p>
    
    <script src="project.js"></script>
    <script>
        function submitName() {
            let userName = document.getElementById('userName').value;
            let greetingElement = document.getElementById('greeting');
            let nameInputDiv = document.getElementById('name-input');

            if (userName) {
                // Display the greeting message
                greetingElement.textContent = "Welcome, " + userName + "!";
                
                // Hide the input field and button after name submission
                nameInputDiv.style.display = 'none';
            } else {
                greetingElement.textContent = "Please enter your name!";
            }
        }
    </script>

</body>
</html>
