<!DOCTYPE html>
<html>
<head>
    <title>Circle Calculator</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
        }
        input, button {
            margin: 10px 0;
            padding: 10px;
        }
    </style>
    <script>
        function calculateCircleProperties() {
            const radius = parseFloat(document.getElementById("radius").value);

            if (isNaN(radius) || radius <= 0) {
                alert("Please enter a valid radius greater than 0.");
                return;
            }

            const circumference = 2 * Math.PI * radius;
            const area = Math.PI * radius * radius;

            document.getElementById("circumference").textContent = The circumference is ${circumference.toFixed(2)};
            document.getElementById("area").textContent = The area is ${area.toFixed(2)};
        }
    </script>
</head>
<body>
    <h1>Circle Calculator</h1>
    <p>Enter the radius of a circle to calculate its circumference and area.</p>
    
    <label for="radius">Radius:</label>
    <input type="number" id="radius" placeholder="Enter radius" required>
    <br>
    <button onclick="calculateCircleProperties()">Calculate</button>

    <h2>Results:</h2>
    <p id="circumference">The circumference is: </p>
    <p id="area">The area is: </p>
</body>
</html>
