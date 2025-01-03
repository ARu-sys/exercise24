<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>1113572 - Exercise 24</title>
  <style>
    /* General styles */
    body {
      font-family: Arial, sans-serif;
      background-color: #f4f4f4;
      margin: 0;
      padding: 0;
    }
    .container {
      max-width: 600px;
      margin: 50px auto;
      padding: 20px;
      background-color: #fff;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
      border-radius: 8px;
    }
    h1 {
      text-align: center;
      color: #333;
    }
    label {
      font-size: 1.1em;
      margin-bottom: 10px;
      display: block;
    }
    input {
      width: 100%;
      padding: 10px;
      margin-bottom: 20px;
      font-size: 1em;
      border: 1px solid #ccc;
      border-radius: 4px;
      box-sizing: border-box;
    }
    button {
      width: 100%;
      padding: 10px;
      font-size: 1.1em;
      background-color: #007bff;
      color: white;
      border: none;
      border-radius: 4px;
      cursor: pointer;
    }
    button:hover {
      background-color: #0056b3;
    }
    .results {
      margin-top: 20px;
      padding: 20px;
      background-color: #f9f9f9;
      border-radius: 8px;
      box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    }
    .results p {
      font-size: 1.2em;
      margin: 10px 0;
      color: #333;
    }
  </style>
</head>
<body>

  <div class="container">
    <h1>Circle Properties Calculator</h1>

    <label for="radius">Enter the radius of the circle:</label>
    <input type="number" id="radius" placeholder="Radius" step="any" />

    <button onclick="calculateCircleProperties()">Calculate</button>

    <div class="results">
      <p id="circumferenceResult">The circumference is: </p>
      <p id="areaResult">The area is: </p>
    </div>
  </div>

  <script>
    // Function to calculate and display the circumference
    function calcCircumference(radius) {
      const circumference = 2 * Math.PI * radius;
      return circumference.toFixed(2);
    }

    // Function to calculate and display the area
    function calcArea(radius) {
      const area = Math.PI * Math.pow(radius, 2);
      return area.toFixed(2);
    }

    // Function to handle user input and update results
    function calculateCircleProperties() {
      const radius = parseFloat(document.getElementById('radius').value);
      if (isNaN(radius) || radius <= 0) {
        alert('Please enter a valid positive number for the radius.');
        return;
      }

      const circumference = calcCircumference(radius);
      const area = calcArea(radius);

      document.getElementById('circumferenceResult').textContent = `The circumference is: ${circumference}`;
      document.getElementById('areaResult').textContent = `The area is: ${area}`;
    }
  </script>

</body>
</html>
