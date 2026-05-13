4.. Write a JavaScript program to validate form inputs (e.g., email, empty fields). 
<!DOCTYPE html> 
<html> 
<head> 
    <title>Form Validation</title> 
    <script> 
        function validateForm()  
        { 
            // Get values 
            var name = document.getElementById("name").value; 
            var email = document.getElementById("email").value; 
            // Check empty fields 
            if (name == "" || email == "") { 
                alert("All fields must be filled!"); 
                return false; 
            } 
            // Email validation (simple pattern) 
            var pattern = /^[^ ]+@[^ ]+\.[a-z]{2,3}$/; 
            if (!email.match(pattern)) { 
                alert("Enter a valid email!"); 
                return false; 
            } 
            alert("Form submitted successfully!"); 
            return true; 
        } 
    </script> 
</head> 
<body> 
<h2>Form Validation</h2> 
<form onsubmit="return validateForm()"> 
Name: <input type="text" id="name"><br><br> 
Email: <input type="text" id="email"><br><br> 
<input type="submit" value="Submit"> 
</form> 
</body> 
</html> 
Create a web page that uses JavaScript to display dynamic content using DOM. 
<!DOCTYPE html> 
<html> 
<head> 
    <title>DOM Example</title> 
    <script> 
        function showMessage() { 
            // Access element and change content 
            document.getElementById("output").innerHTML = "Hello! This is dynamic content."; 
        } 
    </script> 
</head> 
<body> 
<h2>DOM Manipulation Example</h2> 
<button onclick="showMessage()">Click Me</button> 
<p id="output"></p> 
</body> 
</html> 
